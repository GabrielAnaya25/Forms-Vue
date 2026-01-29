Guía mínima de estilo y uso de variables CSS
===========================================

Propósito
--------
Proveer reglas sencillas para usar los tokens de color y los componentes base del proyecto.

Dónde están las variables
-------------------------
- Archivo principal de tokens: `src/styles/variables.css`.
- Está importado desde `src/style.css`, por lo que las variables están disponibles globalmente.

Convenciones principales
-----------------------
- Nombres semánticos: usar `--color-primary`, `--color-primary-dark`, `--color-accent`, `--bg-muted`, `--error`, `--success`, etc.
- Evitar usar valores hex directos en componentes/páginas; preferir las variables.
- Para estados (hover, focus) crear variantes `-600`, `-700` o usar opacidades: `rgba(...)`.

Ejemplos rápidos
---------------
- Usar variable en CSS:

  .mi-componente {
    background: var(--color-accent);
    color: var(--color-primary-dark);
  }

- En `*.vue` preferir clases y componentes base en lugar de repetir estilos inline.

Uso de componentes base
-----------------------
- `BaseButton` (ubicado en `src/components/BaseButton.vue`) soporta `variant` (`primary`, `accent`, `ghost`) y `to` (para `RouterLink`).
- Reusar `Navbar` y `Footer` desde `src/components/` para evitar duplicación.

Añadir nuevos tokens
---------------------
1. Añade la variable en `src/styles/variables.css` con nombre semántico.
2. Usa la variable en `src/style.css` o en componentes scoped.
3. Si afecta a varios componentes, documenta el uso en este archivo.

Buenas prácticas
---------------
- Mantener separación de estilos globales (tokens y resets) y estilos scoped para UI local.
- Nombrar variables por rol (p. ej. `--color-success`) no por apariencia (`--green`).
- Revisar contraste y accesibilidad cuando se añadan nuevos colores.

¿Dónde documentar cambios?
-------------------------
Extiende este archivo con ejemplos y decisiones de diseño (contrastes, accesibilidad, variantes).
