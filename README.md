# Flor azul para mi novio 💙

## 1. Agrega tu foto
Pon tu foto collage aquí, con exactamente este nombre:
```
imagenes/collage.jpg
```
(Si tu foto es .png o .jpeg, cambia también el nombre dentro de `index.html` en la línea que dice `src="imagenes/collage.jpg"`).

## 2. Música
Ya está integrada la canción que elegiste mediante el reproductor oficial de Spotify (el botón 🎵 arriba a la derecha la despliega). No necesitas subir ningún archivo de audio.

Si más adelante quieres cambiar la canción:
1. Abre la canción en Spotify → ⋯ → Compartir → Copiar enlace.
2. Del link copia solo el código que va después de `/track/` y antes del `?` (ejemplo: en `open.spotify.com/track/3Y4m9Td603gbfMB86UNafs?si=...` el código es `3Y4m9Td603gbfMB86UNafs`).
3. En `index.html`, busca la línea con `open.spotify.com/embed/track/` y reemplaza el código por el nuevo.

La carpeta `musica/` ya no se usa, puedes eliminarla si quieres.

## 3. Sube el proyecto a GitHub
1. Crea una cuenta en https://github.com si no tienes una.
2. Crea un repositorio nuevo, público, con el nombre que quieras (ej. `flor-para-ti`). NO marques "Add a README" si ya tienes esta carpeta.
3. Sube estos 3 elementos a ese repositorio: `index.html`, la carpeta `imagenes/` y la carpeta `musica/`.
   - Más fácil: en la página del repo, dale clic a "Add file" → "Upload files", arrastra los archivos y dale "Commit changes".
4. Ve a **Settings** → **Pages** (en el menú lateral).
5. En "Source", selecciona la rama `main` y la carpeta `/root`, luego "Save".
6. Espera 1-2 minutos y GitHub te dará una URL como:
   ```
   https://tu-usuario.github.io/flor-para-ti/
   ```
7. ¡Esa es la liga que puedes mandar por WhatsApp! 💙

## Notas
- Si el archivo de música pesa mucho, considera comprimirlo o usar una versión más corta (WhatsApp y GitHub no tienen problema, pero carga más rápido si pesa poco).
- El botón 🔇/🔊 arriba a la derecha controla la música (no suena automático porque los navegadores lo bloquean si no hay un clic primero).
