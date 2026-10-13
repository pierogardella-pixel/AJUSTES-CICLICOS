# Firebase para dashboard de Inventarios 3A

La integración está preparada en la rama `firebase-integracion` y NO se ha fusionado a la web principal.

## Falta conectar el proyecto Firebase

- Conectar Firebase desde ChatGPT o crear un proyecto en https://console.firebase.google.com.
- Habilitar Cloud Firestore y Firebase Authentication: proveedor Google.
- En Firebase Auth → Authorized domains agregar `pierogardella-pixel.github.io`.
- Registrar la aplicación web en Firebase y copiar la configuración pública de la app a `firebase-config.js`.
- Configurar la regla `firestore.rules` sustituyendo `REEMPLAZAR_CORREO_EDITOR_AUTORIZADO` por el correo Google del editor autorizado y publicarla.
- Probar lectura y escritura usando una cuenta autorizada. Después fusionar `firebase-integracion` a `main`.

## Arquitectura

GitHub Pages aloja HTML, scripts y logo original de 3A. El ícono de pestaña sigue siendo AJE. Firestore sirve la última versión del inventario a todos los visitantes. Solo el editor autenticado mediante Google puede guardar y publicar datos. JSZip comprime el conjunto de datos y el cliente lo divide en documentos menores a 1 MiB, con puntero `aje_public/current` actualizado tras la subida completa. El sistema detecta conflictos de versión para evitar sobrescrituras accidentales.

**Importante**: el repositorio y las lecturas de Firestore serán públicos. No publicar información confidencial ni credenciales, ni habilitar escritura indiscriminada.
