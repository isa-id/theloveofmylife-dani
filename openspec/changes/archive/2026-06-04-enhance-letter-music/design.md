## Context

La sección de carta actual usa un diseño sutil (fondo transparente, bordes suaves). Se necesita realzarla visualmente para que sea el punto focal emocional de la página. Además se agregará un reproductor de música con archivos locales .mp3 que funcionen en Netlify (static hosting).

## Goals / Non-Goals

**Goals:**
- La carta debe ser visualmente más prominente que la galería de fotos
- Usar verde pastel y rosa pastel como colores decorativos destacados
- Reproductor de música con controles: play/pausa, siguiente/anterior canción
- Los archivos de audio deben estar en el repo (funcionan en Netlify sin backend)
- Diseño responsive

**Non-Goals:**
- No se modificará el contenido textual de la carta
- No se cambiará la galería ni el hero
- No se usarán servicios externos de streaming (Spotify, SoundCloud)

## Decisions

| Decisión | Opción elegida | Alternativas | Razón |
|---|---|---|---|
| Formato audio | .mp3 con HTML5 Audio API | YouTube embed, Spotify iframe | .mp3 funciona en Netlify static hosting, sin dependencias externas |
| Ubicación reproductor | Flotante fijo (fixed) en esquina inferior | Integrado en la página | Siempre accesible mientras se lee la carta |
| UI del reproductor | Controles minimalistas con iconos Font Awesome | Reproductor nativo `<audio>` | El nativo tiene estilo distinto al proyecto; custom se ve mejor |
| Lista de canciones | Array JS con rutas a archivos locales | Playlist dinámica desde API | Sin backend, archivos locales estáticos |
| Énfasis visual carta | Fondo semitransparente más intenso, bordes decorativos dobles, sombra más pronunciada, glow hover | Solo cambiar colores | Se necesita que destaque claramente sobre el resto |

## Risks / Trade-offs

- [Compatibilidad] .mp3 no funciona en algunos navegadores muy antiguos → Usar también .ogg como fallback o aceptar limitación
- [Tamaño] Archivos de música aumentan el tamaño del repo → Usar archivos pequeños (<3MB cada uno)
- [Auto-play] Navegadores bloquean autoplay de audio → El reproductor empieza en pausa, el usuario hace clic para iniciar
