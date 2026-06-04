## Why

La sección de la carta actual se ve bien pero no destaca lo suficiente. Al ser el mensaje más personal del sitio, merece una presentación más emotiva con colores que resalten. Además, agregar música de fondo con controles le dará una capa extra de sentimiento al visitar la página.

## What Changes

- Mejorar el diseño visual de la sección de la carta (letter-section) para que destaque más que la galería de fotos
- Aplicar colores verde pastel y rosa pastel con énfasis decorativo (bordes, sombras, fondos, tipografía)
- Agregar un reproductor de música con controles de reproducción, pausa y cambio de canción
- El reproductor debe funcionar en Netlify (archivos de audio locales o embebidos)
- Mantener la coherencia estética con el resto del proyecto

## Capabilities

### New Capabilities
- `letter-enhance`: Mejora visual de la sección de carta con colores destacados y diseño decorativo
- `music-player`: Reproductor de música embebido con controles de play/pausa y cambio de canción

### Modified Capabilities
<!-- No existing specs to modify -->

## Impact

- `index.html`: Modificar la sección de carta existente y agregar el reproductor de música
- `styles.css`: Nuevos estilos decorativos para la carta y estilos para el reproductor
- `images/` o `audio/`: Agregar archivos de música (formato .mp3 o .ogg compatibles con Netlify)
- Sin dependencias externas nuevas (reproductor con HTML5 Audio API + JS vanilla)
