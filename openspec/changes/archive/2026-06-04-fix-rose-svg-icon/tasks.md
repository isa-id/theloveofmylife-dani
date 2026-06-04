## 1. Reemplazo del ícono Font Awesome por SVG inline

- [x] 1.1 Reemplazar `<i class="fa-solid fa-rose"></i>` en `index.html` con un SVG inline de rosa con pétalos, sépalos, tallo y hojas
- [x] 1.2 Agregar gradiente radial con colores de la paleta del sitio (#FAD0C9, #E99E95, #D4837A, #C1D7AE)

## 2. Actualización de estilos CSS

- [x] 2.1 Modificar `.icon-rose` en `styles.css`: remover `font-size: 4rem` y `color`, ya que el SVG tiene su propio tamaño y color
- [x] 2.2 Agregar clase `.rose-svg` con dimensiones `width: 64px; height: 64px`
- [x] 2.3 Actualizar responsive: cambiar tamaño del SVG a 48px en viewport <= 480px

## 3. Verificación

- [x] 3.1 Verificar que la rosa se ve correctamente en la página 2
- [x] 3.2 Verificar que la animación `sway` funciona en el SVG
- [x] 3.3 Verificar que el ícono de corazón en la página 1 no fue afectado
- [x] 3.4 Verificar responsive: la rosa se reduce correctamente en móvil
