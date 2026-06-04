## Why

La segunda carta (página 2) usaba `fa-rose` de Font Awesome, pero este ícono es parte del set **Pro** (no incluido en la versión gratuita 6.4.0), por lo que no se renderizaba — quedaba invisible. Se necesita reemplazar con un SVG inline de una rosa que sea autónomo, sin dependencias externas, y que además se vea más realista y detallado.

## What Changes

- **Reemplazar** `<i class="fa-solid fa-rose"></i>` por un SVG inline de una rosa con múltiples pétalos, sépalos, tallo y hojas.
- **Actualizar CSS** de `.icon-rose` para que funcione con SVG (remover `font-size`, agregar clase `.rose-svg` con dimensiones).
- **Ajustar responsive** para que el SVG se reduzca correctamente en móvil.
- **Mantener animación `sway`** existente en la rosa.

## Capabilities

### New Capabilities
- `rose-svg-icon`: SVG inline de rosa con gradiente radial rosa-verde, pétalos en capas, espiral central, sépalos, tallo y hojas — sin dependencias externas.

### Modified Capabilities
_(ninguna)_

## Impact

- **Archivos afectados**: `index.html` (SVG inline reemplaza ícono FA), `styles.css` (ajuste de clases para SVG).
- **Sin dependencias nuevas**: El SVG es 100% autónomo.
- **Sin cambios en estructura**: Solo se modifica el contenido del `.icon-rose` y su CSS asociado.
