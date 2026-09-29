# The Copilot Chronicle

## Qué es

Un resumen diario de noticias de IA con formato de periódico, creado para Microsoft Copilot Cowork. Cada mañana revisa las últimas noticias externas del sector de la IA sobre Microsoft Copilot, Anthropic, Google y OpenAI, además de las novedades internas de tu organización, que obtiene a través de las señales de Microsoft Graph del correo, Teams y Viva Engage.

El resultado es un periódico en HTML con formato que te llega directamente por correo, pensado para leerlo en 5 minutos con el café.

> [!TIP]
> Antes de ejecutarlo, sustituye tu dirección de correo, tu puesto, los términos de búsqueda internos, los boletines, los resúmenes y los canales de comunidad por los tuyos.

---

## Copia rápida

```
---
name: daily-news
description: Genera "The Copilot Chronicle", un resumen matutino diario en HTML con formato de periódico que cubre noticias externas del sector de la IA (Microsoft Copilot, Anthropic/Claude, Google/Gemini, OpenAI/ChatGPT y el sector de la IA en general) y novedades internas obtenidas a través de las señales de Microsoft Graph del correo, Teams y Viva Engage. El resultado es un correo HTML con cabecera, cuerpo a dos columnas, línea de fecha, noticia principal con letra capital, tres bandas de sección, teletipo y pie de página, enviado directamente a ti. Cada noticia enlaza a su fuente.

---

## Cuándo usarlo

Actívalo cuando le pidas a Copilot:

- "Ejecuta mis noticias diarias"
- "Genera mis noticias de la mañana"
- "Envíame mi resumen diario de noticias"
- "Crea el Copilot Chronicle de hoy"
- "Ejecuta el Chronicle"
- "Dame mis noticias de IA de hoy"

---

## Cuándo NO usarlo

- Búsquedas de noticias puntuales → usa directamente la búsqueda web
- Resúmenes diarios de tu agenda y tu bandeja de entrada → usa tu prompt de resumen diario
- Comunicaciones con partes interesadas o con la dirección → usa un prompt de comunicaciones con partes interesadas
- Informes de cuentas concretas → usa tu prompt de informe diario para dirección

---

## Flujo de trabajo

### Paso 1: determina la fecha de hoy

Establece la fecha de la edición en tu zona horaria local. Usa este formato de nombre de archivo y de asunto:

- **Nombre de archivo:** `output/the-copilot-chronicle-AAAA-MM-DD.html`
- **Asunto:** `The Copilot Chronicle — [día de la semana], [DD] de [mes] de [AAAA]`

---

### Paso 2: reúne la información (en paralelo)

**Fuentes externas (búsqueda web, últimas 24 a 48 horas):**

- Noticias de Microsoft Copilot y Microsoft 365 Copilot
- Noticias de Anthropic y Claude
- Noticias de Google Gemini
- Noticias de OpenAI y ChatGPT
- Noticias del sector de la IA y del ámbito empresarial

**Fuentes internas (señales de Microsoft Graph a través de Outlook y Teams):**

> [!IMPORTANT]
> Sustituye los marcadores siguientes por tus propios boletines internos, resúmenes, canales de comunidad y novedades del equipo. Copilot usará Microsoft Graph para extraer información de tu correo de Outlook y de tu actividad en Teams según lo que indiques aquí.

- `{Añade aquí el nombre de tu boletín interno o de tus avisos para el equipo comercial}`
- `{Añade aquí el nombre del resumen de tu equipo o de la reunión semanal}`
- `{Añade aquí tu comunidad interna o tu canal de Viva Engage}`
- `{Añade los correos de novedades de producto o las comunicaciones de la dirección que quieras incluir}`
- `{Añade las comunicaciones de eventos o formación relevantes para tu puesto}`

Guarda el `webLink` de Outlook de cada elemento interno para que los titulares enlacen directamente a la fuente.

---

### Paso 3: selecciona las noticias

| Sección | Qué incluir |
|---|---|
| **Noticia principal** | La noticia más importante de Copilot o del sector de la IA de las últimas 24 horas. Incluye antetítulo, titular, entradilla, cuerpo con letra capital y una cita destacada de una fuente primaria. |
| **Actualidad del sector de la IA** | De 4 a 6 noticias sobre Anthropic, Google, OpenAI, Microsoft y el sector en general. Diseño a dos columnas. |
| **Desde la redacción interna** | De 3 a 8 elementos internos de Outlook y Teams relevantes para tu puesto. Enlaza a la fuente cuando esté disponible. |
| **Breves de Copilot** | De 2 a 4 notas breves sobre precios, certificaciones, gobernanza, administración o novedades de versiones. |
| **Teletipo** | De 6 a 10 titulares breves de todas las categorías. |

Si una sección no tiene contenido nuevo, redúcela u omítela. Nunca te inventes noticias.

---

### Paso 4: genera el HTML

Referencias de estilo para el diseño de periódico:

- **Fondo:** `#f5efe1` | **Papel:** `#fbf6e9` | **Tinta:** `#1a1a1a` | **Acento:** `#a02a2a`
- **Tipografías:** Georgia / Old Standard TT con serifa
- **Cabecera:** "The Copilot Chronicle" con el lema *Veritas · Productivitas · Intelligentia*
- **Línea de fecha:** día de la semana, fecha completa, contexto de puesto o equipo, "Precio: un café"
- **Noticia principal:** antetítulo, titular h2 enlazado, entradilla en cursiva, primer párrafo con letra capital y cita destacada con una línea roja a la izquierda
- **Bandas de sección:** barra negra, texto crema, con espaciado entre letras
- **Diseño del cuerpo:** dos columnas mediante `column-count: 2`
- **Pie de página:** doble línea superior, todas las publicaciones de origen enlazadas
- **Enlaces al pasar el ratón:** subrayado rojo `#a02a2a`

---

### Paso 5: enlaces (obligatorio)

- **Noticias externas:** enlaza el titular, la firma y un enlace final "Leer más →"
- **Elementos internos de la redacción:** enlaza al `webLink` de Outlook
- **Elementos de Teams:** enlaza a la URL del chat, del canal o de la reunión
- **Pie de página:** enumera y enlaza todas las publicaciones de origen
- Nunca te inventes un enlace. Si no hay URL disponible, muestra texto sin enlace.

---

### Paso 6: guarda y envía

1. Escribe el archivo en `output/the-copilot-chronicle-AAAA-MM-DD.html`
2. Comprueba que el archivo existe
3. Envíalo por correo:
   - **Para:** `{escribe aquí tu dirección de correo}`
   - **Asunto:** `The Copilot Chronicle — [día de la semana], [DD] de [mes] de [AAAA]`
   - **Cuerpo:** el archivo HTML guardado
   - **Tipo de contenido:** HTML

---

### Paso 7: confirma

Responde con la fecha de la edición, el número de noticias por sección y la confirmación de que se ha enviado por correo. No pegues el HTML en el chat.

---

## Normas de estilo

- Cada noticia debe proceder de una fuente real. Nunca te inventes noticias, nombres, cifras ni citas.
- Voz nítida y con un punto de ingenio. Los titulares pueden ser llamativos, pero nunca ridículos.
- Limita los textos breves a entre 2 y 4 frases. La noticia principal tiene 3 párrafos cortos y una cita destacada.
- Si una sección no tiene nada nuevo, omítela en lugar de rellenarla.

---

## Salvaguardas

- No envíes el correo hasta que el archivo HTML exista en `output/`
- No te inventes valores de `webLink` de Outlook. Enlaza solo elementos devueltos por consultas reales a Graph.
- No incluyas evaluaciones de desempeño de personas con nombre.
- No incluyas datos personales ni de salud extraídos de correos.
```

---

[Volver a Prompt Playground](../README.md#prompt-playground)
