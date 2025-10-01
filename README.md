# zx_debate — Trabajo final MAES

Proyecto para la asignatura Complementos de Formación del Máster en Profesorado (Universidad de Granada).

- Demo: https://erseco.github.io/zx_debate/
- Emulador: JSSpeccy 2 (créditos más abajo)

## Descripción
Aplicación web estática que embebe un emulador de ZX Spectrum y carga un programa en formato `TAP` escrito en BASIC (archivos `.bas`/`.tap`) para lanzar una pregunta de debate en clase.

- Programa por defecto: `ernesto.tap` (definido en `index.html`).
- Programa alternativo: `juanbe.tap` (puedes cambiarlo editando `loadFile` en `index.html`).

## Requisitos y entorno
- Navegador moderno. Para ejecutar en local es recomendable servir los archivos con un servidor HTTP estático (para evitar problemas de CORS).
- Opcional (solo si quieres reconstruir los `.tap`): compilador ZX Basic (`zxb`).

## Inicio rápido
1) Ver la demo online: https://erseco.github.io/zx_debate/
2) Ejecutar en local:
   - Lanza un servidor estático en la carpeta del proyecto, por ejemplo:
     - Con Python 3: `python3 -m http.server 8000`
   - Abre `http://localhost:8000` en el navegador.

## Compilar los programas BASIC a TAP
Este repositorio incluye los fuentes en BASIC (`.bas`) y sus binarios para ZX Spectrum (`.tap`). Para regenerar un `.tap` a partir del `.bas` con ZX Basic:

```
zxb -o ernesto.tap -t -B -a ernesto.bas
```

Sustituye `ernesto` por `juanbe` si quieres compilar el otro programa.

## Estructura del proyecto
- `index.html`: página que inicializa JSSpeccy y carga el `.tap` indicado en `loadFile`.
- `ernesto.bas` / `ernesto.tap`: versión de la actividad de Ernesto.
- `juanbe.bas` / `juanbe.tap`: versión de la actividad de Juan.
- `jsspeccy-core.min.js`, `jsspeccy.css`, `jdataview.js`: dependencias del emulador.
- `favicon.ico`, otros estáticos.

## Notas y limitaciones
- Resolución de texto: 32 columnas × 24 filas = 768 caracteres en pantalla.
- Evitar vocales acentuadas: el juego de caracteres del Spectrum es limitado y puede no representar tildes correctamente.

## Créditos
Este proyecto utiliza parte del fantástico trabajo de JSSpeccy 2: https://github.com/gasman/jsspeccy2

## Licencia
GPL-3.0. Consulta el archivo `LICENSE` para más detalles.

---

# English Summary

Static web app embedding a ZX Spectrum emulator (JSSpeccy 2) that autoloads a `TAP` program written in BASIC to present a classroom debate prompt.

- Online demo: https://erseco.github.io/zx_debate/
- Default tape: `ernesto.tap` (set in `index.html` → `loadFile`). You can switch to `juanbe.tap` by editing that value.
- To run locally, serve the folder with any static web server (e.g., `python3 -m http.server 8000`) and open `http://localhost:8000`.
- To rebuild `.tap` from `.bas`, use ZX Basic (`zxb`), e.g.: `zxb -o ernesto.tap -t -B -a ernesto.bas`.

License: GPL-3.0. See `LICENSE`.
