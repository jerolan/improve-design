# Con mockups: reservar un libro

## Petición

```text
Usa $improve-design con mockup.jpg como referencia. Conserva la apariencia
editorial de la biblioteca y construye el recorrido para reservar el libro:
consultar disponibilidad, elegir recogida, confirmar y ver la reserva.
Quiero dar feedback después de llegar al final.
```

## Referencia y alcance

[mockup.jpg](mockup.jpg) muestra el estado inicial de la app a 390 × 844. Es una referencia de ejemplo creada para este repositorio, capturada desde ese estado con los mismos datos y componentes. No procede de un producto externo. El resto del recorrido amplía esa dirección visual; no afirma reproducir mockups de pantallas que no existen.

![Mockup de referencia](mockup.jpg)

## Probar

Abre [index.html](index.html). Lee la ficha, pulsa Iniciar y completa:

1. Consulta el libro disponible.
2. Selecciona el día de recogida.
3. Revisa y confirma tu elección.
4. Comprueba el recibo con el libro y el día elegido.
5. Pulsa Dar feedback. Puedes salir antes y guardar una revisión parcial.

Volver conserva la selección. Reiniciar restablece la reserva simulada y conserva los comentarios. El botón final sólo marca el recorrido como completado después de confirmar.

Las reservas son ficticias y no se envían. El ejemplo guarda comentarios en este navegador cuando dispone de almacenamiento y permite descargarlos. El agente no los recibe automáticamente.

## Resultado del recorrido

![Reserva confirmada](result.jpg)
