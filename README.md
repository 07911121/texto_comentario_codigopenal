# Texto y Comentario del Código Penal Chileno, t. I — edición de lectura (HTML/XML)

Conversión del PDF (490 páginas impresas, pp. 4–493) a:
- `libro_completo.xml`: todo el texto, con paginación original.
- `divisiones/dNN.xml` y `divisiones/dNN.html`: una versión por parte del libro (según el Índice de autores).
- `index.html`: portada con enlaces. `manifest.json`: mapa para máquinas. `LEEME_IA.md`: instrucciones para pegar a una IA.

## Publicar en GitHub
1. Crea un repositorio y sube el contenido de esta carpeta (incluido `.nojekyll`).
2. **GitHub Pages:** Settings → Pages → «Deploy from a branch» → rama `main`, carpeta `/ (root)`. La URL será `https://TU-USUARIO.github.io/NOMBRE-REPO/`.
3. Alternativa sin Pages: enlaces `raw.githubusercontent.com/TU-USUARIO/NOMBRE-REPO/main/divisiones/d12.xml` (solo funcionan para una IA si el repositorio es público).
4. Instrucción sugerida para la IA: «Lee `https://…/LEEME_IA.md` y sigue sus reglas; luego consulta `manifest.json` y abre solo las divisiones necesarias. Cita por autor y página impresa.»

Nota: un repositorio privado no es legible por una IA externa sin credenciales; si quieres mantener el texto privado, entrega los archivos directamente a la IA en lugar de enlazarlos.
