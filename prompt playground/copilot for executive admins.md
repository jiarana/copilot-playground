# Copilot para asistentes de dirección

## Qué es

Este es el pack que el autor entrega a asistentes de dirección y profesionales administrativos después de una sesión práctica en directo. Está agrupado según el momento en que de verdad lo necesitarías. La conversación caótica que tu directivo te reenvía con un "organiza esto". El borrador que lleva en tu carpeta de borradores desde ayer. El viaje repartido en seis pestañas y tres correos de confirmación. La reunión que te perdiste. El archivo que no encuentras.

El método tiene tres pasos. Apunta, di qué forma quieres y quédate con el criterio. Todo lo que sigue es ese mismo método aplicado a un martes cualquiera.

> [!TIP]
> Sustituye todo lo que esté `[entre corchetes]` por tus datos antes de ejecutarlo. Nombres, fechas, buzones, títulos de conversaciones. Cuanto más concreto seas, menos tendrás que corregir después.

> [!NOTE]
> Copilot solo puede trabajar con lo que ve. Cuando un prompt haga referencia a una conversación, un archivo o una reunión, escribe `/` y selecciónalo. Si no, Copilot adivina, y pasarás más tiempo corrigiéndolo del que te has ahorrado.

---

## El método en tres pasos

- **Apunta.** Escribe `/` para dirigir a Copilot a un archivo, una conversación o una reunión.
- **Di qué forma quieres.** Pide un orden del día, un resumen previo, una lista de comprobación. No solo un resumen.
- **Quédate con el criterio.** Tú editas, tú decides, tú envías.

---

## Los cuatro ingredientes de un prompt que funciona

A la mayoría de los prompts que decepcionan les faltan dos de estos.

| Ingrediente | La pregunta que responde | Cómo es uno bueno |
| --- | --- | --- |
| **Objetivo** | ¿Qué quieres recibir? | Nombra el resultado. Un orden del día. Un resumen previo. Un correo de seguimiento. No "ayúdame con esto". |
| **Contexto** | ¿Para qué lo necesitas? | Quién estará en la sala, qué está en juego, qué le importa a tu directivo. Todo el mundo se lo salta, y es precisamente en lo que tú eres mejor. |
| **Fuente** | ¿Dónde debe buscar? | Escribe `/` y selecciona la conversación, el archivo o la reunión. Si no, adivina. |
| **Expectativas** | ¿Cómo debe devolverlo? | Formato, extensión, tono. Tiempos por punto. Viñetas. Menos de 200 palabras. |

### Los cuatro en un solo prompt

```
Dame un asunto para la reunión y un orden del día de 45 minutos [OBJETIVO] para la reunión de dirección de mañana, en la que la dotación de personal es el punto conflictivo [CONTEXTO], usando /Reunión de coordinación de la dirección regional [FUENTE], con tiempos por punto, y señala los dos puntos en los que todavía hay desacuerdo [EXPECTATIVAS].
```

---

## Algo que debes saber antes de empezar

Tu acceso como delegado no cambia. Puedes seguir leyendo el correo de tu directivo, enviar en su nombre y gestionar su calendario exactamente como siempre. Lo que cambia es dónde se sitúa Copilot. Los botones de Resumir y Redactar aparecen en tu propio buzón, no en el suyo. Dentro de su buzón, usa el panel de Copilot Chat e indica el buzón en tu prompt.

### Para trabajar dentro del buzón de tu directivo, indica el buzón

```
Resume los correos recientes del buzón [directivo@tuempresa.com] y dime cuáles necesitan respuesta hoy.
```

---

## 1. El orden del día a partir de una conversación caótica

Para cuando tu directivo te reenvía una conversación larga y te dice "organiza esto".

### El orden del día

```
Lee /[nombre de la conversación] y dame un asunto para la reunión y un orden del día de 45 minutos con tiempos por punto. Señala los dos puntos en los que todavía hay desacuerdo.
```

### La lectura previa

```
A partir de esa misma conversación, dime qué tiene que decidir cada asistente y enumera todo lo que sigue sin respuesta. Que quepa en una pantalla.
```

### La comprobación de asistentes

```
Según esta conversación, ¿quién tiene que estar realmente en la sala y a quién le basta con recibir las notas?
```

> [!TIP]
> Cuando Copilot no pueda acceder al contenido, pega el texto de la conversación directamente en Copilot Chat y haz la misma pregunta. El prompt no cambia. Solo cambia la fuente.

---

## 2. El borrador que no querías escribir

Para el correo que lleva en tu carpeta de borradores desde ayer.

### El volcado de ideas, empieza por aquí

```
Estas son mis notas sin pulir. Conviértelas en un correo breve, cercano y claro para nuestro [nombre del equipo]. Menos de 200 palabras y con las fechas en una lista.
[pega tus notas desordenadas; valen viñetas y frases sueltas]
```

### El cambio de tono

```
Reescribe esto para que sea directo pero no frío. Va dirigido a un vicepresidente que tiene poco tiempo y lo leerá en el móvil.
```

### El difícil

```
Tengo que decirle a un grupo que un plazo ha cambiado y que no ha sido culpa suya. Redáctalo para que sea sincero, asuma la responsabilidad y no suene a estar a la defensiva.
```

### La comprobación antes de enviar

```
Lee este borrador y dime cómo le llegará a alguien que ya está molesto. ¿Qué cambiarías?
```

---

## 3. El resumen del viaje en una página

Para el viaje repartido en seis pestañas y tres correos de confirmación.

### El resumen de una página

```
Prepara un resumen de viaje de una página para [directivo], que viaja a [ciudad] el [fechas]. Vuelos, hotel, transporte en destino, reuniones y notas sobre la zona horaria. Día a día, y tiene que caber en una pantalla.
```

### Las preguntas abiertas

```
Revisando este itinerario, ¿qué está todavía sin confirmar o falta? Dame una lista numerada de preguntas que pueda enviar en un solo mensaje.
```

### La lista de comprobación

```
Dame una lista de comprobación previa al viaje para este itinerario, ordenada según lo que tiene que ocurrir primero y lo que tiene plazo.
```

### Reunir el chat de planificación

```
Resume la conversación de planificación de /[nombre del chat de Teams], enumera lo que se acordó y dime qué sigue abierto.
```

---

## 4. Ponerse al día de la reunión que te perdiste

Funciona con los resúmenes de reuniones de Teams, los chats de Teams y las conversaciones largas de Outlook.

### Ponerse al día

```
Resume esta reunión. ¿Qué se decidió, qué sigue abierto y qué afecta a [nombre del directivo]?
```

### Solo lo mío

```
¿Surgió en esta reunión alguna tarea para [nombre del directivo] o para mí? Dame solo esas, con el responsable de cada una.
```

### El seguimiento

```
Redacta un correo de seguimiento con las decisiones y las tareas pendientes, con un responsable y una fecha de vencimiento para cada una. Que sea lo bastante breve como para leerlo en el móvil.
```

> [!TIP]
> Lo mismo en Outlook. Abre la conversación larga, usa el resumen de Copilot de la parte superior y después pregunta: ¿qué tiene que hacer realmente [nombre del directivo] aquí?

---

## 5. Encontrar cualquier cosa

Describe lo que buscas en lugar de nombrarlo. Una descripción vaga vale. Una descripción vaga es incluso mejor.

### Encontrar el archivo

```
Busca la presentación sobre [tema] que compartió [persona], probablemente en los últimos meses. No recuerdo cómo se llamaba.
```

### Encontrar la decisión

```
¿Qué decidimos sobre [tema]? Muéstrame dónde se tomó esa decisión y quién participó en ella.
```

### Encontrar el sitio

```
Localiza el sitio de SharePoint de [equipo o proyecto] y dime qué contiene realmente.
```

### Encontrar al responsable

```
¿Quién es responsable de [proceso o documento] y cuándo lo actualizó por última vez?
```

---

## Cinco más que no cupieron en la hora

### El repaso matutino

```
¿Qué ha llegado durante la noche que necesite a [nombre del directivo] antes de mediodía? Agrúpalo en lo que necesita una decisión, lo que necesita una respuesta y lo que es solo información.
```

### Preparar el encuentro con una persona

```
Mañana tengo una reunión con [nombre]. ¿Qué nos hemos intercambiado últimamente y qué sigue abierto entre nosotros?
```

### La petición escondida

```
Lee esta conversación y dime si alguien nos ha pedido algo que todavía no se ha respondido.
```

### Reducir un documento

```
Resume /[nombre del documento] en las cinco cosas que [nombre del directivo] necesita saber antes de entrar en la sala.
```

### La semana que viene

```
Revisa mi calendario de la próxima semana y dime qué reuniones siguen sin orden del día y sin lectura previa.
```

---

## Una petición sincera

Elige una sola técnica y ponla en práctica esta semana. No cinco. Una. Después cuéntale a quien esté liderando el despliegue en tu empresa si ha funcionado de verdad y qué tuviste que corregir. Esa información es lo que hace que la siguiente ronda sea mejor para todos, y es la parte que solo tú puedes aportar.

---

[Volver a Prompt Playground](../README.md#prompt-playground)
