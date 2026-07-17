# Instrucciones de desarrollo

Estas reglas aplican a todo el proyecto.

## Flujo obligatorio

1. Leer `TODO.md` antes de iniciar cualquier cambio.
2. Trabajar las tareas en el orden de prioridad acordado, salvo indicación explícita del usuario.
3. Marcar la tarea como `En progreso` al comenzar y como `En revisión` al terminar la implementación.
4. Validar el cambio en proporción a su riesgo antes de entregarlo.
5. Actualizar siempre `TODO.md` como último paso de cada tarea:
   - reflejar el estado actual;
   - añadir una entrada fechada al registro de ejecución;
   - indicar qué se cambió y cómo se validó;
   - señalar la siguiente tarea propuesta.
6. Cambiar una tarea de `En revisión` a `Hecho` cuando el usuario la haya aprobado o cuando la aceptación esté explícitamente delegada.

## Reglas técnicas

- Mantener los archivos de texto en UTF-8 y conservar correctamente tildes, eñes y signos de apertura.
- Usar rutas con la misma capitalización que los archivos y carpetas reales. Los recursos locales deben referenciarse desde `images/`.
- Mantener sincronizados los tokens visuales de `index.html` y su documentación en `DESIGN.md`.
- Para el tema oscuro, reutilizar los tokens `dark-*`; no introducir colores aislados sin documentarlos.
- Preservar accesibilidad básica: HTML semántico, navegación por teclado, foco visible, textos alternativos y atributos ARIA cuando sean necesarios.
- No mezclar correcciones ajenas a la tarea activa sin registrarlas primero en `TODO.md`.
- No crear commits, hacer push ni publicar cambios salvo que el usuario lo solicite.

## Publicación de este repositorio

- Repositorio: `https://github.com/DegolladoC/mayam-courses-landing.git`.
- Rama principal: `main`.
- GitHub CLI está instalado en `C:\Program Files\GitHub CLI\gh.exe` y la cuenta esperada es `DegolladoC`.
- La frase **“sube todo”** autoriza incluir todos los cambios visibles del proyecto, después de una sola revisión de `git status` y del resumen del diff.
- Si la rama actual es `main`, publicar mediante commit y push directo a `origin/main`. No crear otra rama ni PR salvo que el usuario lo pida expresamente.
- Si la rama actual ya tiene un PR abierto, añadir el commit y hacer push a esa misma rama. No crear una segunda rama o PR.
- Crear una rama y un PR únicamente cuando el usuario pida un PR, una revisión aislada o cuando `main` no permita pushes directos.
- Reutilizar las validaciones realizadas desde el último cambio de archivos. No repetir capturas, comprobaciones de autenticación o validaciones idénticas si el contenido no cambió.
- Antes del commit, ejecutar una revisión final de sintaxis relevante y `git diff --check`; después del push, verificar una sola vez que la rama esté sincronizada.
- Informar siempre rama, commit, destino del push y, cuando exista, enlace del PR.
- Las imágenes grandes pueden hacer que el push tarde aunque el flujo esté automatizado; no confundir el tiempo de transferencia con un bloqueo.
