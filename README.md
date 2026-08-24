# PFO1 · Landing de portafolio personal

**Desarrollo de Sistemas Web · Front End · 2026 · 4to semestre**

Landing estática personal para la entrega individual PFO1. Construida con HTML semántico y CSS propio, desplegada en Vercel.

## Ver en línea

> URL de Vercel: `https://<pendiente>.vercel.app`
>
> Se actualizará tras el deploy en la Fase F.

## Estructura

- `index.html` — landing semántica con ARIA, skip-link y comentarios explicativos.
- `styles.css` — variables `ev_`, Flexbox + Grid, animación `@keyframes blink`, responsive mobile-first.
- `public/` — `favicon.svg` e `Emma.png`.

## Decisiones

- **Voz honesta**: declaro abiertamente que programo desde 2021 (Java), que hice cursos fullstack + React, y que esta PFO fue armada con agentes de IA.
- **Marca `ev_`**: navy `#020617`, oro `#d4a017`, slate `#94a3b8`, cursor `ev_` como favicon.
- **Tipografía**: Google Fonts `Onest` con `display=swap`.
- **Layout**: Flexbox en header, nav, footer, about y formulario; Grid en habilidades y timeline.
- **Contacto**: formulario visible con `<label>` y `action="mailto:contact@evaldez.ar"` (sin backend).
- **Animación**: cursor `ev_` parpadeante y lift sutil en tarjetas, con `prefers-reduced-motion`.
- **Imágenes**: `Emma.png` es foto propia; `favicon.svg` es logo propio `ev_`.

## Perfil de GitHub

[github.com/Emmanuel-Valdez](https://github.com/Emmanuel-Valdez)

Repositorio de esta entrega: [Emmanuel-Valdez/portfolio-frontend](https://github.com/Emmanuel-Valdez/portfolio-frontend)

## Declaración de uso de IA

Esta PFO fue desarrollada con asistencia de agentes de IA:

- `hy3` y `ox alpha` — plan **gratuito** de [opencode](https://opencode.ai).
- `Kimi Code` — suscripción **de pago**.

**No se utilizó Claude.**

Experiencia previa: uso agentes de IA de forma cotidiana en mi flujo de ingeniería (skills, MCP, alias `rtk`, prompts iterativos). Revisé y adapté con criterio propio la estructura semántica, la paleta `ev_`, la reducción de over-engineering (disciplina ponytail) y la voz honesta del texto.
