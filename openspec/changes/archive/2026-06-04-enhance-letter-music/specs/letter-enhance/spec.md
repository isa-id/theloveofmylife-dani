## ADDED Requirements

### Requirement: Carta visualmente destacada
La sección de la carta SHALL tener un diseño visual que la haga más prominente que la galería de fotos, usando colores verde pastel y rosa pastel como acentos decorativos.

#### Scenario: Carta con énfasis visual
- **WHEN** el usuario hace scroll hasta la sección de la carta
- **THEN** la carta SHALL tener un fondo más intenso, bordes decorativos dobles (rosa y verde), una sombra más pronunciada que la galería, y un efecto glow/hover

### Requirement: Decoración con colores del proyecto
La carta SHALL usar las variables CSS --primary-pink, --dark-pink, --primary-green, --dark-green con énfasis decorativo adicional.

#### Scenario: Acentos decorativos
- **WHEN** la carta se renderiza
- **THEN** los bordes SHALL combinar rosa y verde, el fondo SHALL tener un gradiente sutil, y los íconos decorativos (corazones) SHALL ser más visibles

### Requirement: Efecto hover en la carta
La carta SHALL tener un efecto hover que la haga "brillar" o resaltar aún más al pasar el mouse.

#### Scenario: Hover con glow
- **WHEN** el usuario pasa el mouse sobre la carta
- **THEN** la carta SHALL aumentar ligeramente su sombra y brillo, con una transición suave de 0.3 segundos
