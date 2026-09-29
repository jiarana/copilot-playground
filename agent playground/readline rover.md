# Redline Rover

![Redline Rover principal](assets/redline%20rover/redline%20rover%20main.png)

Redline Rover es un agente especializado en análisis de contratos, diseñado para automatizar la comparación entre las plantillas internas de acuerdos de calidad y las versiones que aporta el cliente. Lo creó [Sue Vencill](https://www.linkedin.com/in/suevencill/), compañera del autor en Microsoft. Su objetivo es garantizar que los documentos externos que requieren firma sigan alineados con los requisitos de los procedimientos normalizados de trabajo (SOP) internos. El agente realiza una auditoría profunda y en ambos sentidos de cada cláusula para detectar redacciones más débiles por parte del cliente o requisitos internos que faltan.

## Cómo usarlo

Sube los dos documentos:
- La plantilla interna del acuerdo de calidad
- El documento del acuerdo de calidad del cliente

El agente analiza ambos archivos y genera dos tablas:
1. Carencias del acuerdo del cliente, con los cambios recomendados
2. Carencias de la plantilla interna según los requisitos del cliente

Usa estas tablas como guía para marcar cambios (redlining) y negociar.

## Compatibilidad

- Creado con Copilot Studio o Copilot Studio Lite
- Microsoft 365 Copilot (Premium)
- Microsoft 365 Copilot Chat (licencia gratuita)**

**Notas:**
Copilot Chat funciona si los archivos se suben manualmente cada vez. No añadas estos archivos a la base de conocimiento.

## Cómo crearlo

### Descripción

```
Un agente de aseguramiento de la calidad que realiza auditorías en ambos sentidos entre las plantillas internas de calidad y los acuerdos con clientes. Identifica carencias de cumplimiento, evalúa la solidez de la redacción y recomienda cambios para alinear los documentos del cliente con las normas internas.
```

### Instrucciones

```
Tu trabajo es comparar nuestra plantilla de acuerdo de calidad con la versión del cliente. Como estamos obligados a usar el documento del cliente, nuestro SOP exige que su acuerdo contenga requisitos equivalentes a los nuestros.

Revisa el contenido completo de ambos documentos. Haz una comparación en ambos sentidos:
- Identifica las cláusulas o requisitos del acuerdo del cliente que no son equivalentes a los nuestros.
- Identifica las cláusulas o requisitos de nuestra plantilla que faltan o son más débiles que los suyos.

### Requisitos del resultado
Proporciona dos tablas:

Tabla 1: Carencias del cliente (respecto a nuestra plantilla)
Enumera:
- Carencias o diferencias
- Cambios recomendados

Tabla 2: Carencias de la plantilla interna (respecto al documento del cliente)
Enumera:
- Requisitos del cliente que son equivalentes (si los hay)
- Carencias o diferencias
- Cambios recomendados

Incluye los números o títulos de sección siempre que sea posible. La comparación debe incluir:
- Definiciones
- Anexos
- Requisitos incluidos dentro del texto
```

### Plantillas que incluir en la base de conocimiento

```
[Añade al conocimiento las plantillas de tu organización]
```

![Instrucciones de Redline Rover](assets/redline%20rover/redline%20rover%20instructions.png)
![Conocimiento de Redline Rover](assets/redline%20rover/redline%20rover%20knowledge.png)
![Capacidades de Redline Rover](assets/redline%20rover/redline%20rover%20capabilities.png)

## Uso

### Auditoría estándar

```
He subido nuestra plantilla interna y el acuerdo del cliente. Haz una comparación en ambos sentidos y genera las tablas de análisis de carencias.
```

### Enfoque en riesgos

```
Analiza el acuerdo del cliente frente a nuestra plantilla. Destaca las redacciones más débiles que podrían aumentar el riesgo de calidad o legal.
```

### Comprobación de trazabilidad

```
Haz una comparación y confirma que se han incluido todas las definiciones y anexos. Añade los números de sección de ambos documentos.
```

### Resumen ejecutivo

```
Según la comparación, ¿cuáles son las tres carencias principales que hay que resolver con el cliente antes de firmar?
```

![Prompts iniciales de Redline Rover](assets/redline%20rover/redline%20rover%20starter%20prompts.png)

---

[Volver a Agent Playground](../README.md#agent-playground)
