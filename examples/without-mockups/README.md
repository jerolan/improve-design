# Sin mockups: programar una sesión

## Petición

```text
Usa $improve-design para diseñar una forma sencilla de programar una sesión
de concentración. No tengo mockups. Quiero elegir una actividad, ajustar la
duración y la fecha, confirmar y ver la sesión programada antes de opinar.
```

## Dirección elegida

Una interfaz de planificación tranquila: fondo marfil, texto ciruela, superficies claras y controles lavanda. La tipografía del sistema mantiene una lectura familiar; una jerarquía amplia distingue actividad, duración y fecha. La dirección queda definida dentro del propio prototipo mediante variables de color y componentes comunes.

No hace falta un mockup previo. Cada estado del recorrido tiene contenido, medidas, controles y resultados terminados. Una petición que sólo necesitara revisar la composición podría usar una única pantalla estática con esta misma calidad visual.

## Probar

Abre [index.html](index.html). Lee la ficha, pulsa Iniciar y completa:

1. Elige una actividad.
2. Indica duración y fecha. Prueba también un valor inválido.
3. Revisa los datos y confirma.
4. Comprueba que la sesión programada conserva tus elecciones.
5. Pulsa Dar feedback. Puedes salir antes y guardar una revisión parcial.

Volver conserva las entradas. Reiniciar restablece la sesión simulada y conserva los comentarios. El botón final sólo marca el recorrido como completado después de confirmar.

La sesión no crea un evento de calendario real. Los comentarios se guardan en este navegador cuando dispone de almacenamiento y se pueden descargar. No se transmiten al agente ni a otro dispositivo.

## Resultado del recorrido

![Sesión programada](result.jpg)
