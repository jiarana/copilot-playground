# Corrección de textos

## Qué es

Una revisión de estilo de nivel profesional para cualquier texto que hayas escrito. Pegas un fragmento y Copilot te devuelve cada cambio con su justificación, agrupado bajo encabezados, y al final la versión revisada y limpia.

Está pensado para ajustar y aclarar el texto sin aplanar tu voz.

> [!TIP]
> Sustituye `[tipo de texto]` en la primera línea por el tipo de escrito que quieres que se revise, por ejemplo `documentación técnica`, `correo a dirección` o `textos de una página web`. Cuanto más concreto seas, más fina será la corrección.

## Requisitos

- Microsoft 365 Copilot (Premium)
- Microsoft 365 Copilot Chat (gratuito)

---

## Copia rápida

```
Actúa como un redactor sénior con más de 20 años de experiencia escribiendo [tipo de texto].

Quiero que mejores mi redacción. Te compartiré un fragmento y tu tarea es corregirlo y darme recomendaciones según los criterios siguientes.

Desglosa cada cambio y explica el motivo de cada corrección antes de compartir el fragmento revisado completo. Agrúpalos con encabezados para que se lean fácilmente.

Criterios de corrección:
- Elimina lo que sobra: cada frase debe tener un propósito claro, sin palabras de más.
- Mejora la claridad de mi texto para que el lector entienda el mensaje con facilidad.
- Busca y corrige todas las faltas de ortografía y los errores gramaticales.
- Usa la voz activa en todo el texto.
- Cuando sea posible, usa sinónimos más cortos de las palabras largas, divide las frases demasiado largas, mantén los párrafos breves y usa transiciones eficaces.
- Conserva todo lo posible el tono y el estilo originales, y no añadas contenido de relleno.
- Usa un tono informal pero profesional: se admiten expresiones coloquiales siempre que se mantenga la credibilidad.

Este es mi fragmento:
[escribe aquí el fragmento]
```

---

## Qué hace cada instrucción

| Instrucción | Qué controla |
|---|---|
| `redactor sénior con más de 20 años de experiencia` | Pone el listón alto. Obtienes decisiones de criterio, no un corrector ortográfico. |
| `Desglosa cada cambio ... antes de compartir el fragmento revisado completo` | Le obliga a explicarte la corrección en lugar de reescribir en silencio. Es lo que se les escapa a la mayoría de los prompts de corrección. |
| `Agrúpalos con encabezados` | Hace que una corrección larga se pueda leer, en lugar de un bloque compacto de notas. |
| `Elimina lo que sobra` | La línea de más valor. La mayoría de los primeros borradores pierden aquí un 20 % de sus palabras. |
| `Conserva todo lo posible el tono y el estilo originales` | La salvaguarda. Sin ella, el modelo te reescribe con una voz corporativa genérica. |
| `informal pero profesional` | Cámbialo si necesitas otra cosa. `Académico`, `lenguaje sencillo` o `técnico y escueto` funcionan igual de bien. |

### Formas de adaptarlo

- **Revisión más dura:** añade `Sé contundente. Señala todo lo que suene a relleno, evasivas o jerga corporativa.`
- **Mantener la extensión:** añade `No acortes el texto. Mejóralo manteniendo aproximadamente el mismo número de palabras.`
- **Comparar versiones:** añade `Muestra la frase original y la revisada una junto a otra en una tabla.`

---

[Volver a Prompt Playground](../README.md#prompt-playground)
