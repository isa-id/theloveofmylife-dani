## ADDED Requirements

### Requirement: Plantilla de carta en segunda página
La segunda página SHALL contener una plantilla de carta que mantenga la estética del proyecto (colores pastel rosa/verde, tipografía Playfair Display para títulos y Lato para contenido).

#### Scenario: Visualización de la carta
- **WHEN** el usuario navega a la segunda página
- **THEN** la plantilla de carta SHALL mostrarse con:
  - Un título decorativo (ej. "Queridx...")
  - Un área de contenido con tipografía Lato
  - Una línea de firma decorativa
  - Un corazón animado (como en la sección de carta existente)

### Requirement: Consistencia visual con el proyecto
La plantilla de carta SHALL usar las mismas variables CSS (--primary-pink, --dark-pink, --primary-green, --dark-green, --bg-color) y seguir el mismo diseño general del proyecto.

#### Scenario: Estilos heredados
- **WHEN** la carta se renderiza en la segunda página
- **THEN** los colores, tipografías, bordes redondeados y sombras SHALL coincidir con los definidos en `:root` de `styles.css`

### Requirement: Diseño tipo carta abierta
La plantilla SHALL tener el diseño visual de una carta abierta (fondo tipo papel, bordes decorativos, espaciado generoso).

#### Scenario: Apariencia de carta
- **WHEN** el usuario ve la segunda página
- **THEN** la carta SHALL tener un fondo blanco con sombra suave, bordes redondeados (20px), y un espaciado interior de al menos 2rem
