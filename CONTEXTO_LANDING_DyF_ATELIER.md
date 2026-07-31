# D&F ATELIER — Landing Page · Contexto y handoff

> Documento de traspaso para Hermes/Elsa. Aquí está TODO lo que se hizo en la landing page
> de acuarelas D&F Atelier, para que puedas continuar el trabajo. Escrito por Claude (Cowork).
>
> **En vivo:** https://jesussaes-ai.github.io/dyf-atelier-landing/
> **Repo:** https://github.com/jesussaes-ai/dyf-atelier-landing
> **Carpeta local:** `ACUARELAS/Landing DyF Atelier/`

## Marca
- **Nombre correcto:** D&F ATELIER  (logo dice "D&F ATELIER — FINE ARTS & PIGMENTS")
- Giro: acuarelas artesanales hechas a mano en México. Enfoque de la página: catálogo / informativo.
- Paleta de marca (del logo): azul #3f7fb0, rojo #b12a2a, ocre #cf8b2c, verde #2f5233, dorado #a9822f, tinta #20201e, papel #faf7f1.
- Tipografías: Cormorant Garamond (títulos serif) + Jost (texto). El logo va embebido en base64 dentro del index.html.

## Producto insignia — Colección Mineral Mate (5 ml, precios PÚBLICO MXN)
| Clave | Color | Precio |
|---|---|---|
| DFAM01-005 | Ocre del Desierto | $110 |
| DFAM02-005 | Tierra Terracota | $110 |
| DFAM03-005 | Arcilla Rosada | $110 |
| DFAM04-005 | Piedra Salvia | $110 |
| DFAM05-005 | Oliva Mineral | $110 |
| DFAM06-005 | Azul Pizarra | $110 |
| DFAM07-005 | Marrón Cañón | $160 |
| DFAM08-005 | Negro Volcánico | $160 |
| DFAM09-005 | Arenisca | $120 |
| DFAM10-005 | Lavanda Mineral | $160 |
| DFAM11-010 | Set / Gama 10 piezas | $1,070 |
(También hay precios Distribuidor/Mayorista/Mercado Libre en `ACUARELAS/Precios Acuarelas/`.)

## Catálogo de colores
103 pigmentos en 9 familias (PY amarillos, PO naranjas, PR rojos, PV violetas, PB azules,
PG verdes, PBr tierras, PW blancos, PBk negros), cada uno con Color Index, transparencia,
granulación. Fuente: `ACUARELAS/Informacion de los colores y las ACUARELAS/base_maestra_pigmentos_compact.md`.

## Secciones de la landing (archivo: index.html en esta misma carpeta)
1. Hero con logo + acuarela animada + CTAs de compra.
2. Colección Mineral Mate (10 productos + set) con precios.
3. "En acción": 5 escenas EN VIDEO REAL (bosque, selva, bodegón, ave, gato), con indicador
   EN VIVO, botón play y lightbox.
4. Catálogo de colores filtrable por familia (103 pigmentos).
5. Historia / Sobre nosotros.
6. Próximamente (modular): Pinceles Meyers, Papel para acuarela, Godetes, Accesorios.
7. Precios (público) y Contacto.
Es un solo archivo HTML autocontenido. Fuentes vía Google Fonts.

## Medios de IA — HECHO ✅
Las 5 escenas de "En acción" ya usan VIDEOS reales estilo acuarela (una mano pintando cada
escena), de ~15 segundos, generados con **Grok Imagine** y comprimidos a ~1 MB cada uno
(H.264, sin audio, +faststart, en bucle/autoplay/silenciado). Están en `media/`:
- `bosque.mp4` — bosque de pinos pintándose (15 s, 16:9)
- `selva.mp4` — follaje de selva (15 s, 2:3)
- `bodegon.mp4` — duraznos y jarra de barro (15 s, 2:3)
- `ave.mp4` — pájaro azul y naranja (15 s, 2:3)
- `pintando.mp4` — retrato de gato (video del gato)
Cada uno tiene su `.jpg` como póster de respaldo (bosque.jpg, selva.jpg, bodegon.jpg, ave.jpg, gato.jpg).

Nota técnica: la generación se hizo con Grok Imagine (grok.com/imagine, cuenta SuperGrok) desde
el navegador. fal.ai sigue sin ser accesible desde el entorno de Cowork/Claude; si quieres generar
más medios desde la PC, Elsa/Hermes puede usar su FAL_KEY, o repetir el flujo en Grok.

## Cómo se publica (deploy)
- El sitio se publica con **GitHub Pages** desde la rama `main` del repo `jesussaes-ai/dyf-atelier-landing`.
- Al hacer push a `main`, GitHub Pages reconstruye solo en ~1 minuto.
- Nota: la carpeta local está en OneDrive y a veces deja un `.git/index.lock` bloqueado que no se
  puede borrar desde Cowork; si el commit local falla por eso, borra ese archivo manualmente.

## Cómo agregar productos futuros
El HTML es modular. Los datos de productos y pigmentos están en arreglos JS al final del archivo:
`MIN` (colección mineral), `PIG` (pigmentos), `TH` (escenas de "En acción", con `img` y `vid`).
Para pinceles Meyers, papel, godetes: agregar sus fotos/precios y crear tarjetas en la sección
"Próximamente" o una nueva sección de producto.
