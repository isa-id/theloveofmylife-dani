## Context

El sitio web "Para ti, mi amor" es un libro digital romántico con dos páginas (flip-book). La página 1 contiene una galería de fotos y una primera carta. La página 2 contiene una segunda carta titulada "Queridx..." que actualmente tiene un fondo CSS plano (`linear-gradient(135deg, var(--bg-color) 0%, #fdfbfb 100%)`). La paleta del sitio usa rosa pastel (`#FAD0C9`) y verde pastel (`#C1D7AE`).

La estructura actual de la página 2:
- `.page-2-letter` — sección envolvente con fondo gradiente simple.
- `.letter-card` — tarjeta contenedora de la carta con fondo blanco semitransparente, bordes rosa y verde.

## Goals / Non-Goals

**Goals:**
- Generar imágenes decorativas con IA en tonos rosa pastel y verde pastel.
- Aplicar una imagen como fondo externo de `.page-2-letter` (la sección completa).
- Aplicar una imagen como fondo/decoración del `.letter-card` en la página 2.
- Mantener la legibilidad del texto sobre los nuevos fondos.
- Mantener coherencia visual con la paleta existente del sitio.

**Non-Goals:**
- No modificar la estructura HTML existente.
- No cambiar los fondos de la página 1 (primera carta).
- No agregar dependencias JavaScript ni librerías nuevas.

## Decisions

### 1. Generación de imágenes con herramienta IA
**Decisión**: Usar la herramienta `generate_image` para crear las imágenes de fondo.
**Razón**: Permite crear imágenes personalizadas que coincidan exactamente con la paleta rosa pastel/verde pastel del sitio sin necesidad de buscar assets externos.

### 2. Tipo de imágenes a generar
**Decisión**: Generar imágenes de estilo abstracto/orgánico suave con formas fluidas, flores acuareladas o texturas delicadas.
**Razón**: Un estilo acuarelado/suave complementa la temática romántica del sitio y no compite visualmente con el texto de la carta.

### 3. Aplicación CSS con overlays de opacidad
**Decisión**: Usar `background-image` con un overlay de color semitransparente encima para asegurar legibilidad.
**Razón**: Permite ver las imágenes decorativas sin sacrificar la lectura del texto.

### 4. Scoping al page-2 con selectores CSS específicos
**Decisión**: Usar `.page-2-letter` y `.page-2-letter .letter-card` como selectores para no afectar la carta de la página 1.
**Razón**: Ambas cartas comparten las mismas clases base; necesitamos selectores más específicos para diferenciarlas.

## Risks / Trade-offs

- **Rendimiento de imágenes grandes** → Mitigación: generar imágenes de resolución razonable (~1200x800 para el fondo externo, ~800x600 para la tarjeta) y asegurar que sean comprimidas.
- **Legibilidad del texto** → Mitigación: usar overlays semitransparentes blancos sobre las imágenes de fondo del letter-card.
- **Consistencia de colores generados** → Mitigación: ser explícito en los prompts de generación con los códigos de color exactos de la paleta.
