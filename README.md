# AJE · Inventario cíclico y ajustes

Dashboard de inventarios publicado con GitHub Pages.

## Datos compartidos

La página lee la última versión del archivo comprimido `data/latest.b64` desde la API pública de GitHub. Se cargan las sesiones de inventario, data maestra y ajustes AJU. Si no se ha publicado una actualización compartida, se muestran los datos iniciales incorporados en `index.html`.

Para editar datos compartidos, el propietario pulsa **Conectar GitHub** en la página, introduce un token **fine-grained** restringido a este repositorio con permiso **Contents: Read and write**, e importa el Excel o edita registros. Los cambios se publican automáticamente en el repositorio. El token permanece solo en memoria; nunca se añade al HTML ni al GitHub.

**Aviso:** este es un repositorio **público**. La información publicada en `data/latest.b64` puede ser vista por cualquier persona. No subir datos personales, secretos ni información que requiera acceso privado.

### Publicación

Este repositorio incluye un flujo de trabajo de GitHub Actions para GitHub Pages. Si la web no se activa automáticamente, abrir **Settings → Pages → Build and deployment → Source: GitHub Actions** y ejecutar el workflow **Publish dashboard AJE**.
