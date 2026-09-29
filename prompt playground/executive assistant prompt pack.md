# Pack de prompts para asistentes de dirección

## Qué es

Este es el conjunto de prompts que el autor entrega a asistentes de dirección y profesionales administrativos que quieren que Copilot se encargue de las partes del trabajo que, sin hacer ruido, se comen el día entero. Clasificación de la bandeja de entrada, cálculos de calendario entre zonas horarias, actas de reuniones, esquemas de presentaciones, contratos con proveedores y logística de eventos.

Ninguno es especialmente ingenioso. Esa es la idea. Son las mismas peticiones que le harías a una nueva incorporación espabilada, redactadas con el detalle suficiente para que Copilot pueda actuar sobre ellas.

> [!TIP]
> Sustituye todo lo que esté `[entre corchetes]` por tus datos antes de ejecutarlo. Nombres, fechas, ciudades, proveedores, número de personas. Cuanto más concreto seas, menos tendrás que corregir después.

> [!NOTE]
> Copilot solo puede trabajar con lo que ve. Si un prompt hace referencia a una reunión, una conversación o un documento, ábrelo o adjúntalo primero para que Copilot tenga la fuente en lugar de adivinar.

---

## Bandeja de entrada y correo

La bandeja de entrada es donde la mayoría de los asistentes pierden la mañana. Estos prompts te llevan directamente a la lista corta.

### Ponerse al día después de una ausencia

```
Resume mi correo no leído de los últimos [3] días en una lista priorizada. Pon arriba todo lo que tenga un plazo o necesite una decisión, a continuación lo que necesite una respuesta mía, y agrupa abajo las novedades informativas. Dime quién está esperando una respuesta nuestra y cuánto tiempo lleva esperando.
```

### Redactar una respuesta con la voz de tu directivo

```
Redacta una respuesta a este correo como si fueras [nombre del directivo]. Imita su forma habitual de escribir: [breve, cercana, sin rodeos]. Trata [punto uno], [punto dos] y [punto tres]. Deja una línea en blanco al final para lo que quiera añadir personalmente.
```

### Aviso de retraso en un proyecto

```
Redacta una actualización para el equipo de [nombre del proyecto] de parte de [nombre del directivo]. Vamos [dos] días por detrás del calendario. Que sea directa pero sin dureza, centrada en la solución más que en el fallo, y pide a cada responsable de equipo que envíe un plan de recuperación en tres puntos antes del final del [viernes]. Menos de 200 palabras.
```

### Encontrar lo que debes a otras personas

```
Reúne todos los compromisos que he adquirido por correo esta semana y que todavía no se han cerrado. Muestra a quién se lo prometí, qué prometí y para cuándo era.
```

---

## Calendario y planificación

El trabajo con el calendario es aritmética más política. Copilot puede encargarse de la aritmética.

### Tres zonas horarias sin reuniones a deshoras

```
Encuentra los tres mejores horarios para una reunión de [60] minutos con asistentes en [Tokio], [Londres] y [Nueva York]. Nada antes de las 9:00 ni después de las 18:00 en la hora local de nadie. Muestra cada opción en las tres zonas horarias y dime cuál es la menos incómoda en conjunto y por qué.
```

### Ordenar la próxima semana

```
Revisa el calendario de [nombre del directivo] de [la próxima semana] y encuentra todos los conflictos, todas las series de reuniones seguidas sin hueco y todo lo que esté reservado dos veces. Para cada caso, dime qué mover y dame dos horarios alternativos que ya les vengan bien a los demás asistentes.
```

### Proteger una semana de viaje

```
[Nombre del directivo] viaja a [ciudad] el [fechas]. Revisa su calendario de esos días y dime qué hay que mover, qué puede quedarse en formato virtual y qué debería bloquear para el viaje y para descansar. Dame la lista de personas a las que tengo que escribir para avisar del cambio.
```

---

## Reuniones y actas

Tres peticiones distintas, así que usa la que corresponda a quien lo vaya a leer.

### Resumen de un párrafo para quien no asistió

```
Escribe un resumen de un párrafo de esta reunión para [nombre del directivo], que no asistió. Empieza por lo que se decidió y lo que ocurre a continuación. Omite los detalles del debate salvo que cambien una decisión.
```

### Acta formal a partir de una grabación o transcripción

```
Convierte esta transcripción en un acta formal con estas secciones: Asistentes, Orden del día, Resumen del debate, Decisiones, Tareas pendientes y Siguientes pasos. Pon las tareas pendientes en una tabla con responsable y fecha de vencimiento. Usa un lenguaje conciso y profesional. Si nunca se llegó a indicar un responsable o un plazo, márcalo como POR CONFIRMAR en lugar de suponerlo.
```

### Tareas pendientes ordenadas por persona

```
Lee esta transcripción de la reunión y extrae todas las frases que impliquen una tarea, un plazo o un seguimiento. Organízalas por persona en una tabla con la acción, el responsable y la fecha de vencimiento. Esto va en el correo de resumen, así que cada línea debe ser lo bastante corta como para leerse de un vistazo.
```

> [!TIP]
> La instrucción POR CONFIRMAR del prompt del acta es más importante de lo que parece. Sin ella, Copilot se inventará un responsable plausible o una fecha que nadie acordó, y no te darás cuenta hasta que alguien no la cumpla.

---

## Documentos y presentaciones

### De informe a esquema de cinco diapositivas

```
Convierte este informe en un esquema de cinco diapositivas para que [nombre del directivo] lo presente ante [audiencia]. Un mensaje clave por diapositiva, un máximo de tres puntos de apoyo, y dime qué elemento visual funcionaría en cada una. Señala cualquier cifra del informe que debería verificar antes de que aparezca en una diapositiva.
```

### Revisión de un contrato con un proveedor

```
Revisa este contrato de [nombre del proveedor]. Extrae todo lo relativo a renovación automática, plazos de preaviso, penalizaciones por rescisión anticipada y subidas de precio después del primer año. Después dame cinco preguntas para enviar al departamento jurídico antes de firmar. No soy abogado, así que explica en lenguaje sencillo cualquier término con un significado jurídico concreto.
```

### Resumen previo a una reunión

```
Prepara un resumen de una página para [nombre del directivo] antes de la reunión [nombre de la reunión] del [fecha]. Incluye quién asiste y qué papel tiene cada uno, qué se decidió la última vez, qué sigue abierto y las tres preguntas que es más probable que le hagan.
```

---

## Investigación y preparación

### Panorama de la competencia antes de una presentación comercial

```
Prepara una comparación breve entre [competidor A] y [competidor B]. Incluye cómo les ha ido en los últimos 12 meses, cómo describen su propia misión y estrategia, y tres aspectos en los que parecen débiles. Que ocupe una página y cita de dónde sale cada punto para que pueda verificarlo antes de que llegue a [nombre del directivo].
```

> [!IMPORTANT]
> Pide siempre las fuentes en la investigación externa. Si Copilot no puede mostrarte de dónde sale una afirmación, no la pongas delante de un directivo.

---

## Eventos y logística

### Un catering que de verdad sirva a todos

```
Dame tres opciones de catering para una comida de equipo de [25] personas, con tres tipos de cocina distintos. Para cada una, indica el plato principal y un equivalente vegetariano, vegano y sin gluten que sea una comida de verdad y no solo una ensalada de acompañamiento. Incluye un coste estimado por persona e indica lo que se transporte mal o haya que servir caliente.
```

### Guion de una jornada fuera de la oficina

```
Prepara el guion de una jornada fuera de la oficina de [media jornada] para [25] personas el [fecha]. Incluye los horarios de llegada, sesiones, descansos y comida, y quién es responsable de cada bloque. Añade una columna con lo que necesito tener preparado con antelación para cada punto.
```

---

## Tres hábitos que hacen que funcionen mejor

- **Dale la fuente.** Copilot es tan bueno como aquello a lo que le apuntas. Adjunta el archivo, abre la conversación, nombra la reunión. Un prompt vago sin fuente es de donde salen los malos resultados.
- **Di quién lo va a leer.** "Para mi directivo" y "para el consejo" dan borradores muy distintos. Indicar la audiencia es la mejora de calidad más barata de todo este pack.
- **No envíes nunca el primer borrador.** Tú conoces la voz, la historia y la política de la sala. Copilot no. Te lleva al 80 % en segundos, y el 20 % restante sigue siendo tu trabajo.

---

*Adaptado y ampliado a partir de un artículo de LinkedIn sobre prompts cotidianos de Copilot para profesionales administrativos. Los prompts se han reescrito y ampliado.*

[Volver a Prompt Playground](../README.md#prompt-playground)
