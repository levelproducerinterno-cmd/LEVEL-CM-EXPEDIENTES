# Level Expedientes

Sistema para generar el expediente de marca de cada cliente (Community Manager) en PDF, con el diseño de Level Producer. Incluye, dentro de la misma página, la guía completa de los 4 prompts que se corren en Claude antes de generar el PDF.

## Flujo de uso

1. Abre el sistema y sigue la leyenda de pasos ("Abrir chat nuevo en Claude" + los 4 prompts con botón Copiar).
2. Corre los 4 prompts en un chat nuevo de Claude, pegando primero el onboarding del cliente.
3. Copia el resultado completo del Prompt 04 ("Expediente completo").
4. Pégalo en la caja de este sistema y da clic en "Extraer campos automáticamente".
5. Revisa/ajusta los campos (incluye subir capturas de pantalla de cada red social activa).
6. Da clic en "Generar Expediente PDF" — descarga el documento completo, listo para enviar.

## Cómo subirlo a GitHub + Vercel (igual que tus otros sistemas Level)

1. Crea un repo nuevo en GitHub, por ejemplo `LEVEL-EXPEDIENTES` (bajo tu mismo usuario/organización `levelproducerinterno-cmd`).
2. Sube el archivo `index.html` de este zip a la raíz del repo.
3. Entra a [vercel.com](https://vercel.com), dale "Add New... → Project", elige el repo `LEVEL-EXPEDIENTES`.
4. Vercel detecta automáticamente que es un sitio estático — no necesita Build Command ni Framework Preset. Dale "Deploy".
5. En unos segundos te da una URL tipo `level-expedientes.vercel.app`.

## Notas

- El logo y el fondo con textura están incrustados en base64 dentro del `index.html` — no dependen de archivos externos, salvo las fuentes de Google Fonts y las librerías jsPDF/html2canvas (cargadas por CDN).
- El parseo automático del texto del Prompt 04 es una ayuda, no magia — siempre revisa los campos antes de generar el PDF, sobre todo si el texto que te dio Claude no siguió el formato exacto.
- Las capturas de pantalla de redes sociales que subas solo viven en el navegador mientras generas el PDF — no se guardan en ningún lado, así que tendrás que volver a subirlas si repites el proceso para el mismo cliente en otra sesión.
