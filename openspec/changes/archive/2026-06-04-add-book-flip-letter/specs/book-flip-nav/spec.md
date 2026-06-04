## ADDED Requirements

### Requirement: Tab lateral de navegación
El sistema SHALL mostrar un tab lateral fijo en el lado derecho de la pantalla con un ícono de flecha (>) que indique avance a la siguiente página.

#### Scenario: Tab visible en página principal
- **WHEN** el usuario carga la página principal
- **THEN** el tab lateral derecho SHALL ser visible con el ícono (>) y un texto o tooltip que indique "Siguiente"

#### Scenario: Tab oculto en segunda página
- **WHEN** el usuario navega a la segunda página
- **THEN** el tab lateral derecho SHALL desaparecer u ocultarse

### Requirement: Animación de volteo de página
El sistema SHALL animar la transición entre páginas con un efecto 3D de volteo tipo libro usando CSS transforms.

#### Scenario: Transición suave al avanzar
- **WHEN** el usuario hace clic en el tab (>) de la página principal
- **THEN** la página principal SHALL rotar sobre el eje Y con perspectiva 3D, revelando la segunda página en 0.8 segundos

#### Scenario: Transición suave al retroceder
- **WHEN** el usuario hace clic en el botón (<) de la segunda página
- **THEN** la segunda página SHALL rotar sobre el eje Y en sentido inverso, revelando la página principal en 0.8 segundos

### Requirement: Botón de retroceso
La segunda página SHALL tener un botón o tab lateral izquierdo con ícono (<) para volver a la página principal.

#### Scenario: Botón visible en segunda página
- **WHEN** el usuario está en la segunda página
- **THEN** el botón (<) SHALL ser visible en el lado izquierdo de la pantalla

#### Scenario: Retroceso a página principal
- **WHEN** el usuario hace clic en el botón (<) en la segunda página
- **THEN** el sistema SHALL mostrar la página principal con la animación de volteo inversa

### Requirement: Comportamiento responsive
El sistema SHALL adaptar el tamaño del tab y la animación para pantallas pequeñas (menos de 768px de ancho).

#### Scenario: Tab en mobile
- **WHEN** la pantalla tiene menos de 768px de ancho
- **THEN** el tab SHALL tener un tamaño reducido (padding y font-size menor) para no obstruir el contenido

#### Scenario: Animación funcional en mobile
- **WHEN** la pantalla tiene menos de 768px de ancho
- **THEN** la animación 3D SHALL seguir funcionando correctamente
