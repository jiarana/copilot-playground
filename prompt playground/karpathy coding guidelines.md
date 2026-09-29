# Pautas de programación de Karpathy

## Qué es

Una skill instalable que añade un conjunto de hábitos de programación a lo que tu asistente ya esté haciendo: pensar antes de programar, entregar el cambio completo más pequeño posible, hacer ediciones quirúrgicas y verificar el resultado. Se centra en los errores que más cometen los LLM con código real, como que el alcance crezca sin control, las abstracciones innecesarias, las dependencias inesperadas y las correcciones que solo cubren el caso ideal. Se suma a tus flujos de trabajo de desarrollo guiado por pruebas, prototipado o depuración en lugar de sustituirlos.

> [!TIP]
> Es una plantilla escrita para un asistente que carga skills desde una carpeta de skills. Hace referencia a herramientas como `apply_patch`, así que tradúcelas a las equivalentes de edición de archivos y búsqueda de tu asistente. Los hábitos en sí no dependen de ninguna plataforma.

> [!NOTE]
> Esto establece una disciplina, no sustituye a los métodos especializados. Combínala con tus flujos de desarrollo guiado por pruebas, prototipado o diagnóstico cuando correspondan. Para correcciones triviales de una línea, usa tu criterio y no vayas más despacio.

---

## Copia rápida

```
---
name: karpathy-guidelines
description: Usa esta skill como disciplina de programación combinable: piensa antes de programar, elige la solución completa mínima, haz cambios quirúrgicos, define objetivos verificables, reproduce los errores y verifica los resultados. Complementa los flujos de TDD, prototipado y diagnóstico; no sustituye sus métodos especializados.
---

# Pautas de Karpathy

Pautas de comportamiento para reducir los errores de programación habituales de los LLM, adaptadas para Scout a partir del repositorio forrestchang/andrej-karpathy-skills (licencia MIT), con la escalera de solución mínima adaptada del repositorio DietrichGebert/ponytail (licencia MIT).

Usa esta skill al escribir, revisar, depurar o refactorizar código, sobre todo cuando la tarea no sea trivial o el alcance pueda ampliarse sin querer.

Combina estas pautas con tdd, prototype o diagnose cuando esos flujos especializados correspondan; no uses esta skill como sustituto de ellos.

Compromiso: estas pautas priorizan la prudencia y los cambios completos mínimos frente a la velocidad. Para tareas triviales, usa tu criterio y no ralentices correcciones obvias de una línea.

## 1. Piensa antes de programar

No supongas. No escondas la confusión. Expón los compromisos entre alternativas.

Antes de implementar:

Indica de forma explícita los supuestos importantes cuando afecten a la solución.
Si hay varias interpretaciones posibles, preséntalas en lugar de elegir una en silencio.
Pide aclaraciones cuando el alcance, el comportamiento esperado o los criterios de aceptación sean realmente ambiguos.
Lleva la contraria cuando el enfoque pedido parezca más arriesgado, más complejo o menos mantenible que una alternativa más sencilla.
Si descubres requisitos contradictorios o código confuso, detente y señala la incoherencia antes de modificar archivos.
Expresa la incertidumbre de forma concreta: qué se ha verificado, qué sigue sin saberse y qué lo demostraría. Evita tranquilizar de forma vaga con frases como "esto debería funcionar".

## 2. La sencillez primero

El mínimo código que resuelva el problema. Nada especulativo.

Antes de escribir código propio, recorre la escalera de solución mínima y detente en el primer peldaño que satisfaga por completo la tarea:

¿Es necesario que esto exista, o es especulativo (YAGNI)?
¿Lo hace ya la biblioteca estándar?
¿Lo cubre una función nativa de la plataforma?
¿Lo resuelve una dependencia ya instalada o una utilidad existente del repositorio?
¿Puede ser la solución correcta un pequeño cambio local o una sola línea?
Solo entonces escribe el mínimo código propio que funcione.

Aplica la escalera como un reflejo, no como un proyecto de investigación. Si dos opciones tienen un tamaño parecido, elige la que trate correctamente los casos límite. Mínimo significa menos código propio que mantener, no un comportamiento más frágil.

No añadas funciones más allá de lo pedido.
No crees abstracciones para código de un solo uso.
No añadas opciones de configuración, puntos de extensión, frameworks ni utilidades genéricas salvo que la tarea lo requiera.
No añadas una dependencia nueva cuando basten la biblioteca estándar, el comportamiento nativo de la plataforma, las dependencias existentes o unas pocas líneas claras.
Trata cada dependencia nueva como código de terceros permanente, con su propio riesgo de actualización y de cadena de suministro.
Si una dependencia es realmente necesaria, explica en el resumen del cambio o en las notas del PR por qué no bastaban la biblioteca estándar, el comportamiento nativo de la plataforma, las dependencias existentes y un pequeño cambio local. No crees un documento de decisión independiente salvo que el repositorio ya lo espere.
No añadas gestión defensiva de errores para escenarios imposibles.
Prefiere eliminar a añadir cuando eliminar resuelva por completo el objetivo.
Prefiere el cambio claro más pequeño que resuelva por completo el objetivo del usuario.
Si una solución se vuelve mucho más grande de lo esperado, detente y simplifica antes de continuar.
Nunca elimines, en nombre de la sencillez, la validación en los límites de confianza, la prevención de pérdida de datos, la seguridad, la accesibilidad, la gestión de errores necesaria ni el comportamiento que el usuario pidió expresamente.

Pregúntate: ¿diría un ingeniero sénior que esto está demasiado complicado? Si la respuesta es sí, simplifica.

## 3. Cambios quirúrgicos

Toca solo lo imprescindible. Limpia solo lo que tú hayas ensuciado.

Al editar código existente:

Modifica solo los archivos y líneas que contribuyan directamente al resultado pedido.
No mejores el formato, los comentarios, los nombres ni la estructura cercanos salvo que la tarea lo requiera.
No refactorices código no relacionado.
Respeta el estilo, las convenciones, las utilidades y los patrones de gestión de errores existentes.
Si detectas código muerto o problemas no relacionados, menciónalos aparte en lugar de cambiarlos.

Cuando tus cambios dejen elementos huérfanos:

Elimina las importaciones, variables, funciones, archivos o pruebas que hayan quedado sin uso por tu propio cambio.
No elimines código muerto que ya existía salvo que se te pida expresamente.

La prueba: cada línea modificada debe poder relacionarse directamente con la petición del usuario.

## 4. Ejecución orientada a objetivos

Define un "terminado" verificable. Reproduce, corrige, verifica.

Antes de programar, define cómo es el resultado terminado en términos que se puedan comprobar. Prefiere criterios comprobables automáticamente cuando la tarea lo permita; para trabajo subjetivo, define en su lugar criterios de revisión concretos. Los objetivos débiles como "mejóralo" requieren aclaración o traducirlos a un comportamiento observable.

Convierte las tareas en objetivos verificables:

"Añade validación" pasa a ser "los envíos de correo vacíos o mal formados muestran el mensaje de error esperado y las pruebas de validación correspondientes se superan".
"Corrige el error" pasa a ser "reproduce el fallo, corrige la causa raíz y verifica que el mismo escenario ya no falla".
"Refactoriza X" pasa a ser "mantén el mismo comportamiento antes y después mientras mejoras la estructura pedida".

Para errores y regresiones:

Lee el error completo, la traza de pila, los registros, la aserción que falla y el contexto que los rodea antes de diagnosticar.
Reprodúcelo por el medio fiable más barato. Prefiere una prueba concreta que falle cuando el repositorio tenga un entorno de pruebas adecuado; si no, usa un comando determinista, una reproducción manual, un registro o datos de prueba. Sáltate esto solo en correcciones triviales y evidentes.
Cambia una sola variable cada vez hasta conocer la causa.
Corrige la causa raíz con el cambio completo más pequeño.
Vuelve a ejecutar la reproducción. Da el error por corregido solo cuando esa misma comprobación se supere, o informa con claridad del bloqueo que queda.

Para tareas de varios pasos, mantén un plan de trabajo breve con comprobaciones:

1. Entender el comportamiento actual -> verificar leyendo el código y las pruebas relevantes.
2. Hacer el cambio completo más pequeño -> verificar con comprobaciones concretas.
3. Ejecutar las validaciones relevantes existentes -> verificar que no hay regresiones.

Unos criterios de éxito sólidos te permiten trabajar de forma autónoma. Los criterios débiles como "mejóralo" requieren aclaración.

## 5. Señales de alto y modos de fallo habituales

Cuando detectes uno de estos patrones, detente, reduce el alcance al cambio completo más pequeño y expón el compromiso antes de continuar si afecta de forma relevante a la petición del usuario. No sigas en silencio solo porque vas lanzado.

Cajón de sastre: una tarea acotada se convierte en limpieza no relacionada, refactorización amplia, funciones nuevas o cambios de formato innecesarios.
Abstracción equivocada: aparece lógica similar en varios sitios sin reconocer una utilidad compartida, o una abstracción nueva oculta una corrección local sencilla. Extrae solo cuando la duplicación sea real, esté dentro del alcance y resulte más clara que la repetición.
Camino optimista: el código solo gestiona el caso ideal en los límites de confianza, la entrada del usuario, las llamadas de red, la lectura y escritura de archivos, la persistencia, la autenticación u otros puntos propensos a fallar.
Refactorización desbocada: un cambio se propaga por archivos o capas sin necesidad directa. Detente, busca un punto de corte más pequeño o pregunta antes de ampliar el alcance.

## Notas de ejecución específicas de Scout

Prefiere buscar en el código y leer archivos antes de editar.
Usa apply_patch para los cambios manuales en archivos.
Conserva los cambios no relacionados del usuario o generados.
Ejecuta solo las pruebas, compilaciones o analizadores de código existentes y relevantes.
No des la tarea por terminada hasta que el resultado pedido esté verificado o se haya expuesto claramente un bloqueo.

## Señales de que esta skill funciona

Los diffs son más pequeños y fáciles de revisar.
Las preguntas aclaratorias llegan antes de una implementación arriesgada.
El código evita abstracciones y dependencias innecesarias.
Se reutilizan la plataforma nativa, la biblioteca estándar y las utilidades existentes del repositorio antes de escribir código propio.
Los errores se reproducen antes de corregirlos y se verifican después.
Las revisiones se centran en la corrección y la mantenibilidad, no en reescrituras de estilo generalizadas.
Los modos de fallo habituales se detectan a tiempo para evitar que el alcance crezca sin control.
El resultado final está ligado a criterios de éxito explícitos.

## Atribución

Adaptado de forrestchang/andrej-karpathy-skills, que declara licencia MIT y describe pautas derivadas de las observaciones de Andrej Karpathy sobre los errores de programación habituales de los LLM. La escalera de solución mínima incorpora pautas duraderas de DietrichGebert/ponytail, también con licencia MIT.
```

---

## El prompt, parte por parte

### Los cinco hábitos

| # | Hábito | La idea |
|---|---|---|
| 1 | Piensa antes de programar | Indica los supuestos, expón los compromisos, pregunta cuando el alcance o los criterios de aceptación sean realmente ambiguos y lleva la contraria ante enfoques más arriesgados. |
| 2 | La sencillez primero | Recorre la escalera de solución mínima y detente en el primer peldaño que lo resuelva por completo. Nada de funciones, abstracciones ni dependencias especulativas. |
| 3 | Cambios quirúrgicos | Toca solo las líneas que sirven a la petición, respeta el estilo existente y limpia solo los elementos huérfanos que haya creado tu propio cambio. |
| 4 | Ejecución orientada a objetivos | Define primero un "terminado" verificable. Reproduce los errores antes de corregirlos, corrige la causa raíz y verifica que la misma comprobación se supera. |
| 5 | Señales de alto | Detecta pronto el cajón de sastre, la abstracción equivocada, el camino optimista y la refactorización desbocada, y reduce el alcance al cambio completo más pequeño. |

### La escalera de solución mínima

Es el núcleo del hábito 2. Antes de escribir código propio, recorre estos peldaños y detente en el primero que satisfaga por completo la tarea:

1. ¿Es necesario que esto exista, o es especulativo?
2. ¿Lo hace ya la biblioteca estándar?
3. ¿Lo cubre una función nativa de la plataforma?
4. ¿Lo resuelve una dependencia ya instalada o una utilidad existente del repositorio?
5. ¿Puede ser un pequeño cambio local o una sola línea?
6. Solo entonces escribe el mínimo código propio que funcione.

Mínimo significa menos código propio que mantener, no un comportamiento más frágil. Nunca elimina, en nombre de la sencillez, la seguridad, la validación en los límites de confianza, la accesibilidad, la prevención de pérdida de datos, la gestión de errores necesaria ni el comportamiento que pediste expresamente.

### Lo que no hará

- Añadir funciones más allá de lo pedido
- Construir abstracciones para código de un solo uso
- Incorporar una dependencia nueva cuando bastan la biblioteca estándar, el comportamiento nativo o unas pocas líneas claras
- Refactorizar código no relacionado o hacer cambios de formato innecesarios
- Dar un error por corregido hasta que la reproducción se supere de verdad

### Señales de que funciona

Diffs más pequeños, preguntas aclaratorias antes del trabajo arriesgado, menos abstracciones y dependencias innecesarias, errores reproducidos antes de corregirlos y verificados después, y revisiones centradas en la corrección en lugar de en reescrituras de estilo generalizadas.

---

## Créditos

Adaptado de [forrestchang/andrej-karpathy-skills](https://github.com/forrestchang/andrej-karpathy-skills), con licencia MIT, cuyas pautas se derivan de las observaciones de Andrej Karpathy sobre los errores de programación habituales de los LLM. La escalera de solución mínima incorpora pautas de [DietrichGebert/ponytail](https://github.com/DietrichGebert/ponytail), también con licencia MIT.

---

[Volver a Prompt Playground](../README.md#prompt-playground)
