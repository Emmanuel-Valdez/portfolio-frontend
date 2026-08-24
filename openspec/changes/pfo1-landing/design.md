## Context

La PFO1 es una landing estática individual de HTML + CSS sin frameworks ni backend. El repo ya tiene `.gitignore`, `consigna.md` y `PLAN.md`. La marca `ev_` existe en el portfolio anterior (`portfolioDevAstro`), por lo que se reutilizan colores y el favicon cursor.

## Goals / Non-Goals

**Goals:**
- Cumplir y superar la rúbrica en las cinco dimensiones: semántica+ARIA, Flexbox+Grid, fuentes+variables CSS, animación propia, documentación+commits.
- Mantener una voz honesta: no venderse como profesional, declarar el uso de IA.
- Lograr un diseño responsive fluido con unidades relativas.
- Reutilizar recursos visuales del portfolio anterior (`Emma.png`, `favicon.svg`).

**Non-Goals:**
- No se agrega JavaScript funcional ni backend.
- No se usa framework CSS ni build step.
- No se crean páginas adicionales.

## Decisions

### Paleta `ev_`
- `--navy: #020617` — fondo principal, heredado del portfolio Astro.
- `--navy-light: #0d1625` — superficies secundarias (tarjetas, header).
- `--gold: #d4a017` — acento para títulos, enlaces, cursor y estados de foco.
- `--slate: #94a3b8` — texto secundario y bordes suaves.
- `--text: rgba(255, 255, 255, 0.9)` — texto principal sobre fondo oscuro.

### Tipografía
- Google Fonts: `Onest` (variable 400-700) para display y body.
- Se carga con `?display=swap` para evitar flash de texto invisible.

### Layout: Flexbox + Grid
- **Flexbox** en `header`, `nav`, `footer` y los contenedores de CTA porque son distribuciones lineales de pocos elementos.
- **Grid** en la grilla de habilidades y en el timeline "Mi camino de aprendizaje" porque son estructuras bidimensionales que ganan claridad con filas y columnas explícitas.
- Esta combinación justifica el nivel "supera" de la rúbrica de maquetación.

### Animaciones
- `@keyframes blink` en el cursor del logo `ev_`: alterna `opacity` 1 → 0.4 → 1, duración 1.2s, infinito.
- Transición `transform` + `box-shadow` en hover de tarjetas (`translateY(-0.25rem)`), duración 200ms.
- Se respeta `prefers-reduced-motion` desactivando animaciones para usuarios que lo soliciten.

### Estructura de contenido
1. `header` con marca `ev_` + navegación.
2. Sección "Sobre mí" con bio honesta y foto `Emma.png`.
3. Sección "Habilidades" con grid de cards: HTML, CSS, Flexbox/Grid, Responsive, Java, JavaScript, React, Fullstack, ASP.NET, PostgreSQL, Docker, Git/GitHub.
4. Sección "Mi camino de aprendizaje" con timeline 2021→2026, cerrando con el uso de IA para esta PFO.
5. Sección "Contacto" con formulario `mailto:contact@evaldez.ar`.
6. `footer` con enlace a GitHub, año y firma `ev_`.

### Accesibilidad
- Roles ARIA: `banner`, `navigation`, `main`, `contentinfo`.
- Skip-link para saltar navegación.
- `alt` en foto y favicon.
- Foco visible con outline dorado.
- Labels explícitas en el formulario.

## Risks / Trade-offs

- **Trade-off:** el formulario usa `mailto:` sin backend. Es suficiente para la consigna pero no guarda mensajes. Se documenta en el README.
- **Trade-off:** se reutiliza `Emma.png` del portfolio anterior. Se declara en README si es necesario.
- **Riesgo:** la URL de Vercel no estará disponible hasta la Fase F. El README usará un placeholder hasta entonces.
