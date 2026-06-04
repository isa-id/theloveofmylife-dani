## ADDED Requirements

### Requirement: Hero section responsive
El hero SHALL ocupar el viewport completo en mobile sin desbordamiento horizontal ni elementos cortados.

#### Scenario: Hero en pantalla <480px
- **WHEN** la pantalla tiene menos de 480px de ancho
- **THEN** el hero SHALL ocupar 100vh, el título SHALL tener font-size de al menos 1.8rem, y el background-attachment SHALL ser scroll (no fixed)

### Requirement: Galería responsive
La galería SHALL adaptar su grid a 1 columna en pantallas menores a 480px y 2 columnas entre 480px y 768px.

#### Scenario: Grid de galería en mobile
- **WHEN** la pantalla tiene menos de 480px
- **THEN** gallery-grid SHALL usar 1 columna con gap reducido

#### Scenario: Grid de galería en tablet
- **WHEN** la pantalla está entre 480px y 768px
- **THEN** gallery-grid SHALL usar 2 columnas

### Requirement: Carta responsive
La carta SHALL tener padding y espaciado adecuados para lectura en pantallas pequeñas.

#### Scenario: Carta en mobile
- **WHEN** la pantalla tiene menos de 480px
- **THEN** el letter-card SHALL tener padding reducido (2rem 1rem) y font-size de 1rem

### Requirement: Flip book en mobile
La navegación tipo libro SHALL funcionar correctamente en pantallas pequeñas.

#### Scenario: Flip en mobile
- **WHEN** la pantalla tiene menos de 480px
- **THEN** los tabs de navegación flip SHALL tener tamaño reducido y la animación SHALL seguir funcionando

### Requirement: Reproductor collapsable
El reproductor de música SHALL colapsarse a un diseño más compacto en pantallas muy pequeñas.

#### Scenario: Reproductor en <480px
- **WHEN** la pantalla tiene menos de 480px
- **THEN** el reproductor SHALL ocultar la información de la canción y mostrar solo los controles
