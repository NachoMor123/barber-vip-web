# Barber VIP — Web comercial independiente

Esta carpeta contiene una web comercial estática para Barber VIP. No incluye ni modifica el código de la aplicación original.

## Publicar en Vercel
1. Descargá y descomprimí el ZIP.
2. Creá un repositorio nuevo en GitHub, separado del repositorio de la aplicación.
3. Subí `index.html`, `README.md` y `vercel.json` a la raíz del repositorio.
4. En Vercel, importá ese repositorio nuevo y desplegá. No hace falta configurar variables de entorno ni Firebase.
5. Vercel detecta la web estática automáticamente.

## Acceso a la aplicación
Los dos botones del cuadro de acceso apuntan a la misma URL:
https://barber-vip-three.vercel.app/

La web comercial no inicia sesión, no crea cuentas, no procesa pagos ni se conecta a Firebase. Solo presenta el producto y enlaza con la aplicación.

## Editar textos
La web está en un único `index.html` para que sea fácil de mover y editar. La demo de ciclos de cortes es ilustrativa; no guarda datos reales.
