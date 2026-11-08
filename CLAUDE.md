# Contexto del proyecto: Portal web — Redes Neuronales y Deep Learning

## Quién soy
Carlos, estudiante de la Maestría en Estadística (ESPOCH). Asignatura: Redes Neuronales y Deep Learning.
Respóndeme en español, de forma concisa y paso a paso.

## Encargo del profesor (clase 07-11-2026)
1. Partir de la plantilla `index.html` (copia de `data_science_hub2.html`, generada con Gemini).
2. Reemplazar la información del ejemplo por la nuestra: textos, equipo, fotos, videos, imágenes, PDF y enlaces.
3. Incluir **todo lo visto en la asignatura**: perceptrón simple, feedforward (MLP), CNN y las apps Shiny de ML clásico y de ANN.
4. Mostrar resultados y llegar con **un clic al dashboard** (app Shiny publicada en shinyapps.io).
5. Subir a GitHub y publicar con **GitHub Pages** (`https://USUARIO.github.io/REPO/`).
   Ejemplo del profesor: `msmejia.github.io/data_analitycs1/`.

## Estructura de esta carpeta (`subir/`)
```
subir/
├── index.html   ← página a editar
├── img/         ← fotos, capturas y gráficas (rutas relativas: img/archivo.png)
└── docs/        ← PDF (docs/informe.pdf)
```
Apps Shiny en la carpeta hermana `../clase031126/`: `app_ML.rar` y `app_ANNs.rar`.

## Mapa de `index.html` (484 líneas)
| Sección | id | Líneas | Qué reemplazar |
|---|---|---|---|
| CSS / colores (`:root`) | — | 7-295 | Solo los colores, si se desea (líneas 9-19) |
| Logo + menú | header | 300-311 | Nombre del portal |
| Inicio | `#inicio` | 315-321 | Título, subtítulo y descripción |
| Equipo (4 fotos ovaladas) | `#equipo` | 324-349 | `src`/`alt` de las fotos, nombres y roles |
| Análisis (2 imágenes) | `#analisis` | 352-367 | Imágenes y textos del EDA |
| ML vs DL (videos + enlaces) | `#comparativa` | 370-404 | Videos (YouTube embed) y URLs de las apps Shiny |
| Análisis predictivo | `#analisis` (**duplicado**) | 407-422 | Cambiar a `id="predictivo"`; imágenes y textos |
| Evidencia & Resultados | `#publicaciones` | 425-446 | PDF (`docs/`) e imagen de métricas |
| Pie: contacto + enlaces | footer | 450-481 | Enlaces y © |

## Problemas conocidos de la plantilla
- `id="analisis"` aparece dos veces (líneas 352 y 407).
- Las fotos usan rutas locales `c:/Libros/...` (líneas 329 y 334), que no funcionan publicadas. Usar `img/...`.
- El enlace DL (línea 400) apunta a `app_ML`. Debería ir a la app de ANN.
- Las imágenes de `gstatic` pueden dejar de cargar. Reemplazarlas por imágenes propias.
- El formulario de contacto solo muestra una alerta y no envía nada.
- El PDF viene de arXiv. Es mejor usar un PDF propio en `docs/`.
- Videos de YouTube: usar el formato `https://www.youtube.com/embed/ID`.
- Enlaces al dashboard: agregar `target="_blank"`.

## Publicación
1. Crear un repositorio **Public** en GitHub.
2. **Add file → Upload files** con el *contenido* de `subir/`. Git no sube carpetas vacías.
3. **Settings → Pages**: rama `main`, carpeta `/ (root)`, y **Save**.

## Pendiente por confirmar
- Integrantes (individual o en grupo), fecha de entrega y rúbrica.
- Si se pueden añadir secciones nuevas.
- URLs de las apps Shiny publicadas.
