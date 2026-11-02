# Barber VIP — web comercial (Firebase Spark)

Sitio estático comercial de Barber VIP. No contiene cuentas, base de datos ni lógica de pagos: enlaza a la aplicación principal.

## Firebase

- Proyecto existente: `barbervip-309dc`
- Hosting target: `commercial`
- Site ID: `barber-vip-comercial-309dc`
- Dirección prevista: `https://barber-vip-comercial-309dc.web.app`
- CTA principal: `https://barbervip-309dc.web.app`

No crear otro proyecto Firebase ni registrar otra app web. Crear únicamente el segundo sitio de Hosting con ese Site ID.

## Publicación

Desde esta carpeta, una vez creado el sitio en Firebase Console:

```bash
npm install -g firebase-tools
firebase login
firebase use barbervip-309dc
firebase deploy --only hosting:commercial
```

La web es HTML/CSS/JS estático. No necesita funciones de servidor, secretos ni facturación Blaze. La aplicación conectada a este sitio utiliza Cloudflare Workers para Checkout y confirmación automática de Mercado Pago; esta web sólo enlaza a la app.

## Precio

La oferta visible es de ARS 8.000 por 30 días. El profesional paga desde el Checkout de Mercado Pago; cuando Mercado Pago confirma la acreditación, el Worker de la aplicación renueva automáticamente el acceso. No hay débitos automáticos.
