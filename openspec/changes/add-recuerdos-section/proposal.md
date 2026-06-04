## Why

La página 2 actualmente solo tiene la carta "Las noches". Después de ella no hay nada más, lo que hace que el contenido se sienta incompleto. Una sección "Recuerdos" con imágenes decorativas hará que la página 2 sea más especial y emotiva, manteniendo la temática romántica del sitio.

## What Changes

- **Agregar sección "Recuerdos"** debajo de la carta en la página 2, dentro del `#page-2` div.
- **Image placeholders** con estilo de marco/polaroid (diferente a la galería de la página 1 que usa grid con overlay hover).
- **Nuevo diseño visual** que se diferencie de la primera galería: layout de filas con imágenes enmarcadas, animación fade-in desde abajo, y un hover con elevación (shadow + translateY sutil).
- **Estilos CSS** específicos para la sección de recuerdos, responsivos para mobile.

## Capabilities

### New Capabilities
- `recuerdos-section`: Sección decorativa "Recuerdos" debajo de la segunda carta con image placeholders en estilo polaroid/marco, con animaciones propias y diseño responsive.

### Modified Capabilities
_(ninguna — no hay specs existentes para modificar)_

## Impact

- **Archivos afectados**: `index.html` (nueva sección dentro de `#page-2`), `styles.css` (nuevos estilos para la sección de recuerdos, responsive).
- **Sin dependencias nuevas**: Solo HTML y CSS puro.
- **Sin cambios en estructura existente**: La sección se agrega después de la carta, no modifica nada previo.
