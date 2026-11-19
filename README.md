# Barber VIP — web comercial

Sitio comercial estático de Barber VIP. Esta carpeta publica únicamente la página de presentación; no contiene ni modifica la aplicación, los usuarios, Firebase Authentication ni Firestore.

## Archivos

- `index.html`: página comercial completa.
- `vista-barbero.webp`: captura de la vista del profesional.
- `vista-cliente.webp`: captura de la vista del cliente.
- `firebase.json`: configuración de Firebase Hosting para el sitio comercial independiente.
- `.firebaserc`: proyecto Firebase existente `barbervip-309dc`.

Las dos capturas aparecen en el hero desde que se abre la página. Se precargan con prioridad alta y vuelven a mostrarse en la sección de vistas. Los archivos de imagen se sirven desde la raíz del sitio.

## 1. Copiar los archivos al repositorio comercial

Descomprimí este ZIP dentro de la carpeta raíz del repositorio `NachoMor123/barber-vip-web` y aceptá reemplazar los archivos existentes. No lo descomprimas dentro del repositorio de la aplicación `barber-vip`.

Desde la terminal, ubicada en la raíz de `barber-vip-web`, ejecutá:

```bash
git pull origin main
git add index.html vista-barbero.webp vista-cliente.webp firebase.json .firebaserc README.md
git commit -m "Actualiza web comercial con vistas de Barber VIP"
git push origin main
```

## 2. Publicar únicamente la web comercial en Firebase Hosting

Requiere Node.js y Firebase CLI. Si todavía no tenés Firebase CLI:

```bash
npm install -g firebase-tools
```

Después:

```bash
firebase login
firebase hosting:sites:list --project barbervip-309dc
```

La configuración apunta al sitio comercial independiente `barber-vip-comercial-309dc`. Si no aparece en el listado, crealo una sola vez:

```bash
firebase hosting:sites:create barber-vip-comercial-309dc --project barbervip-309dc
```

Finalmente, desde la raíz de `barber-vip-web`:

```bash
firebase deploy --only hosting --project barbervip-309dc
```

URL prevista: <https://barber-vip-comercial-309dc.web.app/>

Este deploy actualiza únicamente el sitio comercial configurado en este repositorio. No publica ni modifica el Hosting de la aplicación.
