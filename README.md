# PizarrIA

Pizarra táctica para aprender y enseñar baloncesto, balonmano, fútbol y voleibol. Aplicación web de un solo fichero (`index.html`), sin servidor.

**Idiomas:** español (por defecto), inglés y portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- **Pizarra** a escala para los cuatro deportes: fichas arrastrables, desplazamientos, botes o conducciones, pases, lanzamientos o remates, fintas, bloqueos y recuperaciones; fases con reproducción animada, deshacer/rehacer, exportación de la jugada en JSON y de la vista en SVG.
- **Plantillas didácticas:** sistemas defensivos de balonmano (6:0, 5:1, 3:2:1, 4:2), formaciones de fútbol (4-4-2, 4-3-3, 3-5-2, 4-2-3-1) y rotaciones y recepción en W de voleibol.
- **Biblioteca** de 12 jugadas de ejemplo (3 por deporte), editables.
- **Texto a jugada con IA:** describes una jugada y la IA propone fases y acciones. El código descarta lo incoherente, recorta los puntos fuera del campo, comprueba que cada fase cita un fragmento literal de tu texto y compara el número de pases si lo mencionas.
- **Retos con corrección automática:** preguntas sobre una jugada y jugadas que se construyen en la pizarra. Las respuestas las calcula el código.
- **Actividades para clase:** el profesorado elige retos, genera una página para el alumnado y carga sus entregas para obtener un informe (pantalla, CSV y Word).

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador. Sin clave funciona todo salvo «Generar la jugada»; el ejemplo funciona sin ella.

## Privacidad

Las jugadas, retos y entregas se guardan en el navegador (IndexedDB). Solo sale hacia el proveedor de IA el texto con el que se describe una jugada, con correos, teléfonos e identificadores enmascarados y tras un aviso previo con muestra. No se envían imágenes. No escribas datos de personas reales.

## Límites

- No se comprueban las reglas de los deportes (solapamientos del voleibol, faltas, tiempos) ni si una jugada es buena; las plantillas son ejemplos didácticos.
- Los defensores o rivales no se mueven automáticamente: hay que dibujar sus acciones.
- Los retos son los de la biblioteca; no se pueden crear retos propios.
- La huella de las entregas detecta ediciones por descuido; no es una prueba de autoría.
- La IA puede equivocarse. No se ha probado con una clave real de ningún proveedor, solo con respuestas simuladas.
- En fútbol, 1 unidad de la pizarra equivale a unos 3,28 m (campo de 68 × 105 m) para que las fichas tengan un tamaño legible.

## Pruebas

`NODE_MODULES=/ruta/node_modules python3 tests/pizarria_test.py` (Playwright, IA simulada que miente a propósito) y `node tests/claves.js` (traducciones). Para reconstruir: `python3 build.py`.

## Autoría

Fernando Borrás Rocher y Tomás Urbán Infantes (Universidad Miguel Hernández de Elche).


ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Tomás Urbán Infantes [0000-0002-2550-418X](https://orcid.org/0000-0002-2550-418X)

## Cómo citar

Borrás Rocher, F. y Urbán Infantes, T. (2026). *PizarrIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
