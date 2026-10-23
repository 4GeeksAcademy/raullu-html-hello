# Especificación: Landing page de Damián Vesper

- **Identificador:** 001-HTML
- **Fase:** Especificación de la fase HTML
- **Estado:** Lista para implementar
- **Idioma del sitio:** Español (`es`)

## 1. Objetivo

Definir una landing page profesional, accesible y semántica para **Damián Vesper**, diseñador gráfico e ilustrador ficticio especializado en portadas e ilustraciones de novelas victorianas postapocalípticas, Steampunk industrial y Gótico Neo-Victoriano. El sitio debe presentar su universo visual, servicios, obras conceptuales y vías de contacto, y quedar preparado para una segunda fase de diseño visual.

El nombre, la biografía y los proyectos presentados son ficticios y editables. No se afirmará que las obras son encargos reales ni se inventarán premios, clientes reales, exposiciones celebradas, fechas, lugares o experiencia profesional verificable. Los eventos se mostrarán explícitamente como pendientes de confirmación.

## 2. Alcance y fases

### Fase actual: HTML

- Crear exclusivamente `index.html`.
- Implementar estructura, textos, navegación, semántica, accesibilidad, metadatos SEO y datos estructurados Microdata.
- Referenciar un futuro `styles.css` desde el documento, sin crear ni incluir estilos en esta fase.
- Referenciar imágenes futuras en `images/` con nombres descriptivos; no es necesario crear los archivos de imagen.

### Fase posterior: CSS

- `styles.css` se implementará únicamente cuando comience la fase visual.
- La presentación futura tendrá una estética oscura, industrial, victoriana, Steampunk y Gótico Neo-Victoriana, con diseño responsive.

### Fuera de alcance

- JavaScript, frameworks, bibliotecas, CSS inline, estilos embebidos, dependencias externas y cualquier tecnología distinta de HTML5 en esta fase.
- Crear imágenes o añadir perfiles sociales reales.
- Inventar o confirmar datos profesionales, eventos, clientes, premios o credenciales.

## 3. Usuarios y necesidades

La página está dirigida principalmente a escritores, editoriales independientes, creadores de sagas y personas que desarrollan proyectos de fantasía o ciencia ficción. Debe permitirles:

- Comprender rápidamente la identidad artística y las especialidades.
- Explorar obras, colecciones y proceso creativo.
- Conocer el enfoque de colaboración y consultar preguntas frecuentes.
- Encontrar fácilmente la información de contacto y los enlaces sociales cuando se proporcionen perfiles reales.

## 4. Requisitos globales de documento

1. El documento debe ser HTML5 válido e incluir `<!DOCTYPE html>`, `<html lang="es">`, `<head>` y `<body>`.
2. El `<head>` debe incluir `meta charset`, `meta name="viewport"`, un `<title>` descriptivo, una `meta description` optimizada para SEO y un enlace al futuro `styles.css`.
3. El HTML debe estar correctamente indentado, ser legible y utilizar clases CSS descriptivas que permitan implementar el diseño en la fase posterior.
4. Debe existir un único `h1`. Los títulos de sección usarán `h2` y los títulos internos una jerarquía descendente lógica, sin saltos injustificados.
5. Cada sección principal tendrá un `id` único y estable para habilitar navegación interna.
6. Se usarán elementos semánticos adecuados, incluyendo `header`, `nav`, `main`, `section`, `article` y `footer`; `aside` se utilizará solo cuando su contenido sea complementario y no imprescindible para el flujo principal.
7. La página ofrecerá un enlace para saltar al contenido principal, visible al recibir foco de teclado en la futura presentación.
8. El contenido y los enlaces deben ser comprensibles y utilizables con teclado, sin depender de interacciones JavaScript.
9. Cada referencia a imágenes utilizará rutas organizadas bajo `images/` y nombres descriptivos. Las imágenes informativas tendrán `alt` descriptivo; las puramente decorativas tendrán `alt=""`.
10. Los atributos ARIA se añadirán únicamente cuando el HTML nativo no proporcione ya la semántica o el nombre accesible necesarios.
11. Se incluirá Microdata de Schema.org: `Person` para el artista y `CreativeWork` para las obras. No se utilizará JSON-LD.
12. No se incluirá información no proporcionada. Si se requieren enlaces de redes sociales, serán marcadores identificables o enlaces pendientes, nunca perfiles inventados.
13. La estructura debe permitir que cada sección se aproxime a una altura de pantalla en la futura fase CSS, pero el contenido debe poder crecer sin recortes.

## 5. Arquitectura y navegación

El documento incluirá encabezado con navegación principal, un `main` con las 14 secciones descritas a continuación y un pie de página.

La navegación principal debe incluir estos enlaces, en este orden:

- Inicio → `#inicio`
- Sobre mí → `#sobre-mi`
- Especialidades → `#especialidades`
- Portafolio → `#portafolio`
- Trayectoria → `#trayectoria`
- Presentaciones → `#presentaciones`
- Contacto → `#contacto`

Los apartados no incluidos en el menú principal deberán seguir siendo accesibles mediante desplazamiento, navegación contextual o enlaces internos pertinentes. Los destinos de todos los enlaces internos deben existir.

## 6. Contenido requerido por sección

### 6.1 Inicio — Hero (`#inicio`)

- Un único título principal (`h1`): **«Ilustrando los mundos que sobrevivieron al fin.»**
- Subtítulo: **«Donde la elegancia victoriana se encuentra con las ruinas del mañana.»**
- Descripción: **«Soy Damián Vesper. Transformo historias en universos visuales, creando portadas e ilustraciones para novelas que habitan entre el vapor, el óxido y la oscuridad.»**
- Enlaces de acción: **«Explorar mis obras»** hacia `#portafolio` y **«Hablemos de tu historia»** hacia `#contacto`.
- Espacio para una ilustración principal de una ciudad victoriana postapocalíptica, con alternativa textual adecuada.

### 6.2 Manifiesto — El arte después del colapso (`#manifiesto`)

- Título: **«La belleza también habita entre las ruinas.»**
- Texto: **«Creo en las historias que no temen explorar la oscuridad. En las ciudades que conservan su grandeza bajo toneladas de ceniza. En las máquinas que siguen respirando cuando la humanidad parece haber olvidado cómo hacerlo.»**
- Texto: **«Mi trabajo nace de una obsesión: dar forma a lo imposible. Cada trazo, cada textura y cada sombra buscan abrir una puerta hacia mundos que todavía no existen, pero que merecen ser descubiertos.»**
- Frase destacada: **«No dibujo el fin del mundo. Ilustro lo que viene después.»**

### 6.3 Sobre mí — El creador detrás de las sombras (`#sobre-mi`)

- Título: **«Detrás de cada ruina hay una historia.»**
- Texto: **«Soy Damián Vesper, diseñador gráfico e ilustrador especializado en la creación de universos visuales para literatura fantástica, distópica y de ciencia ficción.»**
- Texto: **«Mi lenguaje artístico combina la elegancia ornamental de la época victoriana, la crudeza de la maquinaria industrial y la fuerza expresiva del arte urbano contemporáneo.»**
- Texto: **«Entiendo cada portada como una promesa al lector: una pequeña ventana hacia el universo que descubrirá al abrir el libro.»**
- Frase: **«Mi objetivo no es decorar historias, sino darles una identidad visual inolvidable.»**
- Espacio para un retrato o ilustración representativa del artista, con `alt` apropiado.
- Incluir Microdata `Person` asociada al nombre y a la ocupación proporcionada. No agregar propiedades biográficas desconocidas.

### 6.4 Mi universo visual — Tres mundos, una identidad (`#universo-visual`)

- Título: **«Entre el vapor, la ceniza y el asfalto.»**
- Tres bloques temáticos, cada uno con imagen, título y descripción:
  1. **Gótico Neo-Victoriano:** «Catedrales imposibles, filigranas, arquitectura monumental y una elegancia oscura que parece resistirse al paso del tiempo.»
  2. **Steampunk industrial:** «Engranajes, calderas, maquinaria de vapor y mecanismos de supervivencia que cuentan historias de civilizaciones reconstruidas.»
  3. **Distopía urbana:** «Ciudades cubiertas de grafitis, calles abandonadas, propaganda desgastada y destellos de neón entre las sombras.»

### 6.5 Especialidades — Lo que puedo crear (`#especialidades`)

- Título: **«Cada historia merece su propio universo.»**
- Cuatro tarjetas semánticas, cada una con encabezado y descripción:
  1. **Portadas de novelas:** «Cubiertas que condensan la esencia de una historia y despiertan la curiosidad antes de abrir el libro.»
  2. **Ilustración editorial:** «Escenas, personajes y escenarios que acompañan la lectura y enriquecen la experiencia narrativa.»
  3. **Mapas y mundos ficticios:** «Cartografías, ciudades y territorios imaginarios que dan coherencia visual a universos literarios.»
  4. **Identidad gráfica para sagas:** «Sistemas visuales consistentes que conectan portadas, símbolos, títulos y elementos promocionales.»

### 6.6 Portafolio — Obras del otro mundo (`#portafolio`)

- Título: **«Fragmentos de universos que nunca existieron.»**
- Introducción: **«Cada ilustración es una historia detenida en el tiempo. Explora una selección de conceptos artísticos y proyectos editoriales imaginarios.»**
- Incluir seis proyectos ficticios. Cada uno tendrá imagen, título, categoría y descripción, usando `figure`, `img` y `figcaption` cuando corresponda:
  1. **Las Cenizas de Londres** — Portada de novela distópica. «Una metrópolis victoriana donde las chimeneas nunca dejaron de arder.»
  2. **El Corazón de Hierro** — Ilustración steampunk. «La última máquina capaz de mantener con vida una ciudad olvidada.»
  3. **Crónicas del Último Imperio** — Diseño editorial. «El esplendor de una civilización que se niega a desaparecer.»
  4. **La Ciudad Sin Amanecer** — Concept art urbano. «Calles inundadas de neón, humo y secretos bajo una noche interminable.»
  5. **Los Hijos del Vapor** — Portada de ciencia ficción. «Supervivientes de un mundo gobernado por engranajes y acero.»
  6. **El Jardín de las Máquinas Muertas** — Ilustración gótica. «La naturaleza recupera lentamente los restos de una civilización mecánica.»
- Marcar cada obra como concepto o proyecto imaginario, sin insinuar que es un encargo real.
- Incluir Microdata `CreativeWork` para las obras y utilizar únicamente propiedades respaldadas por el contenido presente.

### 6.7 Colecciones y universos (`#colecciones`)

- Título: **«Archivos de mundos perdidos.»**
- Introducción: **«Algunas ideas no caben en una sola ilustración. Estas colecciones exploran mundos imaginarios a través de diferentes piezas visuales.»**
- Tres colecciones, cada una con imagen representativa, título y descripción:
  1. **Archivo I: La Era del Óxido** — «Máquinas monumentales, fábricas abandonadas y los últimos vestigios de la revolución industrial.»
  2. **Archivo II: Ciudades de Ceniza** — «Arquitectura gótica, decadencia urbana y ciudades que siguen respirando bajo cielos contaminados.»
  3. **Archivo III: El Nuevo Imperio** — «Una sociedad que ha reconstruido su identidad entre reliquias victorianas y tecnologías imposibles.»

### 6.8 Proceso creativo (`#proceso`)

- Título: **«Del manuscrito a la última pincelada.»**
- Introducción: **«Cada proyecto comienza escuchando una historia. Mi proceso busca encontrar la imagen capaz de representar su esencia.»**
- Representar los cinco pasos en una lista ordenada:
  1. **Descubrir:** «Conocer la historia, su atmósfera, personajes y público lector.»
  2. **Investigar:** «Construir referencias visuales, paletas cromáticas y elementos narrativos.»
  3. **Imaginar:** «Explorar composiciones y desarrollar los primeros bocetos.»
  4. **Crear:** «Convertir el concepto en una ilustración detallada y coherente.»
  5. **Perfeccionar:** «Revisar los últimos detalles y preparar la obra para su aplicación editorial.»

### 6.9 Anatomía de una portada (`#anatomia-portada`)

- Título: **«Nada está dibujado por casualidad.»**
- Introducción: **«Una buena portada es mucho más que una imagen atractiva. Cada elemento debe contribuir a contar una historia.»**
- Destacar cuatro componentes:
  - **Composición:** «Guiar la mirada hacia el conflicto central.»
  - **Tipografía:** «Encontrar letras que pertenezcan al universo narrativo.»
  - **Color:** «Transmitir emociones mediante bronces, negros, ocres y luces artificiales.»
  - **Simbolismo:** «Ocultar pequeños significados que el lector descubrirá al avanzar en la novela.»
- Incluir una imagen grande de portada conceptual con texto alternativo descriptivo.

### 6.10 Trayectoria — La evolución de una mirada (`#trayectoria`)

- Título: **«Un camino construido a base de tinta y óxido.»**
- Texto: **«Mi recorrido artístico nace de la fascinación por los libros ilustrados, la arquitectura histórica, el diseño editorial y los universos de ficción.»**
- Texto: **«Con el tiempo, estos intereses se han combinado hasta dar forma a un lenguaje propio, donde conviven la ornamentación victoriana y la estética de las ciudades industriales abandonadas.»**
- Texto: **«Actualmente, mi trabajo se centra en explorar la narrativa visual y en desarrollar proyectos de ilustración aplicados a la literatura fantástica.»**
- Organizar el contenido en tres etapas, sin años ni fechas:
  - **Los orígenes:** exploración del dibujo, la literatura y las referencias visuales.
  - **La búsqueda:** experimentación con técnicas, composición y estilos gráficos.
  - **El presente:** desarrollo de una identidad artística enfocada en la ilustración editorial.

### 6.11 Colaboraciones y encargos (`#colaboraciones`)

- Título: **«Tu historia. Mi próxima obsesión.»**
- Texto: **«¿Estás escribiendo una novela y buscas una identidad visual que esté a la altura de su universo?»**
- Texto: **«Trabajo propuestas gráficas para autores independientes, proyectos editoriales y creadores que desean transformar sus ideas en imágenes memorables.»**
- Indicar como destinatarios: escritores, editoriales independientes, creadores de sagas y proyectos de fantasía o ciencia ficción.
- Llamada a la acción **«Cuéntame tu proyecto»**, enlazada a `#contacto`.

### 6.12 Próximas presentaciones (`#presentaciones`)

- Título: **«Encuentros más allá del papel.»**
- Texto: **«El arte también merece salir de las páginas. Este espacio reunirá futuras exposiciones, encuentros literarios, ferias y actividades relacionadas con la ilustración.»**
- Tres tarjetas de ejemplo, cada una identificada claramente como pendiente de confirmación:
  1. **Exposiciones de ilustración** — «Fecha y lugar por confirmar.»
  2. **Encuentros con escritores** — «Próximamente.»
  3. **Ferias y eventos editoriales** — «Programación pendiente.»
- No presentar ninguna actividad como confirmada ni añadir fechas o lugares.

### 6.13 Preguntas frecuentes (`#preguntas-frecuentes`)

- Título: **«Antes de abrir el siguiente capítulo.»**
- Usar exclusivamente elementos HTML `details` y `summary` para revelar respuestas, sin JavaScript.
- Incluir estas preguntas y respuestas:
  1. **¿Realizas portadas para autores independientes?** — «Sí. Cada propuesta se plantea según las necesidades narrativas y editoriales del proyecto.»
  2. **¿Puedes adaptar tu estilo a otras temáticas?** — «Mi especialidad es la estética victoriana postapocalíptica, aunque puedo explorar enfoques relacionados con la fantasía oscura y la ciencia ficción.»
  3. **¿Cómo empieza un encargo?** — «Todo comienza con una conversación sobre la historia, sus referencias y los objetivos visuales.»
  4. **¿Entregas archivos preparados para impresión?** — «Los formatos y requisitos de entrega se definirán según las necesidades de cada proyecto.»
  5. **¿Cuánto tarda una ilustración?** — «Los plazos dependen de la complejidad, el alcance y las revisiones acordadas.»

### 6.14 Contacto — Escribamos el próximo mundo (`#contacto`)

- Título: **«Toda gran historia comienza con una idea.»**
- Texto: **«Puede que tu próximo universo todavía exista únicamente entre las páginas de un manuscrito. Hagamos que cobre vida.»**
- Texto: **«Si tienes una novela, una saga o un proyecto creativo entre manos, estaré encantado de conocerlo.»**
- Botón/enlace **«Enviar un correo»** con destino `mailto:contacto@ejemplo.com`. El correo es provisional y debe ser fácilmente editable.
- Reservar enlaces para Behance, ArtStation e Instagram sin inventar perfiles reales. Pueden utilizarse marcadores descriptivos no navegables hasta que se proporcionen URLs, siempre con nombres accesibles y sin `href` ficticios.
- Frase final: **«El mundo puede terminar. Las historias, jamás.»**

## 7. Pie de página

El `footer` incluirá:

- Nombre artístico: **Damián Vesper**.
- Frase: **«Ilustración editorial para mundos extraordinarios.»**
- Enlaces internos principales, con destinos válidos.
- Aviso de derechos de autor editable, sin asignar un año o titular no confirmado.
- Enlace para volver al inicio (`#inicio`).

## 8. Requisitos de accesibilidad

- Usar HTML nativo para navegación, listas, enlaces, figuras y controles siempre que sea posible.
- Proporcionar un enlace de salto a `main` al comienzo del contenido.
- Mantener un orden de lectura lógico, jerarquía de encabezados válida y enlaces cuyo propósito se entienda fuera de contexto.
- Todas las imágenes deben tener atributo `alt`; texto descriptivo para contenido informativo y cadena vacía para decoración.
- El contenido de `details` debe ser accesible por teclado a través del comportamiento nativo de `summary`.
- Evitar ARIA redundante. Si se etiqueta una navegación con `aria-label`, debe distinguirse claramente de otras regiones de navegación.
- El diseño de la siguiente fase deberá conservar foco visible, contraste suficiente y legibilidad; la estructura HTML no debe obstaculizarlo.

## 9. SEO y Microdata

- Crear un título de página y descripción únicos, concisos y coherentes con la especialidad de ilustración editorial victoriana, Steampunk y distópica.
- Usar idioma español, metadatos esenciales y contenido semántico rastreable.
- Usar `itemscope`, `itemtype` e `itemprop` para `https://schema.org/Person` y `https://schema.org/CreativeWork` donde corresponda.
- No marcar como hechos estructurados datos no confirmados. Los ejemplos del portafolio deben seguir identificándose como conceptos ficticios dentro del contenido visible.
- No incluir JSON-LD, scripts ni propiedades Schema.org sin base en la información disponible.

## 10. Criterios de aceptación

La implementación HTML se considerará conforme cuando:

1. Exista `index.html` y sea el único archivo de implementación creado en esta fase; `styles.css` solo se referencia y no se crea.
2. El documento use doctype HTML5, idioma `es`, metadatos requeridos y enlace a `styles.css`.
3. Estén presentes las 14 secciones con sus contenidos, títulos e identificadores únicos.
4. La navegación principal incluya exactamente los destinos requeridos y todos los enlaces internos apunten a identificadores existentes.
5. Haya exactamente un `h1` y el resto de encabezados mantenga jerarquía correcta.
6. El hero, las obras y el resto de contenido incluyan los textos especificados sin omisiones sustanciales ni afirmaciones inventadas.
7. Todas las imágenes estén referenciadas bajo `images/`, tengan `alt` apropiado y usen nombres de archivo descriptivos.
8. Las seis obras conceptuales incluyan categoría, descripción y Microdata `CreativeWork`, sin presentarse como trabajos reales.
9. El artista incluya Microdata `Person`, sin propiedades profesionales inventadas.
10. Las preguntas frecuentes utilicen `details` y `summary`, y funcionen sin JavaScript.
11. Los eventos aparezcan como pendientes de confirmación y carezcan de fechas o lugares inventados.
12. El contacto incluya el `mailto:` provisional y no simule perfiles sociales reales.
13. El documento contenga enlace de salto, HTML semántico, atributos ARIA solo cuando sean necesarios y esté preparado para navegación por teclado.
14. No se incluya CSS inline, JavaScript, framework, librería ni archivo fuera del alcance de esta fase.

## 11. Decisiones editables pendientes

Los siguientes datos deben poder sustituirse cuando se disponga de información confirmada:

- Correo provisional `contacto@ejemplo.com`.
- URLs de Behance, ArtStation e Instagram.
- Aviso de derechos de autor y titularidad definitiva.
- Fotografías e ilustraciones reales que sustituyan los espacios de imagen conceptuales.
- Cualquier dato biográfico o profesional adicional que el artista confirme.
