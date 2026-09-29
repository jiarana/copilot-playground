# Claude en Copilot con el modo agente para Excel

[![Claude en Copilot](assets/copilot%20webinar/Agent%20Mode/Claude%20in%20Copilot%206.png)](https://youtu.be/zkaRUDSDBwk?si=KNPnsIOLPI9amS8A)


Últimamente se habla mucho de Claude y de lo bien que trabaja con Excel y con datos estructurados.
Lo que la mayoría no sabe es que, si usas Microsoft 365 Copilot, ya tienes acceso a ese nivel de capacidad dentro de Excel.

Este repositorio acompaña una reconstrucción práctica de la demostración del vídeo. Puedes verlo de principio a fin, o descargar los archivos y seguirlo paso a paso con los mismos prompts que usa el autor.

Mira el vídeo completo en YouTube (en inglés):
https://youtu.be/zkaRUDSDBwk?si=6EGZujNUsCmeYfIl

> [!NOTE]
> El libro de Excel de ejemplo está en inglés, así que los prompts mantienen los nombres de hojas, tablas y columnas originales (por ejemplo, `Overtime_Raw` o `Dashboard`). Si traduces el libro, cambia también esos nombres en los prompts.

## Cómo seguir la demostración (recomendado)
Si quieres reconstruirla tú mismo, sigue estos pasos en orden.
### 1) Descarga los datos de ejemplo sin procesar
Esta demostración usa datos sintéticos generados con fines formativos y de demostración.

[Descarga el archivo AQUÍ](https://github.com/heyitsgoad/copilot-playground/raw/main/education%20playground/assets/copilot%20webinar/Agent%20Mode/Q2_2025_ParamedicOvertime_RAW.xlsx)

Qué contiene (para que resulte realista):
- Overtime_Raw (3.416 filas): registros por turno con puesto, estación, turno, horas extra, motivo de las horas extra, datos de retribución, volumen de llamadas e indicadores de falta de personal
- Employee_Roster (74 empleados): combinación de puestos, jornada equivalente (FTE), estación asignada, tramo de antigüedad y tarifas base
- Call_Volume_Daily (91 días): total de llamadas, llamadas de alta gravedad, traslados, ayuda mutua, e indicadores de meteorología y eventos
- Staffing_Daily (182 filas): plantilla prevista frente a real de día y de noche, bajas por enfermedad, vacantes y faltas de personal
- OT_Budget: objetivos mensuales de presupuesto de horas extra (horas y coste)
- Quick_Aggregates: una tabla de agregados básica que puedes usar como comprobación
Decisiones de diseño incluidas en los datos:
- Estacionalidad con un claro repunte en mayo del volumen de llamadas y de las faltas de personal
- Diversos motivos de horas extra (prolongación de turno, cobertura de vacantes, cobertura de bajas, retén para eventos, picos por meteorología)
- Un pequeño grupo de empleados con muchas horas extra repetidas a finales de mayo (genera riesgo y debate)
- Incluye el plus de nocturnidad y los multiplicadores de horas extra
### 2) Activa el modo agente en Excel
El modo agente es necesario para los prompts de analista que siguen.
1. Abre el libro en Excel para escritorio
2. Abre Copilot
- Puedes ver Copilot en la cinta de opciones o como el icono flotante de Copilot abajo a la derecha (cualquiera de los dos sirve)
3. Selecciona Editar con Copilot
4. Elige el modo agente
- Esto habilita un razonamiento más profundo, análisis de varios pasos y la creación de elementos nativos de Excel
5. Si está disponible, confirma que Claude está habilitado en la selección de modelo
- Si no ves Claude, probablemente tu administrador de TI todavía no ha habilitado Anthropic
Con el modo agente activado, ya puedes ejecutar los prompts.
## 3) Pack de prompts para analistas (modo agente)
Estos prompts convierten los datos sin procesar en paneles, conclusiones y materiales para la dirección. Ejecútalos en orden.
### Prompt 0: prepara el modelo de datos (ejecútalo primero)
Prompt:
Crea un modelo de informes limpio a partir de las hojas existentes. Convierte Overtime_Raw, Call_Volume_Daily, Staffing_Daily y OT_Budget en tablas de Excel con nombres claros. Asegúrate de que las columnas Date tienen formato de fecha. Añade a Overtime_Raw las columnas Month (Apr, May, Jun) y WeekStart (lunes). Crea relaciones por Date entre Overtime_Raw, Call_Volume_Daily y Staffing_Daily. Crea hojas nuevas llamadas Dashboard y SBAR.
Resultado esperado:
- Tablas: tblOvertimeRaw, tblCallsDaily, tblStaffingDaily, tblOTBudget
- Hojas nuevas: Dashboard, SBAR
### Prompt 1: crea la franja de KPI para la dirección
Prompt:
En la hoja Dashboard, crea una franja de KPI del segundo trimestre (del 1 de abril al 30 de junio de 2025) que muestre el total de horas extra, el coste total de las horas extra, el coste frente al presupuesto (desviación en $ y %), las horas frente al presupuesto (desviación en horas y %), el coste por llamada y el principal motivo de horas extra por número de horas. Dale formato de resumen ejecutivo limpio.
### Prompt 2: crea los gráficos principales del panel
Prompt:
Crea un panel para la dirección con gráficos del coste de horas extra por mes (con una línea de presupuesto), las horas extra por semana, las horas extra por estación, las horas extra por motivo (Pareto) y un gráfico de dispersión del total de llamadas frente a las horas extra por día que destaque los valores atípicos de mayo. Añade segmentaciones por Month, Station, Shift y Role. Mantén un diseño sencillo y adecuado para la dirección.
### Prompt 3: encuentra la historia (¿qué cambió en mayo?)
Prompt:
Analiza qué provocó las horas extra de mayo en comparación con abril y junio. Identifica los 3 factores principales y cuantifica su impacto en horas y en dólares. Señala riesgos operativos como la concentración, las prolongaciones de turno repetidas o las faltas de personal persistentes. Añade al Dashboard una sección "Factores de mayo" con las conclusiones en viñetas.
### Prompt 4: crea un SBAR para el director financiero
Prompt:
En la hoja SBAR, crea un resumen SBAR listo para el director financiero que cubra Situación, Antecedentes, Evaluación y Recomendaciones. Incluye cifras, riesgos y acciones agrupadas en inmediatas, a corto plazo y estructurales. Mantén un tono directo y con las cifras por delante.
### Prompt 5: argumentos para el vicepresidente
Prompt:
Crea una sección "Argumentos del vicepresidente para el director financiero" con cinco puntos destacados numerados, tres preguntas probables del director financiero con sus respuestas y dos decisiones necesarias con su impacto estimado. Colócala en el Dashboard y vincula los valores a las tablas de origen.
### Prompt 6: prueba de resistencia (escenarios hipotéticos)
Prompt:
Crea una hoja What If que modele cambios de plantilla y de políticas y muestre el ahorro estimado en horas extra, el coste de las medidas y el impacto neto. Presenta los resultados en una tabla limpia y en un gráfico de cascada sencillo.
## 4) Pack de prompts para directivos (después de la entrega)

Una vez creado el libro, el vicepresidente debe centrarse en las **decisiones**, no en el análisis.

**Prompts de ejemplo incluidos:**

- **Resumen principal para el director financiero**
  - **Prompt:**
    - En un párrafo: resume las horas extra del personal de emergencias sanitarias del segundo trimestre en el condado de Platte (Misuri).
      Incluye el coste de las horas extra, las horas, la desviación respecto al presupuesto y el factor principal.
      Después dame 3 viñetas que le importarían a un director financiero.

- **Identificación de riesgos**
  - **Prompt:**
    - Identifica las 5 principales señales de riesgo de este libro (fatiga, concentración, faltas de personal recurrentes, prolongaciones de turno repetidas, estaciones críticas).
      Para cada riesgo, indica: qué es, por qué importa y la métrica que lo demuestra.

- **Cambios de un mes a otro**
  - **Prompt:**
    - Compara abril, mayo y junio.
      ¿Qué cambió, por qué cambió y qué esperamos para el próximo trimestre si nada cambia?
      Limítalo a 6 viñetas, cada una con una cifra.

- **Opciones de decisión con sus compromisos**
  - **Prompt:**
    - Dame 3 opciones de decisión para que el director financiero reduzca las horas extra el próximo trimestre.
      Para cada opción, indica: coste estimado, ahorro estimado, tiempo hasta ver el impacto, compromisos operativos y una valoración de confianza basada en los datos.

- **Argumentos para el consejo de administración**
  - **Prompt:**
    - Genera argumentos para una intervención de 90 segundos que expliquen:
      - el problema de las horas extra
      - los factores que lo provocan
      - la decisión necesaria
      - el retorno de la inversión
    - Usa un lenguaje sencillo e incluye 3 cifras que pueda decir en voz alta.

## Por qué funciona esta demostración
- El director financiero hace una pregunta en lenguaje corriente
- Los analistas usan el modo agente para crear elementos nativos de Excel
- Los directivos extraen decisiones, no gráficos
- El retorno de la inversión se ve en el tiempo hasta obtener la respuesta y en la calidad de la decisión
El modo agente no se limita a escribir fórmulas.
Produce libros de Excel utilizables, itera y valida hasta que el resultado está listo.

---

[Volver a Education Playground](../README.md#education-playground)
