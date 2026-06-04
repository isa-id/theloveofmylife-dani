## ADDED Requirements

### Requirement: Sección Recuerdos en página 2
La página 2 SHALL tener una sección "Recuerdos" debajo de la carta, que contenga image placeholders con estilo polaroid/marco. La sección SHALL tener un título "Recuerdos" y una breve descripción.

#### Scenario: Visualización de la sección Recuerdos
- **WHEN** el usuario navega a la página 2 y desplaza hacia abajo después de la carta
- **THEN** se muestra una sección titulada "Recuerdos" con image placeholders en estilo polaroid

#### Scenario: La primera galería no se modifica
- **WHEN** el usuario visualiza la galería de la página 1
- **THEN** la galería mantiene su estilo original sin cambios

### Requirement: Image placeholders con estilo polaroid
Cada recuerdo SHALL tener un contenedor con borde blanco (simulando marco de polaroid), una imagen placeholder SVG y un texto descriptivo debajo de la imagen.

#### Scenario: Estilo polaroid en cada recuerdo
- **WHEN** el usuario ve un recuerdo en la sección Recuerdos
- **THEN** el recuerdo muestra un marco blanco alrededor de la imagen con una sombra suave, y un texto corto debajo

#### Scenario: Imagen placeholder SVG
- **WHEN** el usuario ve un recuerdo
- **THEN** la imagen es un SVG placeholder decorativo en tonos de la paleta del sitio (rosa pastel, verde pastel) que el usuario puede reemplazar después

### Requirement: Diseño responsive de la sección
La sección Recuerdos SHALL adaptar su layout según el viewport: 2 columnas en desktop (>= 768px), 1 columna en mobile (< 768px).

#### Scenario: Layout en desktop
- **WHEN** el viewport es 768px o mayor
- **THEN** los recuerdos se muestran en 2 columnas

#### Scenario: Layout en mobile
- **WHEN** el viewport es menor a 768px
- **THEN** los recuerdos se muestran en 1 columna

### Requirement: Animación fade-up
Cada recuerdo SHALL tener una animación de entrada "fade-up" al hacer scroll, usando AOS (ya incluido en el proyecto) con delays escalonados.

#### Scenario: Animación al hacer scroll
- **WHEN** el usuario desplaza la página y un recuerdo entra al viewport
- **THEN** el recuerdo aparece con una animación fade-up

### Requirement: Hover con elevación
Al hacer hover sobre un recuerdo, este SHALL elevarse ligeramente (translateY negativo) con una sombra más pronunciada.

#### Scenario: Efecto hover en recuerdo
- **WHEN** el usuario pasa el cursor sobre un recuerdo
- **THEN** el recuerdo se eleva ligeramente y su sombra se intensifica

### Requirement: Uso de la paleta de colores del sitio
La sección Recuerdos SHALL usar los colores definidos en las variables CSS del proyecto: rosa pastel, verde pastel, fondo claro.

#### Scenario: Coherencia visual
- **WHEN** el usuario navega entre la página 1 y la página 2
- **THEN** los colores de la sección Recuerdos se integran armoniosamente con el resto del sitio
