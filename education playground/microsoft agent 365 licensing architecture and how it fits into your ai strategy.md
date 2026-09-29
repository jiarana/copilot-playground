# Microsoft Agent 365: licencias, arquitectura y cómo encaja en tu estrategia de IA

> **Sobre este documento:** es una referencia técnica elaborada íntegramente a partir de documentación pública de Microsoft. Cada afirmación enlaza a una fuente pública (la mayoría en inglés). Explica qué es Agent 365, cómo funcionan sus licencias y cómo se relaciona con Copilot Studio, Copilot Chat y Foundry, incluidas las preguntas sobre licencias mixtas que surgen con más frecuencia.

---

## Resumen ejecutivo

**Microsoft Agent 365 no es una herramienta para crear agentes ni el entorno en el que se ejecutan.** Es el **plano de control de Microsoft para agentes de IA**: el producto que usan los equipos de TI y de seguridad para **observar, gobernar y proteger** los agentes de toda la organización, desde el **centro de administración de Microsoft 365** y las consolas de seguridad y administración relacionadas.

Microsoft crea y ejecuta agentes mediante **Microsoft Copilot Studio**, los **agentes declarativos o personalizados de Microsoft 365** y **Microsoft Foundry Agent Service**. Agent 365 es la capa que gestiona el **conjunto de agentes** de todos esos sistemas.

**La clave de las licencias:** las preguntas frecuentes sobre licencias de Microsoft indican que **Agent 365 se licencia por usuario, no por agente**, tanto si se compra por separado como dentro de **Microsoft 365 E7**. **Los agentes no necesitan su propia licencia de Agent 365.** Precio oficial: **15 $/usuario/mes** por separado, **99 $/usuario/mes** con Microsoft 365 E7.

**En resumen:** Agent 365 abarca **toda la organización como consola de gestión**, pero se **asigna por usuario como licencia**. Es un plano de control para todo el inquilino con un modelo comercial por usuario, no un "modo premium" por agente que cambie el propio agente.

**Fuentes:** [microsoft.com/en-us/microsoft-agent-365](https://www.microsoft.com/en-us/microsoft-agent-365), [learn.microsoft.com/en-us/microsoft-agent-365/overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview), [microsoft.com/licensing/faqs/122](https://www.microsoft.com/licensing/faqs/122)


---

## 1. Qué es Microsoft Agent 365

### El modelo mental de los tres planos

| Plano | Qué es | Productos |
|---|---|---|
| **Creación** | Donde se crean los agentes | Agentes declarativos o personalizados de Microsoft 365, Microsoft Copilot Studio, Microsoft Foundry Agent Service |
| **Ejecución** | Donde se ejecutan los agentes | Canales de Microsoft 365 (Copilot Chat, Teams, Outlook, SharePoint), entorno de ejecución de Foundry Agent Service |
| **Control** | Donde TI y seguridad gobiernan el conjunto de agentes | Microsoft Agent 365, Copilot Control System (CCS) |

### Relación de cada producto con Agent 365

| Producto o marco | Qué es | Cómo se relaciona Agent 365 |
|---|---|---|
| **Agentes de Microsoft 365** | Agentes que amplían Copilot en Microsoft 365 | Agent 365 es el plano de control para observarlos, gobernarlos y protegerlos como parte del conjunto de agentes de la organización |
| **Microsoft Copilot Studio** | Experiencia de bajo código o completa para crear agentes | Agent 365 no sustituye la facturación ni la ejecución de Copilot Studio; gobierna los agentes una vez que existen en el entorno |
| **Microsoft 365 Copilot Chat** | Interfaz de chat para el usuario final con agentes | Agent 365 no es el medidor de ejecución de Copilot Chat; es el plano de gobernanza, seguridad y observabilidad en torno a los agentes y su uso |
| **Microsoft Foundry Agent Service** | Plataforma de agentes totalmente gestionada en Azure / Microsoft Foundry | Agent 365 aporta gobernanza, identidad y seguridad centralizadas para todo el conjunto, incluidos los agentes creados fuera de las herramientas propias de Microsoft 365 |
| **Otros marcos, de terceros o no de Microsoft** | Marcos externos o personalizados | Agent 365 puede gestionar agentes independientemente de dónde se hayan creado o adquirido; el SDK de Agent 365 admite expresamente cualquier SDK o plataforma de agentes |

### CCS frente a Agent 365

Se confunden con frecuencia:

**Copilot Control System (CCS)** es el **marco de gobernanza** de Microsoft 365 Copilot y los agentes. Abarca la seguridad y la gobernanza, los controles de gestión y la medición y los informes de Microsoft 365 Copilot, Copilot Chat, los agentes precompilados de Microsoft 365 y los agentes de Copilot Studio publicados en canales de Microsoft 365.

**Microsoft Agent 365** es el **producto y plano de control para agentes de IA**: una SKU con registro centralizado, ciclo de vida, seguridad y supervisión específica por rol para el conjunto de agentes de toda la organización.

La diferencia práctica: CCS es el marco general de gobernanza de Microsoft para Copilot y las experiencias de agentes de Microsoft 365; Agent 365 es el producto concreto de plano de control para gobernar el conjunto de agentes.

---

## 2. Arquitectura, identidad, ciclo de vida, acceso a datos y registros

### 2.1 Ciclo de vida y registro de agentes

Agent 365 ofrece a los administradores un **registro único y centralizado** de todos los agentes de la organización, con una visión unificada de su **adopción, actividad y estado**. La gobernanza se realiza a través del **registro de Agent 365 en el centro de administración de Microsoft 365**, **Microsoft Entra** y **Microsoft Purview**.

La documentación de los controles de gestión de CCS cubre la gestión del ciclo de vida, incluida la visibilidad del **estado, la gobernanza y el ciclo de vida de agentes y conectores**, con gestión **desde el despliegue inicial hasta la retirada**, además de flujos de aprobación, reglas de uso compartido y coautoría, y restricciones de publicación basadas en DLP.

El inventario y el registro del ciclo de vida de los agentes están pasando a primer plano: quién es su propietario o patrocinador, dónde se creó, qué directivas se le aplican y si sigue aprobado para ejecutarse. Es un cambio importante respecto al modelo anterior, en el que la gobernanza llegaba a posteriori.

### 2.2 Identidad y contexto de ejecución

Microsoft Entra Agent ID es la base técnica de la identidad de los agentes. Una **identidad de agente es una entidad de servicio especial de Microsoft Entra ID**. Se crea a partir de un **modelo (blueprint) de identidad de agente**, puede tener un **patrocinador** que asuma la responsabilidad humana y, opcionalmente, puede ir asociada a una **cuenta de usuario del agente** cuando este necesita una cuenta de usuario de Entra completa para autenticarse en sistemas que lo exigen.

Dos patrones de ejecución fundamentales:

1. **Delegado por el usuario / en nombre de (OBO):** los agentes interactivos invocados con un token de usuario obtienen tokens de usuario en nombre de la identidad del agente
2. **Propio del agente / autónomo:** los agentes autónomos obtienen tokens de aplicación en nombre de la identidad del agente

El SDK de Agent 365 puede dar a los agentes una **identidad de agente respaldada por Entra**, sus propios recursos de usuario, como un **buzón**, telemetría auditable mediante **OpenTelemetry** y acceso a **servidores MCP** gobernados para cargas de trabajo de Microsoft 365, bajo el control de los administradores.

### 2.3 Límites de autorización y privilegio mínimo

Microsoft introdujo las identidades de agente porque los registros de aplicaciones normales o las cuentas de usuario no se adaptan bien a los agentes de IA. Microsoft impide expresamente que los agentes tengan muchos **roles o permisos con privilegios elevados** para preservar el **privilegio mínimo**.

La arquitectura se basa en un **modelo de identidad restringido** para los agentes, con un tratamiento especial porque los agentes de IA pueden actuar de forma autónoma y a gran escala.

### 2.4 Acceso a datos y herramientas

En los **agentes vinculados a Microsoft 365**, el acceso a los datos se gobierna mediante los controles estándar de Microsoft 365, Purview y SharePoint. Las organizaciones pueden usar **Microsoft Purview** y **SharePoint Advanced Management** para detectar el uso compartido excesivo, restringir el acceso, aplicar etiquetas y controlar la exposición de datos a Copilot y a los agentes.

En los **agentes de Foundry**, el entorno de ejecución de Foundry admite herramientas con autenticación gestionada, como las **credenciales gestionadas por el servicio** y la autenticación **en nombre de (OBO)**. Foundry puede publicar y compartir a través de Microsoft Teams, Microsoft 365 Copilot y el **registro de agentes de Entra**.

Los agentes **habilitados para Agent 365** pueden invocar servidores MCP de Work IQ gobernados para acceder a cargas de trabajo de Microsoft 365 a través de la puerta de enlace de herramientas de Agent 365. Entre las cargas de trabajo admitidas están el correo y el calendario de Outlook, SharePoint, OneDrive, Teams, Word y otras. Los administradores de TI gestionan qué servidores están activos y qué permisos se aplican directamente desde el centro de administración de Microsoft 365. El acceso a través de estos servidores está limitado al usuario, es auditable y requiere la licencia de Microsoft 365 Copilot.


### 2.5 Registros, observabilidad y telemetría de seguridad

La observabilidad abarca el plano de control y el entorno de ejecución:

- **Agent 365:** registro centralizado, adopción, actividad y estado, y supervisión específica por rol para administradores de IA, responsables de seguridad y responsables de negocio
- **SDK de Agent 365:** OpenTelemetry, interacciones auditadas y trazables, eventos de inferencia y uso de herramientas
- **Foundry Agent Service:** trazabilidad de extremo a extremo, métricas e integración con Application Insights
- **Blog de seguridad de Microsoft (anuncio de disponibilidad general):** Agent 365 se basa en la observabilidad de extremo a extremo, porque no se puede gobernar lo que no se ve

Cobertura de seguridad y cumplimiento normativo:

- **Purview** para la protección de la información, DLP y las salvaguardas frente a riesgos
- **Defender** para la detección de amenazas y la protección en tiempo real
- **Entra** para el control de acceso basado en riesgos de los usuarios y de los agentes que actúan en su nombre

---

## 3. Modelo de licencias: por usuario, en todo el inquilino y consumo en ejecución

### La distinción clave

Las licencias de Agent 365 **no** son lo mismo que el consumo en ejecución de Copilot Studio ni lo mismo que las licencias de usuario de Microsoft 365 Copilot. Hay tres capas comerciales distintas:

1. **Microsoft Agent 365**: licencia de plano de control por usuario; los agentes no necesitan su propia licencia; precio oficial de **15 $/usuario/mes**; de momento Agent 365 no tiene costes por consumo
2. **Microsoft 365 Copilot**: licencia por usuario para la productividad y el uso de agentes en las experiencias de Microsoft 365; parte del uso de agentes en los canales de Microsoft 365 está incluido o tiene coste cero
3. **Medición de Copilot Studio / Copilot Chat**: pago por uso, prepago o créditos de Copilot para determinados escenarios de agentes, sobre todo para usuarios de Copilot Chat y para agentes que acceden a datos del inquilino o usan orquestación o acciones más avanzadas

### Lo que Microsoft documenta oficialmente

- Agent 365 se licencia **por usuario**, no por agente
- **Los agentes no necesitan su propia licencia de Agent 365**
- Agent 365 se puede comprar por separado o mediante **Microsoft 365 E7**
- Los usuarios con licencia de Microsoft 365 Copilot pueden usar agentes en los canales de Microsoft 365, y determinadas interacciones tienen **coste cero** en Copilot Chat, Teams y SharePoint
- Los usuarios de Copilot Chat pueden usar algunos agentes **sin coste adicional**, pero los agentes que acceden a **datos compartidos del inquilino** se **miden** y requieren configurar la facturación en el centro de administración de Microsoft 365 o en el de Power Platform

### Por qué importa

Un error habitual es tratar Agent 365 como un interruptor de todo o nada para el inquilino que cambia el comportamiento de los agentes para todos. No es lo que documenta Microsoft. La distinción es:

- **Agent 365** = capa de plano de control, gobernanza, seguridad y observabilidad
- **Microsoft 365 Copilot / Copilot Chat / Copilot Studio** = experiencia de usuario + creación y ejecución + mecánica de consumo y licencias

---

## 4. Licencias mixtas: un agente compartido, algunos usuarios con licencia y otros sin ella

### El agente no se convierte en otro agente

Microsoft describe Agent 365 como un **plano de control** y afirma que **los agentes no necesitan su propia licencia**. No hay documentación de Microsoft que diga que asignar Agent 365 a algunos usuarios transforme el agente existente en un elemento "premium" distinto o retire el acceso a usuarios que ya lo tienen por la vía del canal o producto subyacente.

**El propio agente no cambia.** Lo que cambia es la **cobertura del plano de control y el nivel de gestión** en torno a ese agente, no el objeto del agente en sí.

### La posibilidad de que un usuario use el agente sigue dependiendo de la vía subyacente

- Para los **usuarios con licencia de Microsoft 365 Copilot**, el uso de agentes viene con esa licencia, y parte del uso tiene coste cero en los canales de Microsoft 365
- Para los usuarios de **Copilot Chat**, algunos agentes (solo instrucciones + sitios web públicos) no tienen coste adicional, pero los que acceden a datos del inquilino se miden y requieren configurar la facturación

Agent 365 no es la puerta que determina si un usuario puede invocar un agente compartido. Eso depende de las reglas de acceso y medición de Copilot, Copilot Chat, Teams, SharePoint y Copilot Studio.

### El derecho de uso de Agent 365 es por usuario

Las preguntas frecuentes sobre licencias de Microsoft indican que Agent 365 es **por usuario**, no por agente, y está vinculado al usuario asociado al caso de uso del agente.

Un agente compartido puede seguir compartiéndose. El derecho de uso de Agent 365 se asocia a los usuarios y escenarios que licencies. Agent 365 no es una licencia de ejecución por agente que obligue a todos los usuarios finales de un agente compartido a tener el derecho de pago.

---

## 5. Qué ocurre realmente con un agente compartido cuando solo algunos usuarios tienen licencia

Una de las preguntas sobre licencias más frecuentes cuando entra en juego Agent 365: si tu organización tiene un agente compartido que usan 1.000 personas pero solo 100 tienen licencia de Agent 365, ¿qué ocurre realmente con las otras 900?

Es la pregunta que más surge en el trabajo con clientes, y la respuesta sincera es que la documentación pública de Microsoft cubre la mayor parte, pero no todo.

Esto es lo que se sabe con certeza.

**El propio agente no cambia.** Agent 365 es el plano de control en torno al agente, no el agente en sí. Asignar licencias de Agent 365 a algunos usuarios no convierte el agente compartido en una versión "premium" distinta para esas personas.

**Que un usuario pueda usar realmente el agente no tiene nada que ver con Agent 365.** Depende de su vía de licencia subyacente (Microsoft 365 Copilot, Copilot Chat, Teams, SharePoint) y de cómo esté creado el agente. Si el agente solo usa datos de la web pública, algunos usuarios de Copilot Chat pueden acceder a él sin coste adicional. Si accede a datos del inquilino, se mide y requiere configurar la facturación, con independencia de Agent 365.

**El derecho de uso de Agent 365 es por usuario.** Los usuarios con licencia están dentro de ese ámbito comercial. Los que no la tienen, no. Pero eso no significa que los usuarios sin licencia pierdan el acceso al agente, sino que quedan fuera del derecho de gobernanza y observabilidad de Agent 365.

**Los controles de seguridad y gobernanza como Entra, Purview y Defender se aplican a nivel de inquilino y de agente, no solo a los usuarios con licencia.** Esas protecciones no dependen de las licencias individuales de Agent 365.

> [!NOTE]
> **Dónde sigue habiendo una laguna en la documentación:** Microsoft todavía no ha publicado una respuesta clara sobre cómo son la telemetría y la observabilidad de Agent 365 cuando un agente compartido lo usan a la vez usuarios con y sin licencia. El plano de control para toda la organización está bien documentado. La división exacta de la visibilidad en escenarios con usuarios mixtos, no. Es una laguna de la documentación, no necesariamente del producto.
---

## 6. Tabla 2: funciones a nivel de inquilino frente a funciones con licencia por usuario

| Ámbito | Función o capacidad | Lo que Microsoft documenta oficialmente |
|---|---|---|
| **Inquilino / toda la organización / conjunto de agentes** | Registro centralizado de agentes, con visibilidad de adopción, actividad y estado | Los administradores pueden ver todos los agentes en un registro centralizado, con supervisión específica por rol para distintos responsables y administradores. |
| **Inquilino / toda la organización / conjunto de agentes** | Gestión del ciclo de vida (estado, gobernanza, despliegue, retirada) | Los controles de gestión de CCS cubren el ciclo de vida desde el despliegue hasta la retirada, incluidos los flujos de aprobación, los controles de uso compartido y coautoría, y las restricciones de publicación con DLP. |
| **Inquilino / toda la organización / conjunto de agentes** | Controles de seguridad y gobernanza para Copilot y los agentes | La documentación de seguridad y gobernanza de CCS describe los controles de seguridad de los datos, seguridad de la IA, cumplimiento normativo y privacidad mediante el centro de administración de Microsoft 365, SharePoint Advanced Management, Purview y Defender. |
| **Inquilino / toda la organización / configuración de ejecución y facturación** | Configuración del pago por uso y la medición de Copilot Chat o Copilot Studio | Los administradores pueden configurar la facturación por uso, de prepago o de Azure para los escenarios de consumo de Copilot Chat y Copilot Studio. |
| **Por usuario** | Asignación de licencias de Agent 365 | Las preguntas frecuentes oficiales sobre licencias indican que Agent 365 es por usuario, no por agente. |
| **Por usuario** | Uso incluido o con coste cero de Microsoft 365 Copilot en determinadas interacciones con agentes | Los usuarios con licencia de Microsoft 365 Copilot tienen coste cero en las respuestas clásicas, las respuestas generativas y la fundamentación con datos del inquilino mediante Graph en los canales de Microsoft 365. |
| **Por usuario** | Vía de acceso de Copilot Chat a agentes sin coste o medidos | Algunos agentes no tienen coste adicional y otros se miden para los usuarios de Copilot Chat, según el acceso a datos y sus capacidades. |
| **Por usuario / escenario asociado al usuario** | Asociación de la identidad del agente / contexto delegado / modelo de patrocinador y propietario | Las preguntas frecuentes oficiales sobre licencias vinculan Agent 365 al usuario asociado al uso del agente; la documentación de Entra Agent ID describe la responsabilidad del patrocinador y los flujos de tokens delegados por el usuario frente a los autónomos. |

---

## 7. Qué cambia, y qué no, cuando añades Agent 365

### Qué cambia

**1. Tu organización obtiene un plano de control centralizado.**

Obtienes el registro de Agent 365 con un inventario unificado, ciclo de vida, supervisión específica por rol e integración con los controles de Entra, Purview y Defender para el entorno de agentes gestionados.

**2. Los usuarios con licencia quedan dentro del derecho comercial de Agent 365.**

Como Agent 365 es por usuario, los usuarios a los que asignas la licencia son aquellos cuyos escenarios de agentes quedan claramente dentro de ese modelo de derecho de uso.

**3. La postura de seguridad y gobernanza en torno a los agentes se hace más explícita.**

La identidad de los agentes, los límites de privilegio mínimo, la DLP y la protección de la información, y la detección y protección frente a amenazas están documentadas para los agentes gestionados y para los agentes que actúan en nombre de usuarios.

### Qué no cambia

**1. El agente se sigue creando y ejecutando donde se creaba y ejecutaba.**

Si es un agente de Copilot Studio, Copilot Studio sigue siendo el motor de creación, ejecución y facturación. Si es un agente de Foundry, Foundry sigue siendo el entorno de ejecución. Agent 365 no sustituye esos servicios.

**2. El agente no necesita su propia licencia de Agent 365.**

Las preguntas frecuentes oficiales sobre licencias de Microsoft indican expresamente que los agentes no necesitan su propia licencia.

**3. La mecánica de consumo en ejecución se mantiene.**

Copilot Studio sigue usando créditos de Copilot, pago por uso o prepago en los escenarios correspondientes, y los escenarios de agentes medidos de Copilot Chat siguen requiriendo la configuración de facturación cuando proceda.

**4. Las reglas básicas de acceso a los datos no se relajan.**

El acceso sigue limitado por Entra, Purview y los controles de privilegio mínimo. Agent 365 no permite que agentes ni usuarios eludan esos controles.

---

## 8. Gobernanza, seguridad, observabilidad y dónde tiene lagunas la documentación

### Lo que Microsoft documenta con claridad

- Registro centralizado y supervisión específica por rol en Agent 365
- Control de la identidad y del ciclo de vida mediante Entra Agent ID y el patrocinio o los modelos (blueprints)
- DLP de Purview, protección de la información y controles del uso compartido excesivo para Copilot y los agentes
- Detección de amenazas y protección en tiempo real de Defender, y ampliación a la "IA en la sombra" (shadow AI) en los anuncios de versiones preliminares

### Dónde la documentación todavía no está al día

Microsoft no ha publicado ningún artículo que aborde expresamente este escenario: "Si un agente compartido lo usan 500 personas y solo 100 tienen Agent 365, ¿qué muestra el portal de Agent 365?".

Esa división exacta de la telemetría todavía no está cubierta en la documentación pública. El plano de control para toda la organización está bien documentado; la división del derecho de uso de los usuarios finales en escenarios de agentes compartidos mixtos, no.

### Cómo interpretar la situación actual

**Aplicar controles y tener visibilidad no son lo mismo.** Microsoft documenta muchos controles como controles de plataforma, inquilino o conjunto de agentes (identidad, DLP, control de acceso, ciclo de vida, protección frente a amenazas), mientras que las licencias son por usuario. Eso significa que:

- **Aplicación de controles y salvaguardas** = a menudo con ámbito de agente, inquilino o plataforma
- **Derecho comercial** = por usuario
- **Ámbito de la observabilidad en escenarios de agentes compartidos mixtos** = todavía sin documentar expresamente

---

## 9. Qué está disponible de forma general y qué sigue ampliándose

### Disponible de forma general (a 1 de mayo de 2026)

- **Fecha de disponibilidad general de Microsoft Agent 365:** 1 de mayo de 2026, comercial, por usuario
- **Precio oficial:** 15 $/usuario/mes por separado, o incluido en Microsoft 365 E7
- **Posicionamiento principal:** observar, gobernar y proteger los agentes de toda la organización

### En versión preliminar o en ampliación

- Observabilidad, gobernanza y seguridad para agentes que funcionan **de forma independiente con sus propias credenciales y permisos**
- Detección de agentes y de **IA en la sombra** mediante Defender e Intune para agentes locales y en la nube
- **Windows 365 for Agents** y una cobertura ampliada del ecosistema SaaS

La arquitectura de identidad para agentes autónomos o con acceso propio ya se ve en la documentación de Entra Agent ID, pero el planteamiento comercial y de plano de control completo para los agentes con credenciales propias sigue evolucionando. Esa es la forma honesta de describir la situación actual.

---

## 10. Explicaciones clave

### Resumen ejecutivo en 30 segundos

**Microsoft Agent 365 es el plano de control de Microsoft para agentes de IA.** Es la capa que usan TI y seguridad para ver, gobernar y proteger los agentes de toda la empresa. **No** es la herramienta con la que se crean los agentes y **no** es el medidor de su ejecución. Esas funciones siguen en productos como los agentes de Microsoft 365, Copilot Studio y Foundry. Comercialmente, Agent 365 **se licencia por usuario, no por agente.**

### Para directores de TI y arquitectos

Piensa en **tres planos**: **crear**, **ejecutar** y **gobernar**. Los agentes se crean en Copilot Studio o Foundry (o con las herramientas de agentes de Microsoft 365), se ejecutan en los canales de Microsoft 365 o en el entorno de ejecución de Foundry, y **Agent 365** es el plano de gobernanza, seguridad y observabilidad que abarca todo ese conjunto. El plano de gestión está centralizado, pero la **licencia se asigna por usuario**, no al objeto del agente.

### Sobre la cuestión de las licencias mixtas

Agent 365 **no** es un "interruptor premium" de todo o nada por agente. Es un **plano de gestión y control para todo el inquilino** con un **modelo de licencias por usuario**. Un agente compartido puede seguir compartiéndose entre usuarios con y sin licencia de Agent 365. Lo que Microsoft todavía no ha explicado con claridad es la división exacta de la telemetría y la visibilidad cuando un mismo agente compartido lo usan usuarios con y sin licencia, y conviene reconocer esa laguna con franqueza en lugar de hacer suposiciones.

---

## 11. Resumen: un agente compartido y una población de usuarios mixta

### Lo que se sabe

- **El propio agente no cambia.** Agent 365 está documentado como el plano de control, no como la identidad de ejecución del agente.
- **Los usuarios con licencia** quedan claramente dentro del modelo de derecho comercial de Agent 365.
- **Los usuarios sin licencia** pueden seguir usando el agente compartido si sus derechos de Copilot, Copilot Chat o del canal y su vía de medición lo permiten. Agent 365 no es la puerta de ejecución de ese agente compartido.
- **La pregunta abierta** es cómo delimita Microsoft la telemetría y la observabilidad premium cuando ese mismo agente compartido lo usan usuarios mixtos. La documentación pública todavía no ofrece una matriz explícita para ese caso.

### La conclusión

**Agent 365 abarca todo el inquilino como plano de gestión y control, pero se asigna por usuario como licencia.** No es un interruptor premium por agente, y Microsoft todavía no ha documentado públicamente la división exacta de la observabilidad cuando un agente compartido lo usan usuarios con y sin licencia.

---

## Fuentes principales

- [microsoft.com/en-us/microsoft-agent-365](https://www.microsoft.com/en-us/microsoft-agent-365)
- [learn.microsoft.com/en-us/microsoft-agent-365/overview](https://learn.microsoft.com/en-us/microsoft-agent-365/overview)
- [learn.microsoft.com/en-us/microsoft-agent-365/](https://learn.microsoft.com/en-us/microsoft-agent-365/)
- [microsoft.com/licensing/faqs/122](https://www.microsoft.com/licensing/faqs/122)
- [learn.microsoft.com/en-us/microsoft-365/copilot/agent-essentials/m365-agents-faq](https://learn.microsoft.com/en-us/microsoft-365/copilot/agent-essentials/m365-agents-faq)
- [learn.microsoft.com/en-us/azure/foundry/agents/overview](https://learn.microsoft.com/en-us/azure/foundry/agents/overview)
- [learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing](https://learn.microsoft.com/en-us/microsoft-copilot-studio/billing-licensing)
- [learn.microsoft.com/en-us/copilot/agents](https://learn.microsoft.com/en-us/copilot/agents)
- [learn.microsoft.com/en-us/microsoft-365/copilot/copilot-control-system/overview](https://learn.microsoft.com/en-us/microsoft-365/copilot/copilot-control-system/overview)
- [microsoft.com/en-us/security/blog/2026/05/01/microsoft-agent-365-now-generally-available-expands-capabilities-and-integrations/](https://www.microsoft.com/en-us/security/blog/2026/05/01/microsoft-agent-365-now-generally-available-expands-capabilities-and-integrations/)
- [learn.microsoft.com/en-us/microsoft-agent-365/developer/](https://learn.microsoft.com/en-us/microsoft-agent-365/developer/)

---

[Volver a Education Playground](../README.md#education-playground)
