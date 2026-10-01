# Dos regalos 🧡💙

Dos páginas estáticas, cada una con su fecha. Sin build, sin dependencias: HTML, CSS y JS en un solo archivo cada una.

## Qué es cada archivo

| Archivo | Para qué | Link |
|---|---|---|
| `sorpresa.html` | Pista Hot Wheels, 30 de septiembre | `/para-ti/sorpresa.html` |
| `flor.html` | Flor azul, 3 de octubre | `/para-ti/flor.html` |
| `index.html` | Página puente sin pistas, para que recortar la URL no revele nada | `/para-ti/` |

Base del sitio: `https://algoritmo-app.github.io/para-ti/`

Medios:

```
imagenes/collage.jpeg            → flor.html
imagenes/collage-sorpresa.jpeg   → sorpresa.html
video/clip.mp4                   → sorpresa.html
originales/                      → fotos sin editar, IGNORADA por git
```

## Cómo no arruinar la sorpresa

El `<title>` y la `<meta description>` de ambas páginas son neutros a propósito: es lo que WhatsApp lee para armar la vista previa del enlace. Si los cambias por algo descriptivo, el link delata el regalo antes de que lo abran.

`index.html` nunca debe enlazar a `sorpresa.html` ni a `flor.html`. Es justo lo que evita que recortando la URL se llegue al otro regalo antes de su fecha.

## Cambiar la canción

Cada página trae su propio track de Spotify.

1. En Spotify: canción → ⋯ → Compartir → Copiar enlace.
2. Del link toma solo el código entre `/track/` y el `?`. En `open.spotify.com/track/3Y4m9Td603gbfMB86UNafs?si=...` el código es `3Y4m9Td603gbfMB86UNafs`.
3. En el archivo que quieras, reemplázalo en **dos** lugares: la constante `spotifyTrackUri` y el enlace de respaldo `spotifyFallback`.

## Cambiar las fotos

El collage de `sorpresa.html` se armó con un script a partir de las cinco fotos de `originales/`. Si cambias las fotos hay que volver a generarlo; no se actualiza solo.

## Publicar cambios

```powershell
git add <archivos>
git commit -m "mensaje"
git push
```

GitHub Pages reconstruye en uno o dos minutos.

## Si no ves tus cambios en el navegador

No es el código. GitHub Pages manda `Cache-Control: max-age=600`, así que tu navegador guarda el HTML diez minutos. Como las frases van embebidas en ese mismo archivo, un HTML viejo significa textos viejos.

Recarga con **Ctrl + Shift + R**, o deja el DevTools abierto (F12) con "Disable cache" marcado en la pestaña Network.

Solo te pasa a ti por estar recargando. Quien abra el link por primera vez recibe la versión actual.

## Advertencia

`originales/` está en `.gitignore`, o sea que **solo existe en esta máquina** y no se respalda en GitHub. Si formateas, esas fotos se pierden. Los collages sí están en el repo, pero no los originales en resolución completa.
