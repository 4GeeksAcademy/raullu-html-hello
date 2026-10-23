# BRIEFING DEL PROYECTO — LANDING PAGE DE DAMIÁN VESPER

## Propósito y uso de este documento

Este briefing es la referencia permanente del proyecto para su contenido, estructura, identidad visual y forma de implementación. Debe consultarse antes de iniciar cualquier desarrollo o escribir código. Los requisitos concretos de una fase se detallarán en su especificación correspondiente (`spec.md`), que deberá respetar y no contradecir este briefing sin aprobación explícita.

## Contexto del proyecto

Crear una landing page profesional para **Damián Vesper**, diseñador gráfico e ilustrador especializado en portadas e ilustraciones de novelas victorianas postapocalípticas, Steampunk industrial y Gótico Neo-Victoriano.

El nombre del artista y todos los proyectos son ficticios y editables. No inventar premios, clientes reales, exposiciones celebradas ni experiencia profesional verificable. Tampoco inventar datos biográficos, fechas, lugares, tarifas, testimonios, perfiles sociales o credenciales que no se hayan proporcionado expresamente.

## Proceso de desarrollo obligatorio: trabajo por especificaciones

El desarrollo se organiza por fases y mediante documentos de especificación. Para cada desarrollo, seguir este flujo en orden y no avanzar hasta que el documento de la etapa actual haya sido revisado y aprobado:

1. **`spec.md`:** elaborar primero la especificación del desarrollo solicitado, usando este briefing y el contexto del repositorio. No implementar código durante esta etapa.
2. **Aprobación de la especificación:** esperar aprobación explícita de `spec.md`. Si se solicitan cambios, actualizar la especificación y volver a solicitar aprobación.
3. **`plan.md`:** una vez aprobada la especificación, preparar un plan de implementación ordenado, detallado y verificable.
4. **Aprobación del plan:** no crear la lista de tareas hasta recibir aprobación explícita de `plan.md`. Incorporar y volver a someter a aprobación cualquier corrección solicitada.
5. **`tasks.md`:** una vez aprobado el plan, crear tareas numeradas, ordenadas, con casillas `[ ]` y verificaciones que deben superarse antes de avanzar a la siguiente.
6. **Aprobación de las tareas:** no empezar la implementación hasta recibir aprobación explícita de `tasks.md`.
7. **Implementación:** solo después de aprobar `spec.md`, `plan.md` y `tasks.md`, y de recibir autorización para implementar, ejecutar las tareas estrictamente en orden. Marcar `[x]` únicamente las tareas que se hayan completado y verificado.

Si una solicitud pide saltarse una etapa, aclarar el conflicto antes de continuar. La implementación debe limitarse a la fase y los archivos autorizados por la especificación aprobada.

## Tecnologías y fases del sitio

- Utilizar exclusivamente **HTML5 y CSS3**.
- JavaScript, frameworks, librerías, preprocesadores, dependencias y tecnologías adicionales están prohibidos.
- La fase HTML debe preceder a la fase CSS: primero estructura, contenido, accesibilidad y SEO en `index.html`; después diseño visual en `styles.css`.
- No modificar archivos de fases anteriores salvo que sea estrictamente necesario, esté justificado y se autorice.
- No cargar recursos externos ni introducir dependencias si la especificación aprobada no lo autoriza explícitamente.

## Contenido y estructura de la landing page

La página contiene 14 secciones principales, en el orden indicado. Cada sección tendrá un identificador único para navegación interna.

### 1. INICIO — Hero (`#inicio`)

- **Título principal:** «Ilustrando los mundos que sobrevivieron al fin.»
- **Subtítulo:** «Donde la elegancia victoriana se encuentra con las ruinas del mañana.»
- **Descripción:** «Soy Damián Vesper. Transformo historias en universos visuales, creando portadas e ilustraciones para novelas que habitan entre el vapor, el óxido y la oscuridad.»
- **Botones:** «Explorar mis obras» y «Hablemos de tu historia».
- Espacio para una ilustración principal de una ciudad victoriana postapocalíptica.

### 2. MANIFIESTO — El arte después del colapso (`#manifiesto`)

- **Título:** «La belleza también habita entre las ruinas.»
- **Texto:** «Creo en las historias que no temen explorar la oscuridad. En las ciudades que conservan su grandeza bajo toneladas de ceniza. En las máquinas que siguen respirando cuando la humanidad parece haber olvidado cómo hacerlo.»
- **Texto:** «Mi trabajo nace de una obsesión: dar forma a lo imposible. Cada trazo, cada textura y cada sombra buscan abrir una puerta hacia mundos que todavía no existen, pero que merecen ser descubiertos.»
- **Frase destacada:** «No dibujo el fin del mundo. Ilustro lo que viene después.»

### 3. SOBRE MÍ — El creador detrás de las sombras (`#sobre-mi`)

- **Título:** «Detrás de cada ruina hay una historia.»
- **Texto:** «Soy Damián Vesper, diseñador gráfico e ilustrador especializado en la creación de universos visuales para literatura fantástica, distópica y de ciencia ficción.»
- **Texto:** «Mi lenguaje artístico combina la elegancia ornamental de la época victoriana, la crudeza de la maquinaria industrial y la fuerza expresiva del arte urbano contemporáneo.»
- **Texto:** «Entiendo cada portada como una promesa al lector: una pequeña ventana hacia el universo que descubrirá al abrir el libro.»
- **Frase:** «Mi objetivo no es decorar historias, sino darles una identidad visual inolvidable.»
- Espacio para retrato o ilustración representativa del artista.

### 4. MI UNIVERSO VISUAL — Tres mundos, una identidad (`#universo-visual`)

- **Título:** «Entre el vapor, la ceniza y el asfalto.»
- **Gótico Neo-Victoriano:** «Catedrales imposibles, filigranas, arquitectura monumental y una elegancia oscura que parece resistirse al paso del tiempo.»
- **Steampunk industrial:** «Engranajes, calderas, maquinaria de vapor y mecanismos de supervivencia que cuentan historias de civilizaciones reconstruidas.»
- **Distopía urbana:** «Ciudades cubiertas de grafitis, calles abandonadas, propaganda desgastada y destellos de neón entre las sombras.»
- Cada bloque tendrá imagen, título y descripción.

### 5. ESPECIALIDADES — Lo que puedo crear (`#especialidades`)

- **Título:** «Cada historia merece su propio universo.»
- **Portadas de novelas:** «Cubiertas que condensan la esencia de una historia y despiertan la curiosidad antes de abrir el libro.»
- **Ilustración editorial:** «Escenas, personajes y escenarios que acompañan la lectura y enriquecen la experiencia narrativa.»
- **Mapas y mundos ficticios:** «Cartografías, ciudades y territorios imaginarios que dan coherencia visual a universos literarios.»
- **Identidad gráfica para sagas:** «Sistemas visuales consistentes que conectan portadas, símbolos, títulos y elementos promocionales.»

### 6. PORTAFOLIO — Obras del otro mundo (`#portafolio`)

- **Título:** «Fragmentos de universos que nunca existieron.»
- **Introducción:** «Cada ilustración es una historia detenida en el tiempo. Explora una selección de conceptos artísticos y proyectos editoriales imaginarios.»
- Incluir seis proyectos de ejemplo. Cada uno tendrá imagen, título, categoría y descripción; utilizar `figure`, `img` y `figcaption` cuando corresponda.
	1. **Las Cenizas de Londres** — Portada de novela distópica. «Una metrópolis victoriana donde las chimeneas nunca dejaron de arder.»
	2. **El Corazón de Hierro** — Ilustración steampunk. «La última máquina capaz de mantener con vida una ciudad olvidada.»
	3. **Crónicas del Último Imperio** — Diseño editorial. «El esplendor de una civilización que se niega a desaparecer.»
	4. **La Ciudad Sin Amanecer** — Concept art urbano. «Calles inundadas de neón, humo y secretos bajo una noche interminable.»
	5. **Los Hijos del Vapor** — Portada de ciencia ficción. «Supervivientes de un mundo gobernado por engranajes y acero.»
	6. **El Jardín de las Máquinas Muertas** — Ilustración gótica. «La naturaleza recupera lentamente los restos de una civilización mecánica.»
- Identificar claramente las obras como ficticias/conceptuales; no presentarlas como encargos reales.

### 7. COLECCIONES Y UNIVERSOS (`#colecciones`)

- **Título:** «Archivos de mundos perdidos.»
- **Introducción:** «Algunas ideas no caben en una sola ilustración. Estas colecciones exploran mundos imaginarios a través de diferentes piezas visuales.»
- **Archivo I: La Era del Óxido:** «Máquinas monumentales, fábricas abandonadas y los últimos vestigios de la revolución industrial.»
- **Archivo II: Ciudades de Ceniza:** «Arquitectura gótica, decadencia urbana y ciudades que siguen respirando bajo cielos contaminados.»
- **Archivo III: El Nuevo Imperio:** «Una sociedad que ha reconstruido su identidad entre reliquias victorianas y tecnologías imposibles.»
- Cada colección tendrá una imagen representativa.

### 8. PROCESO CREATIVO (`#proceso`)

- **Título:** «Del manuscrito a la última pincelada.»
- **Introducción:** «Cada proyecto comienza escuchando una historia. Mi proceso busca encontrar la imagen capaz de representar su esencia.»
- Representar los cinco pasos mediante una lista ordenada:
	1. **Descubrir:** «Conocer la historia, su atmósfera, personajes y público lector.»
	2. **Investigar:** «Construir referencias visuales, paletas cromáticas y elementos narrativos.»
	3. **Imaginar:** «Explorar composiciones y desarrollar los primeros bocetos.»
	4. **Crear:** «Convertir el concepto en una ilustración detallada y coherente.»
	5. **Perfeccionar:** «Revisar los últimos detalles y preparar la obra para su aplicación editorial.»

### 9. ANATOMÍA DE UNA PORTADA (`#anatomia-portada`)

- **Título:** «Nada está dibujado por casualidad.»
- **Introducción:** «Una buena portada es mucho más que una imagen atractiva. Cada elemento debe contribuir a contar una historia.»
- **Composición:** «Guiar la mirada hacia el conflicto central.»
- **Tipografía:** «Encontrar letras que pertenezcan al universo narrativo.»
- **Color:** «Transmitir emociones mediante bronces, negros, ocres y luces artificiales.»
- **Simbolismo:** «Ocultar pequeños significados que el lector descubrirá al avanzar en la novela.»
- Incluir una imagen grande de una portada conceptual.

### 10. TRAYECTORIA — La evolución de una mirada (`#trayectoria`)

- **Título:** «Un camino construido a base de tinta y óxido.»
- **Texto:** «Mi recorrido artístico nace de la fascinación por los libros ilustrados, la arquitectura histórica, el diseño editorial y los universos de ficción.»
- **Texto:** «Con el tiempo, estos intereses se han combinado hasta dar forma a un lenguaje propio, donde conviven la ornamentación victoriana y la estética de las ciudades industriales abandonadas.»
- **Texto:** «Actualmente, mi trabajo se centra en explorar la narrativa visual y en desarrollar proyectos de ilustración aplicados a la literatura fantástica.»
- Organizar el contenido en tres etapas sin inventar años:
	- **Los orígenes:** exploración del dibujo, la literatura y las referencias visuales.
	- **La búsqueda:** experimentación con técnicas, composición y estilos gráficos.
	- **El presente:** desarrollo de una identidad artística enfocada en la ilustración editorial.

### 11. COLABORACIONES Y ENCARGOS (`#colaboraciones`)

- **Título:** «Tu historia. Mi próxima obsesión.»
- **Texto:** «¿Estás escribiendo una novela y buscas una identidad visual que esté a la altura de su universo?»
- **Texto:** «Trabajo propuestas gráficas para autores independientes, proyectos editoriales y creadores que desean transformar sus ideas en imágenes memorables.»
- Destinatarios: escritores, editoriales independientes, creadores de sagas y proyectos de fantasía o ciencia ficción.
- Llamada a la acción: «Cuéntame tu proyecto».

### 12. PRÓXIMAS PRESENTACIONES (`#presentaciones`)

- **Título:** «Encuentros más allá del papel.»
- **Texto:** «El arte también merece salir de las páginas. Este espacio reunirá futuras exposiciones, encuentros literarios, ferias y actividades relacionadas con la ilustración.»
- Tres tarjetas de eventos de ejemplo, claramente pendientes de confirmar:
	- **Exposiciones de ilustración** — Fecha y lugar por confirmar.
	- **Encuentros con escritores** — Próximamente.
	- **Ferias y eventos editoriales** — Programación pendiente.
- No inventar fechas, lugares ni eventos confirmados.

### 13. PREGUNTAS FRECUENTES (`#preguntas-frecuentes`)

- **Título:** «Antes de abrir el siguiente capítulo.»
- Implementar preguntas desplegables con los elementos HTML `details` y `summary`, sin JavaScript.
- **¿Realizas portadas para autores independientes?** — «Sí. Cada propuesta se plantea según las necesidades narrativas y editoriales del proyecto.»
- **¿Puedes adaptar tu estilo a otras temáticas?** — «Mi especialidad es la estética victoriana postapocalíptica, aunque puedo explorar enfoques relacionados con la fantasía oscura y la ciencia ficción.»
- **¿Cómo empieza un encargo?** — «Todo comienza con una conversación sobre la historia, sus referencias y los objetivos visuales.»
- **¿Entregas archivos preparados para impresión?** — «Los formatos y requisitos de entrega se definirán según las necesidades de cada proyecto.»
- **¿Cuánto tarda una ilustración?** — «Los plazos dependen de la complejidad, el alcance y las revisiones acordadas.»

### 14. CONTACTO — Escribamos el próximo mundo (`#contacto`)

- **Título:** «Toda gran historia comienza con una idea.»
- **Texto:** «Puede que tu próximo universo todavía exista únicamente entre las páginas de un manuscrito. Hagamos que cobre vida.»
- **Texto:** «Si tienes una novela, una saga o un proyecto creativo entre manos, estaré encantado de conocerlo.»
- Botón: «Enviar un correo».
- Añadir enlace `mailto:` con el correo provisional `contacto@ejemplo.com`.
- Reservar espacios para enlaces a Behance, ArtStation e Instagram, sin inventar perfiles reales.
- **Frase final:** «El mundo puede terminar. Las historias, jamás.»

## Pie de página

Incluir:

- Nombre artístico: Damián Vesper.
- Frase: «Ilustración editorial para mundos extraordinarios.»
- Enlaces internos principales.
- Aviso de derechos de autor editable.
- Enlace para volver al inicio.

## Requisitos técnicos y de calidad

### HTML

- Utilizar `<!DOCTYPE html>`, `<html lang="es">`, `<head>` y `<body>`.
- Incluir `meta charset`, `viewport`, `title` y `meta description` optimizada para SEO.
- Usar correctamente `header`, `nav`, `main`, `section`, `article`, `aside` cuando tenga sentido y `footer`.
- Utilizar un único `h1` y una jerarquía lógica de `h2`, `h3`, etc.
- Cada sección debe tener su propio `id` para navegación interna.
- Navegación principal: Inicio, Sobre mí, Especialidades, Portafolio, Trayectoria, Presentaciones y Contacto. Los demás apartados serán accesibles mediante desplazamiento y enlaces contextuales.
- Incorporar un enlace para saltar directamente al contenido principal.
- Usar atributos `alt` descriptivos en imágenes informativas y `alt=""` en imágenes puramente decorativas.
- Añadir `aria-label` únicamente cuando sea necesario para mejorar la accesibilidad.
- Implementar Schema.org mediante Microdata HTML: `Person` para el artista y `CreativeWork` para las obras. No usar JSON-LD.
- Utilizar listas, figuras, enlaces y demás elementos semánticos adecuados.
- Referenciar imágenes bajo una carpeta `images/` con nombres descriptivos; no es necesario crear los archivos de imagen de antemano. Si se solicitan imágenes provisionales, deben identificarse claramente como imágenes de prueba.
- Incluir clases CSS descriptivas para facilitar la fase visual.
- Vincular `styles.css`; no crear ni escribir estilos en la fase HTML.
- Preparar una estructura para que posteriormente las secciones puedan aproximarse al alto de pantalla, sin exigir alturas rígidas ni recortar contenido.
- No utilizar CSS inline, JavaScript, frameworks ni librerías.

### Diseño visual futuro

- La estética general es oscura, elegante, cinematográfica e industrial, con referencias victorianas postapocalípticas, Steampunk, Gótico Neo-Victoriano y arte urbano distópico.
- Paleta sugerida para la fase CSS: negro carbón, bronce envejecido, ocres, óxido y detalles limitados de verde neón.
- Usar tipografía serif ornamental/editorial para títulos y sans-serif industrial para cuerpo, siempre con recursos locales/de sistema y contraste adecuado.
- El hero debe ser inmersivo; las galerías y tarjetas deben ser responsive.
- Usar Flexbox, Grid y media queries cuando se implemente CSS; los efectos hover, animaciones y transiciones deben ser sutiles y solo CSS.
- Garantizar legibilidad, navegación por teclado, `:focus-visible`, contraste suficiente y respeto a `prefers-reduced-motion`.
- Cada sección puede aproximarse a `100vh` mediante altura mínima, pero debe poder crecer con el contenido.

## Reglas permanentes de contenido y veracidad

- El proyecto, el artista y sus obras son ficticios y editables; no presentarlos como información profesional verificable.
- No inventar premios, clientes reales, exposiciones celebradas, años, lugares, experiencia, datos de contacto ni perfiles sociales.
- No presentar las tarjetas de presentaciones como actividades confirmadas.
- Usar marcadores claros para datos pendientes y pedir confirmación cuando sea necesario.
- Priorizar accesibilidad, estructura semántica, mantenibilidad, legibilidad y ampliación sencilla sobre adornos visuales.
- Antes de cada implementación, consultar este briefing y los documentos aprobados de la fase correspondiente. Si hay contradicción entre una solicitud nueva y este briefing, aclararla antes de modificar código.
