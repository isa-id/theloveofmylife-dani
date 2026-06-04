## Why

La página actual tiene toda la información en una sola vista (hero, galería, carta). Agregar una navegación tipo libro (paginación con animación de volteo) permitirá expandir el contenido sin saturar la pantalla, ofreciendo una experiencia más íntima y nostálgica — como hojear un álbum de recuerdos.

## What Changes

- Agregar un tab lateral derecho con animación que al hacer clic (>) navegue a una segunda página con efecto de volteo de libro
- La segunda página contendrá una plantilla de carta editable que mantenga la estética del proyecto (colores, tipografía, estilo visual)
- Agregar un botón de retroceso (<) para volver a la página principal
- Mantener la hero section, galería y sección de carta actual intactas en la página principal
- La navegación tipo libro debe funcionar en desktop y mobile

## Capabilities

### New Capabilities
- `book-flip-nav`: Navegación tipo libro con animación de volteo de página y tabs laterales de avance/retroceso
- `letter-template`: Plantilla de carta en página independiente que mantiene la identidad visual del proyecto

### Modified Capabilities
<!-- No existing specs to modify -->

## Impact

- `index.html`: Agregar estructura de páginas tipo libro con contenedores apilados
- `styles.css`: Agregar estilos para animación 3D de volteo, tabs laterales, y nueva página de carta
- `images/`: Sin cambios
- Sin nuevas dependencias externas (la animación se hará con CSS puro + JS vanilla)
