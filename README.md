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

## Panel de administración (`/admin`)

Los productos y los posts de Instagram se editan desde un panel web sin tocar código.
Los datos viven en `data/products.json` y `data/instagram.json`; la landing los lee al cargar.

**Cómo entrar:** andá a `tu-sitio.vercel.app/admin`. Te pide un **token de GitHub**
(se guarda solo en tu navegador). Con el token, el panel guarda cada cambio haciendo
un commit al repo y Vercel republica solo en ~30s.

**Crear el token (una sola vez):**
1. GitHub → **Settings → Developer settings → Personal access tokens → Fine-grained tokens → Generate new token**.
2. **Resource owner:** tu usuario. **Repository access:** *Only select repositories* → `Maximogargiulo11/Raiza`.
3. **Permissions → Repository permissions → Contents:** *Read and write*.
4. Generá el token (`github_pat_...`), copialo y pegalo en el panel. Guardá una copia en un lugar seguro.

**Qué podés hacer:**
- **Productos:** agregar / editar / borrar, con foto (la subís desde tu compu), categoría, precio, stock.
- **Instagram:** pegar las URLs de los posts que querés mostrar en la sección "Comunidad" (se ven como embeds reales).

> Nota: los productos con variantes (Yerba por tamaño, Set por color) se conservan y podés
> editarles nombre/foto/descripción; el editor de variantes queda para una etapa siguiente.

## Configuración

- **WhatsApp:** el número está en `index.html` (variable `WA`, formato
  `54` + `9` + número, hoy `5493834021235`). Cambialo ahí si hace falta.
- **Instagram:** el botón de perfil apunta a `instagram.com/raizaclubdemate` (en `index.html`).

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

**Más fácil:** desde el panel `/admin` podés editar cada producto y subirle la foto
directamente (sin nombres exactos ni commits manuales).

## Estructura

```
index.html                 · la landing (lee los datos de data/*.json)
admin.html                 · panel de administración (se abre en /admin)
data/products.json         · catálogo (categorías + productos)
data/instagram.json        · posts de Instagram a mostrar
vercel.json                · cleanUrls (para que /admin funcione sin .html)
uploads/                   · imágenes (logo, fondo, nosotros, fotos de producto)
fonts/                     · tipografía Sanchez
```
