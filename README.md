# Manual de Ginger

Sitio estático con el manual de la app Ginger. Se publica en Vercel.

- `manual/index.html`: el manual (una sola página, sin dependencias).
- `manual/img/`: capturas de la app (390 × 844, build web, español, modo claro), la mascota y el ícono.
- `vercel.json`: `/` redirige a `/manual`.

## Actualizar las capturas

En el repo de la app: `node tool/capturas/capturas.mjs`. Se toman las de `capturas/*-es-AR-claro.png`, se pasan a WebP de 585 × 1266 y se reemplazan en `manual/img/` con el mismo nombre.

## Publicar en Vercel (una sola vez)

1. En Vercel: **Add New → Project** e importar `FamilyBussiness/manual-site`.
2. Framework preset: **Other**. Sin comando de build y con el directorio de salida por defecto (la raíz).
3. **Deploy.** Cada merge a `main` vuelve a publicar solo.

Para probarlo en tu computadora: `npx serve .` y abrir `http://localhost:3000/manual`.
