# improve-design

[English](README.md)

Prepara mejoras de interfaz para revisión mediante propuestas visuales o recorridos
interactivos completos. Conserva las decisiones existentes cuando hay referencias.
Cuando se solicite, usa un wireframe en grises para revisar estructura e interacción.

Parte de una app existente, capturas, archivos de diseño o una descripción. No exige
un editor de diseño ni una especificación formal. El alcance sigue la petición:
una propuesta por defecto, con alternativas cuando se pidan o ayuden a resolver una
pregunta de diseño abierta. La skill funciona por sí sola; `prototype` puede
complementarla cuando explorar alternativas forme parte del encargo.

## Casos de uso

Los ejemplos usan una interfaz en español y datos ficticios. Cada uno muestra
cuatro etapas: lista de escenarios, detalle, interacción y formulario de feedback.
Los prompts son ejemplos de uso, no transcripciones de una generación independiente.

### 1. Con mockups: reservar un libro

Conserva el diseño de la biblioteca y confirma la franja de recogida elegida.

#### Prompt

```text
Usa $improve-design con examples/with-mockups/mockup.jpg como referencia.
Conserva su tipografía, colores, espaciado, contenido e interfaz en español.
Muestra lista y detalle del escenario; al iniciar permite completar la reserva:
disponibilidad, recogida, revisión, confirmación y recibo.
Muestra el formulario de feedback después del resultado.
Guarda en review/book-reservation/.
```

#### Capturas

| 1. Lista de escenarios | 2. Detalle del escenario |
| --- | --- |
| <img src="examples/with-mockups/01-scenarios.jpg" width="220" alt="Lista de escenarios"> | <img src="examples/with-mockups/02-detail.jpg" width="220" alt="Detalle del escenario"> |

| 3. Escenario interactivo | 4. Formulario de feedback |
| --- | --- |
| <img src="examples/with-mockups/03-scenario.jpg" width="220" alt="Reserva del libro"> | <img src="examples/with-mockups/04-feedback.jpg" width="220" alt="Formulario de feedback"> |

[Mockup de referencia](examples/with-mockups/mockup.jpg) ·
[Detalles del ejemplo](examples/with-mockups/README.es.md) ·
[Archivo del prototipo](examples/with-mockups/index.html)

La referencia se creó a partir del estado inicial del ejemplo. No es una
traducción independiente desde una herramienta de diseño externa.

### 2. Wireframe en escala de grises: programar una sesión

Sin mockups de entrada, este ejemplo usa blanco, negro y grises. La sesión debe
conservar actividad, duración y fecha hasta la confirmación. La ausencia de un
mockup no obliga por sí sola a usar wireframe; elige la fidelidad visual según
la tarea y la petición de la persona.

#### Prompt

```text
Usa $improve-design para crear un wireframe en grises de un planificador.
Muestra la lista y detalle del escenario y después inicia el recorrido.
Déjame elegir actividad, duración y fecha, revisar, confirmar y ver
la sesión programada. Muestra el formulario de feedback al terminar.
Mantén la interfaz en español. Guarda en review/focus-session/.
```

#### Capturas

| 1. Lista de escenarios | 2. Detalle del escenario |
| --- | --- |
| <img src="examples/without-mockups/01-scenarios.jpg" width="220" alt="Lista de escenarios"> | <img src="examples/without-mockups/02-detail.jpg" width="220" alt="Detalle del escenario"> |

| 3. Escenario interactivo | 4. Formulario de feedback |
| --- | --- |
| <img src="examples/without-mockups/03-scenario.jpg" width="220" alt="Wireframe de sesión"> | <img src="examples/without-mockups/04-feedback.jpg" width="220" alt="Formulario de feedback"> |

[Detalles del ejemplo](examples/without-mockups/README.es.md) ·
[Archivo del prototipo](examples/without-mockups/index.html)

## Instalación

Usa Node.js 22.20 o posterior y npm, como requiere la
[CLI skills](https://github.com/vercel-labs/skills#install-a-skill):

```bash
npx skills add jerolan/improve-design
```

Selecciona la skill y los agentes. La instalación es local al proyecto por
defecto. Para usarla en Codex entre proyectos:

```bash
npx skills add jerolan/improve-design --skill improve-design -a codex -g
```

Para consultar las skills sin instalar:

```bash
npx skills add jerolan/improve-design --list
```

## Revisión y feedback

Para una misma app y encargo de revisión, usa una entrada común con los recorridos
agrupados por contexto y los comentarios reunidos. Una vez comprobada y lista la
propuesta, el agente la entrega. Revisa cuando puedas y vuelve con feedback;
no se exige aceptación inmediata.

Elige un escenario, lee su contexto y resultado esperado y pulsa **Iniciar**.
Completa el recorrido hasta el resultado final antes de dar feedback. Para una
pregunta únicamente visual puede bastar un mockup estático.

El feedback vive temporalmente en la pestaña actual. Navegar y repetir conserva
los comentarios; cerrar o recargar los pierde. Descarga los comentarios en
Markdown antes de salir. Adjunta el archivo a tu agente o pega su contenido como
prompt. No se envían ni se sincronizan automáticamente.

```text
Usa $improve-design para aplicar el feedback adjunto. Conserva las decisiones
aceptadas y verifica cada recorrido modificado hasta su resultado final.
```

## Ejecutar los ejemplos localmente

Descarga o clona el repositorio y abre cada `index.html` en un navegador.
GitHub muestra el código HTML. No hay dependencias de aplicación ni servicios
externos. Si tienes Python, ejecuta desde la raíz:

```bash
python3 -m http.server 8765 --bind 127.0.0.1
```

Abre [con mockups](http://127.0.0.1:8765/examples/with-mockups/) o
[wireframe](http://127.0.0.1:8765/examples/without-mockups/). Detén con Ctrl+C.
La dirección es local a la computadora. Las operaciones son ficticias.

La skill no exige editor, framework o plugin concreto. Aprobar el diseño no
autoriza implementar ni desplegar el producto. Consulta [VALIDATION.md](VALIDATION.md)
para el historial de comprobaciones.

## Licencia

[MIT](LICENSE), Copyright 2026 jerolan.
