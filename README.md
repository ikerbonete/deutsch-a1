# Deutsch A1 Trainer

App web (PWA) para estudiar alemán A1 con *Netzwerk neu A1.1*: artículos der/das/die, plurales, ein/kein, números, verbos, orden de la frase y vocabulario de los temas 1, 2 y 3.

Se publica con **GitHub Pages** desde la rama `main`, carpeta raíz. Funciona sin internet una vez abierta y se puede instalar en el móvil («Añadir a pantalla de inicio»).

## Archivos
- `index.html`: toda la app (HTML, CSS y JS en un solo archivo). Los datos están al principio del `<script>`: `N` (sustantivos), `VERBS`, `SENT` (frases), `PREP`, `SH`, `T1`, y las unidades en `UNITS`.
- `sw.js`: service worker (modo sin internet y actualizaciones).
- `manifest.webmanifest` e `icons/`: instalación como app.

## Cómo actualizar
1. Sustituir `index.html` por la versión nueva (y cualquier archivo nuevo que venga).
2. En `sw.js`, cambiar `VERSION` (por ejemplo `v2-2026-11-27`). Si no se cambia, los móviles pueden seguir mostrando la versión vieja.
3. `git add -A && git commit -m "Actualización: ..." && git push`.

El progreso del usuario se guarda en `localStorage` del móvil y no se pierde al actualizar.
