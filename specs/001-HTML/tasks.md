# Tareas de implementación — Landing page de Damián Vesper

Sigue esta lista **estrictamente en orden**. No empieces una tarea posterior hasta terminar y verificar la tarea actual. Marca cada tarea como `[x]` únicamente después de completar su comprobación. Si una verificación falla, corrige el problema dentro de la tarea actual y repite la verificación; no avances con errores pendientes.

## Reglas de ejecución

- La especificación de referencia es [`spec.md`](./spec.md); el plan detallado es [`plan.md`](./plan.md). También se debe respetar el `AGENTS.md` de la raíz.
- La fase actual autoriza exclusivamente la creación de `index.html` con HTML5. No crear `styles.css` todavía; solo vincularlo desde el HTML.
- No utilizar JavaScript, CSS inline o embebido, frameworks, librerías, dependencias ni tecnologías adicionales.
- No inventar información profesional, fechas, lugares, clientes, premios, eventos confirmados ni perfiles sociales.
- No marcar una tarea como completada si su verificación no se ha realizado.

## Lista ordenada

### Preparación y alcance

1. [ ] **Leer las instrucciones del proyecto.** Leer completamente `AGENTS.md`, `specs/001-HTML/spec.md` y `specs/001-HTML/plan.md`. Verificar que se entiende el orden de fases, los 14 contenidos, los límites de tecnologías y los datos que no deben inventarse. **No avanzar hasta confirmar estos puntos.**

2. [ ] **Confirmar el alcance de esta fase.** Asegurarse de que el único archivo de implementación que se creará o modificará es `index.html`; `styles.css` solo será referenciado. No crear imágenes, carpetas de imágenes ni otros entregables de implementación. **Verificar el alcance antes de escribir código.**

3. [ ] **Preparar el inventario de destinos internos.** Registrar los IDs de las 14 secciones: `inicio`, `manifiesto`, `sobre-mi`, `universo-visual`, `especialidades`, `portafolio`, `colecciones`, `proceso`, `anatomia-portada`, `trayectoria`, `colaboraciones`, `presentaciones`, `preguntas-frecuentes` y `contacto`. Registrar también el destino del `main` para el enlace de salto. **Verificar que no haya nombres duplicados o contradictorios antes de continuar.**

### Documento base y navegación

4. [ ] **Crear el documento HTML5 mínimo.** Crear `index.html` con `<!DOCTYPE html>`, `<html lang="es">`, `<head>` y `<body>`, correctamente indentado. **Verificar que los elementos raíz están presentes y bien anidados antes de continuar.**

5. [ ] **Añadir metadatos SEO esenciales.** Incluir `meta charset`, `meta name="viewport"`, `<title>` descriptivo y una `meta description` concisa, en español y ajustada al contenido sin afirmaciones no confirmadas. **Verificar cada metadato y la validez de su sintaxis antes de continuar.**

6. [ ] **Vincular los estilos futuros sin implementarlos.** Incluir en `<head>` la referencia a `styles.css`. No crear ese archivo ni añadir `<style>`, atributos `style` o reglas CSS. **Verificar que solo hay una referencia y que no se han escrito estilos antes de continuar.**

7. [ ] **Crear el enlace de salto y la estructura global.** Añadir al principio del contenido un enlace «Saltar al contenido principal» y crear `header`, `nav`, `main` con ID `contenido-principal` (o equivalente consistente) y `footer`. **Verificar que el enlace apunta al `main` y que los landmarks están correctamente estructurados antes de continuar.**

8. [ ] **Implementar la navegación principal.** Añadir en este orden los enlaces Inicio (`#inicio`), Sobre mí (`#sobre-mi`), Especialidades (`#especialidades`), Portafolio (`#portafolio`), Trayectoria (`#trayectoria`), Presentaciones (`#presentaciones`) y Contacto (`#contacto`). **Verificar los siete enlaces y sus fragmentos previstos antes de continuar.**

### Estructura de secciones

9. [ ] **Crear los 14 contenedores de sección.** Añadir cada sección dentro de `main`, en el orden de `spec.md`, con los IDs únicos del inventario. **Verificar que aparecen las 14 secciones, en el orden correcto, sin IDs duplicados y sin secciones omitidas antes de continuar.**

10. [ ] **Definir la jerarquía de encabezados.** Colocar un solo `h1` en Inicio; asignar `h2` a cada sección y usar `h3` para sus subsecciones/tarjetas según corresponda. **Contar los `h1` y revisar toda la jerarquía de encabezados; corregir saltos o duplicados antes de continuar.**

11. [ ] **Añadir clases descriptivas para la fase visual.** Asignar nombres de clase semánticos y consistentes a las secciones y componentes repetibles. Mantener los `id` para navegación y las clases para el futuro diseño. **Verificar que las clases no sustituyen elementos semánticos ni incluyen estilos antes de continuar.**

### Contenido requerido

12. [ ] **Completar Inicio — Hero (`#inicio`).** Incorporar el título, subtítulo, descripción y los enlaces «Explorar mis obras» (`#portafolio`) y «Hablemos de tu historia» (`#contacto`), además del espacio de imagen principal. **Comparar palabra por palabra con `spec.md` y comprobar destinos antes de continuar.**

13. [ ] **Completar Manifiesto (`#manifiesto`).** Añadir título, ambos textos y frase destacada. Usar elementos semánticos adecuados, como `blockquote` para la cita si corresponde. **Verificar que no falta ninguna frase ni se altera su sentido antes de continuar.**

14. [ ] **Completar Sobre mí (`#sobre-mi`).** Añadir título, los tres párrafos, la frase final y el espacio para retrato/ilustración. **Verificar los textos y que no se incorporen datos biográficos no suministrados antes de continuar.**

15. [ ] **Completar Mi universo visual (`#universo-visual`).** Añadir los tres bloques: Gótico Neo-Victoriano, Steampunk industrial y Distopía urbana, cada uno con imagen, título y descripción. **Verificar que los tres textos están completos y que cada imagen tiene alternativa antes de continuar.**

16. [ ] **Completar Especialidades (`#especialidades`).** Añadir las cuatro tarjetas de servicios con encabezado y descripción: portadas, ilustración editorial, mapas/mundos ficticios e identidad gráfica para sagas. **Contar cuatro tarjetas y cotejar sus textos con `spec.md` antes de continuar.**

17. [ ] **Completar Portafolio (`#portafolio`).** Añadir introducción y las seis obras indicadas, cada una con título, categoría, descripción, imagen y estructura `figure`/`figcaption` cuando corresponda. Identificarlas visiblemente como conceptos/proyectos imaginarios. **Verificar que hay exactamente seis fichas y que ninguna se presenta como encargo real antes de continuar.**

18. [ ] **Completar Colecciones (`#colecciones`).** Añadir introducción y tres colecciones, cada una con título, descripción e imagen representativa. **Verificar número y contenido de las tres colecciones antes de continuar.**

19. [ ] **Completar Proceso creativo (`#proceso`).** Añadir introducción y los cinco pasos en una lista ordenada: Descubrir, Investigar, Imaginar, Crear y Perfeccionar. **Verificar orden, numeración y texto completo antes de continuar.**

20. [ ] **Completar Anatomía de una portada (`#anatomia-portada`).** Añadir introducción, los cuatro componentes (Composición, Tipografía, Color y Simbolismo) con sus descripciones y una imagen conceptual grande. **Verificar los cuatro componentes y la alternativa de imagen antes de continuar.**

21. [ ] **Completar Trayectoria (`#trayectoria`).** Añadir los tres párrafos y las etapas Los orígenes, La búsqueda y El presente. No añadir años ni fechas. **Verificar que las tres etapas están presentes y no hay credenciales o hitos inventados antes de continuar.**

22. [ ] **Completar Colaboraciones (`#colaboraciones`).** Añadir ambos textos, identificar a escritores, editoriales independientes, creadores de sagas y proyectos de fantasía/ciencia ficción, e incluir «Cuéntame tu proyecto» enlazado a `#contacto`. **Verificar destinatarios y destino del CTA antes de continuar.**

23. [ ] **Completar Próximas presentaciones (`#presentaciones`).** Añadir el texto y tres tarjetas: Exposiciones de ilustración, Encuentros con escritores y Ferias y eventos editoriales. Señalar cada una como pendiente de confirmación con los estados especificados. **Verificar que no aparecen fechas, lugares ni actividades presentadas como confirmadas antes de continuar.**

24. [ ] **Completar Preguntas frecuentes (`#preguntas-frecuentes`).** Añadir las cinco preguntas y respuestas dentro de `details`/`summary`, sin JavaScript. **Verificar las cinco respuestas y confirmar que cada pregunta puede desplegarse mediante HTML nativo antes de continuar.**

25. [ ] **Completar Contacto (`#contacto`).** Añadir título, los dos textos, enlace `mailto:contacto@ejemplo.com` con nombre «Enviar un correo», espacios para Behance, ArtStation e Instagram sin perfiles inventados y la frase final. **Verificar el enlace provisional y que no existen URLs sociales fabricadas antes de continuar.**

26. [ ] **Completar el pie de página.** Añadir «Damián Vesper», «Ilustración editorial para mundos extraordinarios», enlaces internos principales válidos, aviso de derechos de autor editable y enlace de retorno a `#inicio`. **Verificar los destinos y que no se haya inventado titularidad o año antes de continuar.**

### Imágenes, semántica y Microdata

27. [ ] **Revisar todas las referencias de imagen.** Confirmar que las rutas están bajo `images/` y tienen nombres descriptivos. Incluir las referencias requeridas para hero, retrato, mundos visuales, obras, colecciones y portada conceptual. No crear recursos gráficos. **Contar y revisar las referencias con respecto a la especificación antes de continuar.**

28. [ ] **Verificar atributos `alt`.** Dar texto alternativo descriptivo a imágenes informativas y `alt=""` a las puramente decorativas. Evitar describir recursos pendientes como si ya fueran hechos o imágenes reales. **Comprobar una por una todas las etiquetas `img`; no avanzar con ninguna sin `alt`.**

29. [ ] **Añadir Microdata `Person`.** Marcar el contenido del artista con `itemscope` y `itemtype="https://schema.org/Person"`; usar solo nombre y ocupación conocidos, con `itemprop` coherentes. **Verificar sintaxis y datos antes de continuar.**

30. [ ] **Añadir Microdata `CreativeWork` al portafolio.** Marcar cada uno de los seis proyectos con `itemscope` y `itemtype="https://schema.org/CreativeWork"`, usando únicamente nombre, descripción e imagen visibles o confirmados. **Verificar que hay seis obras marcadas y que no se incluyen propiedades inventadas antes de continuar.**

31. [ ] **Revisar uso de elementos semánticos y ARIA.** Confirmar uso apropiado de `header`, `nav`, `main`, `section`, `article`, `figure`, `figcaption`, listas, `details`, `summary` y `footer`. Añadir ARIA solo si la semántica nativa no basta. **Eliminar roles y etiquetas redundantes y revisar el orden de lectura antes de continuar.**

### Validación final

32. [ ] **Validar todos los enlaces y fragmentos.** Comprobar cada `href` interno contra un ID existente, incluidos navegación, CTAs, footer y enlace de salto; revisar también el `mailto:`. **Corregir enlaces rotos o fragmentos inexistentes antes de continuar.**

33. [ ] **Revisar integridad y veracidad del contenido.** Comparar las 14 secciones con `spec.md`; buscar fechas, lugares, clientes, premios, testimonios, credenciales, perfiles y afirmaciones no autorizadas. **No avanzar hasta asegurar que todo está suministrado o marcado como pendiente/ficticio.**

34. [ ] **Revisar restricciones tecnológicas y archivos modificados.** Confirmar que no hay JavaScript, CSS inline/embebido, frameworks, librerías, dependencias ni archivos adicionales de implementación; `styles.css` debe estar solo referenciado. **Revisar la lista de archivos modificados y corregir cualquier desviación antes de continuar.**

35. [ ] **Realizar revisión final de calidad.** Revisar indentación, etiquetas correctamente anidadas, idioma, título, descripción, jerarquía de encabezados, IDs únicos, metadatos, Microdata, imágenes, FAQ y enlaces. Si hay errores, volver a la tarea pertinente, corregirla y repetir sus verificaciones y las afectadas. **Marcar esta tarea solo cuando todas las comprobaciones hayan pasado.**

36. [ ] **Cerrar la fase HTML.** Confirmar que `index.html` está completo según los criterios de aceptación de `spec.md`, que no queda contenido requerido pendiente y que esta fase no generó CSS. No empezar la fase CSS hasta recibir autorización explícita y dar por cerrada la implementación HTML. **Verificar y dejar registrado el estado final antes de concluir.**
