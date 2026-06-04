## ADDED Requirements

### Requirement: Fondo externo de la sección página 2
La sección `.page-2-letter` SHALL tener una imagen de fondo decorativa en tonos rosa pastel y verde pastel que reemplace el gradiente CSS actual. La imagen MUST cubrir toda la sección usando `background-size: cover` y MUST estar centrada con `background-position: center`.

#### Scenario: Visualización del fondo externo
- **WHEN** el usuario navega a la página 2 (flip a "Queridx...")
- **THEN** la sección completa muestra una imagen de fondo decorativa en colores rosa pastel y verde pastel, en lugar del gradiente plano anterior

#### Scenario: Fondo se adapta a diferentes tamaños de pantalla
- **WHEN** el usuario visualiza la página 2 en cualquier tamaño de pantalla (desktop, tablet, móvil)
- **THEN** la imagen de fondo se escala y recorta automáticamente para cubrir toda la sección sin deformarse

### Requirement: Fondo interno del contenedor letter-card en página 2
El `.letter-card` dentro de `.page-2-letter` SHALL tener una imagen de fondo decorativa sutil en tonos rosa pastel y verde pastel. La imagen MUST tener un overlay semitransparente encima para garantizar la legibilidad del texto.

#### Scenario: Visualización del fondo de la tarjeta
- **WHEN** el usuario ve la segunda carta
- **THEN** la tarjeta `.letter-card` muestra un fondo decorativo con textura/patrón suave en rosa pastel y verde pastel, con texto completamente legible

#### Scenario: Legibilidad del texto sobre el fondo decorativo
- **WHEN** el usuario lee el contenido de la segunda carta
- **THEN** el texto mantiene contraste suficiente contra el fondo decorativo gracias al overlay blanco semitransparente

### Requirement: Aislamiento de estilos a la página 2
Los nuevos estilos de fondo MUST aplicarse exclusivamente a la página 2 y NO MUST afectar la primera carta en la página 1.

#### Scenario: La primera carta no se modifica
- **WHEN** el usuario visualiza la primera carta (página 1)
- **THEN** la carta mantiene su estilo original sin cambios en fondos ni apariencia

### Requirement: Imágenes generadas en la paleta del sitio
Las imágenes de fondo generadas SHALL usar predominantemente tonos de rosa pastel (`#FAD0C9`, `#E99E95`) y verde pastel (`#C1D7AE`, `#8DA87A`) consistentes con la paleta definida en las CSS variables del sitio.

#### Scenario: Coherencia visual con el diseño existente
- **WHEN** el usuario navega entre la página 1 y la página 2
- **THEN** los colores de los fondos de la página 2 se integran armoniosamente con el resto del sitio sin generar contraste discordante
