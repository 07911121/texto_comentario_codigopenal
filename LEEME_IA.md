# Instrucciones para la IA lectora

Esta carpeta contiene una edición de lectura de **«Texto y Comentario del Código Penal Chileno», t. I (Libro Primero, arts. 1° a 105)**, dirs. S. Politoff Lifschitz y L. Ortiz Quiroga, coord. J. P. Matus Acuña, Editorial Jurídica de Chile, 2002. Uso personal, con autorización de autor y editorial.

## Cómo leerla
1. Parte por `manifest.json`: lista las 23 divisiones con páginas, artículos y autores. Cada división tiene su `.html` y su `.xml`.
2. Abre solo la división que corresponda a la pregunta (p. ej. «art. 11» → `divisiones/d12.html`). `libro_completo.xml` reúne todo, pero es muy extenso (≈1,3 MB): úsalo solo si necesitas buscar en todo el libro.
3. Cada `<pagina n="…">` lleva el **número de página impreso del libro**. Cada párrafo tiene un `id` del tipo `p67-3` (página 67, párrafo 3).

## Reglas de citación y rigor
- Cita siempre por **autor de la división + página impresa** (p. ej. «Politoff/Matus, p. 69»). Los autores están en el atributo `autores` de cada `<division>`.
- No atribuyas una opinión a un autor distinto del de la división. Dentro de un comentario, los autores citados (Cury, Etcheberry, Novoa, etc.) son fuentes secundarias del comentarista.
- Distingue el **texto legal** (`<texto-legal>`, normalmente entre comillas, p. ej. «Art. 5°. "La ley penal…"») del **comentario** (`<p>` y `<apartado>`).
- Si una cita textual es decisiva, indica que proviene de un texto obtenido por OCR y que conviene verificarla en el original.
- Si la información no está en el texto entregado, dilo; no la completes de memoria.

## Calidad del texto (OCR)
- El texto proviene de un escaneo con OCR de 2006. Pueden quedar errores de caracteres: `N°` leído como `N-`, `N2` o `N^`; `°` como `-` o `"`; comillas y guiones cambiados.
- Los guiones de fin de línea se unieron; compuestos como «jurídico-penal» a veces quedan sin guion si cortaban en el salto de línea.
- Atributo `calidad_ocr` por página: `normal`; `tabular` (Tabla cronológica de modificaciones, págs. 21–46, legible pero numérica); `reocr-tesseract` (págs. 30–37, tabla rotada, re-leída con otro OCR); `baja` (págs. 39, 469, 492 y 493: leer con cautela).
- Los apartados numerados («1. Historia legislativa.», «5. Bibliografía.») y los textos legales se etiquetaron automáticamente; pueden existir omisiones o falsos positivos.
- Las notas al pie son pocas: el libro usa citas autor-año en el cuerpo, y la bibliografía va al final de cada comentario.
