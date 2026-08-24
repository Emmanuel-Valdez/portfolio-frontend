# PFO1 · Landing de portafolio personal

**Desarrollo de Sistemas Web · Front End · 2026 · 4to cuatrimestre**

Landing estática personal para la entrega individual PFO1. Construida con HTML semántico y CSS propio, desplegada en Vercel.

## Ver en línea

> URL de Vercel: https://portfolio-frontend-orcin-xi.vercel.app/

## Estructura

- `public/index.html` — landing semántica con ARIA, skip-link y comentarios explicativos.
- `public/styles.css` — variables `ev_`, Flexbox + Grid, animación `@keyframes blink`, responsive mobile-first.
- `public/favicon.svg` — favicon `ev_`.
- `public/Emma.png` — foto de perfil.

## Decisiones

- **Posicionamiento**: backend .NET en formación (C#, ASP.NET Core, SQL), con proyectos desplegados desde 2021 en lugar de una lista genérica de tecnologías.
- **Marca `ev_`**: navy `#020617`, oro `#d4a017`, slate `#94a3b8`, cursor `ev_` como favicon.
- **Tipografía**: Google Fonts `Onest` con `display=swap`.
- **Layout**: Flexbox en header, nav, footer, about y formulario; Grid en proyectos y camino; acordeón de habilidades tipo explorador de archivos con `grid-template-rows` (CSS puro, sin JS).
- **Sección Camino**: educación formal con estados (en curso / completado) más certificaciones agrupadas por año, para mostrar trayectoria verificable.
- **Contacto**: formulario visible con `<label>` y `action="mailto:contact@evaldez.ar"` (sin backend).
- **Animación**: cursor `ev_` parpadeante, lift sutil en tarjetas, botones del hero y acordeón de habilidades, con `prefers-reduced-motion`.
- **Imágenes**: `Emma.png` es foto propia; `favicon.svg` es logo propio `ev_`. Los íconos de GitHub y LinkedIn son SVG inline.

## Perfil y redes

- GitHub: [github.com/Emmanuel-Valdez](https://github.com/Emmanuel-Valdez)
- LinkedIn: [linkedin.com/in/evaldezdev](https://linkedin.com/in/evaldezdev)

Repositorio de esta entrega: [Emmanuel-Valdez/portfolio-frontend](https://github.com/Emmanuel-Valdez/portfolio-frontend)

## Uso de IA

Trabajo con agentes de IA como parte de mi flujo cotidiano de ingeniería: me ayudan a iterar más rápido, pero las decisiones finales son mías. En esta PFO dirigí la arquitectura semántica, la paleta y marca `ev_`, la accesibilidad (ARIA, skip-link, `prefers-reduced-motion`) y la reducción de complejidad innecesaria.

Herramientas utilizadas:

- `hy3` y `ox alpha` — plan **gratuito** de [opencode](https://opencode.ai).
- `Kimi Code` — suscripción **de pago**.

**Para qué las usé (trazabilidad por herramienta):**

- **hy3 (opencode, gratuito)** → andamiaje inicial HTML semántico (`header/nav/main/footer`, `skip-link`, jerarquía `h1→h4`) y preguntas sobre roles ARIA. Prompt base: _"armá el esqueleto HTML semántico PFO1 con 5 secciones y comentarios explicativos"_. Descarté un `nav` con `role="menubar"` que propuso y lo dejé en `navigation` simple.
- **ox alpha (opencode, gratuito)** → sistema de diseño `ev_` con variables CSS y `grid-template-rows: 0fr→1fr` para el acordeón sin JS. Prompt: _"pasá el acordeón de habilidades a CSS puro sin JS, accesible con teclado"_. Reescribí el `visibility` sync y el `counter` de líneas para contraste 4.5:1.
- **Kimi Code (de pago)** → refinamiento responsive y pulido visual (clamp, `scroll-padding`, full-bleed en móvil `639px`, estados `current/done` en educación). Prompt: _"revisá responsive mobile-first y proponé 2 breakpoints máximo"_. Rechacé una propuesta con 4 breakpoints y otra con JS para el árbol.

**Experiencia previa:** uso diario de agentes en flujo de ingeniería (skills, MCP, `rtk`); esta PFO es el primer uso documentado para entregar con trazabilidad académica.

**Qué revisé/cambié con criterio propio:** estructura semántica final, paleta `ev_` (`#020617/#d4a017/#94a3b8`), todos los textos (bio honesta desde 2021, camino verificable), decisiones de accesibilidad y simplificación ponytail (quitar sobre-ingeniería, dejar `0fr` en lugar de librería). Cada línea fue revisada y adaptada antes de publicar: la IA fue herramienta de iteración, no autora.
