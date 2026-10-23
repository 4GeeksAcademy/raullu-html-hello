# Instrucciones permanentes para GitHub Copilot

Estas reglas se aplican a todo el desarrollo de este proyecto. Antes de realizar cualquier cambio, léelas y respétalas. Toda futura implementación debe cumplirlas; si una petición entra en conflicto con ellas, no introduzcas una solución incompatible y solicita aclaración.

## 1. Contexto y objetivo

- El proyecto es una landing page para un diseñador gráfico especializado en portadas e ilustraciones de novelas.
- La dirección artística combina estética victoriana postapocalíptica, Steampunk industrial y Gótico Neo-Victoriano.
- El resultado debe ser atractivo, moderno, coherente con esa identidad y fácil de mantener y ampliar.
- No inventes el nombre, la biografía, la experiencia, los clientes, los premios, los datos de contacto ni ningún otro dato profesional real del artista. Usa únicamente información proporcionada explícitamente. Si falta un dato necesario, deja un marcador claramente identificable y solicita la información cuando corresponda.

## 2. Tecnologías permitidas

- Utiliza exclusivamente **HTML5 y CSS3**.
- No añadas JavaScript, frameworks, bibliotecas, preprocesadores, herramientas de compilación ni otras tecnologías.
- No introduzcas dependencias ni código que requiera una tecnología no autorizada.
- Mantén la estructura y los estilos en sus archivos correspondientes: `index.html` y `styles.css`.

## 3. Fases de trabajo y alcance de cambios

Sigue estas fases en este orden:

1. **Fase HTML — `index.html`:** crea primero la estructura, el contenido, la accesibilidad y los elementos SEO usando HTML5 semántico y Microdata.
2. **Fase CSS — `styles.css`:** solo después de completar la fase HTML, implementa la presentación visual y el comportamiento responsive con CSS3.

- No empieces la fase CSS antes de terminar la estructura HTML.
- Trabaja únicamente en la fase solicitada y evita modificar archivos de fases anteriores salvo que sea imprescindible para cumplir los requisitos o corregir un defecto. Explica brevemente por qué es necesario cualquier cambio de ese tipo.
- No crees archivos HTML o CSS mientras no se haya solicitado empezar la implementación. Para esta etapa inicial, el único archivo que se debe crear es `AGENTS.md`.
- No modifiques archivos ajenos al alcance de la tarea ni reformatees o reorganices partes no relacionadas.

## 4. Requisitos de HTML y contenido

- Escribe HTML5 válido, semántico, correctamente indentado y con una jerarquía lógica de encabezados (`h1`–`h6`).
- Usa elementos semánticos adecuados, por ejemplo `header`, `nav`, `main`, `section`, `article` y `footer`, según corresponda.
- La landing page debe incluir navegación interna y varias secciones; planifica cada sección para ocupar aproximadamente una altura de pantalla (`100vh`), sin impedir que el contenido crezca cuando sea necesario.
- Mantén los enlaces internos coherentes con los identificadores de sus destinos y asegúrate de que la navegación sea utilizable sin ratón.
- No añadas textos, testimonios, proyectos, imágenes ni afirmaciones factuales inventadas. Los recursos visuales deben ser proporcionados o estar claramente señalados como marcadores pendientes.

## 5. Accesibilidad

- Incluye textos `alt` útiles en las imágenes informativas; usa `alt=""` para imágenes puramente decorativas.
- Añade atributos ARIA solo cuando la semántica HTML nativa no sea suficiente; evita roles y etiquetas redundantes o incorrectos.
- Asegura navegación y operación por teclado, foco visible y un orden de lectura lógico.
- Mantén contraste suficiente entre texto, controles y fondos, especialmente en la paleta oscura.
- Usa etiquetas y nombres accesibles claros para enlaces y controles; no dependas únicamente del color para comunicar información.
- Respeta las preferencias de movimiento reducido cuando se añadan efectos o transiciones.

## 6. SEO y datos estructurados

- Incluye metadatos HTML apropiados, como codificación de caracteres, `viewport`, título y descripción, sin inventar datos del artista.
- Conserva una estructura semántica clara y un encabezado principal reconocible.
- Implementa datos estructurados de Schema.org mediante **Microdata HTML** cuando se construya la página. No uses JSON-LD ni JavaScript para ello.
- Usa únicamente datos confirmados. Omite propiedades desconocidas en lugar de rellenarlas con información inventada.

## 7. Diseño responsive y dirección visual

- Diseña para móviles, tabletas y escritorio; comprueba que el contenido no desborde y que la navegación siga siendo usable en pantallas pequeñas.
- La estética debe ser oscura, industrial y victoriana, inspirada en el Steampunk y el Gótico Neo-Victoriano, sin sacrificar legibilidad ni accesibilidad.
- Usa CSS3 organizado y mantenible, con selectores claros, propiedades agrupadas de forma coherente y estilos responsive mediante media queries cuando sean necesarios.
- No uses dependencias externas para conseguir el diseño. Evita soluciones visuales que dependan de JavaScript.
- Las secciones pueden aproximarse a `100vh`, pero deben adaptarse al contenido y a distintos tamaños de pantalla; no recortes texto ni fuerces alturas que lo oculten.

## 8. Calidad y verificación

- Mantén el código limpio, coherente, fácil de leer y de ampliar; evita duplicación innecesaria y soluciones frágiles.
- Verifica que cada enlace interno tenga un destino, que los encabezados mantengan una jerarquía lógica y que las imágenes tengan el tratamiento alternativo adecuado.
- Comprueba visualmente o revisa las reglas responsive, el foco de teclado, el contraste y la ausencia de desbordamientos cuando se implemente el diseño.
- Antes de terminar una tarea, confirma que solo se modificaron los archivos necesarios y que no se incorporaron tecnologías prohibidas.
