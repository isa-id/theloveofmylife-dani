## Why

La segunda carta (página 2, "Queridx...") actualmente tiene un fondo plano y genérico con un simple gradiente CSS. Se necesita mejorar visualmente esta página generando imágenes decorativas personalizadas en tonos rosa pastel y verde pastel que sirvan como:
1. Fondo interno del contenedor `.letter-card` (la tarjeta de la carta).
2. Fondo externo de la sección `.page-2-letter` (el área detrás de la tarjeta).

Esto hará que la segunda carta se sienta mucho más especial, con fondos ilustrativos y únicos que complementen la paleta del sitio.

## What Changes

- **Generar imágenes decorativas** en tonos rosa pastel (`#FAD0C9`) y verde pastel (`#C1D7AE`) usando IA:
  - Fondo externo para la sección de la página 2 (detrás de la tarjeta).
  - Fondo interno/decorativo para el contenedor `.letter-card` de la segunda carta.
- **Actualizar CSS** de `.page-2-letter` para usar la imagen generada como fondo de sección.
- **Actualizar CSS** de `.letter-card` dentro de la página 2 para incorporar la imagen decorativa como fondo de la tarjeta.
- **Ajustar opacidad y blending** para que el texto siga siendo legible sobre las nuevas imágenes de fondo.

## Capabilities

### New Capabilities
- `page2-backgrounds`: Fondos decorativos personalizados para la segunda carta — imágenes generadas en rosa pastel y verde pastel aplicadas como fondo externo de la sección y fondo interno del contenedor de la carta.

### Modified Capabilities
_(ninguna — no hay specs existentes)_

## Impact

- **Archivos afectados**: `styles.css` (nuevos estilos de fondo para page-2), `images/` (nuevas imágenes generadas).
- **Sin cambios en HTML**: Se usarán las clases CSS existentes (`.page-2-letter`, `.letter-card`); no se requiere modificar la estructura HTML.
- **Sin dependencias nuevas**: Solo imágenes estáticas y CSS puro.
- **Rendimiento**: Las imágenes de fondo se optimizarán para carga rápida.
