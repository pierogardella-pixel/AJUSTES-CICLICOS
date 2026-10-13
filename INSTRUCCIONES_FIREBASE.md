# Dashboard 3A · Firebase + GitHub Pages

**Editor autorizado:** `piero.gardella@ajiles.pe`.

1. Conectar Firebase mediante la integración de ChatGPT o abrir Firebase Console.
2. Crear un proyecto con Firestore Database.
3. Activar Firebase Authentication con Google como proveedor de inicio de sesión.
4. Añadir `pierogardella-pixel.github.io` a los dominios autorizados de Authentication.
5. En Firestore → Rules, publicar el contenido de `firestore.rules`. Está configurado para permitir escritura solo al correo editor y lectura pública.
6. Registrar una app web Firebase y pegar los identificadores públicos en `firebase-config.js`. El archivo actual contiene `null` intencionalmente.
7. Probar lectura sin sesión, escritura con `piero.gardella@ajiles.pe`, denegación de escritura con otras cuentas y actualización desde otro dispositivo.
8. Tras probarlo, integrar la rama `firebase-integracion` con `main` y desplegarla en GitHub Pages.

El dashboard **no solicita tokens de GitHub**. No se ha creado ni vinculado todavía un proyecto Firebase. Hasta terminar los pasos, la web principal sigue usando su sistema anterior.

**Privacidad**: GitHub Pages y los datos configurados con lectura pública pueden verse desde Internet. No subir credenciales ni información privada de trabajadores.
