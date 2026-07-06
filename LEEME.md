# CONTROL SUTRAN — Backoffice · Paquete PWA para GitHub Pages

Contenido:
- `index.html` — el backoffice completo (autónomo, funciona offline)
- `manifest.webmanifest` — metadatos de la app (nombre, íconos, color)
- `sw.js` — service worker (cache offline)
- `icons/` — íconos 192, 512 y maskable

> El backoffice está diseñado para pantalla de escritorio/tablet (1440×900). En móvil se verá reducido; ideal en laptop o tablet horizontal.

## Publicar en GitHub Pages (paso a paso)

1. Crea una cuenta en github.com y un repositorio **Public** (ej. `control-sutran-backoffice`).
2. En el repo: **Add file → Upload files** y arrastra el CONTENIDO de esta carpeta:
   `index.html`, `manifest.webmanifest`, `sw.js` y la carpeta `icons/`.
   - `index.html` debe quedar en la RAÍZ del repositorio (no dentro de una subcarpeta).
3. **Commit changes**.
4. **Settings → Pages** → Source: **Deploy from a branch** → Branch: **main** / carpeta **/(root)** → **Save**.
5. Espera 1–2 min y recarga. Aparece la URL:
   `https://TU-USUARIO.github.io/control-sutran-backoffice/`
6. Ábrela (sirve por HTTPS, así que la PWA es instalable y funciona offline).
   En Chrome: menú ⋮ → **Instalar aplicación**.

## Generar APK (opcional, sin Android Studio) — PWABuilder
1. Con la URL de GitHub Pages publicada, entra a https://www.pwabuilder.com
2. Pega la URL → **Start** → **Package for stores** → Android → **Generate Package**.
3. Package ID sugerido: `pe.gob.sutran.backoffice`. Descarga el `.apk`/`.aab`.

## Alternativa rápida sin cuenta
Netlify Drop (https://app.netlify.com/drop): arrastra esta carpeta y obtén la URL al instante.

## Nota
Descarga de PDF y envío de correos están simulados (prototipo). En producción se conectan al servicio de generación de PDF y al de correo/firma digital (RENIEC).
