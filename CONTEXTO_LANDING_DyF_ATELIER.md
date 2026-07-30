# D&F ATELIER — Landing Page · Contexto y handoff

> Documento de traspaso para Hermes/Elsa. Aquí está TODO lo que se hizo en la landing page
> de acuarelas D&F Atelier, para que puedas continuar el trabajo. Escrito por Claude (Cowork).

## Marca
- **Nombre correcto:** D&F ATELIER  (logo dice "D&F ATELIER — FINE ARTS & PIGMENTS")
- Giro: acuarelas artesanales hechas a mano en México. Enfoque de la página: catálogo / informativo.
- Paleta de marca (del logo): azul #3f7fb0, rojo #b12a2a, ocre #cf8b2c, verde #2f5233, dorado #a9822f, tinta #20201e, papel #faf7f1.
- Tipografías: Cormorant Garamond (títulos serif) + Jost (texto). Logo en:
  `ACUARELAS/LOGO ETIQUETAS Y PROYECTOS DE IMAGEN Y VIDEO para DyF ATELIER/DyF Atelier LOGO fondo claro.jpeg`

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
3. "En acción": 5 escenas de acuarela ANIMADA (bosques, selvas, bodegones, aves, gatos),
   con indicador EN VIVO, botón play y lightbox. Espacios "Video/Foto" listos para medios reales.
4. Catálogo de colores filtrable por familia (103 pigmentos).
5. Historia / Sobre nosotros.
6. Próximamente (modular): Pinceles Meyers, Papel para acuarela, Godetes, Accesorios.
7. Precios (público) y Contacto.
Es un solo archivo HTML autocontenido (logo embebido en base64). Fuentes vía Google Fonts.

## PENDIENTE — medios de IA (imágenes + videos)
Jesús quiere imágenes y videos reales estilo acuarela (gente pintando bosques, selvas,
bodegones, aves, gatos) con efectos y movimiento, para reemplazar las escenas animadas por CSS.
IMPORTANTE: Cowork/Claude NO puede conectarse a fal.ai desde su entorno. La generación
debe hacerla ELSA/Hermes en la computadora (tiene FAL_KEY y red). Tarea sugerida para Hermes:
generar 5 imágenes acuarela (bosque, selva, bodegón, ave/pájaro, gato) + 1-2 videos cortos,
guardarlos en `ACUARELAS/Landing DyF Atelier/media/` y colocarlos en los espacios "Video/Foto"
de cada escena del index.html.

## Cómo agregar productos futuros
El HTML es modular. Los datos de productos y pigmentos están en arreglos JS al final del archivo
(MIN = colección mineral, PIG = pigmentos). Para pinceles Meyers, papel, godetes: agregar sus
fotos/precios y crear tarjetas en la sección "Próximamente" o una nueva sección de producto.
