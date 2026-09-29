# Ensayo general ante las partes interesadas

## Qué es

Una prueba previa al envío para cualquier cosa que estés a punto de presentar ante una sala. Copilot revisa los últimos 60 días de tus correos, conversaciones de Teams, notas de reuniones y documentos, y después interpreta a tres audiencias a la vez: el patrocinador ejecutivo que tiene que financiarlo, el cliente escéptico que tiene que comprarlo y el equipo que tiene que ejecutarlo.

Obtienes un mapa de reacciones que muestra qué apoya, qué cuestiona y qué malinterpreta cada grupo, con las fuentes de trabajo reales detrás de cada reacción. Después reescribe tu mensaje para que convenza a los tres, con un máximo de 300 palabras.

Ejecútalo antes de enviar una propuesta, un anuncio o una recomendación que necesite el respaldo de personas que no comparten las mismas prioridades.

> [!TIP]
> Sustituye el marcador entre corchetes por tu propuesta, anuncio o recomendación real. Pega el borrador de tu mensaje después del prompt para que Copilot tenga algo concreto que reescribir. Si tus tres audiencias son distintas, nómbralas, por ejemplo un miembro del consejo, un partner y un revisor de cumplimiento normativo.

---

## Copia rápida

```
Me estoy preparando para compartir [propuesta, anuncio o recomendación]. Revisa los correos, conversaciones de Teams, notas de reuniones y documentos relacionados de los últimos 60 días. Simula cómo reaccionarían un patrocinador ejecutivo, un cliente escéptico y el equipo responsable de la ejecución: identifica qué apoyará, qué cuestionará y qué malinterpretará cada audiencia; cita las fuentes de trabajo que respaldan cada reacción; y después reescribe mi mensaje para que aborde las tres perspectivas sin superar las 300 palabras.
```

---

## El prompt, parte por parte

### Qué estás poniendo a prueba

Nombra lo que estás a punto de compartir.

- `[propuesta, anuncio o recomendación]`

Sé concreto. "La propuesta de migración de la plataforma del tercer trimestre" es mejor que "mi propuesta". Cuanto más preciso sea el tema, mejor delimitará Copilot qué conversaciones y documentos importan de verdad.

---

### Fuentes que revisar

Los últimos 60 días de:

| Fuente | Qué aporta |
|---|---|
| Correos | Posturas declaradas, objeciones anteriores, quién ha puesto ya reparos |
| Conversaciones de Teams | La versión sin filtros, preocupaciones secundarias, la opinión real |
| Notas de reuniones | Compromisos adquiridos, preguntas que quedaron abiertas |
| Documentos | El alcance, las cifras y los detalles con los que te van a contrastar |

> [!NOTE]
> Sesenta días es el valor predeterminado porque suele cubrir un ciclo de planificación completo sin arrastrar contexto desactualizado. Amplíalo si la decisión tiene un historial más largo. Redúcelo si la situación ha cambiado hace poco.

---

### Las tres audiencias

Copilot simula cada una por separado, no como una media combinada.

**Patrocinador ejecutivo**
Le importan el resultado, el coste, el riesgo y si esto compite con algo que ya ha financiado.

**Cliente escéptico**
Le importa si resuelve su problema, cuánto le cuesta y qué pasa si no funciona.

**Equipo de ejecución**
Le importan el alcance, si los plazos son realistas, las dependencias y quién va a hacer realmente el trabajo.

---

### Qué debe incluir cada reacción

Para cada audiencia, tres cosas:

| Reacción | Qué significa |
|---|---|
| Apoyo | Con qué estarán de acuerdo de inmediato y por qué |
| Cuestionamiento | En qué insistirán antes de comprometerse |
| Malentendido | Dónde tu redacción invita a sacar una conclusión equivocada |

La columna de malentendidos es la que la gente se salta. Y suele ser donde la reunión se tuerce.

---

### Cita las fuentes

Cada reacción tiene que remitir a algo real: un correo, una conversación, una reunión o un documento concreto. Esta es la parte que mantiene honesto el ejercicio.

Si Copilot no puede citar una fuente para una reacción, trátala como una suposición y dale el peso que corresponde.

---

### La reescritura

El resultado final es una nueva versión de tu mensaje que tiene en cuenta las tres perspectivas.

- Límite estricto de 300 palabras
- Dirigirse a más audiencias sin alargar el texto obliga a editar de verdad
- Si el resultado es más largo, vuelve a pedirlo con un límite de 250

---

### Prompts de seguimiento

- "¿Cuál de estas tres audiencias es más probable que lo bloquee y qué le haría cambiar de opinión?"
- "Muéstrame las dos frases de mi borrador original que provocaron más malentendidos."
- "Vuelve a reescribirlo suponiendo que el patrocinador ejecutivo solo leerá el primer párrafo."

---

[Volver a Prompt Playground](../README.md#prompt-playground)
