# Revisión mensual de cuentas

## Qué es

Un prompt completo de inteligencia de cuentas que actúa como tu analista de cuentas personal. Recoge información de todas las fuentes de datos empresariales disponibles en Microsoft 365 para generar una revisión mensual completa de tus cuentas, que se entrega automáticamente el primer día laborable de cada mes.

Cada ejecución produce cuatro resultados: un informe estructurado de revisión mensual de cuentas, un resumen ejecutivo de una página, una presentación de PowerPoint para dirección y una presentación HTML, y todo te llega directamente por correo.

> [!TIP]
> Antes de ejecutarlo, sustituye las cuentas, el puesto y las fuentes de datos por los tuyos. Ajusta la lista de TPID, el perfil y las preferencias de resultado a tu territorio y tu modelo de trabajo con clientes.

---

## Copia rápida

```
Actúa como mi analista de cuentas.
Investiga los `inserta aquí proyectos, cuentas, etc.` que se indican a continuación y a los que doy soporte como `puesto`.

---

### Fuentes de datos

Usa las siguientes fuentes empresariales:

- Correos de Outlook
- Chats y canales de Teams
- Calendario y reuniones
- Archivos de OneDrive y SharePoint
- Dynamics / CRM
- ServiceNow
- Azure DevOps
- Transcripciones y notas de reuniones

Céntrate específicamente en el trabajo relacionado con M365 Copilot y Copilot Chat.

---

## Resultado principal: informe de revisión mensual de cuentas

> [!NOTE]
> Ajusta el enfoque de cada sección según tus preferencias y tu perfil. Los ejemplos siguientes son puntos de partida.

Entrega un único informe completo y estructurado con las secciones siguientes:

---

### Sección 1: Actividades y alcance

Enumera las actividades concretas realizadas en los últimos 6-12 meses:

- Talleres
- Sesiones informativas para directivos
- Sesiones de capacitación
- Pilotos
- Despliegues
- Trabajo de gobernanza
- Creación de agentes
- Formación
- Seguimientos

Incluye para cada una: fecha, audiencia, materiales producidos y documentos enlazados.

---

### Sección 2: Oportunidades y proyectos

Enumera cada oportunidad o proyecto relacionado con M365 Copilot y Copilot Chat.

Incluye para cada uno:

| Campo | Detalles |
|---|---|
| Nombre o ID de la oportunidad | |
| Fase | |
| Productos implicados | |
| Importe del acuerdo, si está disponible | |
| Calendario o hitos | |
| Siguientes pasos | |

---

### Sección 3: Impacto en ingresos

Para cada oportunidad o proyecto, indica:

- ACV o TCV, si se indican
- Número de licencias
- Tipos de SKU
- Conversiones de piloto a pago
- Potencial de ampliación

Si falta el importe exacto de ingresos, proporciona la mejor aproximación disponible:

- Cantidades de licencias presupuestadas
- Menciones a órdenes de compra
- Aprobaciones de presupuesto
- Notas de previsión
- Campos relevantes del CRM

---

### Sección 4: Partes interesadas clave

Enumera las partes interesadas con las que se ha trabajado:

| Nombre | Cargo | Función | Organización | Papel en la decisión |
|---|---|---|---|---|

Opciones de papel en la decisión: comprador económico, evaluador técnico, promotor interno (champion), bloqueador

Incluye enlaces a convocatorias de reunión, conversaciones de correo y chats cuando estén disponibles.

---

### Sección 5: Éxitos (con pruebas)

Resume los resultados medibles:

- Métricas de adopción
- Usuarios activos mensuales de pago
- Asistencia a formaciones
- Resultados de pilotos
- Ahorro de tiempo
- Puntuaciones de satisfacción
- Hitos de gobernanza
- Lanzamientos de agentes

Cita las fuentes, las fechas y las declaraciones relevantes de directivos o del equipo cuando existan.

---

### Sección 6: Bloqueos (con detalle)

Identifica bloqueos y riesgos:

- Problemas de seguridad o de cumplimiento normativo
- Restricciones de licencias
- Dependencias técnicas
- Problemas de configuración del inquilino (tenant)
- Limitaciones de acceso a datos
- Retrasos en compras
- Prioridades que compiten entre sí

Incluye para cada uno: responsable, impacto y medida de mitigación recomendada.

---

### Sección 7: Plan de acción

Recomienda de 3 a 5 acciones concretas para avanzar en:

- Ingresos
- Adopción
- Alineación con la dirección
- Eliminación de bloqueos

Asocia las acciones a los papeles de las partes interesadas siempre que sea posible.

---

### Pautas de formato

- Usa encabezados claros y listas con viñetas
- Enlaza correos, chats, archivos, reuniones y transcripciones cuando estén disponibles
- Incluye una cronología de las principales actividades y decisiones
- Destaca las cifras de forma visible
- Da prioridad a la actividad de los últimos 12 meses y a las oportunidades del próximo trimestre

---

## Resultados secundarios

---

### A. Resumen ejecutivo

Resume:

- La evolución de la cuenta
- Las señales de ingresos
- Los riesgos principales
- Las oportunidades de ampliación
- Las acciones necesarias por parte de la dirección

Limítalo al equivalente de una página.

---

### B. Presentación de PowerPoint para dirección

Incluye diapositivas de:

- Visión general de la cuenta
- Actividades de Copilot realizadas
- Oportunidades activas
- Señales de ingresos
- Mapa de partes interesadas
- Resultados de éxito
- Bloqueos y riesgos
- Siguientes acciones recomendadas
- Puntos de decisión para la dirección

Usa un lenguaje conciso, de nivel directivo, adecuado para una revisión de la dirección.

---

### C. Presentación HTML

Crea una presentación en HTML que:

- Resuma el informe de forma visual
- Destaque tendencias, bloqueos y oportunidades
- Permita revisarlo cuando se quiera

---

## Envío

Envía un correo con:

- **Asunto:** `Revisión mensual de cuentas`
- **Cuerpo:** el resumen ejecutivo dentro del mensaje
- **Adjuntos:** el informe completo de revisión mensual de cuentas, la presentación de PowerPoint para dirección y la presentación HTML

---

## Programación

Ejecuta esta tarea automáticamente y de forma recurrente el primer día laborable de cada mes.
```

---

[Volver a Prompt Playground](../README.md#prompt-playground)
