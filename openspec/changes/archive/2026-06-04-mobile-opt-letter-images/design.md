## Context

Actualmente el sitio tiene estilos responsive básicos (un media query a 768px). Al ser mobile-first, se necesita optimizar toda la experiencia para pantallas pequeñas: hero, galería, carta, reproductor de música y navegación flip. También se agregarán imágenes placeholder decorativas en la carta.

## Goals / Non-Goals

**Goals:**
- Experiencia óptima en pantallas <768px y <480px
- Hero section que ocupe toda la pantalla sin desbordar
- Galería con grid de 1-2 columnas en mobile
- Carta con imágenes placeholder decorativas
- Flip book y reproductor de música funcionales en mobile
- Tipografía y espaciados ajustados para lectura táctil

**Non-Goals:**
- No se cambiará el contenido textual
- No se agregarán dependencias externas
- Las imágenes placeholder son decorativas, no funcionales

## Decisions

| Decisión | Opción elegida | Alternativas | Razón |
|---|---|---|---|
| Enfoque responsive | Mobile-first con media queries progresivos (base mobile, luego tablet/desktop) | Desktop-first con media queries max-width | Mobile-first es más natural cuando el público principal es celular |
| Imágenes en carta | Flebox layout con imágenes laterales decorativas | Background-image en CSS | Más fácil para el usuario reemplazar después |
| Formato imágenes placeholder | SVG inline o imágenes JPG placeholder pequeñas | PNG grandes | SVGs no requieren archivos externos y son ligeros |
| Grid galería mobile | 1 columna en <480px, 2 en <768px | Siempre 1 columna | 2 columnas aprovecha mejor el espacio en phablets |

## Risks / Trade-offs

- [Rendimiento] Imágenes placeholder aumentan peso de página → Usar SVGs o imágenes muy pequeñas (<10KB)
- [Flip book] La animación 3D puede ser exigente en móviles gama baja → Mantener `will-change` y `translate3d`
- [Reproductor] En pantallas muy pequeñas puede estorbar → Colapsar a solo ícono en <480px
