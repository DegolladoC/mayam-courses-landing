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
- Mantener sincronizados los tokens visuales de `code.html` y su documentación en `DESIGN.md`.
- Para el tema oscuro, reutilizar los tokens `dark-*`; no introducir colores aislados sin documentarlos.
- Preservar accesibilidad básica: HTML semántico, navegación por teclado, foco visible, textos alternativos y atributos ARIA cuando sean necesarios.
- No mezclar correcciones ajenas a la tarea activa sin registrarlas primero en `TODO.md`.
- No crear commits, hacer push ni publicar cambios salvo que el usuario lo solicite.
