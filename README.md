# improve-design

Una skill para mejorar interfaces mediante mockups y prototipos de alta fidelidad, recoger feedback y convertirlo en una revisión coherente del diseño.

La fidelidad visual siempre es alta. La complejidad depende de lo que se necesita evaluar: una pantalla puede bastar para revisar composición; un flujo interactivo debe poder completarse de principio a fin.

## Los dos modos

| Modo | Punto de partida | Trabajo |
| --- | --- | --- |
| Con mockups | Existe un archivo de diseño, captura o interfaz de referencia. | Conservar sus decisiones visuales, proponer los cambios y comprobar que el prototipo representa esa propuesta. |
| Sin mockups | No existe una referencia visual definida. | Crear una dirección coherente y materializarla directamente en alta fidelidad. |

En ambos modos se puede entregar un mockup estático o un prototipo interactivo. Tener mockups de entrada no obliga a construir una aplicación; no tenerlos tampoco implica entregar un wireframe.

## Cómo se revisa

Para varios escenarios, la persona elige uno en el índice. Primero ve el contexto, los pasos y el resultado esperado. Al pulsar **Iniciar**, entra a una experiencia como la app, sin instrucciones de revisión encima. Ejecuta las acciones hasta el resultado final y después deja su feedback. La navegación libre puede añadirse como opción.

La skill exige comprobar dos cosas por separado: que la propuesta se parece al diseño que se está revisando y que cada recorrido anunciado llega a su final. Las revisiones parciales siguen siendo parciales. Las decisiones aprobadas se conservan y el diseño, el prototipo y las capturas se actualizan juntos.

## Instalación en Codex

Copia este repositorio en una carpeta de skills con el nombre `improve-design`. El archivo `SKILL.md` debe quedar directamente dentro de esa carpeta.

En macOS o Linux, con la ubicación predeterminada:

```sh
git clone https://github.com/jerolan/improve-design.git ~/.codex/skills/improve-design
```

En Windows PowerShell:

```powershell
git clone https://github.com/jerolan/improve-design.git "$env:USERPROFILE\.codex\skills\improve-design"
```

Si usas un `CODEX_HOME` personalizado, coloca la carpeta dentro de `CODEX_HOME/skills`. Si ya existe una instalación, revisa sus cambios antes de actualizarla; no clones encima. Reinicia Codex para que detecte la skill.

También puedes pedirle a la skill de instalación de Codex que instale `jerolan/improve-design`, usando la raíz del repositorio como carpeta de la skill y `improve-design` como nombre.

El formato `SKILL.md` puede utilizarse con otros agentes que lo admitan. Su descubrimiento e instalación dependen del agente. `agents/openai.yaml` contiene metadatos opcionales para Codex.

## Uso

```text
Usa $improve-design para mejorar esta interfaz. Conserva las decisiones ya
confirmadas y dame una propuesta de alta fidelidad que pueda revisar.
```

Con una referencia:

```text
Usa $improve-design con estos mockups. Respeta su tipografía, componentes,
imágenes y contenido. Prototipa la reserva completa, incluida su confirmación,
y comprueba el resultado visual antes de entregarlo.
```

Sin una referencia:

```text
Usa $improve-design para diseñar un planificador de sesiones de concentración.
No tengo mockups. Crea una propuesta de alta fidelidad, deja que programe una
sesión hasta ver el resultado y recoge mi feedback al terminar.
```

Para una revisión visual breve:

```text
Usa $improve-design para mejorar la jerarquía de esta tarjeta. Un mockup de
alta fidelidad basta; no necesito navegación ni un índice de escenarios.
```

## Dos ejemplos ejecutables

1. [Con mockups: reservar un libro](examples/with-mockups/README.md). Incluye la referencia visual y un recorrido completo para seleccionar recogida, confirmar y ver la reserva.
2. [Sin mockups: programar una sesión](examples/without-mockups/README.md). Define su dirección visual y permite elegir actividad, duración y fecha hasta obtener una sesión programada.

Para verlos, descarga o clona el repositorio y abre el `index.html` de cada ejemplo. No hay dependencias de aplicación ni servicios externos. Si prefieres servirlos localmente y ya tienes Python:

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

Desde la raíz del repositorio, abre:

- [Ejemplo con mockups](http://127.0.0.1:8765/examples/with-mockups/).
- [Ejemplo sin mockups](http://127.0.0.1:8765/examples/without-mockups/).

Detén el servidor con `Ctrl+C`. Esta dirección sólo funciona en la computadora que lo ejecuta. El acceso desde un teléfono requiere una configuración de red local autorizada; no se publica una web al instalar la skill.

Los ejemplos usan datos ficticios y simulan las operaciones en memoria. Guardan comentarios en el navegador cuando está disponible y permiten descargarlos. No envían feedback al agente ni entre dispositivos. Al abrir archivos directamente, el almacenamiento puede no estar disponible; el ejemplo avisa y mantiene la exportación.

## Herramientas y límites

La skill no exige OpenPencil, Figma, un framework ni otra skill. Usa las herramientas disponibles para el proyecto. Las funciones de edición visual, navegador o capturas requieren herramientas que las permitan; si una comprobación no puede realizarse, debe indicarse.

No incluye autenticación, backend de feedback ni publicación automática. Aprobar un diseño no autoriza implementar el producto o desplegarlo. La comprobación manual de ejemplos se documenta en [VALIDATION.md](VALIDATION.md).

## Estructura

```text
SKILL.md
agents/openai.yaml
references/fidelity.md
references/flows-and-feedback.md
examples/with-mockups/
examples/without-mockups/
LICENSE
```

## Licencia

[MIT](LICENSE), Copyright 2026 jerolan.
