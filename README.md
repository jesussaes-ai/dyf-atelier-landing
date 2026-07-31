# D&F ATELIER — Landing Page

Sitio web informativo y de catálogo de **D&F Atelier**, acuarelas artesanales hechas a mano en México · *Fine Arts & Pigments*.

🔗 **En vivo:** https://jesussaes-ai.github.io/dyf-atelier-landing/

---

## Qué es

Una landing page de una sola página (single-file HTML autocontenido) que presenta la marca, su colección insignia, el catálogo completo de pigmentos y escenas en video de las acuarelas cobrando vida sobre el papel. Está pensada como catálogo/vitrina y es **modular** para ir sumando productos.

## Estructura del repositorio

```
dyf-atelier-landing/
├── index.html                        ← la landing completa (HTML + CSS + JS en un archivo)
├── media/                            ← videos e imágenes reales de las escenas
│   ├── bosque.mp4 / .jpg
│   ├── selva.mp4 / .jpg
│   ├── bodegon.mp4 / .jpg
│   ├── ave.mp4 / .jpg
│   ├── pintando.mp4  (gato)          ← video del gato
│   └── gato.jpg      (póster)
├── CONTEXTO_LANDING_DyF_ATELIER.md   ← documento de contexto / handoff (para Hermes)
└── README.md
```

## Secciones

1. **Hero** — logo, acuarela animada y llamadas a la acción.
2. **Colección Mineral Mate** — 10 tonos de 5 ml + set completo, con precios (MXN).
3. **En acción** — 5 escenas en **video real** (bosque, selva, bodegón, ave y gato) de las acuarelas pintándose, cada una con indicador "EN VIVO", botón de reproducción y lightbox.
4. **Catálogo de colores** — 103 pigmentos filtrables por familia, cada uno con su Color Index, transparencia y granulación.
5. **Historia** — sobre el atelier.
6. **Próximamente** — pinceles Meyers, papel para acuarela, godetes y accesorios (módulos listos para crecer).
7. **Precios** y **Contacto**.

## Medios (video)

Las 5 escenas de "En acción" son videos de ~15 segundos generados con IA (Grok Imagine), comprimidos a ~1 MB cada uno para carga rápida (H.264, sin audio, `+faststart`). Se reproducen en bucle, silenciados y en autoplay. Cada video tiene su imagen `.jpg` como póster de respaldo.

## Tecnología

HTML, CSS y JavaScript puro, sin dependencias ni build. Tipografías Cormorant Garamond + Jost (Google Fonts). El logo va embebido en base64. Se publica con **GitHub Pages** desde la rama `main`.

## Cómo editar

Los datos de productos y pigmentos viven en arreglos JavaScript al final de `index.html`:

- `MIN` — colección Mineral Mate (código, nombre, hex, precio).
- `PIG` — los 103 pigmentos (Color Index, familia, transparencia, granulación, hex).
- `TH` — las escenas de "En acción" (título, descripción, imagen `img` y video `vid`).

Para agregar un producto nuevo (pinceles, papel, godetes) se añaden sus datos y una tarjeta en la sección correspondiente.

---

*Hecho a mano en México · © 2026 D&F Atelier*
