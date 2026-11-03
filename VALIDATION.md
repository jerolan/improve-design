# Comprobación histórica de la primera versión

Fecha: 2 de noviembre de 2026.

## Skill y documentación

- El validador `quick_validate.py` de `skill-creator` aceptó el nombre, el frontmatter y el contenido de `SKILL.md`.
- Se revisaron las referencias locales y las instrucciones de instalación para una skill situada en la raíz del repositorio.
- Una revisión independiente de las instrucciones simuló dos peticiones: un flujo completo basado en una captura y un mockup de una tarjeta sin referencias. Eligió el alcance esperado en ambos casos y no detectó una obligación de construir navegación para la tarjeta. Esta revisión fue de decisiones, no una ejecución independiente de los ejemplos.

## Ejemplos ejecutables, versión anterior

Se comprobó la sintaxis de los scripts y se recorrieron ambos ejemplos en navegador con datos ficticios:

- Con mockups: consultar el libro, elegir recogida el sábado, volver a cambiarla, revisar y confirmar. El recibo conservó el título y la franja elegida.
- Sin mockups: elegir Escribir, introducir una duración inválida de 5 minutos, observar el error, cambiarla a 40 minutos, revisar y programar. El resultado conservó actividad, duración y fecha. Repetir volvió al inicio del recorrido.
- Feedback: escribir un comentario, marcar la revisión y recargar. Al volver al feedback, el comentario siguió disponible en el mismo navegador. Se conservó también el resultado anterior en los datos guardados al corregir la recuperación de estado.
- Se guardaron capturas del estado inicial de la biblioteca y del resultado de ambos recorridos. La referencia de biblioteca es un fixture creado con el mismo estado, contenido y componentes de este ejemplo. No prueba una traducción independiente desde una herramienta de diseño externa.

## Límites

La comprobación fue manual y acotada. No es un benchmark de la skill, una prueba exhaustiva de accesibilidad ni una certificación de compatibilidad con todos los navegadores. No se comprobó un teléfono físico, sincronización entre dispositivos ni operaciones reales de biblioteca o calendario. La exportación de feedback está implementada como una descarga local de JSON; la recuperación comprobada se realizó mediante almacenamiento del navegador.

Los ejemplos son artefactos de demostración. No instalan un stack de aplicación ni requieren una cuenta. Los comentarios de prueba permanecen en el navegador utilizado para la comprobación y no forman parte del repositorio.

## Versión actual: wireframe y feedback efímero

La versión actual sustituye el segundo ejemplo por un wireframe en escala de grises. Ambos ejemplos incluyen lista de escenarios, detalle previo, interacción y formulario de feedback. Las ocho capturas de estas etapas se guardaron y las pantallas de interacción y feedback se inspeccionaron visualmente.

Se recorrieron ambos ejemplos hasta su resultado final: reserva con recogida el sábado y sesión de escritura de 40 minutos. En navegador se comprobó que los comentarios se conservan al volver entre pantallas, y que al recargar aparecen vacíos. Los scripts no utilizan almacenamiento persistente del navegador.

La descarga genera ahora un archivo Markdown que contiene un prompt para el agente, escenario, versión, estado de revisión, comentario y resultado probado. Su contenido, tipo y extensión se comprobaron ejecutando los eventos del ejemplo de forma aislada. El controlador del navegador no notificó el evento de descarga durante la comprobación; no se afirma que ese evento se haya observado. La persona debe descargar el archivo y adjuntarlo o pegarlo como prompt al agente antes de cerrar o recargar.

La documentación anterior sobre JSON y persistencia corresponde sólo a la primera versión. No describe el comportamiento actual. Las instrucciones de la skill permiten alta fidelidad o un wireframe cuando se pide; no confunden la ausencia de una referencia con la obligación de usar grises.
