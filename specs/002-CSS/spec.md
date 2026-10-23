# Especificación CSS — Landing page de Damián Vesper

- **Identificador:** 002-CSS
- **Fase:** Diseño visual con CSS3
- **Estado:** Lista para implementar
- **Documento HTML objetivo:** [`../../index.html`](../../index.html)
- **Alcance de implementación cuando se autorice:** crear únicamente `styles.css`

## 1. Objetivo

Definir los requisitos visuales y técnicos para dar estilo al `index.html` existente y crear una landing page profesional, oscura, elegante y cinematográfica para Damián Vesper. La dirección artística combina Steampunk industrial, Gótico Neo-Victoriano y Dystopian Street Art, manteniendo la legibilidad, la accesibilidad y la adaptación a distintos dispositivos.

Esta especificación describe el diseño y los criterios de aceptación de la futura fase CSS. **No autoriza modificar `index.html` ni crear `styles.css` hasta que se solicite explícitamente iniciar la implementación CSS.**

## 2. Alcance y restricciones

### Incluido en la futura fase

- Crear exclusivamente `styles.css` en la raíz del proyecto.
- Dar estilo a la estructura, clases, identificadores y elementos existentes en `index.html`.
- Implementar apariencia responsive con CSS3, Flexbox, Grid, media queries, transiciones y animaciones sutiles.
- Mantener intactos el contenido, semántica, orden, accesibilidad, SEO y Microdata creados en la fase HTML.

### No incluido

- Modificar `index.html`, salvo que una limitación estrictamente necesaria impida implementar el diseño con la estructura existente. Si se requiriera, justificarlo antes de hacer el cambio y mantenerlo mínimo.
- JavaScript, frameworks, bibliotecas, preprocesadores, dependencias externas, imágenes adicionales o herramientas de compilación.
- Cambiar, ocultar o reescribir contenido, sustituir imágenes de prueba, o crear nuevas afirmaciones profesionales.
- Cargar tipografías, estilos, imágenes o recursos desde servicios externos. La página debe seguir funcionando sin dependencias remotas de CSS.

## 3. Fuente de verdad y estructura HTML existente

- Usar `AGENTS.md`, `specs/001-HTML/spec.md`, `specs/001-HTML/plan.md`, `specs/001-HTML/tasks.md` y `index.html` como contexto.
- El HTML contiene un enlace existente a `styles.css`; no se debe cambiar salvo que sea imprescindible.
- El documento ofrece 14 secciones y los siguientes grupos/clases disponibles para el diseño:

| Área | Clases y elementos existentes de referencia |
|---|---|
| Accesibilidad / navegación | `.skip-link`, `.site-header`, `.site-brand`, `.primary-navigation`, `.navigation-list` |
| Hero | `.hero-section`, `.hero-copy`, `.hero-eyebrow`, `.hero-subtitle`, `.hero-actions`, `.hero-artwork` |
| Secciones comunes | `.section`, `.section-heading`, `.section-kicker` |
| Manifiesto / artista | `.manifesto-section`, `.manifesto-copy`, `blockquote`, `.about-section`, `.about-copy`, `.about-emphasis`, `.about-portrait` |
| Universo visual | `.visual-universe-section`, `.visual-worlds-grid`, `.visual-world-card` |
| Servicios | `.specialties-section`, `.specialties-grid`, `.specialty-card` |
| Portafolio | `.portfolio-section`, `.portfolio-grid`, `.portfolio-card`, `.portfolio-category`, `.content-note`, `.image-note` |
| Colecciones | `.collections-section`, `.collections-grid`, `.collection-card` |
| Proceso | `.process-section`, `.process-list`, `.process-step` |
| Anatomía de portada | `.cover-anatomy-section`, `.cover-anatomy-content`, `.cover-elements-list`, `.concept-cover` |
| Trayectoria | `.journey-section`, `.journey-copy`, `.journey-stages` |
| Colaboraciones | `.collaborations-section`, `.collaborations-copy` |
| Presentaciones | `.events-section`, `.events-grid`, `.event-card`, `.event-status` |
| FAQ | `.faq-section`, `.faq-list`, `.faq-item` |
| Contacto | `.contact-section`, `.contact-copy`, `.contact-note`, `.social-links`, `.closing-line` |
| Pie de página | `.site-footer`, `.footer-brand`, `.footer-name`, `.footer-navigation`, `.copyright`, `.back-to-top` |
| Elementos reutilizables | `.button`, `.button-primary`, `.button-secondary` |

- Las imágenes actuales son marcadores `placehold.co` enlazados desde el HTML. CSS puede controlar su tamaño y recorte, pero no debe depender de que cambien ni asumir que existen imágenes definitivas.
- Puede usarse `body`, selectores de etiquetas semánticas y pseudoelementos decorativos con moderación. No añadir reglas con contenido textual indispensable generado por `::before`/`::after`.

## 4. Dirección visual

### Personalidad

- Oscura, elegante, narrativa y cinematográfica.
- Evocar salones victorianos deteriorados, metal envejecido, maquinaria industrial, humo, ceniza y trazos urbanos distópicos.
- Equilibrar ornamentación y textura con jerarquía clara y espacios de descanso visual.
- Evitar que la estética temática degrade la lectura, la navegación o el contraste.

### Paleta

Definir los colores como custom properties en `:root` para poder ajustarlos de forma coherente. La paleta debe incluir:

- Negro carbón y tonos cercanos para fondo general y paneles.
- Marfil ahumado o tono claro equivalente para el texto principal.
- Bronce envejecido para detalles, líneas, bordes y estados interactivos.
- Ocre y óxido para acentos secundarios.
- Verde neón en pequeños detalles puntuales, nunca como color dominante ni como único indicador de estado.

Los colores finales deben proporcionar contraste suficiente para texto y controles. Evitar texto principal en bronce oscuro sobre negro, texto largo en verde neón y fondos de bajo contraste.

### Tipografía

- Títulos: pila serif ornamental o editorial usando familias locales/de sistema, con alternativas robustas y sin descargar recursos externos.
- Cuerpo, navegación, categorías y controles: pila sans-serif de aspecto industrial/moderno con alternativas de sistema.
- Definir escalas tipográficas fluidas con `clamp()` cuando sea compatible con el objetivo, y conservar tamaños cómodos en móvil.
- Mantener longitud de línea, altura de línea, pesos y espaciado que favorezcan lectura prolongada.
- Las mayúsculas, el tracking y los estilos decorativos se usarán principalmente en rótulos breves; no aplicar espaciado excesivo a párrafos.

### Lenguaje ornamental e industrial

- Incorporar bordes, divisores, marcos, filetes dobles, esquinas o motivos geométricos con CSS cuando ayuden a reforzar la identidad.
- Usar sombras, degradados y texturas CSS de forma sutil, controlada y no dependiente de imágenes externas.
- No cubrir textos con ornamentación, no competir con las obras y no simular controles o símbolos que puedan confundirse con contenido interactivo.
- Mantener consistencia entre secciones mediante variables, patrones de componentes y una escala de espacios reutilizable.

## 5. Requisitos de diseño por componentes

### 5.1 Fondo y composición global

- Establecer un fondo carbón con variaciones de superficie y acentos de bronce/óxido.
- Definir un ancho de lectura cómodo para el contenido y márgenes laterales adaptables.
- Dar a las secciones una separación visual reconocible mediante fondos, bordes, espaciado y ritmo, sin fragmentar excesivamente la página.
- Evitar el desbordamiento horizontal en todos los tamaños de pantalla.

### 5.2 Encabezado y navegación

- Diseñar `.site-header` como una barra reconocible y coherente con la estética, con el nombre artístico destacado y los enlaces legibles.
- La navegación debe ser claramente operable en escritorio y adaptarse a pantallas estrechas sin depender de JavaScript. Puede envolverse o permitir distribución en varias líneas; no crear menú hamburguesa que requiera script.
- Si se usa posicionamiento sticky/fixed, reservar espacio visual, prevenir que oculte destinos al usar fragmentos y evitar reducir demasiado el área de contenido en móvil.
- Diferenciar visualmente el enlace actual solo si puede hacerse sin JavaScript; no afirmar que se conoce la sección activa.
- Estilizar estados `:hover`, `:focus-visible` y `:active` con señal perceptible y contraste suficiente.

### 5.3 Enlace para saltar al contenido

- `.skip-link` debe quedar visualmente oculto en estado normal sin retirarlo del orden de tabulación.
- Debe mostrarse de forma clara y con contraste alto cuando reciba `:focus-visible`.
- Su presentación enfocada debe permanecer en una posición visible y no quedar tapada por el encabezado.

### 5.4 Hero

- Crear un primer pantallazo inmersivo con jerarquía inmediata para el título, subtítulo, descripción y llamadas a la acción.
- En escritorio, se puede utilizar una composición a dos columnas con texto e imagen; en pantallas pequeñas debe transformarse en una columna legible.
- Dar protagonismo a `.hero-artwork` y su imagen de prueba con proporción, marco y tratamiento coherentes; evitar recortes que hagan ilegible cualquier contenido significativo.
- Los botones deben tener objetivos táctiles suficientes, diferenciación clara y estados de foco/hover visibles.

### 5.5 Secciones de contenido

- Mantener un patrón reutilizable para `.section`, `.section-heading` y `.section-kicker`, con ritmo consistente en títulos y párrafos.
- `.manifesto-section` y `.about-section` deben poder usar composiciones editoriales diferenciadas sin alterar el orden del DOM.
- Las citas y frases destacadas deberán resaltar por jerarquía, filetes o tratamiento tipográfico, no solo por color.
- En universo visual, especialidades, colecciones, proceso, etapas, colaboraciones y presentaciones, las tarjetas deben tener límites y separación reconocibles y reordenarse de manera natural en pantallas pequeñas.

### 5.6 Portafolio y colección de imágenes

- `.portfolio-grid` debe funcionar como galería responsive, con las seis obras visibles en una composición equilibrada y adaptativa.
- Las imágenes deben ocupar de forma coherente sus contenedores; puede usarse `object-fit` en función del objetivo visual, cuidando que las imágenes de portada conserven su formato vertical.
- Los títulos, categorías y descripciones deben permanecer legibles y accesibles, sin depender de overlays que aparezcan solo al pasar el ratón.
- Los hover pueden añadir elevación, borde, brillo controlado o escala muy leve, pero no pueden ocultar información necesaria ni provocar saltos de diseño.
- Mantener tratamiento compatible para las tarjetas `.visual-world-card` y `.collection-card`.

### 5.7 Proceso, anatomía, trayectoria y FAQ

- Mostrar pasos y etapas como secuencias legibles, sin que CSS altere el orden lógico comunicado por HTML.
- La lista de elementos de portada debe acompañar visualmente a la imagen conceptual en escritorio y apilarse de forma clara en móvil.
- Estilizar `details`/`summary` como acordeones nativos: indicar visualmente estado cerrado/abierto con pseudoelementos o marcador, mantener el control visible y conservar comportamiento de teclado del navegador. No depender de JavaScript.

### 5.8 Contacto y pie de página

- Dar una jerarquía visual clara al CTA de correo y a la frase final.
- Mantener los nombres sociales pendientes como texto visible y distinguirlos de enlaces activos; CSS no debe simular interacción para texto no enlazado.
- Crear un cierre visual consistente, con navegación secundaria y aviso editable legibles.

## 6. Secciones y altura de pantalla

- Cada sección principal debe aproximarse a la altura de una pantalla mediante `min-height: 100vh` o una combinación equivalente que contemple unidades modernas de viewport cuando resulte apropiado.
- La altura mínima no debe forzar que todas las secciones tengan exactamente la misma medida: el contenido de secciones densas, como portafolio o preguntas frecuentes, debe poder crecer naturalmente.
- No usar alturas fijas que corten texto, imágenes, controles o estados de foco.
- Ajustar padding vertical para pantallas bajas, orientación horizontal y tamaños compactos.
- La cabecera y el pie no necesitan imponerse como secciones de pantalla completa.

## 7. Responsive

### Escritorio

- Utilizar Grid/Flexbox para hero, galerías, tarjetas y composiciones editoriales.
- Aprovechar el ancho disponible sin hacer las líneas de texto demasiado largas.
- Mantener la navegación completa y el equilibrio entre texto e imagen.

### Tablet

- Reducir columnas y espaciados según el ancho.
- Permitir que galerías y conjuntos de tarjetas pasen a dos columnas cuando el espacio lo requiera.
- Impedir que la navegación se comprima hasta dificultar la activación.

### Móvil

- Usar una columna para composiciones que lo requieran, conservar jerarquía y limitar paddings laterales sin perder espacio útil.
- Reorganizar la navegación sin ocultar enlaces ni exigir interacción JavaScript.
- Asegurar tamaños de letra, botones y áreas interactivas cómodos.
- Mantener imágenes en proporciones adecuadas, texto sin desbordamientos y controles sin solapamientos.

### Criterio general

- Introducir media queries por necesidades reales del contenido, no por dispositivo nominal exclusivamente.
- Revisar anchos estrechos, pantallas grandes, zoom de navegador y orientación horizontal.

## 8. Movimiento e interacción

- El desplazamiento suave puede activarse con `scroll-behavior: smooth` únicamente si se desactiva o se neutraliza bajo `prefers-reduced-motion: reduce`.
- Las transiciones deben ser breves y sutiles, centradas en color, borde, opacidad o transformaciones limitadas.
- No usar parallax, destellos, animaciones continuas o movimientos que distraigan o dificulten la lectura.
- Añadir `@media (prefers-reduced-motion: reduce)` para suprimir animaciones, transiciones y desplazamiento suave no esencial.
- Toda información debe estar visible sin que el usuario necesite activar hover.
- El foco visible debe mantener contraste en todos los fondos y no depender de una animación.

## 9. Accesibilidad y compatibilidad

- Preservar íntegramente la semántica, el texto alternativo, la jerarquía de encabezados, los destinos, el comportamiento nativo de FAQ y la accesibilidad implementada en HTML.
- Definir estilos explícitos para `:focus-visible` en todos los enlaces y controles interactivos.
- Comprobar contraste suficiente para texto principal, texto secundario, enlaces, botones y bordes que transmiten significado.
- No comunicar estado únicamente con color; conservar texto o estructura visual adicional disponible en HTML.
- No ocultar contenido con `display: none`, `visibility: hidden`, `opacity: 0` o recorte de forma que lo haga inaccesible.
- Evitar depender exclusivamente de pseudo-elementos para información necesaria.
- Asegurar que escalado de texto y zoom no generen solapamientos ni pérdida de información.

## 10. Organización y mantenibilidad del CSS

- Organizar el archivo con secciones/comentarios previsibles, por ejemplo: variables y reset, estilos base, tipografía, navegación, componentes comunes, secciones, interacciones, media queries y movimiento reducido.
- Definir custom properties para paleta, tipografía, espacios, radios, sombras y anchos máximos que se reutilicen.
- Usar selectores claros, de especificidad moderada y alineados con las clases existentes.
- Agrupar reglas responsive de manera consistente y evitar duplicación innecesaria.
- No usar `!important` salvo una justificación excepcional documentada.
- No usar CSS inline, `@import` de fuentes, frameworks CSS, selectores frágiles basados en posición accidental ni nombres de clase que no existan en el HTML, salvo selectores semánticos/pseudoclases necesarios.
- El CSS debe ser fácil de ampliar sin requerir cambios de contenido en el HTML.

## 11. Criterios de aceptación

La fase CSS se considerará conforme cuando se cumplan todos los puntos siguientes:

1. Se haya creado únicamente `styles.css`, sin modificar `index.html` ni otros archivos, salvo excepción justificada y autorizada.
2. La hoja esté organizada y tenga variables reutilizables para paleta, tipografía y dimensiones/espaciado principales.
3. La página refleje claramente el estilo oscuro, cinematográfico, Steampunk industrial, Gótico Neo-Victoriano y Dystopian Street Art.
4. La paleta incluya carbón, bronce envejecido, ocres, óxido y detalles de verde neón discretos.
5. Se utilicen pilas tipográficas serif y sans-serif de sistema/locales, sin cargar recursos externos.
6. El hero tenga jerarquía y tratamiento inmersivos sin sacrificar legibilidad ni CTA.
7. Las secciones se aproximen a `100vh` con altura mínima y puedan crecer sin recortes.
8. Navegación, galería, tarjetas, pasos, FAQ, contacto y pie de página reciban estilos coherentes con la estructura existente.
9. El portafolio y los grupos visuales se adapten fluidamente a escritorio, tablet y móvil mediante Flexbox/Grid/media queries.
10. La navegación y los controles tengan estados de hover y foco visibles; el enlace de salto se revele al recibir foco.
11. La FAQ nativa `details`/`summary` mantenga su operación por teclado y señale visualmente sus estados.
12. El movimiento y el scroll suave respeten `prefers-reduced-motion`.
13. El contraste, legibilidad, zoom y reflujo no se deterioren; no haya desbordamiento horizontal en anchos móviles.
14. No se añadan JavaScript, frameworks, librerías, dependencias, contenido nuevo ni recursos externos.
15. Los estilos no oculten información ni requieran hover para descubrir contenido.

## 12. Plan de verificación

Antes de cerrar la fase:

- Revisar que todos los selectores de clase usados correspondan al HTML o sean selectores de elementos/pseudoclases válidos.
- Inspeccionar el diseño en vista amplia, tablet y móvil; comprobar específicamente encabezado, hero, portafolio, FAQ y footer.
- Comprobar el enlace de salto, navegación por teclado, estados `:focus-visible`, hover y operación de `details`/`summary`.
- Revisar la legibilidad de los colores de texto y controles sobre cada fondo utilizado.
- Probar la regla de movimiento reducido y verificar que no queden animaciones o scroll suave no esencial.
- Confirmar que las secciones densas crecen con su contenido y no tienen recortes ni alturas rígidas.
- Comprobar ausencia de desbordamiento horizontal, superposición del encabezado con fragmentos y pérdida de foco.
- Revisar el diff: la implementación de esta fase debe limitarse a `styles.css`.
