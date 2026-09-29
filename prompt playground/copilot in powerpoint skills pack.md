# Pack de skills de Copilot en PowerPoint

## Qué es

Copilot en PowerPoint te permite guardar skills personalizadas: instrucciones reutilizables que invocas por su nombre en lugar de volver a escribir la misma petición cada vez. Este pack te ofrece 12 skills para el trabajo con diapositivas que el autor hace con más frecuencia: desde aplicar la marca y ordenar diapositivas hasta resúmenes, notas del orador, convertir un documento en una presentación, reescrituras en lenguaje sencillo, unificar tipografías, accesibilidad y preparar una presentación para compartirla fuera. Añádelas, ajusta un par de marcadores y empieza a usarlas.

Cada skill es una pequeña carpeta con un único archivo `SKILL.md` dentro. Ese es el formato que lee Copilot: una cabecera breve arriba (el nombre y cuándo usarla) y un conjunto de instrucciones sencillas debajo.

> [!TIP]
> Solo dos skills necesitan una modificación antes de usarlas. En `apply-brand-template`, cambia las tipografías y los colores de ejemplo por los tuyos. En `customer-ready-pass`, escribe el texto de aviso legal aprobado. Todas las demás funcionan tal cual.

> [!NOTE]
> Los nombres de las skills (`name`) se mantienen en inglés para que coincidan con los nombres de las carpetas y con las menciones del tipo `@executive-summary-slide`. Las descripciones y las instrucciones están traducidas.

---

## Cómo activarlo en PowerPoint

El autor grabó todo el proceso de configuración, desde activar las skills personalizadas hasta escribir las tuyas propias:

**Vídeo (en inglés): [How to Set Up Copilot Skills in PowerPoint (and Build Your Own)](https://www.youtube.com/watch?v=0CA-k3FtPX0)**

> [!IMPORTANT]
> Para esto necesitas Copilot en PowerPoint. Si no ves Copilot en la aplicación, no forma parte de tu suscripción de Microsoft 365 o tu organización todavía no lo ha activado.

Hay tres formas de añadir una skill. Elige la que corresponda a cómo te ha llegado.

### Opción 1: pégala en el formulario Agregar skill

Es lo más fácil cuando copias una skill directamente de esta página. No hay que descargar nada.

1. Abre una presentación y abre el panel de Copilot.
2. Selecciona el **+** del campo de prompt y después **Elegir skills**.
3. Desplázate hasta el final de la lista y selecciona **Administrar skills**.
4. Selecciona **Agregar skill**.
5. Rellena **Título**, **Nombre**, **Descripción** e **Instrucciones** y selecciona **Agregar**.

Cada skill de esta página está escrita como un bloque `SKILL.md`, que encaja directamente con ese formulario. El `name` de la cabecera va en Nombre, la `description` va en Descripción, y todo lo que hay debajo del `---` de cierre son las Instrucciones. El Título es solo el nombre visible.

PowerPoint guarda la skill en la carpeta de skills de tu OneDrive, así que la carpeta se crea de todas formas.

> [!IMPORTANT]
> El cuadro **Instrucciones** admite un máximo de 1024 caracteres. Todas las skills de este pack están escritas para caber. Copia desde el encabezado `#` de la parte superior del bloque hasta la última línea y pega todo ese fragmento en Instrucciones.

### Opción 2: sube el archivo de la skill

Es lo más fácil cuando alguien te pasa un `SKILL.md` o una carpeta de skill comprimida.

1. Ve a **Administrar skills** y después a **Agregar skill**.
2. Arrastra y suelta el archivo o búscalo. Puedes añadir varios a la vez.
3. Se guarda en OneDrive y aparece en la lista de skills. Selecciona **Actualizar** si no aparece.

> [!NOTE]
> Las skills comprimidas admiten archivos de texto como `md`, `txt`, `csv`, `json`, `xml`, `html`, `svg`, `py` y `js`. No se admiten imágenes, PDF ni archivos comprimidos anidados.

### Opción 3: copia tú mismo las carpetas en OneDrive

Es la mejor opción cuando añades varias a la vez, como este pack completo.

1. En el panel de Copilot, abre el menú de configuración, los **...** de la esquina superior derecha.
2. Selecciona **Administrar skills**.
3. Selecciona **Skills personalizadas**.
4. Selecciona **Crear carpeta de OneDrive**. Copilot crea la carpeta de skills en tu OneDrive.
5. Selecciona **Abrir carpeta de skills** para abrirla.
6. Copia dentro tus carpetas de skills. Una carpeta por skill, cada una con su `SKILL.md`, y el nombre de la carpeta tiene que coincidir con el `name` del archivo.
7. De vuelta en el cuadro de diálogo **Skills personalizadas**, selecciona **Actualizar** para que Copilot las detecte.

### Usar una skill

- Selecciona el menú **+** del campo de prompt de Copilot, elige **Elegir skills** y selecciona la que quieras.
- O llámala directamente desde tu prompt con una mención @, como `@executive-summary-slide`.
- Activa o desactiva cualquier skill desde **Administrar skills**.

> [!NOTE]
> ¿Has añadido o cambiado el nombre de una skill en OneDrive? Pulsa **Actualizar** en el cuadro de diálogo Skills personalizadas para que Copilot la vea. Para editar o eliminar una, usa **Editar** o **Eliminar** bajo la skill en **Administrar skills**. Para ocultar una skill sin eliminarla, cambia el nombre de su carpeta para que deje de coincidir con el `name` de su `SKILL.md`. Copilot omite las carpetas que no coinciden.

> [!TIP]
> Los nombres exactos de los menús pueden variar ligeramente según el idioma de tu Office. ¿Quieres la guía oficial con capturas de cada paso? Consulta [Skills de Copilot en PowerPoint](https://support.microsoft.com/es-es/powerpoint/copilot/copilot-in-powerpoint-skills) en el Soporte técnico de Microsoft. Especificación del formato (en inglés): [Agent Skills specification](https://agentskills.io/specification).

---

## Qué incluye el pack

| Skill | Qué hace |
|---|---|
| **apply-brand-template** | Aplica a las diapositivas tus tipografías, colores y logotipo |
| **fix-this-slide** | Ordena el diseño, el espaciado y las viñetas de una diapositiva |
| **executive-summary-slide** | Genera una diapositiva resumen de toda la presentación |
| **speaker-notes** | Escribe las notas del orador en el panel de notas |
| **doc-to-deck** | Convierte un documento o unas notas en una presentación estructurada |
| **de-jargon** | Reescribe las diapositivas en lenguaje sencillo |
| **tighten-copy** | Acorta las viñetas y elimina el relleno |
| **consistency-check** | Revisa tipografías, colores, mayúsculas y espaciado |
| **fix-fonts** | Cambia todas las tipografías a Segoe UI y reajusta el texto |
| **accessibility-pass** | Texto alternativo, contraste, tamaño de letra y orden de lectura |
| **customer-ready-pass** | Elimina el contenido interno y prepara una presentación para compartir |
| **qbr-builder** | Estructura el contenido como una revisión trimestral de negocio (QBR) |

---

## Skills

### apply-brand-template

Aplica tu identidad visual a las diapositivas seleccionadas. Edita primero los valores de marca de la parte superior para que use tus tipografías, colores y la posición de tu logotipo.

```markdown
---
name: "apply-brand-template"
description: "Úsala cuando el usuario pida aplicar la marca, adaptar las diapositivas a la marca, reformatearlas según la plantilla o unificar el formato de las diapositivas seleccionadas o de toda la presentación. Aplica una identidad visual definida (tipografías, colores, diseño, logotipo)."
---

# Aplicar plantilla de marca

Aplica un aspecto de marca coherente a las diapositivas seleccionadas o, si no hay ninguna, a toda la presentación.

## Valores de marca, EDÍTALOS
- Título: Segoe UI, 32 pt, negrita
- Cuerpo: Segoe UI, 18 pt, normal
- Color principal de títulos y detalles: #2563EB
- Color secundario: #505050
- Fondo: #FFFFFF
- Logotipo: abajo a la derecha, pequeño, en todas salvo la portada

## Qué hacer
1. Títulos: tipografía, tamaño y color principal indicados.
2. Cuerpo: tipografía y tamaño indicados. Color secundario para el texto secundario.
3. Unifica las viñetas. Máximo 6 por diapositiva, de una línea.
4. Alinea los objetos a una cuadrícula e iguala el espacio entre ellos.
5. Mantén márgenes uniformes; el contenido nunca toca el borde.
6. Cambia solo el formato. Conserva todo el contenido y su sentido.
7. No toques las imágenes a sangre ni los diseños personalizados intencionados. Corrige solo sus tipografías y colores.
8. Termina con un resumen de una línea de lo que ha cambiado.
```

---

### fix-this-slide

La skill para que "esta diapositiva parezca hecha a propósito". Aplícala a una diapositiva desordenada y deja que alinee, espacie y ajuste.

```markdown
---
name: "fix-this-slide"
description: "Úsala cuando el usuario diga 'arregla esta diapositiva', 'ordena esta diapositiva' o quiera ajustar el diseño, el espaciado, la alineación y las viñetas de una sola diapositiva sin cambiar el mensaje."
---

# Arreglar esta diapositiva

Ordena la diapositiva actual o seleccionada para que parezca intencionada y despejada.

## Qué hacer
1. Alinea todos los objetos (izquierda, arriba o centro, según convenga) a una cuadrícula uniforme.
2. Iguala el espacio horizontal y vertical entre elementos.
3. Máximo 6 viñetas; reescribe cada una en una línea (unas 10 palabras) sin perder el sentido.
4. Crea una jerarquía clara: un título dominante y después los puntos de apoyo.
5. Elimina texto redundante o duplicado y fusiona ideas que se solapen.
6. Deja aire al texto y que nada se salga de la diapositiva.

## Resultado
La diapositiva ordenada y una nota de una línea con las 2 o 3 correcciones principales.

## Salvaguardas
- Conserva el mensaje principal y todos los datos y cifras clave.
- No cambies colores ni tipografías salvo que estén claramente mal o sean incoherentes.
- No añadas contenido que el usuario no haya aportado.
```

---

### executive-summary-slide

Lee toda la presentación y crea una única diapositiva resumen que un directivo pueda leer en 20 segundos.

```markdown
---
name: "executive-summary-slide"
description: "Úsala cuando el usuario pida una diapositiva de resumen ejecutivo, un resumen en una diapositiva, una diapositiva de conclusiones clave o una diapositiva de 'y esto qué significa' que resuma toda la presentación."
---

# Diapositiva de resumen ejecutivo

Lee toda la presentación y genera una única diapositiva resumen lista para directivos.

## Qué hacer
1. Revisa todas las diapositivas para extraer el relato principal.
2. Crea una diapositiva titulada "Resumen ejecutivo" (insértala como diapositiva 2, tras la portada).
3. Incluye:
   - 3 conclusiones clave, de una línea, centradas en resultados y sin jerga.
   - Un siguiente paso recomendado o la petición, claro y concreto.
4. Empieza por el "y esto qué significa", no por el proceso. Escribe para un directivo ocupado que solo leerá esta diapositiva.

## Resultado
Una diapositiva resumen nueva. En el chat, indica de qué diapositivas sale cada conclusión.

## Salvaguardas
- Basa cada conclusión en contenido que esté en la presentación; no inventes afirmaciones ni cifras.
- Una sola diapositiva. Si no cabe, prioriza los 3 puntos de mayor impacto.
```

---

### speaker-notes

Escribe un guion real en el panel de notas para que no tengas que leer las viñetas de la pantalla.

```markdown
---
name: "speaker-notes"
description: "Úsala cuando el usuario pida escribir, añadir o mejorar las notas del orador de las diapositivas, o quiera un guion para la presentación."
---

# Notas del orador

Escribe notas del orador concisas en el panel de notas de cada diapositiva.

## Qué hacer
1. Para cada diapositiva, escribe notas que:
   - Empiecen por la idea clave de la diapositiva.
   - Añadan 2 o 3 puntos de apoyo que el orador pueda desarrollar.
   - Incluyan una frase de transición natural hacia la siguiente.
2. Apunta a unos 30-45 segundos de intervención por diapositiva (unas 60-90 palabras).
3. Usa un tono oral y conversacional: frases cortas, primera persona, sin abreviaturas tipo viñeta.
4. Escríbelas en el panel de notas, no en la diapositiva.

## Resultado
Notas añadidas al panel de notas de cada diapositiva. Termina con el tiempo total estimado de la presentación.

## Salvaguardas
- Las notas deben complementar la diapositiva, no leer las viñetas en voz alta.
- No pongas las notas en la diapositiva visible.
- Mantén las afirmaciones coherentes con la diapositiva.
```

---

### doc-to-deck

Convierte un documento, unas notas o un contenido pegado en un esquema de diapositivas limpio sobre el que construir.

```markdown
---
name: "doc-to-deck"
description: "Úsala cuando el usuario quiera convertir un documento, unas notas, un esquema o un contenido pegado en diapositivas: 'haz una presentación con esto', 'prepara diapositivas a partir de esto', 'convierte este documento en una presentación'."
---

# De documento a presentación

Convierte el contenido de origen en un esquema de diapositivas limpio y con una estructura lógica.

## Qué hacer
1. Lee el contenido e identifica los temas principales.
2. Crea una presentación con esta estructura:
   - Portada (tema y subtítulo).
   - Índice (de 3 a 6 secciones).
   - Una diapositiva por idea clave: título claro y 3-5 viñetas de una línea.
   - Diapositiva de cierre o siguientes pasos.
3. Entre 5 y 7 diapositivas de contenido salvo que el usuario indique otra extensión.
4. Redacta las viñetas de forma paralela y orientada a la acción.
5. Indica dónde reforzaría una diapositiva un gráfico, un diagrama o una imagen (con una línea de marcador).

## Resultado
Un borrador de presentación. En el chat, da un esquema rápido (títulos) para que el usuario lo apruebe o reordene.

## Salvaguardas
- Usa solo los datos de la fuente y señala lo que hayas deducido.
- No sobrecargues las diapositivas; pasa el detalle a las notas si hace falta.
```

---

### de-jargon

Reescribe el texto de las diapositivas en lenguaje sencillo para una audiencia no técnica o directiva, sin cambiar los hechos.

```markdown
---
name: "de-jargon"
description: "Úsala cuando el usuario pida simplificar el lenguaje de las diapositivas, eliminar la jerga, pasar la presentación a lenguaje sencillo o hacer el texto comprensible para una audiencia no técnica o directiva."
---

# Sin jerga

Reescribe el texto de las diapositivas en un lenguaje sencillo y directo que pueda seguir alguien no especialista.

## Qué hacer
1. Sustituye la jerga, las siglas y las abreviaturas internas por términos sencillos (desarrolla la sigla la primera vez si tiene que quedarse).
2. Convierte las expresiones abstractas o de moda en lenguaje concreto y cotidiano.
3. Prefiere la voz activa y las frases cortas.
4. Mantén la exactitud técnica: simplifica las palabras, no los hechos.
5. Aplícalo a títulos y viñetas de las diapositivas seleccionadas (o de toda la presentación).

## Resultado
Las diapositivas reescritas y una lista breve de los términos de jerga cambiados y por qué se cambiaron.

## Salvaguardas
- Nunca cambies el sentido ni la afirmación de fondo.
- Mantén exactos los nombres de productos, los términos legales obligatorios y las métricas.
- Si un término es imprescindible y no se puede simplificar, consérvalo y añade una aclaración sencilla de 3 a 5 palabras.
```

---

### tighten-copy

Elimina el relleno y las viñetas largas para que la diapositiva se lea de un vistazo. Ideal antes de cualquier revisión con directivos.

```markdown
---
name: "tighten-copy"
description: "Úsala cuando el usuario pida ajustar el texto de las diapositivas, acortar las viñetas, eliminar el relleno o hacer el texto más contundente y fácil de leer de un vistazo."
---

# Ajustar el texto

Hace que el texto de las diapositivas sea escueto y fácil de leer de un vistazo sin perder el sentido.

## Qué hacer
1. Reduce cada viñeta a menos de unas 10 palabras.
2. Elimina el relleno ("con el fin de", "cabe destacar que", "básicamente", "muy", "realmente").
3. Empieza cada viñeta con un verbo fuerte o el sustantivo clave.
4. Elimina las viñetas redundantes y fusiona los puntos que se solapen.
5. Máximo 6 viñetas por diapositiva. Si hay más, divide o pasa el detalle a las notas del orador.
6. Redacta de forma paralela las viñetas de una misma diapositiva.

## Resultado
Las diapositivas ajustadas y una nota de una línea sobre cuánto se ha recortado.

## Salvaguardas
- Conserva todos los datos, las cifras y el mensaje principal.
- No elimines un punto por completo salvo que sea un duplicado real; condénsalo.
```

---

### consistency-check

Revisa toda la presentación en busca de esas pequeñas incoherencias que la hacen parecer hecha con prisa: tipografías mezcladas, colores fuera de la paleta, mayúsculas, espaciado.

```markdown
---
name: "consistency-check"
description: "Úsala cuando el usuario pida revisar la presentación en busca de incoherencias (tipografías, colores, mayúsculas o espaciado que no coinciden, o diapositivas que no siguen la marca) y quiera un informe o las correcciones."
---

# Revisión de coherencia

Revisa toda la presentación en busca de incoherencias visuales y de texto.

## Revisa cada diapositiva y señala
1. Tipografías: distintos tipos de letra o tamaños para el mismo elemento.
2. Colores: títulos o detalles fuera de la paleta, color de texto incoherente.
3. Mayúsculas: títulos con mayúscula en cada palabra mezclados con mayúscula solo inicial.
4. Viñetas: estilos, sangrías o puntuación incoherentes.
5. Alineación: objetos fuera de la cuadrícula, márgenes o espacios desiguales.
6. Terminología: la misma cosa con nombres distintos en diapositivas distintas.

## Después
- Devuelve una lista por diapositiva: número, problema y corrección sugerida.
- Pregunta "¿Quieres que aplique todas las correcciones?" y actúa solo si lo confirma. Si el usuario ya pidió corregirlas, aplícalas directamente.
- No cambies decisiones de diseño intencionadas, como otro estilo para los separadores de sección. Indícalas aparte.
```

---

### fix-fonts

Cambio de tipografía y comprobación de ajuste. Toma una presentación que ha acumulado cuatro tipografías distintas al pasar por seis personas, la pone entera en Segoe UI y después la revisa para asegurarse de que nada se ha desbordado, encogido o quedado suelto en su cuadro.

```markdown
---
name: "fix-fonts"
description: "Úsala cuando pida a Copilot unificar, sustituir, arreglar u ordenar las tipografías de la presentación de PowerPoint actual. Cambia el texto editable de las diapositivas a Segoe UI y ajusta los tamaños para que el texto mantenga su escala visual anterior y quepa en su contenedor."
---

# Arreglar tipografías

1. Pon Segoe UI como fuente del tema para que las diapositivas nuevas la hereden.
2. Sustituye en diapositivas, diseños, patrones y notas: Calibri, Georgia, Arial y Aptos por Segoe UI; Calibri Light por Segoe UI Light. Conserva las fuentes de símbolos como Wingdings.
3. Deja vacías las fuentes de Asia oriental y escritura compleja (respaldo por idioma).
4. Conserva negrita, cursiva, color, alineación, viñetas, espaciado, mayúsculas y jerarquía.
5. Revisa cada texto: distingue desbordamiento de texto pequeño o suelto en su cuadro.
6. Aumenta el cuerpo menor de 10 pt si cabe. Deja pequeños pies, citas, textos legales y números de página.
7. Revisa saltos, recortes, desbordamientos y choques. Mantén el texto en su contenedor; mueve objetos solo si no cabe.
8. Ignora solapamientos decorativos (círculos, barras tras el texto).
9. Cambia solo tipografías y tamaños. Nunca reescribas ni recortes contenido.
10. Informa de lo cambiado y de lo que no pudiste cambiar (p. ej., texto en imágenes).
```

> [!TIP]
> ¿Quieres cambiar a otra tipografía? Modifica los dos nombres de fuente del paso 2 y el resto sigue funcionando.

---

### accessibility-pass

Añade texto alternativo, comprueba el contraste y el tamaño de letra, y confirma un orden de lectura lógico para que la presentación funcione para todo el mundo.

```markdown
---
name: "accessibility-pass"
description: "Úsala cuando el usuario pida una revisión de accesibilidad: texto alternativo para las imágenes, contraste de color, orden de lectura y tamaños de letra legibles en toda la presentación."
---

# Revisión de accesibilidad

Hace que la presentación sea más accesible e inclusiva.

## Qué hacer
1. Texto alternativo: conciso y descriptivo en cada imagen, gráfico y elemento no decorativo. Marca los decorativos como tales.
2. Contraste: señala las combinaciones de texto y fondo por debajo del contraste WCAG AA y sugiere un color que cumpla.
3. Tamaño de letra: señala cuerpo menor de 18 pt y títulos menores de 28 pt (difíciles de leer desde el fondo).
4. Orden de lectura: comprueba que el orden de tabulación y de lectura de cada diapositiva es lógico.
5. Enlaces y color: que el significado no dependa solo del color; añade etiquetas donde ocurra.

## Resultado
Una lista por diapositiva de lo corregido y de lo que necesita una decisión del usuario (como elegir colores de contraste).

## Salvaguardas
- El texto alternativo debe describir el contenido o su propósito, no decir solo "imagen".
- No cambies el estilo de toda la presentación; haz solo correcciones de accesibilidad concretas.
```

---

### customer-ready-pass

Toma una presentación interna y la prepara para compartirla: elimina las notas internas y las diapositivas ocultas, señala todo lo sensible y añade un aviso legal. Escribe primero el texto de aviso legal aprobado.

```markdown
---
name: "customer-ready-pass"
description: "Úsala cuando el usuario quiera preparar una presentación para clientes o para compartirla fuera: eliminar notas internas, quitar marcas de confidencialidad, añadir un aviso legal y confirmar que no queda nada de uso exclusivamente interno."
---

# Lista para el cliente

Prepara una presentación interna para compartirla fuera con seguridad.

## Qué hacer
1. Elimina las notas del orador internas, las diapositivas ocultas, las marcas BORRADOR o INTERNO y los comentarios internos.
2. Señala lo confidencial (precios internos, fechas de hoja de ruta bajo NDA, nombres de terceros o métricas internas) y pregunta antes de eliminarlo.
3. Añade un pie o una diapositiva final con un aviso legal. EDITA el texto aprobado: "Solo para debate. Sujeto a cambios."
4. Comprueba que la diapositiva final tiene los datos de contacto correctos del ponente.
5. Confirma que no queda ningún PENDIENTE, texto de marcador ni lorem ipsum.
6. Si dudas de si algo es confidencial, pregunta. Nunca des por hecho que es seguro dejarlo.
7. Elimina solo lo interno o sensible, nunca contenido sustancial.
8. Respeta las etiquetas de confidencialidad y avisa si el archivo parece clasificado.
9. Devuelve la presentación limpia y una lista de todo lo eliminado o señalado.
```

---

### qbr-builder

Estructura el contenido como una revisión trimestral de negocio (QBR) ordenada: logros, estado, pipeline, riesgos y peticiones.

```markdown
---
name: "qbr-builder"
description: "Úsala cuando el usuario pida crear o estructurar una presentación de QBR (revisión trimestral de negocio), o reorganizar contenido con el esquema de una QBR: logros, pipeline/estado, riesgos y peticiones."
---

# Generador de QBR

Estructura el contenido como una presentación ordenada de revisión trimestral de negocio.

## Crea este esquema
1. Portada: cuenta, trimestre, ponente.
2. Resumen ejecutivo: 3 resultados destacados del trimestre.
3. Logros y avances: lo entregado, con métricas si existen.
4. Adopción o estado: situación actual frente a objetivos (uso, licencias, hitos).
5. Pipeline u hoja de ruta: iniciativas clave del próximo trimestre.
6. Riesgos y bloqueos: lista honesta con responsable y mitigación.
7. Peticiones y siguientes pasos: peticiones concretas y acciones acordadas con fechas.

## Reglas
- Coloca el contenido existente o pegado en su sección. Marca los huecos con "[FALTAN DATOS]".
- Un mensaje por diapositiva. Pasa el detalle a las notas del orador.
- Empieza por los resultados y el valor, no por la actividad.
- Nunca inventes métricas, fechas ni compromisos. Usa marcadores.
- Acompaña siempre cada riesgo de una mitigación.
- Termina con la lista de marcadores "[FALTAN DATOS]" por completar.
```

---

[Volver a Prompt Playground](../README.md#prompt-playground)
