# Plan de implementación CSS — Landing page de Damián Vesper

- **Especificación de referencia:** [`spec.md`](./spec.md)
- **Identificador:** 002-CSS
- **Objetivo:** organizar, en orden verificable, la futura implementación visual de `index.html` con CSS3.
- **Estado:** planificación; todavía no autoriza a crear `styles.css`.

## 1. Reglas de ejecución

1. Leer y respetar `AGENTS.md`, `specs/002-CSS/spec.md` y la fase HTML ya implementada antes de comenzar.
2. Implementar estilos únicamente cuando se solicite explícitamente comenzar la fase CSS.
3. En la fase de implementación, crear exclusivamente `styles.css` en la raíz. No modificar `index.html` ni otros archivos salvo necesidad estricta, justificada y autorizada.
4. Utilizar solo CSS3. No incorporar JavaScript, frameworks, librerías, preprocesadores, dependencias, recursos remotos ni herramientas de compilación.
5. Preservar la semántica, textos, navegación, accesibilidad, SEO y Microdata de `index.html`.
6. Seguir las etapas en el orden definido. No avanzar a la siguiente etapa hasta verificar satisfactoriamente la actual; si una comprobación falla, corregir antes de continuar.
7. No sustituir las imágenes de prueba ni añadir contenido. El CSS debe ser compatible con los recursos actualmente referenciados.

## 2. Entregable y límites

### Entregable futuro

- `styles.css`: hoja de estilos organizada, reutilizable, responsive, accesible y alineada con las clases existentes en `index.html`.

### Límites de alcance

- El archivo `index.html` ya enlaza `styles.css`; no se necesita alterar ese enlace.
- No crear ni editar imágenes, fuentes, HTML, scripts, configuración del servidor ni documentación durante la implementación CSS.
- No cargar tipografías u otros recursos desde la red. Utilizar pilas tipográficas locales/de sistema.
- No ocultar contenido ni hacer que información indispensable dependa de hover, animaciones o pseudoelementos.

## 3. Fases de trabajo

### Fase 0 — Preparación y auditoría de HTML

**Acciones**

- Leer la especificación CSS completa y consultar las reglas permanentes del repositorio.
- Inspeccionar el `index.html` para confirmar clases, IDs, estructura de secciones y componentes reales.
- Confirmar que el archivo HTML ya referencia `styles.css`.
- Registrar que las imágenes de prueba son marcadores externos `placehold.co`; no asumir imágenes definitivas ni cambiar las rutas.
- Acordar los puntos de revisión responsive: escritorio, tablet, móvil estrecho, orientación horizontal y zoom.

**Verificación para avanzar**

- El alcance se limita a CSS y existe una lista de selectores basada en el HTML real.
- No se propone cambiar contenido ni estructura durante la fase de diseño.

### Fase 1 — Estructura del archivo CSS y tokens

**Acciones**

- Crear `styles.css` en la raíz del proyecto solo cuando se autorice la implementación.
- Organizar el archivo con comentarios por bloques: variables/reset, base, tipografía, encabezado, componentes, secciones, interacciones, responsive y movimiento reducido.
- Definir variables CSS en `:root` para paleta, tipografía, espacios, anchos máximos, bordes, radios y sombras.
- Establecer `box-sizing`, comportamiento de imágenes y reglas base sin alterar la semántica ni el orden de lectura.

**Verificación para avanzar**

- Las variables cubren negro carbón, superficies oscuras, texto claro, bronce, ocre, óxido y acento verde neón discreto.
- No hay reglas inline, imports externos, dependencias o selectores de clases inexistentes.
- Los colores y la escala inicial permiten lectura cómoda sobre fondos oscuros.

### Fase 2 — Tipografía, ritmo y contenedor global

**Acciones**

- Definir una pila serif editorial/ornamental local para títulos y una pila sans-serif industrial/moderna para cuerpo, controles y navegación.
- Establecer tamaños, pesos, interlineado, anchuras de párrafo, escala fluida y espacios reutilizables.
- Crear reglas generales para `body`, enlaces, imágenes, figuras, encabezados, párrafos y listas.
- Ajustar anchos máximos y márgenes laterales de forma flexible para mantener líneas de lectura cómodas.

**Verificación para avanzar**

- Los textos principales y secundarios son legibles, con jerarquía clara y contraste suficiente.
- El tamaño fluye sin desbordar en móvil ni generar líneas excesivamente largas en escritorio.
- No se importan fuentes ni se aplica tracking excesivo a texto corrido.

### Fase 3 — Encabezado, navegación y acceso por teclado

**Acciones**

- Diseñar `.site-header`, `.site-brand`, `.primary-navigation` y `.navigation-list` con una identidad victoriana industrial elegante.
- Diseñar la adaptación de la navegación a anchuras menores usando wrapping/disposición en varias líneas sin ocultar enlaces ni requerir JavaScript.
- Diseñar `.skip-link` oculto visualmente en reposo y claramente visible al recibir `:focus-visible`.
- Establecer estados `:hover`, `:focus-visible` y `:active` perceptibles para enlaces y controles.
- Si el encabezado se hace sticky, comprobar que los anclajes no quedan cubiertos y que el espacio disponible no se reduce en exceso.

**Verificación para avanzar**

- Todos los enlaces siguen visibles y operables por teclado en escritorio y móvil.
- El foco presenta alto contraste, no depende de animaciones y no queda oculto.
- El enlace de salto aparece en posición visible al tabular.
- Los destinos de fragmento no quedan cubiertos por el encabezado.

### Fase 4 — Componentes reutilizables y Hero

**Acciones**

- Estilizar `.section`, `.section-heading` y `.section-kicker` con espaciado y tratamiento consistentes.
- Definir `.button`, `.button-primary` y `.button-secondary` con contraste, áreas activables cómodas y estados interactivos.
- Diseñar `.hero-section`, `.hero-copy`, `.hero-artwork` y elementos asociados para dar una primera impresión inmersiva.
- En escritorio, organizar texto e imagen con una composición equilibrada; en móvil, apilar los elementos en orden natural.
- Presentar la imagen de prueba con marco, proporción y recorte que no interfieran con el texto.

**Verificación para avanzar**

- Título, subtítulo, descripción y ambos CTA son inmediatamente reconocibles.
- La imagen se adapta sin deformación y conserva su propósito descriptivo.
- El hero no provoca desbordamiento, solapamiento ni pérdida de legibilidad en anchos estrechos.

### Fase 5 — Secciones editoriales y tarjetas

**Acciones**

- Aplicar composiciones diferenciadas a manifiesto y sobre mí, manteniendo el orden del DOM.
- Estilizar citas y frases destacadas con jerarquía tipográfica, filetes o acentos, no solo color.
- Diseñar los grupos `.visual-worlds-grid`, `.specialties-grid`, `.collections-grid`, `.events-grid` y las clases de tarjeta asociadas.
- Dar a las tarjetas estructura reconocible, bordes y superficies relacionadas con la identidad global, sin ornamentación que reste legibilidad.
- Estilizar proceso y etapas como secuencias, preservando el orden semántico de sus listas.
- Diseñar `.cover-anatomy-content` para combinar lista e imagen conceptual en escritorio y apilarla en móvil.

**Verificación para avanzar**

- Todos los textos permanecen visibles y leíbles, sin necesidad de hover.
- Las rejillas disminuyen de columnas de forma natural según el ancho.
- No se cambia visualmente el orden informativo ni se ocultan elementos en pantalla pequeña.

### Fase 6 — Galería del portafolio y tratamiento de imágenes

**Acciones**

- Diseñar `.portfolio-grid` con CSS Grid/Flexbox para acomodar las seis obras.
- Dar formato a `.portfolio-card`, imágenes, `figcaption`, `.portfolio-category`, `.image-note` y `.content-note`.
- Mantener reconocible la proporción vertical de las portadas conceptuales y el ajuste de los demás formatos.
- Aplicar efectos hover discretos (borde, sombra o elevación leve) que no oculten título, categoría ni descripción y no generen saltos bruscos.
- Reutilizar principios de imagen para `.visual-world-card`, `.collection-card`, `.hero-artwork`, `.about-portrait` y `.concept-cover`.

**Verificación para avanzar**

- Las seis obras se pueden explorar sin hover; sus títulos, categorías y descripciones siempre son accesibles.
- Las imágenes no se deforman ni colapsan y las notas de imagen de prueba siguen visibles.
- La composición cambia de columnas correctamente en tablet y móvil.

### Fase 7 — FAQ, contacto y pie de página

**Acciones**

- Estilizar `.faq-list`, `.faq-item` y `summary` manteniendo controles nativos de `details`.
- Mostrar claramente los estados abierto/cerrado usando pseudoelementos o marcadores CSS, sin sustituir contenido semántico.
- Dar jerarquía al CTA de correo, notas de contacto y frase de cierre.
- Mantener los nombres de redes pendientes como texto y no representarlos visualmente como enlaces activos.
- Estilizar `.site-footer`, marca, navegación, copyright y retorno al inicio como un cierre coherente y legible.

**Verificación para avanzar**

- Los `summary` son distinguibles, visibles y operables con teclado.
- Respuestas abiertas se leen con claridad y no dependen de JavaScript.
- Las redes pendientes no parecen botones ni enlaces interactivos.
- Los enlaces y el aviso editable conservan contraste y legibilidad.

### Fase 8 — Altura de secciones y diseño responsive

**Acciones**

- Establecer para secciones principales una altura mínima aproximada de pantalla (`min-height: 100vh` y/o unidades modernas compatibles), sin fijar altura máxima.
- Permitir que secciones densas —portafolio, FAQ, listas y contenido extenso— crezcan por encima del viewport.
- Definir breakpoints según los puntos en que la composición deja de funcionar, no solo por nombres de dispositivos.
- En escritorio, aprovechar columnas sin ensanchar demasiado los párrafos.
- En tablet, ajustar columnas, navegación, espacios y tamaño de imágenes.
- En móvil, apilar contenido, mantener enlaces disponibles, preservar áreas táctiles y prevenir desbordamientos.
- Considerar pantallas bajas y orientación horizontal con ajustes específicos de espaciado si son necesarios.

**Verificación para avanzar**

- Secciones de contenido corto se aproximan a una pantalla; las densas no recortan ni ocultan contenido.
- Encabezado, hero, galería, FAQ y pie de página funcionan en móvil, tablet y escritorio.
- No hay scroll horizontal, solapamientos, botones comprimidos ni columnas ilegibles.
- El diseño mantiene su jerarquía con zoom y escalado de texto.

### Fase 9 — Movimiento y preferencias del usuario

**Acciones**

- Añadir transiciones breves y sutiles a estados interactivos y, solo cuando aporte valor, animaciones de entrada no esenciales.
- Aplicar desplazamiento suave si se desea y si la preferencia de movimiento lo permite.
- Crear una media query `prefers-reduced-motion: reduce` que elimine o minimice animaciones, transiciones y scroll suave no esenciales.
- Evitar efectos continuos, parallax, destellos o movimientos intensos.

**Verificación para avanzar**

- Con reducción de movimiento activa no se ejecutan movimientos no esenciales.
- Ninguna animación es necesaria para comprender contenido o estado.
- Foco e interacción siguen identificables sin transición.

### Fase 10 — Revisión de accesibilidad, calidad y cierre

**Acciones**

- Revisar contraste de texto, enlaces, botones, bordes significativos y foco en todas las superficies.
- Confirmar que los estados interactivos se comunican mediante más de un indicador cuando corresponda.
- Revisar que no se haya ocultado contenido ni alterado el orden visual de lectura de forma confusa.
- Comprobar selectores y evitar especificidad innecesaria, duplicación, reglas frágiles y `!important` injustificados.
- Revisar las reglas de media queries, reduced motion, imágenes, navegación y FAQ.
- Revisar el diff del proyecto y confirmar que la fase implementó exclusivamente `styles.css`.

**Salida**

- Hoja de estilos lista, mantenible, responsive, accesible y basada en el HTML existente.

**Verificación final**

- Todos los criterios de aceptación de `spec.md` se han revisado y están satisfechos.
- No existen cambios no autorizados de HTML, contenido, metadatos o Microdata.
- No se han introducido dependencias externas ni tecnologías prohibidas.

## 4. Matriz de cobertura de estilos

| Componente | Enfoque de presentación | Verificación principal |
|---|---|---|
| Fondo y tokens | Carbón, superficies oscuras, bordes bronce/óxido y variables CSS | Contraste y consistencia global |
| Header/navigation | Barra distintiva, enlaces claros, adaptación sin JS | Navegación completa y foco visible |
| Skip link | Oculto solo visualmente en reposo; visible al foco | Accesible desde teclado |
| Hero | Composición cinematográfica texto/imagen, CTA destacado | Reflujo y legibilidad en móvil |
| Manifiesto/Sobre mí | Composición editorial y cita destacada | Orden del DOM preservado |
| Universo/Servicios/Colecciones/Eventos | Grid de tarjetas reutilizable | Reorganización responsive |
| Portafolio | Galería visual, formatos de imagen adaptados y captions legibles | Seis obras visibles sin hover obligatorio |
| Proceso/Trayectoria | Secuencias numeradas o etapas jerárquicas | Orden y lectura preservados |
| Anatomía de portada | Lista más imagen grande; apilado en móvil | Sin recorte ni desbordamiento |
| FAQ | `details`/`summary` estilizados como acordeón nativo | Teclado y estados abierto/cerrado |
| Contacto | CTA de correo destacado y redes pendientes no interactivas | Diferenciación semántica visual |
| Footer | Cierre compacto, navegación secundaria y copyright | Enlaces y texto legibles |
| Movimiento | Transiciones/scroll suaves con reducción de movimiento | Respeto a `prefers-reduced-motion` |

## 5. Verificación por viewport y uso

Realizar una revisión visual en, como mínimo, estas condiciones:

- **Escritorio amplio:** comprobar balance de hero, máximo de línea, navegación, rejillas y espacio negativo.
- **Tablet/ventana media:** comprobar cambios de columnas y el wrapping del menú.
- **Móvil estrecho:** comprobar que todas las rutas de navegación se mantienen visibles, botones activables, texto sin desbordamiento e imágenes proporcionadas.
- **Orientación horizontal o viewport de poca altura:** comprobar que el contenido no se recorta ni queda oculto por el encabezado.
- **Zoom/aumento de texto:** comprobar que no aparecen solapamientos ni pérdida de contenido.
- **Solo teclado:** recorrer skip link, navegación, CTAs, enlaces del footer y cada `summary`.
- **Movimiento reducido:** confirmar que animaciones y scroll suave no esencial se desactivan.

## 6. Riesgos y mitigaciones

| Riesgo | Mitigación |
|---|---|
| El encabezado sticky tapa secciones enlazadas | Evitar sticky o reservar espacio/usar desplazamiento de destino adecuado y verificar cada fragmento |
| `min-height: 100vh` recorta una sección larga | Usar solo altura mínima; permitir crecimiento natural y ajustar espacios según contenido |
| Contraste insuficiente con bronce, óxido o verde sobre carbón | Reservar los acentos oscuros para decoración y revisar texto/controles con contraste suficiente |
| Diseño móvil oculta enlaces sin JS | Permitir wrapping o reflujo del menú; no implementar hamburguesa visual sin funcionalidad |
| Portafolio depende de hover para revelar títulos | Mantener títulos, categorías y descripciones visibles siempre |
| El tratamiento de imagen recorta elementos esenciales | Mantener formato y `object-position` prudente; evitar recorte agresivo en obras verticales |
| Animaciones causan molestias | Mantenerlas sutiles y neutralizarlas con `prefers-reduced-motion` |
| CSS intenta resolver cambios estructurales del HTML | Ajustar presentación dentro del DOM existente; proponer cualquier modificación estructural por separado y justificarla |
| Recursos remotos no cargan o crean dependencias | No cargar fuentes, imágenes ni CSS externos desde la hoja de estilos |

## 7. Criterios de cierre y transición

La fase CSS puede cerrarse cuando:

1. `styles.css` existe y es el único archivo de implementación añadido o modificado en esta fase.
2. Todos los componentes y las 14 secciones de `index.html` tienen una presentación coherente.
3. Diseño responsive, foco visible, contraste y reduced motion han sido revisados.
4. El contenido puede crecer sin alturas rígidas ni recorte.
5. No se depende de JavaScript, hover, servicios externos o recursos nuevos.
6. La validación visual/estructural se ha completado en los tamaños y modos previstos.

Cualquier ajuste futuro de estructura o contenido deberá tratarse como una solicitud aparte y respetar la especificación HTML original.
