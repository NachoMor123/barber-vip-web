# Barber VIP — Web comercial independiente

Esta carpeta contiene una web comercial estática para Barber VIP. No incluye ni modifica el código de la aplicación original.

## Publicar en Firebase Hosting
La web es estática y se publica como un sitio Hosting separado dentro del mismo proyecto Firebase que usa la aplicación.

1. Seleccioná el proyecto `barbervip-309dc`.
2. Creá el sitio Hosting secundario `barber-vip-web-309dc`.
3. Desde esta carpeta y con la rama `migration/firebase-hosting`, ejecutá `firebase deploy --only hosting:web --project barbervip-309dc`.

No requiere variables de entorno, Auth ni lecturas de Firestore.

## Acceso a la aplicación
Los dos botones del cuadro de acceso apuntan a la misma URL:
https://barbervip-309dc.web.app/

La web comercial no inicia sesión, no crea cuentas, no procesa pagos ni se conecta a Firebase. Solo presenta el producto y enlaza con la aplicación.

## Editar textos
La web está en un único `index.html` para que sea fácil de mover y editar. La demo de ciclos de cortes es ilustrativa; no guarda datos reales.
