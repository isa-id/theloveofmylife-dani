## Context

Actualmente la página es una sola vista con scroll vertical. Se desea agregar una segunda página accesible mediante un tab lateral derecho con animación de volteo tipo libro, manteniendo la estética actual (colores rosas/verdes pastel, tipografía Playfair Display + Lato).

## Goals / Non-Goals

**Goals:**
- Tab lateral derecho con ícono (>) que al clickearlo active una animación 3D de volteo de página
- Segunda página con una plantilla de carta que herede los estilos del proyecto
- Botón de retroceso (<) en la segunda página
- Animación suave en desktop y mobile

**Non-Goals:**
- No se modificará el contenido existente (hero, galería, carta actual)
- No se agregarán dependencias externas nuevas
- No se implementará funcionalidad de guardado/exportación de la carta

## Decisions

| Decisión | Opción elegida | Alternativas | Razón |
|---|---|---|---|
| Animación de volteo | CSS 3D transforms (`rotateY`, `perspective`) con JS vanilla | Librería JS externa (turn.js, pageflip) | Evita dependencias; la animación es simple (una página, no múltiples) |
| Estructura de páginas | Dos contenedores `.page` apilados dentro de un `.book-container` con posicionamiento absoluto | Cambiar el layout completo a un slider | Mínimo impacto en el markup existente |
| Tab lateral | Elemento `div.flip-tab` fijo con posición fixed | Botón inline en el header | Accesible desde cualquier punto de la pantalla, efecto visual tipo solapa de libro |
| Transición | `transform 0.8s ease-in-out` con `backface-visibility: hidden` | Transición más rápida (0.3s) o más lenta (1.5s) | 0.8s da sensación de libro sin ser demasiado lento |

## Risks / Trade-offs

- [Rendimiento] La animación 3D puede ser pesada en dispositivos muy antiguos → Usar `will-change: transform` y `translate3d` para aceleración por GPU
- [Overflow] El contenido de la página actual es largo; al ocultar la página 1 y mostrar la 2, el scroll debe resetearse → Llamar `window.scrollTo(0,0)` al navegar
- [Responsive] En mobile el tab debe ser más pequeño para no estorbar → Media query para reducir tamaño del tab
