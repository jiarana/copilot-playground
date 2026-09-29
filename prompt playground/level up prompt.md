# Siguiente nivel

## Qué es

Dos prompts para obtener mejores respuestas después de la primera. El primero pide a Copilot que profundice por niveles. El segundo establece unas pautas de razonamiento cuidadoso para un chat nuevo.

Úsalos cuando la primera respuesta te parezca demasiado superficial o cuando quieras que el modelo vaya más despacio y sea más deliberado.

> [!TIP]
> Para el prompt de profundización, pega la línea del nivel 2 después de la primera respuesta, y pega la del nivel 3 solo si todavía necesitas una pasada más avanzada.

## Requisitos

- Microsoft 365 Copilot (Premium)
- Microsoft 365 Copilot Chat (gratuito)

---

## Copia rápida

### Niveles de profundización

```
Prompt 1: Esa es una respuesta de nivel 1. ¿Puedes darme una versión de nivel 2 que profundice más?

Ahora llévalo al nivel 3: dame las estrategias más avanzadas que se te ocurran
```

### Instrucciones de razonamiento cuidadoso

```
Voy a hacerte una pregunta. Cuando la haga, sigue estos pasos en este orden:

1. **Interpreta la pregunta.** Antes de intentar responder, piensa en tus respuestas en silencio y de forma deliberada en cuanto recibas la pregunta. No intentes responder de inmediato. Pregúntate qué se está preguntando y si tienes dudas sobre lo que se pide. Si tienes dudas, hazme una pregunta para aclararlo. Si no, reformula la pregunta y piénsala paso a paso. Piensa en lo que yo podría estar dando por supuesto o en los conocimientos que podrían faltarme. Pregúntate continuamente si has tenido en cuenta todos los detalles, conocimientos y comparaciones relevantes necesarios para responder. Piensa también en voz alta sobre cuál podría ser tu respuesta y por qué, incluidos los hechos, las creencias y los supuestos que la respaldan. Todo esto debe ocurrir antes de intentar dar una respuesta final. Debe notarse que estás deliberando con mucho cuidado. No te precipites.

2. **Da tu primera respuesta.** A continuación, escribe tu primera respuesta basándote en el razonamiento anterior y después di: "Esta es mi primera respuesta. Ahora voy a comprobarla."

3. **Comprueba tu respuesta.** Revisa tu primera respuesta con cuidado y sin prisa. Plantéate si podrías estar equivocado. NO te limites a matizar y añadir advertencias. En su lugar, examina las pruebas que respaldan tu primera respuesta y busca pruebas nuevas o distintas que puedan contradecirla. Piensa en voz alta, con cuidado y con todo el rigor posible.

4. **Da tu respuesta final.** Después de pensar con cuidado y deliberar mucho más a fondo, quiero que me des tres cosas: (1) tu respuesta revisada (o confirmada), (2) una lista de los factores más importantes que tuviste en cuenta al dar tu respuesta y (3) los motivos por los que esta respuesta es mejor que las otras que no elegiste, incluidas las incorrectas.

No incluyas tu proceso de razonamiento en esta respuesta que acabas de escribir o recibirás un aviso. Tienes 3 avisos y después perderás tu trabajo. Responde solo cuando hayas hecho todo lo anterior.
```

---

## Qué hace cada instrucción

| Instrucción | Qué controla |
|---|---|
| `versión de nivel 2` | Indica que la primera respuesta era demasiado superficial y pide más profundidad sin cambiar la tarea. |
| `nivel 3` | Empuja al modelo a dar las estrategias más avanzadas que pueda generar. |
| `Interpreta la pregunta` | Obliga al modelo a revisar los supuestos antes de responder. |
| `Comprueba tu respuesta` | Pide al modelo que ponga a prueba su primera respuesta en lugar de quedarse con la primera que parezca plausible. |
| `Da tu respuesta final` | Estructura la respuesta final en torno a la respuesta, los factores clave y las alternativas descartadas. |

---

[Volver a Prompt Playground](../README.md#prompt-playground)
