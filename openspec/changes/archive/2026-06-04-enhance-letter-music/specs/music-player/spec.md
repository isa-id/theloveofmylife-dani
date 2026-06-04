## ADDED Requirements

### Requirement: Reproductor de música embebido
El sistema SHALL incluir un reproductor de música con controles de reproducción, pausa y cambio de canción, usando archivos de audio .mp3 locales que funcionen en Netlify (static hosting).

#### Scenario: Reproductor visible en la página
- **WHEN** el usuario carga la página
- **THEN** el reproductor SHALL ser visible en la esquina inferior derecha como un elemento flotante con ícono de música

### Requirement: Control de play/pausa
El reproductor SHALL tener un botón para reproducir y pausar la canción actual.

#### Scenario: Play y pausa
- **WHEN** el usuario hace clic en el botón de play/pausa
- **THEN** la canción actual SHALL reproducirse si estaba pausada, o pausarse si estaba reproduciendo

#### Scenario: Estado inicial en pausa
- **WHEN** la página se carga por primera vez
- **THEN** el reproductor SHALL estar en estado de pausa (respetando políticas de autoplay del navegador)

### Requirement: Cambio de canción
El reproductor SHALL tener botones para avanzar a la siguiente canción y retroceder a la anterior.

#### Scenario: Siguiente canción
- **WHEN** el usuario hace clic en el botón de siguiente
- **THEN** el reproductor SHALL detener la canción actual y comenzar a reproducir la siguiente de la lista

#### Scenario: Canción anterior
- **WHEN** el usuario hace clic en el botón de anterior
- **THEN** el reproductor SHALL detener la canción actual y comenzar a reproducir la canción anterior

### Requirement: Lista de reproducción
El reproductor SHALL tener una lista predefinida de canciones con metadatos (título y artista) y rutas a archivos .mp3.

#### Scenario: Visualización de canción actual
- **WHEN** una canción está sonando
- **THEN** el reproductor SHALL mostrar el título y artista de la canción actual

### Requirement: Diseño responsive
El reproductor SHALL adaptarse a pantallas pequeñas sin obstruir el contenido.

#### Scenario: Reproductor en mobile
- **WHEN** la pantalla tiene menos de 768px de ancho
- **THEN** el reproductor SHALL reducir su tamaño y opcionalmente colapsarse a un ícono minimalista
