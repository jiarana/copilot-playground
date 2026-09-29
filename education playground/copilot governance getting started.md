# Primeros pasos con la gobernanza de Copilot

![Webinar principal](assets/copilot%20webinar/webinar%20main.png)
Esta es una serie práctica sobre gobernanza que el autor creó junto con varios ingenieros de soluciones (SE) de su equipo. Ofrece un marco práctico para desplegar Microsoft 365 Copilot de forma responsable y a gran escala.

El contenido recorre de principio a fin los controles del centro de administración de M365, Copilot Studio, Power Platform, Microsoft Purview y SharePoint Advanced Management. Se centra en la gobernanza de agentes, la protección de datos, la mitigación del uso compartido excesivo, la gestión de costes y las salvaguardas operativas que usan de verdad los equipos de TI.

Se basa en preguntas reales de clientes y en despliegues reales, no en teoría.

**Dedicación: 4 horas**

> [!NOTE]
> Las grabaciones y los resúmenes de las sesiones están en inglés.

---

- **Sesión 1: fundamentos de la gobernanza de Copilot y de agentes en el centro de administración de M365**
  Enfoque del despliegue, el Copilot Control System, los controles de acceso y facturación, y cómo destacar o restringir agentes.
  [Leer el resumen de la sesión](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/webinar-copilot-governance-session-1-deployment-copilot-control-system-and-agent/4461801)

- **Sesión 2: gobernanza de Copilot Studio + Power Platform**
  Entornos administrados, enrutamiento de entornos, estrategia de DLP, controles de riesgo de los conectores y gestión de costes de los agentes.
  [Leer el resumen de la sesión](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/webinar--session-2-mastering-copilot-governance-with-copilot-studio--power-platf/4463239)

- **Sesión 3: Purview para M365 + agentes**
  Etiquetas de confidencialidad, DLP, riesgo interno, auditoría y eDiscovery, y cómo el etiquetado y el uso compartido excesivo determinan lo que Copilot puede mostrar.
  [Leer el resumen de la sesión](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/webinar--session-3-mastering-copilot-governance-purview-for-microsoft-365--agent/4464860)

- **Sesión 4: SharePoint Advanced Management (SAM) para las señales de contenido**
  Referencias de uso compartido excesivo, limpieza del ciclo de vida, revisiones de acceso, RAC/RCD y cómo hacer que Copilot "vea" el contenido adecuado.
  [Leer el resumen de la sesión](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/mastering-copilot-content-governance-with-sharepoint-advance-management---sessio/4467427)

---

## Sesión 1: los fundamentos del centro de administración

### Resultados que buscar

1. **Un plan de despliegue por fases** con responsables y gestión del cambio desde el primer día.
2. **El Copilot Control System** configurado: quién puede crear agentes, qué agentes se anclan y cómo se delimita la facturación.
3. **Salvaguardas** para la búsqueda web, los conectores externos y los diccionarios de negocio.

### Lista de comprobación

- Limita la creación de agentes a grupos de seguridad. Ancla los agentes clave. Haz seguimiento de los agentes sin propietario.
- Organiza el pago por uso por departamento o grupo, y limita los conectores de terceros de alto riesgo.
- Planifica los conectores de Graph (p. ej., ServiceNow) teniendo en cuenta la gobernanza.

**Recursos**

- [Ver la grabación](https://www.youtube.com/watch?v=Ie7ADxONHtw)
- [Artículo de referencia](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/webinar-copilot-governance-session-1-deployment-copilot-control-system-and-agent/4461801)

---

## Sesión 2: gobernanza de Copilot Studio + Power Platform

### Decisiones clave

- **Entornos administrados** activados, siempre. Eso habilita las directivas avanzadas, la supervisión y el enrutamiento.
- **Estrategia de entornos** con desarrollo, pruebas de aceptación (UAT) y producción, y entornos dedicados a agentes, además de **enrutamiento de entornos** para evitar la proliferación.
- **Niveles de DLP** (una base para todo el inquilino más capas por entorno), acceso basado en roles y avisos sobre conectores de riesgo.
- **Modelo de costes**: paquetes de mensajes de prepago frente a pago por uso, con asignaciones por inquilino, entorno o agente. Usa el estimador antes de escalar.

### Consejos principales

- Actualiza las directivas de DLP a medida que llegan nuevos conectores y funciones.
- Usa **Copilot Studio Authors** para incorporar a los creadores de forma ordenada.
- Conecta **Application Insights** para obtener diagnósticos más detallados.

**Recursos**

- [Ver la grabación](https://www.youtube.com/watch?v=KSkJqHnO_TE)
- [Artículo de referencia](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/webinar--session-2-mastering-copilot-governance-with-copilot-studio--power-platf/4463239)

---

## Sesión 3: Purview para la protección de la información, la auditoría y el riesgo

### Cómo se aplica la protección a Copilot

- **Etiquetas de confidencialidad**: Copilot respeta los controles de acceso. Los resultados que combinan varias fuentes heredan la confidencialidad **más alta** de ellas.
- **DLP y riesgo interno**: bloquea el procesamiento de determinadas etiquetas o proyectos, supervisa la exfiltración y aplica la protección adaptativa.
- **Auditoría y eDiscovery**: registra las interacciones con Copilot e inclúyelas en las investigaciones.

### Modelo de funcionamiento

- Empieza las directivas nuevas en modo de **solo auditoría** para ajustarlas antes de aplicarlas.
- Crea **plantillas de etiquetas personalizadas** junto con el negocio, no solo con TI.
- Aclara las expectativas entre **E3 y E5**: DSPM avanzado y etiquetado automático en E5, más trabajo manual en E3.

**Recursos**

- [Ver la grabación](https://www.youtube.com/watch?v=7dgDo5cKeYY)
- [Artículo de referencia](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/webinar--session-3-mastering-copilot-governance-purview-for-microsoft-365--agent/4464860)

---

## Sesión 4: SharePoint Advanced Management (SAM) para obtener mejores señales

### Objetivo

Restringir el uso compartido, limpiar los sitios obsoletos y reducir los accesos amplios para que Copilot vea el contenido adecuado.

### 5 acciones que importan

1. **Revisa la configuración predeterminada de uso compartido** y elimina "Todos excepto los usuarios externos" cuando proceda. Exige la aprobación del propietario siempre que sea posible.
2. **Limpieza del ciclo de vida** con la directiva de sitios inactivos. Archiva o elimina para reducir riesgo y ruido. Los sitios archivados son más baratos y Copilot no los ve.
3. **Referencia de uso compartido excesivo (DAG)** en todos los sitios, no solo en los de actividad reciente. Exporta, ordena por confidencialidad y alcance, y después corrige.
4. **Delega las revisiones de acceso** en los propietarios de los sitios. Haz seguimiento del avance desde la administración.
5. **Controles a corto plazo**:
   - **RAC** para restringir un sitio a los grupos aprobados
   - **RCD** para ocultar un sitio a Copilot y a la búsqueda entre sitios sin romper los permisos

### Extra

Aplica la **directiva de propiedad de sitios** y plantéate **bloquear la descarga** en los contenedores sensibles. Combina SAM con las etiquetas de Purview para obtener mejores informes.

**Recursos**

- [Ver la grabación](https://www.youtube.com/watch?v=VxTXvDeIGvk)
- [Artículo de referencia](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/mastering-copilot-content-governance-with-sharepoint-advance-management---sessio/4467427)

---

## Todo junto: la estructura de gobernanza

| Capa                    | Qué decides                                                         | Herramientas que usas                                            |
|-------------------------|---------------------------------------------------------------------|------------------------------------------------------------------|
| **Acceso y controles**  | Quién puede crear agentes, qué agentes se anclan, cómo facturas y supervisas | Centro de administración de M365, Copilot Control System   |
| **Plataforma de agentes** | Entornos, enrutamiento, niveles de DLP, gobernanza de conectores, modelo de costes | Copilot Studio, gobernanza de Power Platform (entornos administrados, DLP, enrutamiento) |
| **Protección de la información** | Etiquetas, DLP, riesgo interno, auditoría y eDiscovery     | Purview Information Protection, DLP, Insider Risk, Audit, eDiscovery |
| **Señales de contenido** | Configuración de uso compartido, ciclo de vida, revisiones de acceso, RAC/RCD | SharePoint Advanced Management (SAM)                     |

---

## Inicio rápido para directivos

- **Semanas 1-2**: aprueba la **estrategia de entornos** y los **entornos administrados**. Activa el enrutamiento. Define la base de DLP.
- **Semanas 3-4**: ejecuta los informes de **uso compartido excesivo (DAG)** y de **sitios inactivos**, pon en marcha las revisiones de acceso y aplica RAC/RCD en los puntos críticos.
- **Semanas 5-6**: alinea las etiquetas y la DLP con los términos del negocio, activa las reglas en modo de solo auditoría y después aplícalas. Configura los informes para la dirección.
- **De forma continua**: ancla los agentes aprobados, supervisa los agentes sin propietario y revisa cada mes el consumo y el uso de conectores.

---

## Recursos

- [Copilot Governance: A Practical Guide From Our 4-Part Webinar Series](https://techcommunity.microsoft.com/blog/healthcareandlifesciencesblog/copilot-governance-a-practical-guide-from-our-4%E2%80%91part-webinar-series/4469033), el resumen escrito de las cuatro sesiones en un solo lugar (en inglés)
- [Copilot Success Kit](https://adoption.microsoft.com/es-es/copilot/success-kit/)
- [Guía de implementación](https://aka.ms/Copilot/ImplementationSummaryGuide)
- [Guía de preparación técnica](https://aka.ms/Copilot/TechnicalReadinessGuide)
- [Guía de capacitación de usuarios](https://aka.ms/Copilot/UserEnablementGuide)

---

## Lista de reproducción de YouTube

[Ver todas las sesiones en una lista de reproducción](https://www.youtube.com/playlist?list=PLdkhFJc5w6-F-J9Os8IzyGy969USAMSIx)

![Gobernanza de Copilot](assets/copilot%20webinar/copilot%20governance.png)

---

[Volver a Education Playground](../README.md#education-playground)
