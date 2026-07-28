# Raiza · Club de Mate — Landing

Landing page del catálogo de **Raiza** (mates artesanales, rancheros de algarrobo,
bombillas, yerba y sets). Sitio estático — HTML/CSS/JS puro, sin build ni dependencias.

Materializado desde el diseño de Claude (`RAIZA Catalogo.dc.html`).

## Ver localmente

Abrí `index.html` en el navegador, o serví la carpeta:

```bash
npx serve .
```

## Deploy en Vercel

Es un sitio estático en la raíz del repo, así que Vercel lo detecta solo:

1. En Vercel → **Add New… → Project** → importá `Maximogargiulo11/Raiza`.
2. Framework Preset: **Other** (o *Static*). Root: `/`. Sin build command.
3. Deploy. Listo.

## Configuración

- **WhatsApp:** el número está en `index.html` (variable `WA`, formato
  `54` + `9` + número, hoy `5493834021235`). Cambialo ahí si hace falta.
- **Instagram:** los links apuntan a `instagram.com/raizaclubdemate`.

## Fotos de productos

Las imágenes viven en `uploads/`. Ya están incluidas el logo, el fondo de madera,
la foto de "Nosotros" y una de Instagram. Las **fotos de producto** todavía no
están en el repo (por un límite del canal de importación): cada tarjeta muestra
un placeholder elegante con el nombre del producto hasta que agregues la foto.

Para que aparezcan, copiá tus fotos originales dentro de `uploads/` con **exactamente
estos nombres** (respetá espacios y mayúsculas):

```
uploads/torpedo clasico.JPG
uploads/imperial clasico.JPG
uploads/imperial crudo.JPG
uploads/torpedo base bolita.JPG
uploads/mate criollo.JPG
uploads/porito con base de cuero.JPG
uploads/galleta.JPG
uploads/camionero mundial.JPG
uploads/criollo diselo de autor.JPG
uploads/camionero clasico.JPG
uploads/Sasha standar.JPG
uploads/sasha un color.JPG
uploads/sasha 2 colores.JPG
uploads/sasah ranchero 2 colores.JPG
uploads/ranchero sasha.JPG
uploads/yerba sol y lluvia.JPG
uploads/set matera.JPG
```

En cuanto el archivo exista, la foto reemplaza al placeholder automáticamente
(no hay que tocar código). Las bombillas no llevan foto por diseño.

## Estructura

```
index.html                 · la landing completa (markup + estilos + lógica)
uploads/                   · imágenes (logo, fondo, nosotros, instagram, productos)
```
