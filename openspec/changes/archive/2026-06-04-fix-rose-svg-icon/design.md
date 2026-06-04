## Context

El sitio usa Font Awesome 6.4.0 Free CDN. `fa-rose` es un ícono Pro que no está disponible en la versión gratuita, resultando invisible en la página 2. La paleta del sitio usa rosa pastel (`#FAD0C9`, `#E99E95`) y verde pastel (`#C1D7AE`, `#8DA87A`).

## Goals / Non-Goals

**Goals:**
- Reemplazar `fa-rose` con un SVG inline de rosa que siempre sea visible.
- El SVG debe verse como una rosa realista con pétalos, capas, sépalos, tallo y hojas.
- Usar la paleta de colores existente del sitio.
- Mantener la animación `sway` existente.
- Asegurar responsive (el SVG debe escalar en móvil).

**Non-Goals:**
- No cambiar la estructura de la página.
- No afectar la página 1 ni su ícono de corazón.
- No agregar dependencias externas.

## Decisions

### 1. SVG inline vs imagen externa
**Decisión**: Usar SVG inline.
**Razón**: No requiere carga adicional, es escalable, se puede animar con CSS, y se integra directamente en el HTML.

### 2. Diseño de la rosa
**Decisión**: Rosa con 6 capas de pétalos (exteriores, medios, laterales, interiores, espiral, centro), sépalos verdes en la base, tallo con vena central y 2 hojas con venas.
**Razón**: Provee profundidad y realismo sin ser una imagen bitmap.

### 3. Gradiente radial
**Decisión**: Usar `radialGradient` que va de rosa claro (`#FAD0C9`) a rosa medio (`#E99E95`) a rosa oscuro (`#D4837A`) y verde (`#C1D7AE`) en los bordes.
**Razón**: Simula el sombreado natural de una rosa y conecta con la paleta del sitio.

## Risks / Trade-offs

- **Complejidad del SVG** → El SVG tiene ~15 paths, lo que añade algo de markup al HTML pero sigue siendo mucho más ligero que una imagen.
- **Mantenimiento** → Si se quiere cambiar la rosa, hay que editar los paths del SVG. Es más fácil que generar una imagen nueva.
