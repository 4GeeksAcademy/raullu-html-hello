# Tareas de implementación CSS — Landing page de Damián Vesper

Sigue esta lista **estrictamente en orden**. No empieces una tarea posterior hasta completar y verificar la tarea actual. Marca cada tarea como `[x]` únicamente después de realizar y superar su comprobación. Si una verificación falla, corrige el problema dentro de la tarea actual y repítela; no avances con errores pendientes.

## Reglas de ejecución

- La especificación de referencia es [`spec.md`](./spec.md); el plan detallado es [`plan.md`](./plan.md). También se deben respetar `AGENTS.md` y las especificaciones de la fase HTML.
- Esta lista sirve para la futura fase CSS. No empezar hasta recibir autorización explícita para implementar estilos.
- En la implementación, crear exclusivamente `styles.css` en la raíz del proyecto. No modificar `index.html` ni otros archivos salvo necesidad estricta, justificada y autorizada.
- Utilizar únicamente CSS3. No usar JavaScript, frameworks, librerías, preprocesadores, dependencias, imports de fuentes ni recursos externos.
- Mantener intactos el contenido, la semántica, el SEO, el Microdata y la accesibilidad de `index.html`.
- No cambiar las imágenes de prueba ni inventar contenido profesional.
- No marcar tareas como completadas sin haber hecho su verificación.

## Lista ordenada

### Preparación y alcance

1. [ ] **Leer las instrucciones y documentos de referencia.** Leer `AGENTS.md`, `specs/002-CSS/spec.md`, `specs/002-CSS/plan.md`, `specs/001-HTML/spec.md`, `specs/001-HTML/plan.md`, `specs/001-HTML/tasks.md` y revisar `index.html`. **Verificar que se comprenden las reglas, alcance, estructura real y criterios de aceptación antes de continuar.**

2. [ ] **Confirmar autorización y alcance CSS.** Confirmar que se ha solicitado explícitamente iniciar la implementación visual. Asegurar que solo se creará/modificará `styles.css`; no tocar HTML, imágenes ni documentos de especificación. **No crear estilos si no existe autorización explícita.**

3. [ ] **Auditar estructura, clases e IDs existentes.** Verificar en `index.html` los selectores disponibles para encabezado, hero, secciones, tarjetas, portafolio, FAQ, contacto, footer y enlace de salto. **Registrar cualquier desajuste con la especificación y resolverlo en CSS sin alterar HTML; no avanzar con suposiciones.**

4. [ ] **Establecer puntos de revisión responsive.** Preparar comprobaciones para escritorio amplio, tablet/ventana media, móvil estrecho, orientación horizontal/viewport bajo, zoom y navegación con teclado. **Verificar que las pruebas cubren navegación, hero, portafolio, FAQ y pie de página antes de continuar.**

### Base del archivo y sistema visual

5. [ ] **Crear el archivo CSS autorizado.** Crear `styles.css` en la raíz únicamente. Organizarlo con comentarios para tokens/reset, estilos base, tipografía, navegación, componentes, secciones, interacciones, media queries y movimiento reducido. **Verificar que el único archivo nuevo de implementación sea `styles.css` antes de continuar.**

6. [ ] **Definir tokens visuales reutilizables.** En `:root`, definir custom properties para negro carbón, superficies oscuras, texto claro, bronce envejecido, ocre, óxido y acento verde neón discreto, además de tipografías, espacios, ancho máximo, bordes, radios y sombras. **Verificar que la paleta no utiliza acentos de bajo contraste para texto principal y que los tokens se reutilizan antes de continuar.**

7. [ ] **Añadir normalización y estilos base.** Establecer `box-sizing`, márgenes base, tratamiento de imágenes, figuras, listas, enlaces y elementos de página. Mantener el documento refluible y sin desbordamiento horizontal. **Verificar que las reglas base no ocultan contenido, no cambian el orden informativo y no requieren modificar el HTML antes de continuar.**

8. [ ] **Definir tipografía y ritmo editorial.** Aplicar pila serif local/de sistema a títulos y pila sans-serif local/de sistema a cuerpo, navegación y controles. Definir tamaños fluidos, interlineado, pesos, longitud de línea y espacios. **Verificar legibilidad en pantallas pequeñas y grandes, sin `@import`, recursos remotos ni tracking excesivo antes de continuar.**

### Navegación y componentes globales

9. [ ] **Estilizar el encabezado y la navegación.** Diseñar `.site-header`, `.site-brand`, `.primary-navigation` y `.navigation-list` con presencia industrial-victoriana. Adaptar el menú para que todos sus enlaces sigan visibles y utilizables sin JavaScript. **Probar wrapping/reflujo en móvil y foco por teclado antes de continuar.**

10. [ ] **Estilizar el enlace para saltar al contenido.** Ocultar `.skip-link` solo visualmente en estado normal y mostrarlo claramente en `:focus-visible`, con contraste alto y posición visible. **Tabular desde el inicio del documento y verificar que el enlace no queda tapado por el encabezado antes de continuar.**

11. [ ] **Definir estados interactivos y foco.** Aplicar estados `:hover`, `:focus-visible` y `:active` claramente perceptibles a enlaces y botones, sin depender de color aislado ni movimiento. **Verificar visualmente foco visible sobre fondos y componentes diferentes antes de continuar.**

12. [ ] **Estilizar secciones y encabezados comunes.** Dar formato a `.section`, `.section-heading` y `.section-kicker`, incluyendo ancho de contenido, separación, jerarquía y recursos ornamentales discretos. **Verificar que los textos de sección siguen legibles y que el motivo visual no compite con los títulos antes de continuar.**

13. [ ] **Estilizar botones reutilizables.** Diseñar `.button`, `.button-primary` y `.button-secondary` con contraste adecuado, áreas activables cómodas, diferenciación y estados interactivos. **Verificar que ambos CTA del hero y demás llamadas a la acción se distinguen sin depender solo del color antes de continuar.**

### Composición principal y secciones

14. [ ] **Diseñar el Hero.** Crear una composición inmersiva para `.hero-section`, `.hero-copy`, `.hero-eyebrow`, `.hero-subtitle`, `.hero-actions` y `.hero-artwork`; usar columnas en escritorio y apilado en móvil. **Verificar jerarquía inmediata del contenido, proporción de la imagen y ausencia de solapamientos antes de continuar.**

15. [ ] **Estilizar Manifiesto y Sobre mí.** Diseñar `.manifesto-section`, `.manifesto-copy`, citas, `.about-section`, `.about-copy`, `.about-emphasis` y `.about-portrait` con tratamiento editorial coherente. **Verificar que las frases destacadas se reconocen sin depender exclusivamente del color y que el orden del DOM permanece legible antes de continuar.**

16. [ ] **Diseñar el universo visual.** Estilizar `.visual-universe-section`, `.visual-worlds-grid` y `.visual-world-card`, incluyendo imagen, título, descripción, borde y superficie. **Verificar que las tres tarjetas fluyen en columnas adecuadas y se apilan sin pérdida de contenido en móvil antes de continuar.**

17. [ ] **Diseñar las tarjetas de especialidades.** Estilizar `.specialties-section`, `.specialties-grid` y `.specialty-card` para mostrar cuatro servicios con jerarquía y separación claras. **Verificar adaptación del grid y legibilidad de las descripciones en cada ancho antes de continuar.**

18. [ ] **Diseñar la galería del portafolio.** Estilizar `.portfolio-section`, `.portfolio-grid`, `.portfolio-card`, categorías, `figure`, imágenes, `figcaption`, `.content-note` e `.image-note`. Mantener títulos, categorías, descripciones y notas visibles sin hover. **Verificar que las seis obras se muestran en una galería responsive, que las portadas conservan proporción y que ningún efecto tapa información antes de continuar.**

19. [ ] **Diseñar tarjetas de colecciones.** Estilizar `.collections-section`, `.collections-grid` y `.collection-card`, con tratamiento consistente de las imágenes y las descripciones. **Verificar las tres tarjetas en escritorio, tablet y móvil antes de continuar.**

20. [ ] **Diseñar proceso creativo y trayectoria.** Dar presentación visual a `.process-section`, `.process-list`, `.process-step`, `.journey-section`, `.journey-copy` y `.journey-stages`, preservando la secuencia semántica. **Verificar que el orden visual coincide con el orden HTML y que las listas no se recortan antes de continuar.**

21. [ ] **Diseñar Anatomía de una portada.** Estilizar `.cover-anatomy-section`, `.cover-anatomy-content`, `.cover-elements-list` y `.concept-cover` con lista e imagen combinadas en escritorio y apiladas en móvil. **Verificar que los cuatro componentes y la imagen permanecen visibles, legibles y sin deformación antes de continuar.**

22. [ ] **Diseñar Colaboraciones y encargos.** Estilizar `.collaborations-section` y `.collaborations-copy`, incluida la lista de destinatarios y su CTA. **Verificar la jerarquía y el área de activación del CTA en escritorio y móvil antes de continuar.**

23. [ ] **Diseñar las tarjetas de presentaciones.** Estilizar `.events-section`, `.events-grid`, `.event-card` y `.event-status`. Mantener visibles los mensajes pendientes de confirmación. **Verificar que las tarjetas no parezcan eventos confirmados por decoración o estados inventados antes de continuar.**

24. [ ] **Estilizar las preguntas frecuentes nativas.** Diseñar `.faq-section`, `.faq-list`, `.faq-item` y `summary` con estados abiertos/cerrados reconocibles usando marcadores o pseudoelementos, sin JavaScript. **Verificar con teclado que cada `summary` conserva su comportamiento nativo y que las respuestas abiertas se leen bien antes de continuar.**

25. [ ] **Estilizar Contacto y redes pendientes.** Diseñar `.contact-section`, `.contact-copy`, `.contact-note`, `.social-links` y `.closing-line`; destacar el correo sin simular enlaces en las redes pendientes. **Verificar que el correo y los nombres sociales son visualmente distinguibles según su interactividad real antes de continuar.**

26. [ ] **Estilizar el pie de página.** Diseñar `.site-footer`, `.footer-brand`, `.footer-name`, `.footer-navigation`, `.copyright` y `.back-to-top` con jerarquía y cierre coherentes. **Verificar legibilidad, wrapping de enlaces y foco visible antes de continuar.**

### Altura, adaptación y movimiento

27. [ ] **Establecer altura mínima para las secciones.** Aplicar altura aproximada de pantalla usando `min-height` y unidades de viewport apropiadas, sin alturas máximas o fijas que recorten contenido. **Verificar en secciones densas que el contenido puede extenderse más allá del viewport antes de continuar.**

28. [ ] **Adaptar el diseño a escritorio.** Ajustar columnas, anchos máximos, espaciado y densidad visual para pantallas amplias, manteniendo líneas de texto controladas. **Verificar balance del Hero, navegación, tarjetas y portafolio en escritorio antes de continuar.**

29. [ ] **Adaptar el diseño a tablet y ventanas medias.** Ajustar cantidad de columnas, espacios y wrapping del menú en los puntos donde el layout lo requiera. **Verificar que no aparecen tarjetas demasiado estrechas, navegación comprimida o espacios desproporcionados antes de continuar.**

30. [ ] **Adaptar el diseño a móvil.** Apilar composiciones cuando corresponda, mantener visibles todos los enlaces, asegurar áreas táctiles y evitar solapamientos. **Verificar en móvil estrecho que no existe scroll horizontal, contenido cortado ni control inaccesible antes de continuar.**

31. [ ] **Comprobar orientación horizontal, baja altura y zoom.** Revisar encabezado, hero, secciones densas y pie ante viewport de poca altura, orientación horizontal y aumento de texto/zoom. **Corregir recortes y solapamientos antes de continuar.**

32. [ ] **Implementar transiciones y animaciones sutiles.** Añadir solo efectos visuales breves y no esenciales a interacciones o estados, evitando parallax, destellos y movimiento continuo. **Verificar que ninguna información depende de la animación y que no hay saltos de layout antes de continuar.**

33. [ ] **Respetar movimiento reducido.** Añadir `@media (prefers-reduced-motion: reduce)` para suprimir/reducir animaciones, transiciones y scroll suave no esencial. **Activar o inspeccionar esta preferencia y comprobar que se elimina el movimiento prescindible antes de continuar.**

### Revisión y cierre

34. [ ] **Revisar contraste y accesibilidad visual.** Comprobar texto, texto secundario, enlaces, botones, acentos, superficies, foco y estados interactivos. Confirmar que el verde neón es discreto y no el único indicador de estado. **Corregir combinaciones insuficientes antes de continuar.**

35. [ ] **Revisar clases, selectores y mantenibilidad.** Confirmar que las clases usadas existen en `index.html` o que los selectores son etiquetas/pseudoclases intencionales; reducir duplicación, especificidad y `!important` injustificados. **Corregir selectores no utilizados o inválidos antes de continuar.**

36. [ ] **Realizar revisión visual responsive completa.** Inspeccionar escritorio, tablet, móvil, orientación horizontal, zoom, navegación por teclado, `details`/`summary` y movimiento reducido. Revisar en particular header, skip link, hero, portafolio, FAQ y footer. **No avanzar si hay contenido ilegible, recortado, superpuesto o controles sin foco.**

37. [ ] **Comprobar restricciones y cambios del proyecto.** Confirmar que no se añadieron JavaScript, frameworks, librerías, dependencias, fuentes remotas ni recursos externos, y que no se modificó `index.html` u otros archivos sin autorización. **Revisar el diff y corregir cualquier archivo o tecnología fuera de alcance antes de continuar.**

38. [ ] **Cerrar la implementación CSS.** Confirmar que se cumplen todos los criterios de `specs/002-CSS/spec.md`, que las secciones crecen sin recorte y que las preferencias de accesibilidad están atendidas. **Marcar esta tarea solo después de completar todas las comprobaciones anteriores.**
