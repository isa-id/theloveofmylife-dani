## ADDED Requirements

### Requirement: Rosa SVG inline en página 2
La segunda carta (página 2) SHALL mostrar un SVG inline de una rosa en lugar del ícono `fa-rose` de Font Awesome. El SVG MUST ser autónomo (sin dependencias externas) y MUST renderizarse correctamente sin necesidad de librerías adicionales.

#### Scenario: Visualización de la rosa
- **WHEN** el usuario navega a la página 2
- **THEN** se muestra una rosa decorativa en lugar de un ícono vacío/invisible

#### Scenario: Sin dependencias externas
- **WHEN** el sitio se carga sin conexión a internet
- **THEN** la rosa SVG se renderiza igualmente porque está embebida directamente en el HTML

### Requirement: Diseño detallado de la rosa
La rosa SVG SHALL tener una apariencia realista con múltiples capas de pétalos, sépalos verdes en la base, tallo y hojas. SHALL usar un gradiente radial con tonos de la paleta del sitio.

#### Scenario: Apariencia de rosa realista
- **WHEN** el usuario observa la rosa en la página 2
- **THEN** la rosa muestra pétalos en capas con variación de color (gradiente), sépalos verdes, un tallo delgado y al menos una hoja

### Requirement: Animación sway
La rosa SHALL mantener la animación `sway` (balanceo suave) existente, igual que el ícono de corazón en la página 1 mantiene su animación `heartbeat`.

#### Scenario: Animación de balanceo
- **WHEN** la página 2 está visible
- **THEN** la rosa se balancea suavemente de lado a lado con una animación CSS infinita de 2.5s

### Requirement: Diseño responsive
La rosa SVG SHALL escalar apropiadamente en diferentes tamaños de pantalla, reduciéndose en viewports móviles.

#### Scenario: Tamaño en desktop
- **WHEN** el viewport es mayor a 480px
- **THEN** la rosa se muestra con un tamaño de 64x64 píxeles

#### Scenario: Tamaño en móvil
- **WHEN** el viewport es 480px o menor
- **THEN** la rosa se reduce a 48x48 píxeles
