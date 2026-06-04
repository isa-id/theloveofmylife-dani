## ADDED Requirements

### Requirement: Imágenes placeholder en la carta
La sección de la carta SHALL incluir imágenes decorativas placeholder que el usuario pueda reemplazar después.

#### Scenario: Imágenes decorativas visibles
- **WHEN** el usuario hace scroll a la sección de la carta
- **THEN** la carta SHALL mostrar imágenes placeholder (SVG o JPG pequeñas) en los laterales o como decoración de fondo

### Requirement: Layout con imágenes
Las imágenes SHALL estar integradas en el layout de la carta sin romper el diseño responsive.

#### Scenario: Imágenes responsive
- **WHEN** la pantalla cambia de tamaño
- **THEN** las imágenes SHALL redimensionarse proporcionalmente y no desbordar el contenedor de la carta

### Requirement: Fácil reemplazo
Las imágenes placeholder SHALL tener nombres claros y estar organizadas para que el usuario pueda reemplazarlas fácilmente.

#### Scenario: Nombres de archivo
- **WHEN** el usuario revisa los archivos de imagen
- **THEN** los nombres SHALL ser descriptivos (e.g., `letter-decoration-1.png`, `letter-decoration-2.png`)
