# Landing-Page

Pequeña landing estática (HTML + CSS). Este README recoge buenas prácticas y convenciones específicas del proyecto para mantener consistencia y facilitar contribuciones.

Principales puntos

- Estructura

  - `index.html` contiene la maquetación.
  - `styles.css` contiene los estilos globales. No hay sistema de build en el repo actual.

- Tipografía

  - Se usa Google Fonts Roboto (400, 500). Mantén el enlace en `index.html` si añades texto con `font-weight: 500`.

- Variables y tema

  - Colores principales y variables están definidas en `:root` dentro de `styles.css` (ej.: `--bg`, `--logo-color`, `--link-color`). Cambia el tema actual editando estas variables.

- Layout y contenedor

  - Usa la clase `.container` para envolver nuevas secciones y mantener max-width (1200px) y padding consistente (28px 32px).

- Convenciones de clases

  - Usa kebab-case para nombres de clases (ej.: `.site-header`, `.nav-link`, `.hero-title`).
  - Evita estilos inline; añade reglas en `styles.css`.

- Accesibilidad

  - Conserva el estilo `:focus-visible` presente en `.nav-link` para controles interactivos nuevos.
  - Usa `aria-label` en `nav` y en elementos `role="img"` cuando el contenido es decorativo.

- Responsive

  - Punto de quiebre principal: `@media (max-width: 640px)`. Extiende con más breakpoints si es necesario, pero respeta este para móvil.
  - Las nuevas secciones deben comportarse bien en 4/2/1 columnas según ancho de pantalla.

- Estilos y transiciones

  - Duración/curva estándar: `transition: color 160ms ease, transform 160ms ease;`.

- Testing / preview
  - Previsualizar localmente con un servidor estático:

```bash
python3 -m http.server 8000
# luego abrir http://localhost:8000
```

- Commits y mensajes

  - Usa mensajes claros y en infinitivo; por ejemplo: `feat(ui): añadir hero responsivo` o `fix(css): corregir gap en .container`.

- Qué evitar
  - No rompas la convención de clases (no camelCase ni BEM nuevo sin motivo).
  - No elimines el punto de quiebre en 640px.

Contribuciones

Si quieres añadir una nueva sección (hero, features, footer), crea la estructura HTML dentro de una `.container` y añade las reglas en `styles.css` siguiendo las variables y convenciones arriba.

Si necesitas que convierta el proyecto en un pequeño flujo con build (por ejemplo con PostCSS o un bundler), puedo proponer una estructura y `package.json`.
