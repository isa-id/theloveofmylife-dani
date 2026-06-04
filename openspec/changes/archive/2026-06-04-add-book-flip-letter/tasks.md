## 1. Estructura HTML de páginas tipo libro

- [x] 1.1 Envolver el contenido existente (hero, gallery, letter, footer) en un contenedor `.page#page-1`
- [x] 1.2 Crear un segundo contenedor `.page#page-2` con la plantilla de carta
- [x] 1.3 Envolver ambas páginas en un `.book-container` con posicionamiento relativo

## 2. Estilos CSS para animación 3D de volteo

- [x] 2.1 Agregar estilos para `.book-container`, `.page` con perspectiva 3D y `backface-visibility`
- [x] 2.2 Definir la animación de volteo con `transform: rotateY()` para avance y retroceso
- [x] 2.3 Agregar clase `.flipped` para estado activo de la página 2
- [x] 2.4 Agregar `will-change: transform` para aceleración por GPU

## 3. Tab lateral de navegación (botón > )

- [x] 3.1 Agregar HTML del tab lateral derecho con ícono (>) y texto "Siguiente"
- [x] 3.2 Estilizar el tab con posición fixed, colores del proyecto y efecto hover
- [x] 3.3 Agregar estilos responsive para mobile (tamaño reducido)
- [x] 3.4 Ocultar el tab cuando la página 2 esté visible

## 4. Botón de retroceso (botón < )

- [x] 4.1 Agregar HTML del botón de retroceso en la página 2 con ícono (<)
- [x] 4.2 Estilizar el botón consistente con el tab derecho
- [x] 4.3 Ocultar el botón cuando la página 1 esté visible

## 5. JavaScript para la lógica de navegación

- [x] 5.1 Implementar función `flipForward()`: agrega clase `.flipped` al book-container, oculta tab derecho, resetea scroll
- [x] 5.2 Implementar función `flipBack()`: remueve clase `.flipped`, muestra tab derecho, resetea scroll
- [x] 5.3 Vincular eventos click a los botones de navegación

## 6. Plantilla de carta en página 2

- [x] 6.1 Agregar HTML de la carta con título, cuerpo decorativo, línea de firma y corazón animado
- [x] 6.2 Estilizar la carta con las variables CSS del proyecto (colores, tipografía, bordes, sombras)
- [x] 6.3 Asegurar espaciado generoso y diseño tipo carta abierta

## 7. Pruebas y ajustes finales

- [x] 7.1 Verificar animación fluida en navegador (Chrome/Firefox)
- [x] 7.2 Verificar funcionamiento responsive en mobile (<768px)
- [x] 7.3 Verificar que no hay regresión en el contenido existente
