## Why

El sitio está diseñado con desktop en mente pero será visto principalmente en celular. La experiencia mobile necesita ser óptima: textos legibles, elementos bien espaciados, sin scroll horizontal, y navegación táctil cómoda. Además la sección de la carta se beneficiaría de imágenes decorativas placeholder para hacerla más atractiva visualmente.

## What Changes

- Optimizar toda la responsividad para mobile-first (pantallas <768px y <480px)
- Ajustar tamaños de fuente, espaciados, hero, galería, carta y footer para mobile
- Asegurar que la navegación tipo libro (flip) funcione correctamente en pantallas pequeñas
- Agregar imágenes placeholder decorativas en la sección de la carta (que el usuario reemplazará después)
- El reproductor de música no debe obstruir el contenido en mobile

## Capabilities

### New Capabilities
- `letter-images`: Imágenes placeholder decorativas en la sección de la carta
- `mobile-first-responsive`: Optimización completa de responsividad para enfoque mobile-first

### Modified Capabilities
<!-- No existing specs to modify -->

## Impact

- `index.html`: Agregar imágenes placeholder en la sección de carta
- `styles.css`: Revisar y expandir todos los media queries para mobile-first, agregar estilos para imágenes en la carta
- `images/`: Agregar imágenes placeholder para la carta
