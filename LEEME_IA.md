# Instrucciones para la IA lectora

Edición de lectura de **«Texto y Comentario del Código Penal Chileno», t. I (Libro Primero, arts. 1° a 105)**, dirs. S. Politoff Lifschitz y L. Ortiz Quiroga, coord. J. P. Matus Acuña, Editorial Jurídica de Chile, 2002. Uso personal, con autorización de autor y editorial.

## Cómo leerla
1. Fuente principal: `libro_completo.xml` (un solo archivo, ≈1,3 MB). Versión equivalente con índice navegable: `libro_completo.html`.
2. Al inicio del XML está `<indice>`: lista las 23 divisiones (`id`, título, artículos, autores, páginas). Úsalo para ubicar la parte que corresponde a la consulta (p. ej. «art. 11» → división `d12`, pp. 165–186).
3. Si tu herramienta trunca archivos grandes, lee el XML por tramos y avanza división por división (`<division id="dNN">`), o pide al usuario que te entregue solo la división necesaria.
4. Cada `<pagina n="…">` lleva el **número de página impreso del libro**. Cada párrafo tiene un `id` del tipo `p67-3` (página 67, párrafo 3).

## Reglas de citación y rigor
- Cita siempre por **autor de la división + página impresa** (p. ej. «Politoff/Matus, p. 69»). Los autores están en el atributo `autores` de cada `<division>`.
- No atribuyas una opinión a un autor distinto del de la división. Los autores citados dentro de un comentario (Cury, Etcheberry, Novoa, etc.) son fuentes secundarias del comentarista.
- Distingue el **texto legal** (`<texto-legal>`) del **comentario** (`<p>` y `<apartado>`).
- Si una cita textual es decisiva, indica que proviene de un texto obtenido por OCR y que conviene verificarla en el original.
- Si la información no está en el texto entregado, dilo; no la completes de memoria.

## Calidad del texto (OCR)
- Escaneo con OCR de 2006: pueden quedar errores como `N°` leído `N-`, `N2` o `N^`, o `°` como `-`.
- Atributo `calidad_ocr` por página: `normal`; `tabular` (Tabla cronológica, págs. 21–46, legible pero numérica); `reocr-tesseract` (págs. 30–37, tabla rotada: **solo las págs. 30–31 son legibles; 32–37 son ilegibles**); `baja` (págs. 39, 469, 492 y 493: leer con cautela).
- Los apartados numerados y los textos legales se etiquetaron automáticamente; pueden existir omisiones o falsos positivos.
