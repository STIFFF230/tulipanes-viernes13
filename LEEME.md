# Viernes 13 💜

Abre `index.html` con doble clic. La página funciona sin instalar nada; las fuentes de Google se descargan al abrirla con conexión y tienen alternativas locales.

Para personalizarla, abre `index.html` en un editor y busca `const CONFIG` al principio del script. Cambia `para`, `frase`, `frase2` y `mensaje`, conservando las comillas. Si necesitas un apóstrofo dentro del texto, escríbelo como `\'`.

Para añadir música, pon tu canción en esta misma carpeta con el nombre `musica.mp3`. Empieza con el primer toque; el botón ♪ permite pausarla. Si no existe el archivo, el botón permanece oculto.

Toca los tulipanes para soltar pétalos y descubrir el mensaje en el primer toque. Toca el calendario para abrir la nota y de nuevo para restaurarlo. También puedes usar Tab y Enter o Espacio; Escape cierra el mensaje. Se respeta la preferencia de movimiento reducido del dispositivo.

## Publicar en GitHub Pages

Con Git y GitHub CLI instalados y `gh auth login` completado, ejecuta desde esta carpeta (elige otro nombre si el repositorio ya existe):

```sh
git init -b main
git add index.html LEEME.md
# Si añadiste la canción y tienes permiso para publicarla: git add musica.mp3
git commit -m "Crear página de tulipanes para viernes 13"
gh repo create tulipanes-viernes13 --public --source . --remote origin --push
```

En el repositorio de GitHub, abre **Settings → Pages → Build and deployment**, selecciona **Deploy from a branch**, rama **main**, carpeta **/ (root)** y pulsa **Save**. GitHub mostrará el enlace cuando termine la publicación.
