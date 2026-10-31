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

La web es HTML/CSS/JS estático. No necesita funciones de servidor, secretos ni facturación Blaze.

## Precio

La oferta visible es de ARS 8.000 mensuales. En Firebase Spark las renovaciones de los profesionales se verifican y activan manualmente; la web no procesa cobros ni débitos automáticos.
