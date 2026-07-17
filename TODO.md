# TODO — Landing Page de cursos MAYAM

Este archivo es el tablero de trabajo del proyecto. Cada cambio se registra como una tarea independiente para que pueda revisarse y aprobarse antes de continuar con la siguiente.

## Cómo usar este tablero

- Estados: `Pendiente`, `En progreso`, `En revisión`, `Hecho` o `Bloqueado`.
- La prioridad define el orden propuesto: `P0` es imprescindible, `P1` es importante y `P2` es una mejora posterior.
- Al terminar una tarea se actualizarán su estado, la fecha y una nota breve de validación.

## Estado actual

| Área | Estado actual |
| --- | --- |
| Página | Landing page estática de una sola página en `code.html`. |
| Estilos | Tailwind CSS se carga por CDN y la configuración está embebida en el HTML. |
| Diseño | La guía visual y los tokens de marca están documentados en `DESIGN.md`. |
| Contenido | Incluye hero, contador, beneficios, stack de herramientas, resultados, programa, instructor, CTA, preguntas frecuentes y footer. |
| Interactividad | Hay acordeones y un contador cuya fecha y enlaces de inscripción se administran desde `course-config.js`. |
| Recursos | Los recursos locales viven en `images/`; el hero en capas utiliza las imágenes nuevas de estrategia de marketing, redes y producción, y “Transformación Real” usa `antes-despues.png`. También se usan algunas imágenes externas de Google. |
| Licencia | GNU General Public License v3.0 (`GPL-3.0-only`) en `LICENSE`. |
| Repositorio | Publicado en GitHub, rama `main`, con el commit inicial `6da0410`. |

## Hallazgos iniciales

- [Resuelto; pendiente de revisión visual] El tema ahora detecta la preferencia inicial, conserva la selección del visitante y comunica correctamente su estado y acción.
- [Resuelto; pendiente de revisión visual] La paleta oscura cuenta con tokens propios documentados en `DESIGN.md`.
- [Resuelto] La carpeta de recursos y las referencias del código usan de forma consistente `images/` en minúsculas.
- [Resuelto; falta capturar la fecha] El contador usa una fecha absoluta configurable desde `course-config.js`; mientras esté vacía muestra “Próxima fecha por confirmar”.
- [Validado] `code.html` está codificado en UTF-8 y los caracteres españoles son correctos. La representación incorrecta detectada provenía de la salida de la terminal, no del archivo.
- [Resuelto para CTA; enlaces legales pendientes] Los CTA de inscripción comparten el destino de `course-config.js` y “Ver temario completo” apunta a `#programa`.

## Plan de trabajo priorizado

| ID | Prioridad | Tarea | Estado | Criterio de validación |
| --- | --- | --- | --- | --- |
| T-01 | P0 | Rediseñar y corregir el modo claro/oscuro | En revisión | Ambos temas mantienen contraste, legibilidad y consistencia; el control indica la acción disponible, respeta la preferencia inicial y guarda la elección. |
| T-02 | P0 | Corregir la ruta y capitalización de las imágenes locales | En revisión | La foto del instructor y los demás recursos cargan correctamente en un servidor con sistema de archivos sensible a mayúsculas. |
| T-03 | P0 | Reparar la codificación de caracteres en español | En revisión | Tildes, eñes, signos de apertura y símbolos se muestran correctamente en toda la página. |
| T-04 | P1 | Definir una fecha de inscripción real para el contador | En revisión | El contador apunta a una fecha configurada y muestra un estado claro al finalizar. |
| T-05 | P1 | Conectar los CTA y enlaces de navegación | En revisión | Cada botón lleva a una sección, formulario, enlace de contacto o acción previamente acordada. |
| T-06 | P1 | Mejorar navegación móvil | Pendiente | El botón de menú abre y cierra una navegación usable, accesible y con enlaces funcionales. |
| T-07 | P1 | Optimizar imágenes y sustituir dependencias externas críticas | En progreso | Las imágenes tienen tamaño adecuado, atributos `alt` útiles y no dependen innecesariamente de URLs temporales externas. |
| T-08 | P1 | Revisión de accesibilidad | Pendiente | Navegación por teclado, foco visible, etiquetas accesibles y contraste adecuados. |
| T-09 | P2 | Preparar SEO y vista previa al compartir | Pendiente | Título, descripción, Open Graph, favicon y `og-image` configurados. |
| T-10 | P2 | Separar CSS y JavaScript del HTML | Pendiente | Estilos y comportamiento quedan en archivos mantenibles sin alterar la experiencia visual. |
| T-11 | P2 | Añadir analítica y medición de conversiones | Pendiente | Eventos de CTA y conversiones definidos e integrados con la herramienta que se elija. |
| T-12 | P1 | Rediseñar la visualización principal del hero en monitores | En revisión | La composición elegida se siente dinámica en escritorio, conserva legibilidad y se adapta correctamente a móvil. |
| T-13 | P1 | Suavizar y alinear botones y tarjetas antes de “El Camino del Piloto” | En revisión | Botones y tarjetas tienen radios más amplios; las tarjetas de cada fila mantienen la misma altura y alineación. |

## Dirección visual seleccionada — T-12

Se seleccionó la composición de tres capas con estos ajustes definitivos:

- `laptop-persona-marketing.png` inicia como imagen principal al centro.
- `celular-redes-fondotech.png` y `laptop-microfono-luzazul.png` ocupan los planos laterales.
- Desde 768 px, mover el cursor por las zonas izquierda, central o derecha lleva la imagen correspondiente al centro y actualiza el texto descriptivo.
- En tablet, tocar o enfocar una imagen produce el mismo intercambio.
- En celulares la composición permanece estática, sin paralaje ni reordenamiento.
- Los intercambios de posición duran 1040 ms y los ajustes secundarios de profundidad y sombra duran 440 ms.
- `prefers-reduced-motion` elimina las transiciones y el paralaje.

El selector comparativo y el código de la alternativa descartada fueron eliminados.

## Registro de ejecución

| Fecha | ID | Estado | Cambio / validación |
| --- | --- | --- | --- |
| 2026-07-17 | — | Hecho | Se creó este tablero y se documentó el inventario y los hallazgos iniciales. |
| 2026-07-17 | T-01 | En revisión | Se definió la paleta oscura, se añadió detección del sistema, persistencia, estado accesible y control en móvil/escritorio. Los scripts pasan validación sintáctica y los contrastes principales miden entre 11.11:1 y 17.62:1. |
| 2026-07-17 | T-02 | En revisión | Se renombró `Images/` a `images/`, incluido el índice de Git, y se verificó que `images/Nestor.jpg` coincide exactamente con la ruta usada por la página. |
| 2026-07-17 | T-03 | En revisión | Se validó UTF-8 estricto y se comprobó que no existen secuencias mojibake en `code.html`; no fue necesario alterar el contenido. |
| 2026-07-17 | — | Hecho | Se añadió `AGENTS.md` con las reglas de desarrollo y la actualización obligatoria de este tablero. |
| 2026-07-17 | — | Hecho | Se añadió `LICENSE` con el texto oficial íntegro de GNU GPL v3 y se verificó contra `gnu.org`. |
| 2026-07-17 | T-04 | En revisión | Se creó `course-config.js` para editar la fecha sin tocar el HTML. El contador admite fecha pendiente, fecha futura y finalización en cero; se validaron sintaxis, estructura y orden de carga. |
| 2026-07-17 | T-05 | En revisión | Los CTA de inscripción comparten una URL configurable y “Ver temario completo” enlaza a `#programa`. El valor provisional de inscripción es `#programa` hasta recibir la URL definitiva. |
| 2026-07-17 | T-12 | Pendiente | Se documentaron tres composiciones posibles para el hero; la implementación espera la elección del usuario. |
| 2026-07-17 | T-13 | En revisión | Se aumentaron los radios de botones, contadores, tarjetas y medios superiores; se igualaron alturas y se eliminaron desniveles. No se modificó el diseño desde “El Camino del Piloto” hacia abajo. |
| 2026-07-17 | T-12 | En revisión | Se implementaron las opciones 1 y 3 con imágenes locales recientes, selector accesible, animación, paralaje y alternativa sin movimiento. Se validaron con Edge a 1440×1000 y 390×844, además de comprobar estructura HTML/CSS, JavaScript, rutas y UTF-8. |
| 2026-07-17 | T-12 | En revisión | Se consolidó la composición de capas, se cambió la imagen central por `laptop-persona-marketing.png` y se añadió intercambio por zona del cursor desde 768 px, toque/foco en tablet y una versión estática para celulares. Se retiró el comparador y se validó visualmente en Edge a 1440×1000 y 390×844. |
| 2026-07-17 | T-12 | En revisión | Se duplicó la duración de la animación del hero: posiciones de 520 ms a 1040 ms y ajustes de profundidad/sombra de 220 ms a 440 ms. Se verificó que no permanecieran duraciones anteriores. |
| 2026-07-17 | T-07 | En progreso | Se sustituyó la imagen externa de “Transformación Real” por `images/antes-despues.png`, con texto alternativo y carga diferida. Se validaron el archivo, la capitalización y las cinco referencias locales de la página. La optimización de peso continúa pendiente. |

## Próxima tarea propuesta

**Completar T-04/T-05 y continuar con T-07.** Capturar en `course-config.js` la fecha real y la URL definitiva de inscripción; después, optimizar las imágenes nuevas, que actualmente pesan entre 1.7 MB y 2.3 MB cada una.
