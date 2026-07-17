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
| Interactividad | Hay acordeones y un contador implementados con JavaScript inline. |
| Recursos | Los recursos locales viven en `images/`; también se usan imágenes externas de Google. |
| Licencia | GNU General Public License v3.0 (`GPL-3.0-only`) en `LICENSE`. |
| Repositorio | Publicado en GitHub, rama `main`, con el commit inicial `6da0410`. |

## Hallazgos iniciales

- [Resuelto; pendiente de revisión visual] El tema ahora detecta la preferencia inicial, conserva la selección del visitante y comunica correctamente su estado y acción.
- [Resuelto; pendiente de revisión visual] La paleta oscura cuenta con tokens propios documentados en `DESIGN.md`.
- [Resuelto] La carpeta de recursos y las referencias del código usan de forma consistente `images/` en minúsculas.
- El contador siempre empieza a tres días desde la apertura de la página; no representa una fecha de inscripción real.
- [Validado] `code.html` está codificado en UTF-8 y los caracteres españoles son correctos. La representación incorrecta detectada provenía de la salida de la terminal, no del archivo.
- Algunos CTA y enlaces legales usan `href="#"`; todavía no tienen destinos o acciones finales.

## Plan de trabajo priorizado

| ID | Prioridad | Tarea | Estado | Criterio de validación |
| --- | --- | --- | --- | --- |
| T-01 | P0 | Rediseñar y corregir el modo claro/oscuro | En revisión | Ambos temas mantienen contraste, legibilidad y consistencia; el control indica la acción disponible, respeta la preferencia inicial y guarda la elección. |
| T-02 | P0 | Corregir la ruta y capitalización de las imágenes locales | En revisión | La foto del instructor y los demás recursos cargan correctamente en un servidor con sistema de archivos sensible a mayúsculas. |
| T-03 | P0 | Reparar la codificación de caracteres en español | En revisión | Tildes, eñes, signos de apertura y símbolos se muestran correctamente en toda la página. |
| T-04 | P1 | Definir una fecha de inscripción real para el contador | Pendiente | El contador apunta a una fecha configurada y muestra un estado claro al finalizar. |
| T-05 | P1 | Conectar los CTA y enlaces de navegación | Pendiente | Cada botón lleva a una sección, formulario, enlace de contacto o acción previamente acordada. |
| T-06 | P1 | Mejorar navegación móvil | Pendiente | El botón de menú abre y cierra una navegación usable, accesible y con enlaces funcionales. |
| T-07 | P1 | Optimizar imágenes y sustituir dependencias externas críticas | Pendiente | Las imágenes tienen tamaño adecuado, atributos `alt` útiles y no dependen innecesariamente de URLs temporales externas. |
| T-08 | P1 | Revisión de accesibilidad | Pendiente | Navegación por teclado, foco visible, etiquetas accesibles y contraste adecuados. |
| T-09 | P2 | Preparar SEO y vista previa al compartir | Pendiente | Título, descripción, Open Graph, favicon y `og-image` configurados. |
| T-10 | P2 | Separar CSS y JavaScript del HTML | Pendiente | Estilos y comportamiento quedan en archivos mantenibles sin alterar la experiencia visual. |
| T-11 | P2 | Añadir analítica y medición de conversiones | Pendiente | Eventos de CTA y conversiones definidos e integrados con la herramienta que se elija. |

## Registro de ejecución

| Fecha | ID | Estado | Cambio / validación |
| --- | --- | --- | --- |
| 2026-07-17 | — | Hecho | Se creó este tablero y se documentó el inventario y los hallazgos iniciales. |
| 2026-07-17 | T-01 | En revisión | Se definió la paleta oscura, se añadió detección del sistema, persistencia, estado accesible y control en móvil/escritorio. Los scripts pasan validación sintáctica y los contrastes principales miden entre 11.11:1 y 17.62:1. |
| 2026-07-17 | T-02 | En revisión | Se renombró `Images/` a `images/`, incluido el índice de Git, y se verificó que `images/Nestor.jpg` coincide exactamente con la ruta usada por la página. |
| 2026-07-17 | T-03 | En revisión | Se validó UTF-8 estricto y se comprobó que no existen secuencias mojibake en `code.html`; no fue necesario alterar el contenido. |
| 2026-07-17 | — | Hecho | Se añadió `AGENTS.md` con las reglas de desarrollo y la actualización obligatoria de este tablero. |
| 2026-07-17 | — | Hecho | Se añadió `LICENSE` con el texto oficial íntegro de GNU GPL v3 y se verificó contra `gnu.org`. |

## Próxima tarea propuesta

**Revisión de T-01 a T-03.** Verificar visualmente ambos temas en escritorio y móvil, confirmar que la elección persiste al recargar y comprobar la foto del instructor. Después, la siguiente implementación propuesta es **T-04 — Definir una fecha de inscripción real para el contador**.
