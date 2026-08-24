## Purpose

Definir los requisitos de la landing estática PFO1 para que cumpla con la rúbrica de la materia y registre las decisiones de diseño, marca y uso de IA.

## ADDED Requirements

### Requirement: Estructura semántica y accesibilidad
La landing debe usar HTML semántico con `header`, `nav`, `main` y `footer`, incluir roles ARIA, textos `alt` en imágenes y al menos cuatro comentarios explicativos en el HTML.

#### Scenario: Navegación por teclado y lectores de pantalla
- **WHEN** un usuario accede a la página
- **THEN** los roles `banner`, `navigation`, `main` y `contentinfo` comunican la región; las imágenes tienen `alt` descriptivo; el enlace "Saltar al contenido principal" es visible al recibir foco.

### Requirement: Maquetación con Flexbox y Grid
La página debe combinar Flexbox y CSS Grid de forma funcional: Flexbox para header, navegación y footer; Grid para las tarjetas de habilidades y el timeline del camino de aprendizaje.

#### Scenario: Visualización en desktop
- **WHEN** el viewport es ancho
- **THEN** las tarjetas de habilidades se muestran en una grilla de columnas y el timeline usa una estructura de dos columnas.

#### Scenario: Visualización en móvil
- **WHEN** el viewport es estrecho
- **THEN** las tarjetas y el timeline se apilan en una sola columna manteniendo legibilidad.

### Requirement: Tipografía y variables CSS
La página debe usar Google Fonts (Onest) y variables CSS para la paleta `ev_` (navy base, oro, slate) y las familias tipográficas, logrando coherencia visual y jerarquía.

#### Scenario: Cambio de acento
- **WHEN** se modifica la variable `--gold`
- **THEN** todos los elementos de acento (títulos, enlaces, cursor) actualizan su color sin editar selectores individuales.

### Requirement: Animaciones y transiciones
La página debe incluir al menos una animación propia con `@keyframes`: el cursor del logo `ev_` parpadea, y las tarjetas de habilidades tienen un efecto `lift` suave en hover.

#### Scenario: Cursor parpadeante
- **WHEN** la página carga
- **THEN** el cursor dorado junto a `ev_` alterna opacidad de forma continua.

#### Scenario: Hover en tarjetas
- **WHEN** el usuario pasa el mouse sobre una tarjeta de habilidad
- **THEN** la tarjeta se eleva ligeramente y cambia de borde con una transición suave.

### Requirement: Formulario de contacto accesible
El formulario de contacto debe usar etiquetas `<label>` asociadas, campos `name`, `email` y `message`, y `action="mailto:contact@evaldez.ar"` sin backend.

#### Scenario: Envío de correo
- **WHEN** el usuario completa el formulario y presiona enviar
- **THEN** se abre el cliente de correo predeterminado con los datos prellenados y destinatario `contact@evaldez.ar`.

### Requirement: Enlace visible a GitHub
La página debe incluir un enlace visible y funcional al perfil de GitHub `github.com/Emmanuel-Valdez`.

#### Scenario: Acceso al perfil
- **WHEN** el usuario hace clic en el enlace de GitHub
- **THEN** se abre el perfil en una nueva pestaña.

### Requirement: Voz honesta y declaración de IA
El contenido debe reflejar que programo desde 2021 (Java), que hice cursos fullstack + React, y que esta PFO se armó con agentes de IA. El README debe declarar las herramientas y planes usados.

#### Scenario: Lectura de la biografía
- **WHEN** un visitante lee la sección "Sobre mí"
- **THEN** encuentra una presentación realista, sin venderse como profesional, y con mención explícita del uso de IA en esta entrega.

### Requirement: README completo
El repositorio debe contener un `README.md` con descripción de la PFO1, URL de Vercel, decisiones de diseño y declaración de uso de IA completa.

#### Scenario: Entrega del enlace
- **WHEN** el docente revisa el repositorio
- **THEN** encuentra README, enlace funcional a Vercel, perfil de GitHub enlazado y declaración de IA detallada.
