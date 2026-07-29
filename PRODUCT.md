# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Materos argentinos apasionados por el ritual del mate, que buscan piezas
artesanales (no industriales) y valoran que cada mate sea hecho a mano, único y
con identidad. Compran principalmente por WhatsApp, muchos llegando desde
Instagram (@raizaclubdemate). Alcance nacional (envíos a todo el país).

## Product Purpose

Raiza · Club de Mate vende mates y accesorios artesanales y acerca a la gente al
ritual del mate como algo con raíz e identidad, no como un simple objeto de
consumo. El éxito es que el cliente elija una pieza con la que se identifique y
se sume a la comunidad matera de Raiza (consulta/compra por WhatsApp).

## Positioning

Piezas artesanales, hechas y elegidas a mano — calabaza, algarrobo, cuero y
alpaca — donde cada unidad es única y tiene "arraigo". No compite por precio ni
por volumen industrial, sino por autenticidad, oficio y pertenencia a un "Club
de Mate". Lema de marca: *"No vendemos mates, creamos rituales."*

## Operating Context

- Catálogo navegable por categorías: Mates Clásicos, Rancheros (algarrobo),
  Bombillas, Yerba y Sets & Accesorios.
- La venta no es checkout automático: cada producto abre una conversación de
  WhatsApp pre-cargada con el producto (y su variante) hacia el número de Raiza.
- Descubrimiento y prueba social vía Instagram (@raizaclubdemate); posts/reels
  embebidos reales en la landing.
- Base en Córdoba (Argentina); envíos a todo el país.

## Capabilities and Constraints

- Sitio estático (HTML/CSS/JS puro, sin build) desplegado en Vercel desde el
  repo `Maximogargiulo11/Raiza`.
- Catálogo y posts de Instagram son data-driven: `data/products.json` y
  `data/instagram.json`; la landing los lee al cargar.
- Panel de administración cliente en `/admin`: alta/edición de productos con
  foto y edición de posts de Instagram, guardando vía GitHub Git Data API con un
  token personal (Contents R/W) guardado en el navegador. Vercel redepliega solo.
- Productos con variantes: Yerba por tamaño (`sizes`) y Sets por color (`colors`);
  algunos ítems sin precio quedan como "consultar"/sin stock.
- WhatsApp de venta hardcodeado como `WA` en index.html (`5493834021235`).
- Fuente self-hosted **Sanchez** (slab serif). Logo: la "R" transparente
  (`uploads/logo.png`). Favicon con la R sobre cuadrado oscuro.

## Brand Commitments

- Nombre: **Raiza · Club de Mate**. Handle: **@raizaclubdemate**.
- Voz: cálida, criolla, de comunidad ("Somos RAIZA", "Llegamos", "sumate",
  "tu ronda"). Primera persona plural, tuteo argentino.
- Frases de marca vigentes: "No vendemos mates, creamos rituales.",
  "Llegamos. Somos RAIZA.", "Hecho a mano, con raíz."
- Paleta/materialidad actual: tonos madera oscuros, crema (#EDE4D6) y marrón
  (#8A5A34), textura de madera en movimiento de fondo. (Incumbente — se documenta
  aparte en DESIGN.md, no se decide aquí.)

## Evidence on Hand

- Catálogo real de ~23 productos con precios en `data/products.json`.
- Fotos de producto reales en `uploads/` (JPG por producto).
- Testimonios de clientes **reales** en la landing (p. ej. Julián, Córdoba) —
  pueden citarse como prueba genuina.
- Instagram real con contenido propio (@raizaclubdemate), reels embebidos.
- Ediciones especiales reales: Camionero "Copa Mundial '26", Set Edición
  Argentina.

## Product Principles

1. **Artesanal antes que catálogo.** Cada pieza es única y hecha a mano; el
   diseño debe transmitir oficio y autenticidad, no producción en serie.
2. **Comunidad, no transacción.** Raiza es un "Club": pertenencia y ritual pesan
   tanto como el producto. La compra es una conversación (WhatsApp), no un carrito.
3. **Raíz e identidad argentina.** Materiales criollos (calabaza, algarrobo,
   cuero, alpaca) y voz criolla; el "arraigo" es el hilo conductor.
4. **La marca la editan ellos.** El catálogo y las redes se mantienen sin tocar
   código (panel /admin + JSON); las decisiones de contenido son del cliente.
