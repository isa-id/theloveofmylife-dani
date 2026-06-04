## 1. Generación de imágenes

- [x] 1.1 Generar imagen de fondo externo para la sección `.page-2-letter` — estilo acuarela suave con formas orgánicas en rosa pastel (#FAD0C9) y verde pastel (#C1D7AE), resolución ~1200x800
- [x] 1.2 Generar imagen de fondo interno para el `.letter-card` de la página 2 — textura sutil decorativa tipo acuarela floral/orgánica en rosa pastel y verde pastel, resolución ~800x600
- [x] 1.3 Copiar las imágenes generadas a la carpeta `images/` del proyecto (ej: `images/page2-bg-section.png`, `images/page2-bg-card.png`)

## 2. Actualización de estilos CSS

- [x] 2.1 Modificar `.page-2-letter` en `styles.css`: reemplazar el gradiente actual por `background-image` con la nueva imagen de fondo externo, usando `background-size: cover` y `background-position: center`
- [x] 2.2 Agregar estilos para `.page-2-letter .letter-card` en `styles.css`: aplicar la imagen de fondo interno con un overlay blanco semitransparente (`rgba(255,255,255,0.85)`) para mantener legibilidad del texto
- [x] 2.3 Asegurar que los estilos usen selectores específicos (`.page-2-letter`, `.page-2-letter .letter-card`) para no afectar la carta de la página 1

## 3. Verificación

- [x] 3.1 Verificar visualmente que la página 2 muestra los nuevos fondos correctamente en desktop
- [x] 3.2 Verificar que el texto de la segunda carta es legible sobre los nuevos fondos
- [x] 3.3 Verificar que la primera carta (página 1) no fue afectada por los cambios
- [x] 3.4 Verificar responsive: fondos se adaptan correctamente en tablet y móvil
