# Facturación de agentes de Copilot: créditos, imputación de costes y quién paga realmente

![Facturación de agentes de Copilot: quién paga, dónde se carga el coste y cómo estructurar Azure para que llegue al centro de coste correcto](assets/copilot%20agent%20billing/banner.png)

> [!IMPORTANT]
> **Lee esto primero: son opiniones personales del autor.** Es un recurso personal para la comunidad, y los análisis, opiniones y recomendaciones que contiene son de Michael Goad. El autor trabaja en Microsoft, pero esto **no** es una publicación oficial de Microsoft, ni una posición oficial de Microsoft, ni una guía de precios, ni una oferta o compromiso. Cuando interpreta la documentación de Microsoft, saca una conclusión o recomienda un enfoque, se trata de su perspectiva como profesional y no de una declaración en nombre de Microsoft ni de su empresa.
>
> Todas las cifras son valores orientativos de planificación tomados de la documentación pública a 4 de agosto de 2026, y ninguna refleja precios contractuales o negociados. Nada de lo que aquí se dice prevalece sobre los Términos del producto de Microsoft, tu contrato o la tarifa vigente. Confirma cualquier cosa en la que vayas a gastar dinero.

Alguien crea un agente. Un mes después aparece un cargo en la factura de Azure y no está claro quién lo ha provocado ni a qué presupuesto debería imputarse. Esa conversación se da en casi todas las organizaciones que despliegan Copilot, y suele paralizar el despliegue mientras finanzas y TI intentan conseguir una cifra que no es responsabilidad de ninguno de los dos.

Esta guía la responde. Explica cómo se factura el uso de agentes en Agent Builder, Copilot Studio, Cowork y Foundry, cuánto cuestan realmente los créditos de Copilot, dónde se configura cada superficie de facturación y cómo estructurar las suscripciones y los grupos de recursos de Azure para que el consumo llegue al centro de coste correcto en lugar de a un fondo común del que nadie se hace cargo.

> [!TIP]
> Abre la guía interactiva que encontrarás más abajo. Tiene una herramienta de decisión que te dice si un agente concreto te va a costar algo antes de crearlo, una calculadora de créditos para hacer comprobaciones rápidas en una reunión, modo claro y oscuro, y un menú para saltar entre secciones, de modo que un responsable de finanzas pueda leer tres secciones mientras un administrador lee los detalles técnicos.

> [!NOTE]
> La guía interactiva y el PDF están de momento en inglés; los enlaces llevan a las versiones publicadas por el autor original.

---

## Descarga la guía

| Material | Qué es | Abrir o descargar |
|---|---|---|
| **Guía interactiva** | La referencia completa: modelo de licencias, frontera entre lo gratuito y lo medido, tarifa de créditos, las cuatro superficies de facturación, imputación de costes en Azure, opciones de compra, controles del gasto, informes y lista de comprobación del despliegue. Incluye una herramienta de decisión interactiva y una calculadora de créditos. | [Abrir en el navegador](https://heyitsgoad.github.io/copilot-playground/education%20playground/assets/copilot%20agent%20billing/) · [Descargar HTML](https://github.com/heyitsgoad/copilot-playground/raw/main/education%20playground/assets/copilot%20agent%20billing/index.html) |
| **Referencia en PDF** | El mismo contenido en un documento imprimible de 48 páginas, con el glosario y todas las secciones desplegables abiertas. Es el que conviene reenviar a un compañero o adjuntar a una revisión de gobernanza. | [Descargar PDF](https://github.com/heyitsgoad/copilot-playground/raw/main/education%20playground/assets/copilot%20agent%20billing/Copilot-Agent-Billing-Guide.pdf) |

> [!TIP]
> Pulsa Ctrl y haz clic (Cmd y clic en Mac) en cualquier enlace para abrirlo en una pestaña nueva.

---

## Todo en siete líneas

1. **Crear un agente es gratis. Lo que cuesta es ejecutarlo.** La creación nunca es un evento facturable.
2. **Una licencia de pago de Microsoft 365 Copilot es el factor individual más importante, pero no un simple interruptor.** Deja a coste cero el uso habitual, interactivo y por parte de empleados. No cubre las ejecuciones autónomas, el uso del equipo (computer use), los modelos propios (BYOM), el alojamiento externo ni los escenarios de cara a clientes. Y a un usuario sin licencia tampoco se le cobra automáticamente: los agentes que solo tienen instrucciones o que usan la web pública son gratuitos para todos.
3. **A nadie se le factura personalmente.** Dónde se carga el coste depende de la vía de financiación. Normalmente es una suscripción y un grupo de recursos de Azure indicados en una directiva de facturación, pero los paquetes de capacidad de prepago con una directiva de créditos no necesitan ninguna suscripción de Azure.
4. **La moneda son los créditos de Copilot**, a unos 0,01 $ cada uno en pago por uso. Una sola pregunta de un usuario puede generar varios cargos a la vez.
5. **Cada superficie factura en un sitio distinto.** Agent Builder y Copilot Chat en el centro de administración de Microsoft 365, Copilot Studio en el centro de administración de Power Platform, Cowork en Copilot > Administración de costes, y Foundry directamente en Azure con medidores de Azure en lugar de créditos.
6. **Los dos tipos de directiva tienen un alcance diferente.** Las directivas de facturación de Microsoft 365 se aplican a usuarios y grupos. Los planes de facturación de Power Platform se aplican a entornos. Eso convierte los entornos en tu dimensión de informes de Copilot Studio, así que diseña los entornos y tu modelo de costes a la vez.
7. **La mayoría de los presupuestos no detienen nada.** Los presupuestos de Azure y los de las directivas de Microsoft 365 solo envían alertas. Los límites de créditos por agente y los límites de gasto de Cowork sí se aplican de verdad.

---

## La lógica económica, en un párrafo

Una licencia de pago de Microsoft 365 Copilot deja a coste cero el uso habitual e interactivo de agentes por parte de los empleados. Eso ya lo pagaste al comprar la licencia. La medición empieza en los extremos: usuarios sin licencia que acceden a datos de la organización, ejecuciones autónomas o programadas, agentes que usan el equipo y modelos propios. Esa es la diferencia entre la inclusión por licencia y el consumo por interacción. En una plataforma con precios basados únicamente en el consumo, cada interacción es un cargo. Aquí, la mayoría del uso cotidiano ya está cubierta, y el trabajo consiste en mantener el uso dentro de ese núcleo a coste cero y poner controles deliberados en los extremos medidos.

---

## Qué aprenderás

- Por qué "deberíamos comprar licencias de Copilot Premium" es una petición que no se puede cumplir tal cual está formulada, y qué pedir en su lugar
- Las cuatro condiciones que deben cumplirse a la vez para que una licencia de pago haga gratuito el uso de agentes, y los siete escenarios en los que no lo hace
- La línea exacta entre lo gratuito y lo medido para un usuario con Copilot Chat incluido, incluido el único tipo de datos al que no se puede acceder pagando
- Cuánto cuesta un crédito de Copilot, la tarifa publicada completa y por qué los créditos no son tokens
- Dónde se configura cada una de las cuatro superficies de facturación, y la diferencia de alcance que rompe la mayoría de los modelos de repercusión de costes
- Qué es realmente un grupo de recursos en términos de facturación, y la suposición que descarrila los modelos de costes
- Las tres formas de comprar créditos, incluidos los detalles comerciales que conviene confirmar con tu equipo de cuenta
- Si la identidad de los agentes (Entra Agent ID) tiene algo que ver con la facturación, y por qué la respuesta es no
- Si puedes tener más de una directiva de facturación en el mismo servicio, y la regla de Todos los usuarios que hace que parezca que no
- En qué se diferencian realmente los cuatro tipos de objetos de directiva (directivas de facturación, directivas de créditos, directivas de gasto de Cowork y planes de facturación de Power Platform)
- Qué controles del gasto se aplican de verdad y cuáles solo envían correos
- Cómo llevar el uso de Copilot a Power BI, y el único informe que no existe
- Cómo alinear las suscripciones y los grupos de recursos de Azure con las unidades de negocio sin complicarlo en exceso

---

## Para quién es

- **Responsables de TI y de plataforma** que tienen que activar la facturación, delimitarla y explicarla
- **Socios de finanzas y FinOps** que necesitan saber dónde se carga el coste y cómo repartirlo
- **Cualquiera a quien le hayan preguntado "¿cuánto nos va a costar este agente?"** y no haya tenido una respuesta defendible
- **Entornos regulados y sanitarios** en los que tanto el modelo de costes como el límite de cumplimiento normativo tienen que sostenerse

---

## Qué hace diferente a esta guía

La mayoría de las explicaciones sobre facturación pasan de puntillas por las partes difíciles. Esta las aborda. Cada cifra se contrastó con la documentación vigente de Microsoft antes de publicarla, y la guía cita sus fuentes para que puedas verificar cualquier cosa antes de gastar. Cuando la propia documentación de Microsoft se contradice, la guía lo dice y te recomienda probarlo en tu inquilino en lugar de quedarte con la respuesta que suena mejor. Se señalan tres casos de forma explícita:

- Si el pago por uso habilita realmente el conocimiento de SharePoint y OneDrive en Agent Builder
- Si las herramientas de AI Builder tienen coste cero para los usuarios con licencia
- Si Copilot Studio figura expresamente dentro del ámbito de HIPAA

También aclara varios puntos en los que es fácil equivocarse: que una licencia de pago hace gratuito todo el uso de agentes, que un usuario sin licencia siempre te cuesta dinero, que los presupuestos de Azure detienen el gasto, que el panel de Copilot es un informe de Power BI que se puede personalizar, que asignar a un agente un Entra Agent ID es la forma de facturarlo, y que los créditos y los tokens son lo mismo.

> [!NOTE]
> Hay aquí un asunto con fecha sobre el que conviene actuar. **Los créditos de AI Builder incluidos se eliminan el 1 de noviembre de 2026**, y son una moneda distinta de los créditos de Copilot, sin conversión automática. Si alguien de tu organización está planificando con un fondo de créditos, confirma de qué moneda se trata realmente antes de elaborar un presupuesto con él.

---

## Fuentes

La sección 15 de la guía enumera las referencias principales en las que se basa. La versión 1.4 añade un glosario en lenguaje sencillo con los dieciséis términos clave de la guía, definiciones emergentes de esos términos a lo largo del texto, un resumen en lenguaje sencillo al principio de cada sección compleja, y divide la antigua sección 05 en secciones separadas para las cuatro superficies de facturación y para el reparto de costes entre equipos. Las tarifas, los nombres de producto y las consolas de administración cambian a menudo, así que trata cada cifra como un valor de planificación y confírmala con la tarifa vigente y con tu propio contrato antes de comprometer presupuesto. Versión 1.4, actualizada a 4 de agosto de 2026, con próxima revisión prevista antes del 4 de noviembre de 2026.

---

## Relacionado

- [Licencias y despliegue de Copilot: quién recibe qué](./copilot%20licensing%20and%20deployment%2C%20who%20gets%20what.md), para ver puesto a puesto quién debería recibir una licencia de pago en primer lugar
- [Microsoft Agent 365: licencias, arquitectura y cómo encaja en tu estrategia de IA](./microsoft%20agent%20365%20licensing%20architecture%20and%20how%20it%20fits%20into%20your%20ai%20strategy.md), para la capa de gobernanza e identidad que está por encima de la de facturación
- [Primeros pasos con la gobernanza de Copilot](./copilot%20governance%20getting%20started.md), para el panorama más amplio de administración y cumplimiento normativo
- [Dimensionar Cowork correctamente: quién lo necesita de verdad](./right-sizing%20cowork%20who%20actually%20needs%20it.md), para delimitar Cowork antes de activar la medición

---

[Volver a Education Playground](../README.md#education-playground)
