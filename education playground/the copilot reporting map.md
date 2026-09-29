# El mapa de informes de Copilot

Todos los informes que puedes usar para medir, gobernar y demostrar el valor de Microsoft 365 Copilot, en un solo lugar.

Te preguntan "¿cómo va realmente Copilot?" y la respuesta está repartida en nueve portales distintos. Las cifras de adopción están en un sitio, el consumo de créditos en otro, el riesgo de uso compartido excesivo en un tercero y el registro de auditoría en otro completamente distinto. Nadie te da un mapa.

Este es el mapa. Los 36 informes que siguen son informes reales y documentados, del lado del cliente, que puedes abrir hoy mismo en tu propio inquilino. Ni herramientas internas de Microsoft ni paneles para comerciales. Cada fila indica dónde está, qué muestra y qué licencia o rol necesitas para verlo.

**¿Prefieres filtrar y buscar en lugar de desplazarte?** [Abre la versión interactiva](https://heyitsgoad.github.io/copilot-playground/education%20playground/assets/the%20copilot%20reporting%20map/) (en inglés), que te permite filtrar los 36 informes por portal, por disponibilidad general frente a versión preliminar y por tema.

**Contrastado con Microsoft Learn a 20 de agosto de 2026.** Este ámbito cambia rápido, así que en cada fila que lo tiene se indica si el informe está en disponibilidad general (GA) o en versión preliminar (Preview).

> [!NOTE]
> Este es un recurso personal para la comunidad. Los análisis y opiniones son del autor y no representan una posición oficial de Microsoft. Confirma siempre las licencias con tu propio contrato.

> [!TIP]
> Los nombres de los menús y de los informes se indican tal como aparecen en la interfaz en inglés. Si usas los portales en español, los nombres pueden variar ligeramente.

---

## Empieza aquí

Elige la pregunta que realmente te están haciendo.

| La pregunta | El informe | Portal |
| --- | --- | --- |
| ¿La gente usa Copilot? | [Uso de Microsoft 365 Copilot](#1-informe-de-uso-de-microsoft-365-copilot) | Centro de administración de M365 |
| ¿Quién debería recibir las próximas 500 licencias? | [Preparación para Copilot](#2-informe-de-preparación-para-copilot) | Centro de administración de M365 |
| ¿Está ahorrando tiempo a alguien? | [Panel de Copilot, Impacto](#13-panel-de-microsoft-copilot-copilot-dashboard) | Viva Insights |
| ¿Qué hacen las personas sin licencia? | [Uso de Copilot Chat](#3-informe-de-uso-de-microsoft-copilot-chat) | Centro de administración de M365 |
| ¿Qué agentes hay en mi inquilino? | [Registro de agentes](#19-registro-de-agentes-agent-registry) | Centro de administración de M365 |
| ¿Quién está consumiendo créditos? | [Créditos de Copilot](#7-informe-de-créditos-de-microsoft-copilot) y [Panel de consumo](#15-panel-de-consumo-consumption-dashboard) | Centro de administración, Viva |
| ¿Mostrará Copilot algo que no debería? | [Data Access Governance](#26-informes-de-data-access-governance-dag) | Centro de administración de SharePoint |
| ¿Qué ha consultado Copilot para dar esa respuesta? | [Auditoría de Purview](#30-auditoría-de-purview-para-copilot) | Purview |
| ¿Alguien está pegando secretos en ChatGPT? | [DSPM para IA](#29-dspm-para-ia) | Purview |
| El departamento jurídico necesita los prompts de un usuario concreto | [eDiscovery](#31-ediscovery-para-las-interacciones-con-copilot) | Purview |
| ¿Cuánto costará antes de desplegarlo? | [Estima antes de gastar](#sección-8-estima-antes-de-gastar) | Estimadores |

---

## Sección 1: centro de administración de Microsoft 365, los informes de Copilot

Son los de uso diario. Todos están en **Reports > Usage** (Informes > Uso), salvo Cowork, que está en el nodo **Copilot** del menú de la izquierda.

Enlace directo al centro de informes de uso: [admin.microsoft.com/Adminportal/Home#/reportsUsage](https://admin.microsoft.com/Adminportal/Home#/reportsUsage)

### 1. Informe de uso de Microsoft 365 Copilot

| | |
| --- | --- |
| **Dónde** | Reports > Usage > Microsoft Copilot > Copilot > pestaña **Usage** |
| **Qué muestra** | Usuarios habilitados frente a activos y tasa de usuarios activos. Total de prompts enviados y media por usuario. Adopción por aplicación en Teams, Outlook, Word, Excel, PowerPoint, OneNote, Loop, Edge, Copilot Chat (trabajo) y Copilot Chat (web). Tabla por usuario con prompts enviados, días activos y una fecha fija de última actividad por aplicación. |
| **Histórico** | 7 / 28 / 90 / 180 días. La tabla por usuario siempre cubre 180 días, sea cual sea el filtro elegido. |
| **Retraso** | En las 48 horas siguientes al final del día UTC |
| **Nubes** | Pública, GCC, GCC-High, DoD |
| **Estado** | GA |
| **Documentación** | [Microsoft 365 Copilot usage](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-365-copilot-usage) |

Es el informe al que se refiere la dirección cuando pide "las cifras de Copilot". Dos cosas que debes saber antes de presentarlo.

**"Activo" significa una acción intencionada.** Abrir el panel de Copilot o hacer clic en el icono de la cinta no cuenta. Enviar un prompt, sí. Cuando tu cifra parezca más baja que el entusiasmo que se percibe en los pasillos, este suele ser el motivo.

**Los usuarios siguen en la tabla durante 180 días después de retirarles la licencia.** Útil para analizar las bajas, engañoso si lees el número de filas como tu situación de licencias.

### 2. Informe de preparación para Copilot

| | |
| --- | --- |
| **Dónde** | Reports > Usage > Microsoft Copilot > Copilot > pestaña **Readiness** |
| **Qué muestra** | Licencias de requisito previo, usuarios en un canal de actualización válido (Current o Monthly Enterprise), licencias asignadas y licencias disponibles. Ordena a los usuarios sin licencia según su actividad en M365 y señala al 25 % superior como candidatos sugeridos para Copilot. Tabla por usuario con reuniones de Teams, chats de Teams, correo de Outlook y colaboración en documentos de Office. |
| **Histórico** | Últimos 28 días. La exportación a CSV cubre 30 días de actividad. |
| **Retraso** | En 72 horas |
| **Nubes** | Solo pública |
| **Estado** | GA |
| **Documentación** | [Microsoft 365 Copilot readiness](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-365-copilot-readiness) |

El informe más infrautilizado del centro de administración. Exporta el CSV y tendrás una respuesta defendible a "¿quién entra en la próxima oleada?", respaldada por el comportamiento real de colaboración y no por la política del organigrama.

### 3. Informe de uso de Microsoft Copilot Chat

| | |
| --- | --- |
| **Dónde** | Reports > Usage > Microsoft Copilot > **Copilot Chat** |
| **Qué muestra** | Usuarios activos, media de usuarios activos diarios, total de prompts y media de prompts por usuario de las personas **sin** licencia de pago de Copilot. Adopción repartida entre Edge, la aplicación de Copilot, Teams, Outlook, m365.cloud.microsoft/chat, Word, Excel, PowerPoint y OneNote. |
| **Histórico** | 7 / 28 / 90 / 180 días |
| **Retraso** | En 48 horas |
| **Nubes** | Pública, GCC, GCC-High, DoD |
| **Estado** | GA |
| **Documentación** | [Microsoft Copilot usage](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-copilot-usage) |

Es un informe distinto del n.º 1, y la gente lo pasa por alto constantemente. El n.º 1 cubre a los usuarios con licencia. Este cubre a todos los demás. Necesitas ambos para responder "¿cuántas personas de esta empresa usan Copilot?". También es tu mejor señal para ampliar licencias, ya que los usuarios intensivos del chat sin licencia son el caso de negocio más fácil que vas a construir.

### 4. Informe de uso de agentes de Microsoft Copilot

| | |
| --- | --- |
| **Dónde** | Reports > Usage > Microsoft Copilot > **Agents** |
| **Qué muestra** | Total de usuarios activos, divididos entre con licencia y sin licencia, total de agentes activos, una tabla por agente con usuarios activos y superficie, y un gráfico de tendencia de usuarios con licencia frente a sin licencia. Cubre agentes creados por Microsoft, por terceros y por la organización, de tipo declarativo, de SharePoint y de motor personalizado. |
| **Histórico** | 7 o 30 días |
| **Retraso** | En 1 hora |
| **Nubes** | Solo pública |
| **Estado** | **Preview** |
| **Documentación** | [Microsoft 365 Copilot agents usage](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-365-copilot-agents-new) |

Sustituye a un informe de agentes anterior que solo contaba los agentes creados por tu propia organización y tenía un retraso de 72 horas. Si guardaste el antiguo en favoritos, [está obsoleto](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-365-copilot-agents). Pásate a este.

### 5. Informe de uso de conectores de Microsoft 365 Copilot

| | |
| --- | --- |
| **Dónde** | Reports > Usage > Microsoft Copilot > **Connectors** |
| **Qué muestra** | Conexiones usadas por Copilot, conexiones usadas por agentes, usuarios activos de conectores y total de respuestas basadas en conectores. Desglosado por conector y por usuario. |
| **Histórico** | 7 o 30 días |
| **Retraso** | En 1 hora |
| **Nubes** | Solo pública |
| **Estado** | **Preview** |
| **Documentación** | [Copilot connectors usage](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-365-copilot-connectors-usage) |

Una conexión solo cuenta cuando un usuario con licencia recibe una respuesta que cita realmente contenido del conector. Si has dedicado seis meses a poner en marcha un conector de ServiceNow, este es el informe que te dice si ha merecido la pena. El uso de conectores en Cowork todavía no está cubierto.

### 6. Informe de uso de Microsoft Copilot Search

| | |
| --- | --- |
| **Dónde** | Reports > Usage > Microsoft Copilot > **Copilot Search** |
| **Qué muestra** | Usuarios activos, media de usuarios activos diarios, total de búsquedas y media de búsquedas por usuario, además de una tabla por usuario. |
| **Histórico** | 7 / 30 / 90 / 180 días |
| **Retraso** | En 1 hora |
| **Nubes** | Solo pública |
| **Estado** | **Preview** |
| **Documentación** | [Copilot search usage](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-365-copilot-search-usage) |

### 7. Informe de créditos de Microsoft Copilot

| | |
| --- | --- |
| **Dónde** | Reports > Usage > Microsoft Copilot > **Credits** |
| **Qué muestra** | Créditos consumidos por usuarios sin licencia que usan agentes medidos en Copilot Chat. Vistas acumuladas y diarias, desglosadas por usuario, por agente, por directiva de facturación y por pareja agente-usuario. Genera una alerta cuando un usuario supera aproximadamente entre 2.000 y 3.000 créditos en 30 días. |
| **Histórico** | 7 o 30 días durante la versión preliminar. Nada anterior al 3 de mayo de 2025. |
| **Retraso** | En 1 hora |
| **Nubes** | Solo pública |
| **Estado** | **Preview** |
| **Documentación** | [Microsoft Copilot credits](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/microsoft-365-copilot-credits) |

Tu sistema de alerta temprana para las sorpresas del pago por uso. Un solo prompt complejo contra un agente basado en Graph consume unos 12 créditos, así que unos pocos usuarios entusiastas mueven la factura más rápido de lo que esperan la mayoría de los equipos de finanzas.

### 8. Informe de uso de Cowork

| | |
| --- | --- |
| **Dónde** | Centro de administración > **Copilot** (menú de la izquierda) > **Cowork**. No está en Reports > Usage. |
| **Qué muestra** | Usuarios activos de Cowork, total de tareas de Cowork, media de tareas por usuario y usuarios retenidos, medidos en dos periodos consecutivos de 7 días. Tendencia de usuarios activos diarios y reparto entre tareas iniciadas por el usuario y programadas. Tabla por usuario con el total de tareas, las programadas y las iniciadas por el usuario. También muestra la cuenta atrás del periodo de gracia de facturación. |
| **Histórico** | Datos disponibles desde el 1 de abril de 2026 |
| **Nubes** | Solo pública |
| **Estado** | GA |
| **Documentación** | [Cowork usage report](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/cowork-usage-report) |

Sí, ya existen informes de Cowork, y están en disponibilidad general. El contador del periodo de gracia importa: te dice cuánto falta para que se pueda suspender el acceso a Cowork si no has configurado la facturación por consumo. Vigila la métrica de usuarios retenidos más que la de usuarios activos, porque las tareas programadas hacen que la curiosidad puntual parezca adopción.

---

## Sección 2: los informes de cargas de trabajo que indican si el terreno está preparado

Copilot se apoya en Teams, Outlook, SharePoint y OneDrive. Cuando la adopción de Copilot se estanca, la causa suele ser que la gente no colaboraba con esas herramientas desde el principio. Misma ruta: **Reports > Usage**.

| Informe | Qué muestra |
| --- | --- |
| **Active Users** | Qué servicios usa realmente cada persona. Tu denominador de referencia. |
| **Microsoft 365 Apps Usage** | Uso de las aplicaciones de escritorio, web y móviles por plataforma. Compáralo con el canal de actualización. |
| **Teams User Activity** | Reuniones, chats, llamadas y mensajes de canal por usuario. Predice la adopción de Copilot en Teams mejor que cualquier otra cosa. |
| **Teams Device Usage / Team Activity** | Reparto por plataforma y actividad por equipo. |
| **Email Activity / Email Apps Usage / Mailbox Usage** | Volumen de envío y lectura, reparto por cliente de correo y tamaño de los buzones. |
| **SharePoint Site Usage / Activity / Storage** | Archivos vistos, editados y compartidos, y dónde está el contenido. |
| **OneDrive User Activity / Usage** | Actividad de archivos y almacenamiento por usuario. |
| **Microsoft 365 Groups** | Actividad y almacenamiento de los grupos. |
| **Viva Engage Activity / Device / Groups** | Participación en las comunidades. |
| **Viva Learning, Viva Insights, Viva Goals Activity** | Uso de las aplicaciones de Viva. |
| **Forms, Project, Visio, Office Activations, Browser Usage** | El resto. Browser Usage es útil para la preparación de Copilot en Edge. |

Todos usan la misma lista de roles y admiten periodos de 7, 30, 90 y 180 días. Lista completa: [información general de los informes de uso](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/activity-reports).

### 9. Puntuación de adopción (Adoption Score)

| | |
| --- | --- |
| **Dónde** | Reports > **Adoption Score** |
| **Qué muestra** | Puntuación de las experiencias de las personas en comunicación, reuniones, colaboración en contenido, trabajo en equipo y movilidad, además de las experiencias tecnológicas mediante Endpoint Analytics. Ahora incluye una categoría de adopción de IA. |
| **Documentación** | [Adoption Score](https://learn.microsoft.com/es-es/microsoft-365/admin/adoption/adoption-score) |

### 10. Centro de mensajes, estado del servicio y hoja de ruta

No son informes de uso, pero explican por qué han cambiado tus cifras.

| Superficie | Para qué sirve |
| --- | --- |
| **Centro de mensajes** (centro de administración > Health > Message center) | Cambios en las funciones de Copilot que llegan a tu inquilino. Filtra por Copilot y configura el resumen semanal. |
| **Estado del servicio** (centro de administración > Health > Service health) | Si una métrica cayó por una incidencia. El panel de Copilot tuvo un problema real de precisión de datos entre junio de 2025 y febrero de 2026. |
| **[Hoja de ruta de Microsoft 365](https://www.microsoft.com/microsoft-365/roadmap)** | Qué informes llegarán a continuación. |

### 11. Licencias y posición de puestos de Copilot

| | |
| --- | --- |
| **Dónde** | Billing > **Licenses**, Billing > **Your products**, Users > **Active users** |
| **Qué muestra** | Licencias compradas frente a asignadas frente a disponibles por SKU, y detalle de licencias por usuario. |

Para saber "qué personas tienen licencia y no la usan", combina esto con el informe de preparación en lugar de leer solo la facturación.

### 12. Centro de administración de las aplicaciones de Microsoft 365

| | |
| --- | --- |
| **Dónde** | [config.office.com](https://config.office.com) |
| **Qué muestra** | Distribución por canal de actualización, inventario de aplicaciones, estado del mantenimiento y preparación de los complementos. |

Copilot requiere Current Channel o Monthly Enterprise Channel. Cuando un usuario jure que Copilot no le aparece en Word, mira aquí primero.

---

## Sección 3: Copilot Analytics, la capa de adopción e impacto

Todo lo de esta sección está en la **aplicación web de Viva Insights**, en [analysis.insights.cloud.microsoft](https://analysis.insights.cloud.microsoft), no en el centro de administración.

Microsoft está cambiando el nombre en la interfaz a "Microsoft 365 Copilot Analytics", mientras que la documentación de Learn sigue diciendo Viva Insights. Trátalos como lo mismo.

**El umbral de 50 licencias importa más que cualquier otra cosa aquí.** Con menos de 50 licencias de Copilot tienes Preparación, Adopción e Impacto. Con 50 o más licencias de Copilot, o 50 o más licencias de Viva Insights, también tienes el panel de agentes, comparativas de referencia, integración de la opinión de los usuarios, tendencias semanales y mensuales, vistas por grupos de responsables y resúmenes inteligentes. Si haces un piloto con 40 licencias, estás comprando deliberadamente un panel peor.

### 13. Panel de Microsoft Copilot (Copilot Dashboard)

| | |
| --- | --- |
| **Dónde** | Aplicación web de Viva Insights > **Copilot Dashboard** |
| **Qué muestra** | Cuatro secciones. **Preparación (Readiness)**: licencias asignadas, canales de actualización válidos y tarjetas con acciones para desbloquear. **Adopción (Adoption)**: usuarios activos en un periodo de 28 días, usuarios recurrentes, desglose por aplicación y por función, y segmentos de usuarios divididos en avanzados, habituales y principiantes. **Impacto (Impact)**: acciones realizadas con Copilot, horas asistidas por Copilot, valor asistido y tasa de satisfacción. **Opinión (Sentiment)**: resultados de encuestas de Glint, Pulse o un CSV subido. |
| **Quién lo ve** | Los altos directivos automáticamente en inquilinos de más de 2.500 usuarios, los administradores globales, los analistas de Viva Insights con acceso a la partición global y los responsables solo si un administrador los habilita. Los responsables de TI y de adopción deben añadirse manualmente. |
| **Datos** | 28 días móviles, con hasta 6 días de retraso y 6 meses de histórico de tendencias. Las licencias nuevas tardan hasta 7 días en aparecer. |
| **Estado** | GA |
| **Documentación** | [Microsoft Copilot Dashboard](https://learn.microsoft.com/es-es/viva/insights/org-team-insights/copilot-dashboard) |

**Entiende cómo se calculan las horas asistidas antes de ponerlas en una presentación para el consejo.** La fórmula suma las horas de reuniones resumidas, más 6 minutos por cada acción de búsqueda o resumen, más 6 minutos por cada acción de creación, según una investigación de Microsoft WorkLab. El valor asistido multiplica esas horas por una tarifa horaria que por defecto es de 72 $ y que el administrador puede configurar. Es una estimación modelizada, no tiempo medido. Si la presentas así, se sostiene. Si la presentas como ahorro medido, un director financiero la desmontará.

La tasa de satisfacción necesita al menos 30 respuestas de al menos 5 usuarios distintos para mostrarse.

### 14. Panel de agentes (Agent Dashboard)

| | |
| --- | --- |
| **Dónde** | Aplicación web de Viva Insights > **Agent Dashboard** |
| **Qué muestra** | Agentes activos, usuarios activos, respuestas de agentes, sesiones, total de créditos usados en agentes, usuarios recurrentes de agentes y el porcentaje de usuarios de Copilot que usan agentes. Destaca los agentes más populares, más compartidos y más versátiles. Filtra por tipo de creador (usuario, organización, Microsoft, terceros) y por origen (Agent Builder, Copilot Studio, SharePoint, Agents Toolkit). |
| **Requisitos** | 50 o más licencias de Copilot con actividad de agentes. Los responsables no tienen acceso, a diferencia del panel de Copilot. |
| **Dos vistas** | La vista de agentes de Copilot cubre los agentes dentro de Microsoft Copilot, con 6 meses de histórico. La vista de Agent 365 cubre los agentes de todas las aplicaciones de M365 y requiere licencias de Agent 365. |
| **Estado** | **Preview** |
| **Documentación** | [Agent Dashboard](https://learn.microsoft.com/es-es/viva/insights/org-team-insights/agent-dashboard) |

### 15. Panel de consumo (Consumption Dashboard)

| | |
| --- | --- |
| **Dónde** | Aplicación web de Viva Insights > **Consumption Dashboard** |
| **Qué muestra** | **Página de servicios de M365**: usuarios activos, uso total de créditos de Copilot, número de sesiones, uso de créditos por servicio y por grupo de la organización, intensidad de uso por segmento de usuarios (1 % superior, 5 %, del 6 al 25 %, del 26 al 50 %), seguimiento de las directivas de gasto y usuarios que han alcanzado o superado el 90 % de su límite. **Página de GitHub**: créditos de GitHub Copilot, solicitudes de chat por modo, finalizaciones de código y uso de modelos. |
| **Nota de cobertura** | Por ahora, los datos de consumo solo cubren Copilot Cowork y la API de Work IQ. |
| **Estado** | Página de servicios de M365 en GA. Página de GitHub en **Preview**. |
| **Documentación** | [Consumption dashboard](https://learn.microsoft.com/es-es/viva/insights/org-team-insights/ai-cost-dashboard) |

Aquí es donde detectas los problemas de costes mientras todavía son pequeños. La vista de "usuarios cerca de su límite de gasto" es la que conviene revisar cada semana.

### 16. Informes de Copilot Analytics

| | |
| --- | --- |
| **Dónde** | Aplicación web de Viva Insights > Reports > **Copilot Analytics reports** |
| **Qué muestra** | Informes de Power BI predefinidos. El **informe de agentes de Copilot Studio** cubre los agentes conversacionales y autónomos creados en Copilot Studio, con agentes activos, sesiones con participación, tasa de éxito, puntuación de satisfacción y los 5 agentes principales. También hay un **informe de adopción del agente de ventas**. |
| **Requisitos** | 50 o más licencias de Copilot, al menos una licencia de Copilot Studio y agentes funcionando en el entorno predeterminado de producción. |
| **No cubre** | Los agentes declarativos de Copilot Studio, los agentes de Agent Builder ni los agentes creados en SharePoint. |
| **Documentación** | [Copilot Analytics reports](https://learn.microsoft.com/es-es/viva/insights/org-team-insights/copilot-analytics-reports) y el [informe de agentes de Copilot Studio](https://learn.microsoft.com/es-es/viva/insights/advanced/analyst/templates/copilot-studio-agents) |

### 17. Análisis avanzado y el entorno de trabajo del analista

| | |
| --- | --- |
| **Dónde** | Aplicación web de Viva Insights > **Create analysis** |
| **Qué muestra** | Consultas personalizadas de persona, de reuniones, de grupo a grupo y de consumo sobre la biblioteca de métricas de Copilot. Las métricas cubren la adopción y las licencias, el uso y la participación, Copilot Chat y la actividad por aplicación en Teams, Outlook, Word, Excel, PowerPoint, OneNote y Loop. Se exporta a CSV o a plantillas de Power BI. |
| **Requisitos** | Rol de analista de Insights y una licencia de Viva Insights |
| **Documentación** | [Copilot query](https://learn.microsoft.com/es-es/viva/insights/advanced/analyst/copilot-query), [person query](https://learn.microsoft.com/es-es/viva/insights/advanced/analyst/person-query) y la [referencia completa de métricas](https://learn.microsoft.com/es-es/viva/insights/advanced/reference/metrics) |

Úsalo cuando necesites relacionar el uso de Copilot con un atributo de la organización por el que el panel no permite filtrar. También es la única forma de responder preguntas como "¿se redujeron las horas de reuniones de las personas que adoptaron Copilot en Teams?".

### 18. Opinión de los usuarios: Viva Glint y Viva Pulse

| | |
| --- | --- |
| **Qué muestra** | Una plantilla de encuesta de impacto de Copilot con cuatro preguntas sobre productividad, rapidez, esfuerzo y calidad. Los resultados alimentan la sección de opinión del panel de Copilot y se muestran como un mapa de calor por atributo de la organización. |
| **Requisitos** | 50 o más licencias de Copilot o de Viva Insights para la integración con Pulse y Glint. Se aplica un tamaño mínimo de grupo. |

El uso te dice que la gente ha hecho clic. La opinión te dice si le ha ayudado. Necesitas ambas cosas, y la segunda es la que recuerdan los directivos.

---

## Sección 4: agentes

### 19. Registro de agentes (Agent Registry)

| | |
| --- | --- |
| **Dónde** | Centro de administración > **Agents** > All Agents > **Registry** |
| **Qué muestra** | Todos los agentes del inquilino, clasificados como creados por Microsoft, de partners externos, publicados por tu organización o compartidos por un usuario. Columnas de tipo de editor, plataforma, canal, fecha de creación y disponibilidad. Tarjetas resumen con el total de agentes, los agentes sin propietario y los agentes no gestionados. Cubre Copilot Studio, Agent Builder, SharePoint, AI Foundry, Agents Toolkit y plataformas de terceros como Amazon Bedrock y Google Vertex AI. |
| **Acciones** | Habilitar, deshabilitar, asignar, bloquear, eliminar, subir un manifiesto personalizado, gestionar los agentes anclados y exportar a CSV |
| **Requisitos** | Microsoft 365 Copilot, Microsoft Agent 365 o M365 E7. Administrador global o administrador de IA. |
| **Estado** | Agent 365 pasó a disponibilidad general el 1 de mayo de 2026 |
| **Documentación** | [Agent registry](https://learn.microsoft.com/es-es/microsoft-365/admin/manage/agent-registry) |

La tarjeta de "agentes sin propietario" es la que requiere acción. Los agentes sin propietario son la TI en la sombra de la era de los agentes.

### 20. Mapa de agentes (Agent Map)

| | |
| --- | --- |
| **Dónde** | Centro de administración > Agents > All Agents > **Map** |
| **Qué muestra** | Visualización en grupos de los agentes según la plataforma en la que se crearon, con tarjetas del total de agentes, los agentes en riesgo, los agentes sin propietario y los agentes no gestionados. Permite profundizar en cualquier agente. |
| **Limitación** | El filtro de uso solo funciona en inquilinos con menos de 4.000 agentes. |
| **Documentación** | [Agent map](https://learn.microsoft.com/es-es/microsoft-365/admin/manage/agent-map) |

### 21. Información general de agentes (Agent Overview)

| | |
| --- | --- |
| **Dónde** | Centro de administración > Agents > **Overview** |
| **Qué muestra** | Instantánea de 30 días de la actividad de los agentes, tendencias de uso, carencias de gobernanza, solicitudes de aprobación pendientes, agentes sin propietario y las 5 principales plataformas de agentes. |
| **Documentación** | [Agent 365 overview](https://learn.microsoft.com/es-es/microsoft-365/admin/manage/agent-365-overview) |

### 22. Análisis de agentes de Copilot Studio

| | |
| --- | --- |
| **Dónde** | [copilotstudio.microsoft.com](https://copilotstudio.microsoft.com) > abre un agente > **Analytics** |
| **Qué muestra** | Para agentes conversacionales: usuarios activos diarios y mensuales, resultados de las conversaciones divididos en resueltas, escaladas, abandonadas y sin participación, CSAT, opinión, valoraciones positivas y negativas con comentarios, rendimiento de las fuentes de conocimiento y hasta 3 métricas personalizadas que defines en lenguaje natural. Para agentes autónomos: número de ejecuciones, tasas de éxito y de error, y rendimiento de los desencadenadores. |
| **Nota** | Las métricas de usuarios activos requieren que el agente tenga la autenticación habilitada. |
| **Documentación** | [Copilot Studio analytics](https://learn.microsoft.com/es-es/microsoft-copilot-studio/analytics-overview) |

Es por agente, no para todo el inquilino. Para la vista del inquilino, usa el registro de agentes y el panel de agentes.

### 23. Consumo de créditos de Copilot Studio

| | |
| --- | --- |
| **Dónde** | [admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com) > Licensing > **Capacity add-ons**. También Azure Cost Management para el pago por uso. |
| **Qué muestra** | Asignación, consumo y exceso de créditos de Copilot frente a los paquetes comprados, por inquilino y por entorno. |
| **Nombre** | Microsoft cambió el nombre de los "mensajes" de Copilot Studio a **créditos de Copilot** el 1 de septiembre de 2025. La documentación y los artículos más antiguos todavía hablan de mensajes. |
| **Documentación** | [Copilot Studio licensing](https://learn.microsoft.com/es-es/microsoft-copilot-studio/billing-licensing) |

### 24. Análisis del centro de administración de Power Platform

| | |
| --- | --- |
| **Dónde** | [admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com) |
| **Qué muestra** | Análisis de uso de Power Apps y Power Automate, capacidad de Dataverse, inventario de entornos y estado de las directivas de DLP. |

Una nota sobre el **CoE Starter Kit de Power Platform**: la propia documentación de Microsoft indica ahora que ya no recibe mantenimiento activo. Sigue muy desplegado y sigue siendo útil, pero no construyas un programa de gobernanza nuevo sobre él sin saberlo.

### 25. Azure AI Foundry

| | |
| --- | --- |
| **Dónde** | [ai.azure.com](https://ai.azure.com) |
| **Qué muestra** | Panel de supervisión de agentes, trazabilidad, evaluadores integrados de fundamentación y relevancia, y telemetría de tokens y costes mediante Azure Monitor y Cost Management. |

Es donde informan tus agentes creados a medida, a diferencia de los creados en Copilot Studio o Agent Builder.

---

## Sección 5: preparación del contenido, los informes que deciden qué puede ver Copilot

Copilot respeta los permisos. Ese es el problema. Si un archivo está compartido con todo el mundo, Copilot lo encontrará encantado y lo citará en un resumen. Estos informes son la forma de descubrirlo antes que tu director financiero.

### 26. Informes de Data Access Governance (DAG)

| | |
| --- | --- |
| **Dónde** | Centro de administración de SharePoint > Reports > **Data access governance** |
| **Qué muestra** | **Informes de instantánea**: permisos de todos los sitios, los sitios con el acceso más amplio, todos los sitios a los que puede llegar un usuario concreto y los sitios con archivos que tienen una etiqueta de confidencialidad determinada. **Informes de actividad** (28 días): los sitios con más vínculos de uso compartido creados y los sitios compartidos con "Todos excepto los usuarios externos". |
| **Requisitos** | SharePoint Advanced Management para todas las funciones. M365 E5 tiene informes de actividad limitados a 10.000 sitios, sin informes de instantánea ni acciones de corrección. |
| **Documentación** | [Data access governance reports](https://learn.microsoft.com/es-es/sharepoint/data-access-governance-reports) |

Ejecuta el informe de "Todos excepto los usuarios externos" (EEEU) antes de tu primer piloto de Copilot. Siempre.

### 27. Información de agentes de SharePoint (Agent Insights)

| | |
| --- | --- |
| **Dónde** | Centro de administración de SharePoint > Reports > **Agent Insights** |
| **Qué muestra** | Agentes creados recientemente en todos los sitios de SharePoint y OneDrive, los 100 sitios con más agentes, la plantilla del sitio y el estado de las directivas de gobernanza. Aplica Restricted Access Control o Restricted Content Discovery directamente desde el informe. |
| **Histórico** | 1, 7, 14 o 28 días |
| **Requisitos** | SharePoint Advanced Management o una licencia de Microsoft Copilot. Sin SAM tienes que activar primero la recopilación de datos y esperar 24 horas. |
| **PowerShell** | `Start-SPOCopilotAgentInsightsReport`, `Get-SPOCopilotAgentInsightsReport` |
| **Documentación** | [Insights on SharePoint agents](https://learn.microsoft.com/es-es/sharepoint/insights-on-sharepoint-agents) |

### 28. SharePoint Advanced Management, el resto

| Función | Qué hace |
| --- | --- |
| **Content Management Assessment** | Ejecuta juntos los informes clave y genera una vista de preparación para Copilot con recomendaciones. Vuelve a ejecutarlo cada 30 días. |
| **Restricted Content Discovery (RCD)** | Oculta un sitio a Copilot y a la búsqueda de toda la organización sin cambiar los permisos. |
| **Restricted Access Control (RAC)** | Restringe un sitio a grupos de seguridad concretos. |
| **Directivas de propiedad de sitios y de sitios inactivos** | Encuentra los sitios sin propietario y los inactivos, y empuja a los propietarios a actuar. |
| **Certificación de sitios (Site attestation)** | Obliga a los propietarios a confirmar periódicamente los permisos y el uso compartido. |
| **Informes de historial de cambios** | Cambios en la configuración de los sitios en los últimos 180 días. |
| **App insights** | Aplicaciones que no son de Microsoft y que acceden al contenido de SharePoint. |

Documentación: [SharePoint Advanced Management](https://learn.microsoft.com/es-es/sharepoint/advanced-management) y [prepárate para Copilot con SAM](https://learn.microsoft.com/es-es/microsoft-365/copilot/get-ready-copilot-sharepoint-advanced-management).

RCD es la palanca más rápida que tienes. Cuando un sitio es un problema conocido de uso compartido excesivo y no puedes corregir los permisos este trimestre, RCD lo deja hoy mismo fuera del alcance de Copilot.

---

## Sección 6: Microsoft Purview, la vista de seguridad y cumplimiento normativo

Portal: [purview.microsoft.com](https://purview.microsoft.com)

Purview agrupa las aplicaciones de IA en tres categorías, y eso decide qué puedes ver y qué pagas:

| Categoría | Incluye | Coste |
| --- | --- | --- |
| **Experiencias y agentes de Copilot** | M365 Copilot, Security Copilot, Copilot en Fabric, Copilot Studio, Cowork | Incluido en tu licencia de M365 o de Purview |
| **Aplicaciones de IA empresariales** | Aplicaciones de IA registradas en Entra, Microsoft Foundry, ChatGPT Enterprise, Claude Enterprise | Pago por uso, requiere una suscripción de Azure |
| **Otras aplicaciones de IA** | ChatGPT para consumidores, Gemini, DeepSeek y miles más | Pago por uso, más la incorporación de dispositivos y la extensión de navegador de Purview |

### 29. DSPM para IA

| | |
| --- | --- |
| **Dónde** | Purview > Solutions > **DSPM for AI** |
| **Qué muestra** | Total de interacciones con IA a lo largo del tiempo, tipos de información confidencial detectados en los prompts de IA, detecciones de comportamiento poco ético procedentes de Communication Compliance y gravedad del riesgo interno en el uso de la IA. El Explorador de actividad permite llegar a cada evento con el usuario, la aplicación, el AppHost, los tipos de información confidencial y los archivos consultados, incluidas sus etiquetas de confidencialidad. Un inventario de aplicaciones y agentes muestra qué datos toca cada agente. Las evaluaciones semanales de riesgo de datos analizan tus 100 sitios de SharePoint principales. |
| **Además** | Creación de directivas con un clic para detectar comportamientos poco éticos, información confidencial en las interacciones con Copilot y retención de las interacciones con Copilot. |
| **Requisitos** | M365 E3 o superior con la auditoría activada para las experiencias de Copilot. Pago por uso para las aplicaciones de IA empresariales y las demás. Para leer el contenido real de los prompts se necesita el rol Content Explorer Content Viewer o Purview Data Security AI Content Viewer, que los roles de administración estándar no incluyen. |
| **Nota sobre versiones** | Hay dos versiones. **DSPM for AI (clásico)**, antes llamado AI Hub, sigue funcionando pero no recibe funciones nuevas. El más reciente, **Data Security Posture Management**, añade objetivos de seguridad de los datos, cobertura de nubes de terceros y observabilidad de la IA. Construye el trabajo nuevo sobre el nuevo. |
| **Documentación** | [DSPM for AI](https://learn.microsoft.com/es-es/purview/dspm-for-ai) y [DSPM](https://learn.microsoft.com/es-es/purview/data-security-posture-management-learn-about) |

Empieza aquí para la pregunta "¿alguien está pegando datos de pacientes en ChatGPT?". Ver las aplicaciones de IA de terceros requiere facturación por uso y la incorporación de dispositivos, así que presupuéstalo antes de prometer la respuesta.

### 30. Auditoría de Purview para Copilot

| | |
| --- | --- |
| **Dónde** | Purview > Solutions > **Audit** > Search |
| **Qué muestra** | El tipo de registro `CopilotInteraction` recoge `AppHost` (qué superficie), `AppIdentity`, `AgentId` y `AgentName`, y `AccessedResources`, una matriz con cada archivo y correo que Copilot consultó para elaborar la respuesta, incluida la etiqueta de confidencialidad de cada elemento. También marca `JailbreakDetected` y `XPIADetected` para la inyección de prompts. Otros tipos de registro cubren las aplicaciones de IA empresariales conectadas y las aplicaciones de IA de terceros. |
| **Retención** | Audit Standard, 180 días. Audit Premium, 1 año para Entra, Exchange, OneDrive y SharePoint. 10 años con el complemento. |
| **Cómo consultarlo** | Portal de Purview, `Search-UnifiedAuditLog` en PowerShell de Exchange Online, la API de consultas de auditoría de Graph o la Office 365 Management Activity API para el SIEM. |
| **Documentación** | [Audit logs for Copilot](https://learn.microsoft.com/es-es/purview/audit-copilot) |

**Dos cosas en las que la gente se equivoca.**

El texto de los prompts y de las respuestas no está en el registro de auditoría. Obtienes metadatos sobre la interacción y sobre lo que consultó. Para el texto real, usa eDiscovery o el Explorador de actividad con el rol adecuado.

Microsoft indica claramente que el registro de auditoría no es una fuente para informes de uso. Los recuentos que elabores a partir de los datos de auditoría no coincidirán con el informe de uso de Copilot. Usa los informes de uso para las métricas de adopción y el registro de auditoría para las investigaciones.

### 31. eDiscovery para las interacciones con Copilot

| | |
| --- | --- |
| **Dónde** | Purview > Solutions > **eDiscovery** |
| **Qué muestra** | Los prompts y las respuestas de Copilot guardados en una carpeta oculta del buzón de Exchange Online de cada usuario, con clases de elemento como `IPM.SkypeTeams.Message.Copilot.*`. Busca por custodio en Exchange y después aplica retenciones, revisa y exporta. |
| **Requisitos** | E3 para la búsqueda, la retención y la exportación. E5 o E5 Compliance para los conjuntos de revisión, el agrupamiento de conversaciones, el descifrado y el análisis. |
| **Atención** | eDiscovery clásico y Content Search se retiraron el 31 de agosto de 2025 en todas partes salvo en 21Vianet. |
| **Documentación** | [eDiscovery](https://learn.microsoft.com/es-es/purview/edisc) |

### 32. El resto de las soluciones de Purview

| Solución | Qué aporta para Copilot | Licencia |
| --- | --- | --- |
| **Communication Compliance** | Una plantilla de directiva de IA generativa que inspecciona los prompts y las respuestas en busca de infracciones. Alimenta la vista de comportamiento poco ético de DSPM. | E5 o E5 Compliance |
| **Insider Risk Management** | Plantillas de uso arriesgado de la IA y de agentes arriesgados (Risky Agents) que cubren los datos confidenciales en los prompts y las visitas a sitios de IA. La plantilla Risky Agents ahora se aplica por defecto (Preview). | E5 o E5 Compliance |
| **Data Loss Prevention** | Una ubicación de DLP para Microsoft 365 Copilot que puede impedir que se procese el contenido etiquetado. Las alertas llegan al panel de alertas de DLP. | E3 o superior para la ubicación de Copilot |
| **Data Lifecycle Management** | Retención de las interacciones con Copilot, que decide durante cuánto tiempo se puede localizar algo. | E3 o superior |
| **Activity Explorer / Content Explorer** | Actividad de etiquetas y de DLP, y dónde está el contenido etiquetado. El Explorador de actividad muestra 30 días, así que para datos más antiguos ve al registro de auditoría. | E3 o superior |
| **Compliance Manager** | Plantillas de evaluación para la Ley de IA de la UE, ISO 42001 y NIST AI RMF, con acciones de mejora puntuadas. | 3 plantillas premium gratis con E5 |
| **Data Security Investigations** | Investigación a fondo de datos confidenciales exfiltrados, incluidas categorías de riesgo basadas en IA. | Pago por uso |

**Una carencia actual que conviene conocer.** Las alertas de DLP generadas solo por Endpoint DLP, DLP de Teams o DLP de M365 Copilot no las evalúa el indicador de alertas de DLP de Insider Risk Management. Si dabas por hecho que los positivos de DLP de Copilot aumentarían las puntuaciones de riesgo interno, todavía no lo hacen.

### 33. Defender for Cloud Apps, detección de la IA en la sombra

| | |
| --- | --- |
| **Dónde** | [security.microsoft.com](https://security.microsoft.com) > Cloud apps > **Cloud discovery** |
| **Qué muestra** | Las aplicaciones de IA generativa detectadas en uso en toda la organización, con puntuaciones de riesgo del catálogo de aplicaciones en la nube, número de usuarios y volumen de tráfico. |
| **Nota** | Las directivas de archivos de Defender for Cloud Apps se retiran el 6 de enero de 2027. Traslada esa lógica a la DLP de Purview o al etiquetado automático. |
| **Documentación** | [Discovered apps](https://learn.microsoft.com/es-es/defender-cloud-apps/discovered-apps) |

### 34. Microsoft Entra

| | |
| --- | --- |
| **Dónde** | [entra.microsoft.com](https://entra.microsoft.com) > Entra ID > Monitoring & health |
| **Qué muestra** | Registros de inicio de sesión filtrados por las aplicaciones de Copilot, Usage & insights para la actividad de inicio de sesión por aplicación, y registros de auditoría. **Entra Agent ID** añade registros que reconocen a los agentes, con un campo `agentType` que distingue entre modelos (blueprints) de agentes, instancias de agentes y cuentas de usuario de agentes, además de un `blueprintId` para relacionar una instancia con su definición. |
| **Retención** | 30 días en el portal. Exporta a Log Analytics, a almacenamiento o a Event Hub para conservarlos más tiempo. |
| **Estado** | Registros de Entra Agent ID en GA. La API de Graph para los inicios de sesión de agentes está en el punto de conexión beta. |
| **Documentación** | [Entra Agent ID logs](https://learn.microsoft.com/es-es/entra/agent-id/sign-in-audit-logs-agents) |

### 35. Uso de Security Copilot

| | |
| --- | --- |
| **Dónde** | [securitycopilot.microsoft.com](https://securitycopilot.microsoft.com) > Owner settings > **Usage monitoring** |
| **Qué muestra** | Hasta 90 días de consumo de unidades de proceso de seguridad (SCU) por sesión, usuario, complemento, categoría y experiencia, con exportación a Excel y avisos de capacidad. |
| **Requisitos** | Rol de propietario de Copilot. Capacidad de SCU aprovisionada en Azure. |
| **Documentación** | [Manage SCU usage](https://learn.microsoft.com/es-es/copilot/security/manage-usage) |

---

## Sección 7: API, cuando el portal no basta

### 36. API de informes de Microsoft Graph

Úsalas cuando necesites las cifras de Copilot en Power BI, en un almacén de datos o en una exportación programada.

**La ruta actual** es `https://graph.microsoft.com/v1.0/copilot/reports/`. Los antiguos puntos de conexión `/reports/getMicrosoft365Copilot...` en beta siguen funcionando, pero la documentación de Microsoft indica que a partir de ahora se use la ruta `/copilot`.

| Punto de conexión | Devuelve |
| --- | --- |
| `getMicrosoft365CopilotUsageUserDetail(period, version)` | Actividad de Copilot por usuario. Pasa `version='v2'` para obtener los prompts enviados, los días activos, Edge, Copilot Chat de trabajo y web, y la fecha de última actividad con agentes de Copilot. |
| `getMicrosoft365CopilotUserCountSummary(period)` | Número de usuarios activos y habilitados en el periodo |
| `getMicrosoft365CopilotUserCountTrend(period)` | Tendencia diaria de usuarios activos y habilitados |
| `getTeamsUserActivityUserDetail(period)` | Actividad en Teams por usuario, útil como denominador de preparación para Copilot |

Valores de periodo: `D7`, `D30` o `D28`, `D90`, `D180`, `ALL`. Permiso: `Reports.Read.All`.

**Para exportar el texto de los prompts y las respuestas**, usa la API del historial de interacciones con IA:

```http
GET https://graph.microsoft.com/v1.0/copilot/users/{id}/interactionHistory/getAllEnterpriseInteractions
```

Requiere el permiso de aplicación `AiEnterpriseInteraction.Read.All`. No hay opción delegada. Las interacciones con agentes de Copilot Studio quedan excluidas.

**PowerShell.** Todavía no hay cmdlets específicos para los nuevos puntos de conexión `/copilot/reports/`. Llámalos directamente:

```powershell
Connect-MgGraph -Scopes "Reports.Read.All"
Invoke-MgGraphRequest -Uri "https://graph.microsoft.com/v1.0/copilot/reports/getMicrosoft365CopilotUsageUserDetail(period='D30',version='v2')" -OutputFilePath "copilot-report.csv"
```

Documentación: [API de informes de Copilot](https://learn.microsoft.com/es-es/microsoft-365/copilot/extensibility/api/admin-settings/reports/resources/copilotreportroot) e [historial de interacciones con IA](https://learn.microsoft.com/es-es/microsoft-365/copilot/extensibility/api/ai-services/interaction-export/aiinteractionhistory-getallenterpriseinteractions).

---

## Sección 8: estima antes de gastar

Todo lo anterior te dice lo que ya has gastado. Estas herramientas te dicen lo que estás a punto de gastar.

Ese orden importa más que antes. Los agentes y Cowork se facturan por consumo, así que la primera pregunta en la sala es "¿cuánto costará?", y ningún informe de uso puede responderla hasta después de haber gastado el dinero. Estas son las herramientas que la responden por adelantado.

### Las tres que existen de verdad

| Herramienta | Qué estima | Tipo |
| --- | --- | --- |
| **[Copilot Credit Estimator](https://microsoft.github.io/copilot-studio-estimator/)** | El volumen mensual de créditos de Copilot de un agente, según el tipo de agente, el tráfico, el modelo de orquestación, las fuentes de conocimiento y el uso de herramientas. Cubre los agentes personalizados de Copilot Studio (B2E y B2C) y los agentes de Dynamics 365 Sales, Service, Finance y Supply Chain. Exporta un PDF que puedes entregar a una parte interesada. | Interactiva |
| **[Customer Cowork Estimator](https://aka.ms/CustomerCoworkEstimator)** | El consumo de créditos de Cowork antes de comprometerte con la facturación por uso. | Descarga de Excel |
| **[Calculadora de precios de Azure](https://azure.microsoft.com/es-es/pricing/calculator/)** | Azure OpenAI, Microsoft Foundry y las SCU de Security Copilot, ya que los agentes personalizados y Security Copilot se facturan a través de Azure. | Interactiva |

Documentación del estimador de créditos: [agent usage estimator](https://learn.microsoft.com/es-es/microsoft-copilot-studio/agent-usage-estimator).

Tres advertencias sinceras sobre el estimador de créditos, todas con palabras de la propia Microsoft. Modela **un agente cada vez**, así que para una cartera tendrás que ejecutarlo varias veces. La propia recomendación de Microsoft es **añadir un margen del 10 al 20 %** sobre lo que devuelva. Y la herramienta dice abiertamente que no debe usarse como calculadora de precios ni como previsión definitiva. Trata el resultado como un rango de planificación, no como una partida del presupuesto.

### La tarifa publicada

Es útil porque te permite comprobar a mano cualquier estimación. Un crédito de Copilot cuesta 0,01 $. A los usuarios con licencia de Microsoft Copilot no se les cobran créditos por esto.

| Qué hace el agente | Créditos de Copilot |
| --- | --- |
| Respuesta clásica | 1 |
| Respuesta generativa | 2 |
| Acción del agente | 5 |
| Fundamentación con el grafo del inquilino, por mensaje | 10 |
| Acciones de flujos de agente, por cada 100 | 13 |
| Herramientas de IA, básica / estándar / premium, por cada 10 respuestas | 1 / 15 / 100 |
| Procesamiento de contenido, por página | 8 |
| Voz, por minuto: clásica / IA generativa / IA generativa premium | 10 / 35 / 75 |

Fuente: [billing rates and management](https://learn.microsoft.com/es-es/microsoft-copilot-studio/requirements-messages-management). Los "mensajes" pasaron a ser "créditos de Copilot" el 1 de septiembre de 2025, sin cambios en la tarifa ni en el tamaño de los paquetes.

La línea de fundamentación con el grafo del inquilino es la que hay que vigilar. A 10 créditos por mensaje, un agente fundamentado en tu inquilino cuesta aproximadamente cinco veces más que una respuesta generativa, y así es como las facturas de pago por uso sorprenden a la gente.

### Antes de que Cowork funcione siquiera

Cowork requiere que la facturación por uso esté habilitada antes de que los usuarios puedan acceder a él. Es un paso de configuración, no solo de presupuesto.

- [Información general de la facturación por uso y los créditos de Copilot](https://learn.microsoft.com/es-es/microsoft-365/copilot/usage-based-billing-overview-copilot-credits)
- [Configurar la administración de costes, las directivas de gasto y los límites](https://learn.microsoft.com/es-es/microsoft-365/copilot/usage-based-billing-manage-copilot-credits), en el centro de administración > Copilot > Cost Management
- [Gobernanza de Cowork para administradores](https://learn.microsoft.com/es-es/microsoft-365/copilot/cowork/cowork-admin-governance)

### Lo que no existe, para que dejes de buscarlo

Conviene decirlo claramente, porque la gente pierde tardes enteras buscando estas cosas.

**No existe una calculadora oficial de Microsoft del retorno de la inversión de Copilot.** Muchas calculadoras de partners y consultoras aseguran estar vinculadas a Microsoft. Ninguna es una herramienta de Microsoft. Los estudios Total Economic Impact de Forrester son investigaciones encargadas, no calculadoras, y no deberían presentarse como tus propias cifras.

**La calculadora de TCO de Azure ya no existe.** Su antigua URL ahora redirige a una entrada de blog sobre FinOps.

**No hay una página de precios independiente de Agent 365.** Agent 365 existe y está incluido en Microsoft 365 E7, pero la página del producto E7 es la única referencia de precios.

**No hay una calculadora interactiva de licencias de Power Platform.** Tienes la guía mensual de licencias en PDF, las páginas de capacidad dentro del producto y el estimador de créditos anterior.

Para saber cómo se imputan realmente los créditos, quién paga y cómo controlar el gasto una vez en marcha, consulta [Facturación de agentes de Copilot](./copilot%20agent%20billing%2C%20credits%20and%20cost%20attribution.md).

---

## Cómo obtener acceso

La versión interna de este tipo de documento termina con una solicitud de permisos. La tuya termina con roles de Entra.

### Roles para los informes de uso del centro de administración

Cualquiera de estos te da acceso:

- Administrador global
- **Administrador de IA** (el rol más reciente y el adecuado para la mayor parte del trabajo con Copilot)
- Administrador de Exchange, de SharePoint, de Teams o de comunicaciones de Teams
- Lector de informes
- Lector de informes de resumen de uso (solo datos agregados, sin datos por usuario)
- Responsable del éxito de la experiencia de usuario (solo datos agregados)

### Roles para todo lo demás

| Superficie | Rol |
| --- | --- |
| Panel de Copilot y panel de agentes | Administrador global, alto directivo según la jerarquía de la organización o analista de Viva Insights con acceso a la partición global. Los responsables necesitan que un administrador los habilite. |
| Entorno de trabajo del analista | Analista de Insights, más una licencia de Viva Insights |
| Registro, mapa e información general de agentes | Administrador global o administrador de IA |
| Soluciones de Purview | Administrador de cumplimiento o administrador global. Lector de seguridad para solo lectura. |
| Leer el contenido de los prompts de IA en Purview | Content Explorer Content Viewer o Purview Data Security AI Content Viewer. No se incluyen en los roles de administración estándar. |
| Informes de SharePoint | Administrador de SharePoint |
| Power Platform | Administrador de Power Platform |

### Actívalo antes de necesitarlo

Tres opciones de configuración deciden si tus datos servirán de algo más adelante. Hazlo ahora.

**1. Los nombres de usuario están ocultos por defecto.** En Reports > Settings hay una opción "Display concealed user, group, and site names" (mostrar nombres ocultos de usuarios, grupos y sitios). Cuando está activada la ocultación, todos los informes de uso muestran identificadores anonimizados en lugar de nombres, lo que hace inútil el análisis por usuario. Desactivarla es una decisión deliberada de privacidad, así que tómala con las partes interesadas de privacidad y con el comité de empresa, en lugar de cambiarla discretamente. Las API de Graph devuelven los identificadores reales en cualquier caso, algo que conviene saber antes de construir una solución alternativa.

**2. La auditoría tiene que estar activada** para que DSPM para IA muestre la actividad de Copilot. Está activada por defecto en la mayoría de los inquilinos. Confírmalo.

**3. El tamaño mínimo de grupo** en Viva Insights es 10 por defecto y puede bajarse hasta 5. Fíjalo antes de que los directivos empiecen a pedir vistas por equipo, porque determina qué desgloses se muestran.

---

## La retención, de un vistazo

La cifra que da problemas es la más corta de la cadena.

| Datos | Cuánto histórico |
| --- | --- |
| Informes de uso del centro de administración | 7 / 30 / 90 / 180 días |
| Informes de agentes, conectores y créditos de Copilot | 7 o 30 días |
| Uso de Cowork | Desde el 1 de abril de 2026 |
| Panel de Copilot | Periodo móvil de 28 días, 6 meses de tendencia |
| Retraso de los datos del panel de Copilot | Hasta 6 días |
| Panel de agentes | Periodo de 28 días, 6 meses de tendencia |
| Explorador de actividad de Purview | 30 días |
| Audit Standard | 180 días |
| Audit Premium | 1 año, o 10 años con el complemento |
| Registros de inicio de sesión de Entra | 30 días en el portal |
| Informes de actividad de DAG de SharePoint | 28 días |
| Historial de cambios de SharePoint | 180 días |
| Uso de SCU de Security Copilot | 90 días |

Si necesitas informes de Copilot interanuales, nada de lo anterior te los da de forma nativa. Programa ya una exportación de Graph a tu propio almacenamiento, porque no puedes recuperar datos que la plataforma ya ha descartado.

---

## Los errores habituales

Lo que obliga a la gente a rehacer el trabajo.

**El informe de uso y el registro de auditoría nunca coincidirán.** Miden cosas distintas y Microsoft lo dice directamente. Usa los informes de uso para la adopción y la auditoría para las investigaciones. No dejes que nadie construya una métrica de adopción "mejor" con datos de auditoría.

**El uso de Copilot con licencia y sin licencia son dos informes distintos.** El informe n.º 1 y el n.º 3. Consulta ambos o te quedarás corto con tu alcance real.

**Abrir el panel de Copilot no es uso.** El usuario tiene que realizar una acción. Espera que tu cifra de usuarios activos sea más baja de lo que creen los promotores de la adopción.

**Con menos de 50 licencias de Copilot, el panel de Viva es bastante más limitado.** Sin información de agentes, sin comparativas, sin opinión de los usuarios, sin tendencias. Tenlo en cuenta al dimensionar el piloto.

**Las horas asistidas se modelan, no se miden.** 6 minutos por acción, por una tarifa predeterminada editable de 72 $. Está bien como cifra orientativa. Es peligroso como afirmación firme de retorno de la inversión.

**El texto de los prompts no está donde crees.** No está en el registro de auditoría. Está en una carpeta oculta del buzón, accesible mediante eDiscovery o el Explorador de actividad con un rol que la mayoría de los administradores no tienen.

**El antiguo informe de agentes de Copilot está obsoleto.** También eDiscovery clásico, retirado en agosto de 2025. Y las directivas de archivos de Defender for Cloud Apps se retiran el 6 de enero de 2027.

**El CoE Starter Kit ya no recibe mantenimiento activo**, según la propia documentación de Microsoft. Puedes seguir usándolo. No es una base para algo nuevo.

**Los informes en versión preliminar cambian.** A agosto de 2026, el uso de agentes, el uso de conectores, el uso de búsqueda, los créditos, el panel de agentes y la página de consumo de GitHub están todos en versión preliminar. Los esquemas y los nombres de los campos pueden cambiar.

---

## Recursos

- [Informes de uso del centro de administración de Microsoft 365](https://learn.microsoft.com/es-es/microsoft-365/admin/activity-reports/activity-reports)
- [Panel de Microsoft Copilot](https://learn.microsoft.com/es-es/viva/insights/org-team-insights/copilot-dashboard)
- [Seguridad de los datos de Purview para la IA generativa](https://learn.microsoft.com/es-es/purview/ai-microsoft-purview)
- [Prepárate para Copilot con SharePoint Advanced Management](https://learn.microsoft.com/es-es/microsoft-365/copilot/get-ready-copilot-sharepoint-advanced-management)
- [Microsoft Agent 365](https://learn.microsoft.com/es-es/microsoft-agent-365/overview)
- [Copilot Success Kit](https://adoption.microsoft.com/es-es/copilot/success-kit/)

Guías relacionadas de este repositorio: [Gobernanza de Copilot](./copilot%20governance%20getting%20started.md) para los controles que hay detrás de estos informes, [Facturación de agentes de Copilot](./copilot%20agent%20billing%2C%20credits%20and%20cost%20attribution.md) para saber qué significan las cifras de créditos, y [Licencias y despliegue](./copilot%20licensing%20and%20deployment%2C%20who%20gets%20what.md) para saber quién debería tener una licencia.

---

¿Has encontrado algo desactualizado? Abre una incidencia (issue). Esta página tiene fecha de caducidad y es mejor corregirla que dejar que se quede anticuada.

---

[Volver a Education Playground](../README.md#education-playground)
