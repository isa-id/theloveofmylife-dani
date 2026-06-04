## Context

La página 2 contiene actualmente una carta ("Las noches") con decoraciones SVG y fondos personalizados. Debajo de la carta no hay más contenido. La primera galería (página 1) usa un grid de imágenes con overlay hover de gradiente verde y efecto zoom-in. La nueva sección "Recuerdos" debe ser visualmente distinta para no repetir el mismo patrón.

## Goals / Non-Goals

**Goals:**
- Agregar sección "Recuerdos" debajo de la carta en la página 2.
- Usar image placeholders (imágenes placeholder que el usuario reemplazará después).
- Diseño visual diferente a la primera galería: usar estilo polaroid/marco con borde blanco y sombra suave.
- Layout de imágenes en filas (2 columnas en desktop, 1 columna en mobile).
- Animación fade-in con desplazamiento hacia arriba al hacer scroll (AOS).
- Hover con elevación suave (shadow más pronunciada + translateY).
- Mantener la paleta de colores del proyecto (rosa pastel, verde pastel).

**Non-Goals:**
- No modificar la galería existente de la página 1.
- No agregar JavaScript más allá de AOS (ya incluido).
- No usar imágenes reales — solo placeholders SVG inline o generados.
- No cambiar la carta ni las decoraciones existentes.

## Decisions

### 1. Estilo polaroid en lugar de grid con overlay
**Decisión**: Cada recuerdo será un contenedor con borde blanco (simulando marco polaroid), imagen placeholder, y un texto descriptivo debajo.
**Razón**: Se diferencia visualmente de la primera galería que usa overlay hover. El estilo polaroid es más íntimo y combina con la temática romántica.
**Alternativa considerada**: Carrusel horizontal — descartado porque requiere JS adicional y es menos accesible en mobile.

### 2. Layout de 2 columnas en desktop, 1 columna en mobile
**Decisión**: Usar CSS grid con `grid-template-columns: repeat(2, 1fr)` en desktop y `1fr` en mobile.
**Razón**: La primera galería usa `auto-fit` con min 300px; este layout fijo de 2 columnas se ve diferente y es más controlable.
**Alternativa considerada**: Masonry — descartado por complejidad CSS sin librerías.

### 3. Placeholders SVG decorativos
**Decisión**: Generar SVGs placeholder con figuras abstractas (corazones, flores, formas orgánicas) en tonos de la paleta.
**Razón**: Son livianos, escalan bien, y se pueden reemplazar fácilmente por imágenes reales después.
**Alternativa considerada**: Imágenes de placeholder externas (picsum.photos) — descartado para no depender de red.

### 4. Animación con AOS (fade-up)
**Decisión**: Usar `data-aos="fade-up"` con delays escalonados, igual que otras secciones.
**Razón**: AOS ya está incluido en el proyecto, no agrega dependencias. El fade-up es diferente al zoom-in usado en la primera galería.

## Risks / Trade-offs

- **Imágenes placeholder genéricas** → El usuario deberá reemplazarlas por fotos reales después. Los SVGs son fáciles de identificar y reemplazar.
- **2 columnas en mobile muy angostas** → Mitigación: en viewport <= 480px se usa 1 columna.
- **Polaroid se ve muy similar a la carta** → Mitigación: el borde blanco del polaroid es más delgado y la imagen ocupa la mayor parte, mientras la carta es predominantemente texto.
