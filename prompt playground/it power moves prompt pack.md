# Pack de prompts IT Power Moves

## Qué es

Este es el conjunto de prompts que el autor entrega a los equipos de TI cuando quiere que Copilot se gane de verdad su sitio en un entorno técnico. Son frases cortas para copiar y pegar que te llevan de un registro de errores críptico o una ventana de PowerShell en blanco a un siguiente paso claro.

Cubren el trabajo técnico que haces en Copilot Chat y también las mejoras del día a día en Excel, Word y Outlook. Dos hábitos los recorren todos: explicar antes de ejecutar, y primero un borrador que después verificas tú. La persona sigue siendo quien aprueba, algo muy importante cuando trabajas con control de cambios.

> [!TIP]
> Sustituye todo lo que esté `[entre corchetes]` por tus datos, como `[pega aquí]` por tu registro o tu script, o por el formato de tus etiquetas de activos. Cuanto más concreto seas, mejor será el resultado.

> [!IMPORTANT]
> Son borradores y explicaciones, no automatización a ciegas. Lee y verifica siempre cualquier script, comando o cambio de configuración antes de ejecutarlo en producción.

---

## Copilot Chat: el entorno técnico

Los imprescindibles para la consola. Pega un registro, un script o una configuración y deja que Copilot lo interprete, lo explique o redacte algo.

### Clasificación de un registro de errores

```
Pego este error o registro. ¿Qué es, cuál es la causa probable y cuáles son mis siguientes pasos? [pega aquí]
```

### Comprobación de seguridad de PowerShell

```
Explica qué hace este PowerShell y qué cambia antes de que lo ejecute. [pega aquí]
```

### Usuarios inactivos de AD

```
Escribe un comando de PowerShell de una línea para encontrar los usuarios de AD que no han iniciado sesión en 90 días.
```

### Expresión regular para etiquetas de activos

```
Dame una expresión regular para nuestro formato de etiqueta de activos `[AB-1234-CD]` y explica cada parte.
```

### Análisis de una traza de pila

```
Lee esta traza de pila, dime qué componente falla, la causa raíz probable y las tres soluciones más probables ordenadas por esfuerzo. [pega aquí]
```

### Diferencias de configuración en tiempo de ejecución

```
Compara estos dos archivos de configuración y explica solo las diferencias que cambiarían el comportamiento en tiempo de ejecución. [pega A] [pega B]
```

### De Bash a PowerShell

```
Convierte este script de Bash a PowerShell, mantén la lógica idéntica y señala todo lo que no tenga una equivalencia directa. [pega aquí]
```

### Consulta de viajes imposibles

```
Escribe una consulta para encontrar inicios de sesión desde ubicaciones de viaje imposible en las últimas 24 horas y explica cada cláusula.
```

### Revisión de un cambio en el registro

```
Explica qué hace este cambio en el registro, qué riesgo tiene y cómo revertirlo. [pega aquí]
```

### Revisión de un comando para producción

```
Este es el comando que estoy a punto de ejecutar en producción. ¿Qué podría salir mal y cómo lo hago más seguro? [pega aquí]
```

---

## Documenta sobre la marcha

El trabajo que nadie quiere hacer a mano. Convierte notas sueltas e incidencias en documentos limpios y listos para una auditoría.

### Procedimiento de resolución de problemas

```
Convierte estas notas sueltas de resolución de problemas en un procedimiento limpio con requisitos previos, pasos y un plan de reversión. [pega aquí]
```

### Resumen para control de cambios

```
Redacta un resumen para control de cambios de esta corrección: qué cambia, alcance del impacto, plan de marcha atrás y pasos de validación. [pega aquí]
```

### Análisis de causa raíz

```
A partir de esta cronología de la incidencia, redacta un análisis de causa raíz con los factores que contribuyeron y las acciones de seguimiento. [pega aquí]
```

---

## Excel

Para inventarios, seguimiento de licencias y trabajo con registros. Es mejor mostrarlo dentro de la aplicación, para que se vea a Copilot actuar sobre el archivo real.

### Explicación de una fórmula

```
Explica paso a paso qué hace esta fórmula y dime dónde podría fallar. [pega aquí]
```

### Fórmula para dispositivos inactivos

```
Tengo etiquetas de activos en la columna A y fechas del último inicio de sesión en la columna B. Escribe una fórmula que marque cualquier dispositivo que no se haya visto en 90 días o más.
```

### Tabla dinámica de licencias

```
Sugiere una tabla dinámica que resuma este inventario de licencias por departamento y tipo de licencia, y dime exactamente qué campo va en cada sitio.
```

### Limpiar datos exportados

```
Esta exportación tiene formatos de fecha incoherentes y espacios al final. Dame los pasos para normalizarla sin estropear los ID de activos.
```

### Análisis de anomalías de recursos

```
Analiza esta tabla de uso de CPU y memoria y destaca las principales anomalías que merece la pena investigar.
```

### Formato de filas caducadas

```
Dime cómo colorear en rojo cualquier fila en la que el estado sea Caducado y la fecha de renovación esté dentro de los próximos 30 días.
```

### Extracción del nombre de host

```
Extrae el nombre de host de estas entradas FQDN completas de la columna A y ponlo en la columna B.
```

---

## Word

Para políticas, procedimientos normalizados y documentos listos para una auditoría.

### Procedimiento a partir de viñetas

```
Convierte estas viñetas en un procedimiento normalizado de trabajo con formato, con pasos numerados y una sección de requisitos previos. [pega aquí]
```

### Referencia rápida de una política de seguridad

```
Resume esta política de seguridad en una referencia rápida de una página para el servicio de asistencia. [pega aquí]
```

### Aviso de cambio en lenguaje sencillo

```
Reescribe este aviso de cambio técnico para que un departamento no técnico entienda el impacto y el calendario. [pega aquí]
```

### Revisión del plan de respuesta a incidentes

```
Revisa este plan de respuesta a incidentes y enumera lo que falta en comparación con un marco estándar de respuesta a incidentes. [pega aquí]
```

### Plantilla de solicitud de cambio

```
Crea una plantilla reutilizable de solicitud de cambio con secciones de alcance, riesgo, marcha atrás, aprobaciones y validación.
```

### Recortar un procedimiento

```
Reduce este procedimiento un 30 % sin perder ningún paso obligatorio. [pega aquí]
```

---

## Outlook

Para la bandeja de entrada de guardia y las comunicaciones con partes interesadas.

### Resumen de una conversación

```
Resume esta conversación de correo, enumera todas las decisiones tomadas y quién es responsable de cada tarea abierta. [pega aquí o indica la conversación]
```

### Aviso de interrupción del servicio

```
Redacta un aviso de interrupción del servicio claro y tranquilo para los usuarios finales: qué está afectado, qué estamos haciendo y cuándo será la próxima actualización.
```

### Resumen semanal de un remitente

```
Resume todo lo recibido de `[proveedor o persona]` esta semana y señala lo que necesite respuesta hoy.
```

### Respuesta sobre ventanas de mantenimiento

```
Redacta una respuesta a este proveedor proponiendo tres ventanas de mantenimiento la próxima semana, todas después de las 20:00. [pega aquí]
```

### Tareas del correo no leído

```
Extrae todas las tareas que se me han asignado en el correo no leído de los dos últimos días.
```

### Reescritura de un escalado por SLA

```
Reescribe este escalado para que sea directo sobre el incumplimiento del SLA pero siga siendo profesional. [pega aquí]
```

### Resumen para la próxima reunión

```
Busca los correos y archivos recientes relacionados con mi próxima reunión y dame un resumen de un párrafo.
```

---

## Dos hábitos que enseñar junto con estos prompts

- **Explica antes de ejecutar.** Pide a Copilot que te diga qué toca un script o un comando antes de ejecutarlo. Así mantienes el control y cada prompt se convierte en una oportunidad de aprendizaje.
- **Primero un borrador, después verificas tú.** Copilot escribe la expresión regular, el comando de una línea o el procedimiento. Tú confirmas que hace lo que esperas. Ese reparto es la clave, sobre todo en entornos regulados o con control de cambios.

---

[Volver a Prompt Playground](../README.md#prompt-playground)
