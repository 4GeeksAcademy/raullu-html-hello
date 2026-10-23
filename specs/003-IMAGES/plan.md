# Plan de trabajo: revisión del HTML y selección de imágenes locales

- **Especificación:** [`spec.md`](./spec.md)
- **Identificador:** 003-IMAGES
- **Estado:** pendiente de aprobación
- **Alcance:** selección de hasta 15 imágenes, almacenamiento local, créditos y ajustes de `index.html` relacionados con los recursos.

## 1. Restricciones de ejecución

- No descargar ni incorporar archivos, ni editar `index.html`, hasta que este plan y el posterior `tasks.md` tengan aprobación explícita.
- Consultar durante toda la fase `AGENTS.md`, `BRIEFING.md`, `specs/001-HTML/spec.md` y esta especificación.
- No crear ni editar CSS, JavaScript, scripts auxiliares, dependencias, frameworks ni imágenes generadas que se atribuyan a Damián.
- Mantener la página funcional sin depender de hostings de imágenes remotos: los `src` finales serán rutas locales bajo `images/`.
- Si no se encuentra una imagen adecuada o su licencia no puede verificarse, no adivinar ni usarla. Documentar la falta y proponer un marcador local legítimo/alternativa al usuario en vez de dar la tarea por terminada.

## 2. Entregables previstos

1. `images/`: hasta 15 recursos visuales locales, con nombres descriptivos y extensión según el formato original.
2. `index.html`: actualización de las referencias `placehold.co` a las rutas locales y revisión de `alt`/pies vinculados a esas imágenes. Corregir únicamente defectos confirmados por la especificación 001 que sean necesarios para este alcance.
3. `specs/003-IMAGES/credits.md`: registro verificable de título/descrición, autor, URL de fuente, licencia y URL de licencia por recurso; añadir las atribuciones requeridas de forma visible donde aplique.

No se crearán archivos de código auxiliares o de configuración. El directorio de imágenes solo se creará cuando haya recursos aprobados y verificados para añadir.

## 3. Flujo de trabajo

### Fase A — Auditoría previa del HTML

1. Analizar `index.html` completo, en lugar de depender de una lectura parcial, y cotejar orden, títulos, textos, IDs, enlaces, semántica, Microdata, FAQ e imágenes contra las fuentes aprobadas.
2. Crear una lista interna de hallazgos separando:
   - conformidad actual;
   - defectos confirmados dentro del alcance de la sustitución de imágenes;
   - recomendaciones fuera de alcance que deberán notificarse, no corregirse sin aprobación.
3. Revisar los 15 elementos `<img>` y registrar para cada uno su ubicación, dimensiones declaradas, descripción visual requerida, uso informativo/decorativo, texto alternativo actual y nombre de archivo objetivo.
4. Confirmar si el bloque «Sobre mí» requiere imagen simbólica de herramientas/espacio creativo y evitar por completo presentar a una persona desconocida como Damián.

**Control de salida:** inventario de 15 imágenes y lista precisa de cambios HTML, sin modificaciones todavía.

### Fase B — Búsqueda de recursos y revisión de licencias

1. Buscar imágenes en repositorios con páginas de licencia y atribución verificables, priorizando Wikimedia Commons, Openverse con filtros de licencia y colecciones de dominio público de museos/archivos. Consultar la fuente original de cada elemento, no solo la página de resultados.
2. Confirmar antes de seleccionar:
   - que la imagen puede descargarse y almacenarse;
   - licencia aplicable y permisos para el uso previsto;
   - si se exige atribución, el texto y formato exactos;
   - autoría y URL estable de fuente/licencia;
   - que el contenido coincide con la intención descrita en `spec.md`;
   - que no hay marca de agua, identificadores engañosos o limitaciones incompatibles.
3. Crear una ficha de selección por cada ubicación del inventario. Elegir una imagen distinta cuando facilite representar escenas diferentes; reutilizar un recurso solo si la composición y el sentido lo justifican y no afecta a la calidad narrativa.
4. Para el proyecto ficticio «Las Cenizas de Londres», no presentar el recurso como una obra de Damián ni como fotografía real de Londres salvo que su origen/contexto lo confirme y sea pertinente. Mantener la etiqueta visible de concepto ficticio.
5. Para la imagen principal y la portada, preferir recursos de dimensiones y proporciones apropiadas al uso previsto. No recortar ni modificar archivos sin autorización de la licencia y sin documentar el procedimiento.
6. Registrar candidatos y decisiones en una tabla de créditos provisional. Si una licencia exige atribución visible, determinar una ubicación textual accesible y consistente; reflejarla en `credits.md` y proponer la modificación HTML correspondiente.

**Control de salida:** cada recurso que vaya a usarse tiene una fuente y licencia verificadas; los candidatos dudosos se excluyen y se comunican.

### Fase C — Preparación y descarga local

1. Descargar solo los recursos aprobados y verificados a `images/`.
2. Usar nombres descriptivos y extensiones reales, acordes al formato descargado. Mantener la imagen original cuando la licencia no permita derivadas; no convertir ni recomprimir en ese caso.
3. Comprobar que cada descarga es un archivo de imagen legible, no una página HTML de error, redirección o miniatura de baja resolución. Verificar MIME/tipo de archivo y dimensiones mediante herramientas ya disponibles, sin instalar dependencias.
4. Mantener tamaño razonable para web sin alterar el recurso de manera que contradiga la licencia. Si el archivo resulta excesivo y no se permite una versión derivada, buscar otro candidato con resolución apropiada.
5. Actualizar el registro de créditos con el nombre y la ruta exacta de cada archivo incorporado.

**Control de salida:** todos los recursos seleccionados existen localmente y se abren correctamente; ningún archivo se incorporó sin créditos/licencia verificables.

### Fase D — Sustitución de referencias y alternativas textuales

1. Cambiar los 15 `src` temporales por rutas relativas locales bajo `images/`.
2. Actualizar cada `alt` para describir de forma concisa la imagen real, en español, sin inferir detalles que no aparezcan ni repetir mecánicamente «imagen de prueba».
3. Retirar pies «Imagen de prueba» ya obsoletos; mantener o añadir pies solo cuando identifiquen una imagen ilustrativa/de archivo o una atribución necesaria.
4. Preservar la indicación de que los proyectos del portafolio son conceptos ficticios/editables y evitar atribuir a Damián los recursos de terceros. Si los recursos no son las obras mostradas en el texto, considerar descripciones como «Imagen ilustrativa para el concepto...» en `alt` o pie, según la función visual.
5. No convertir la ilustración o fotografía de archivo en retrato real. Si la imagen del bloque «Sobre mí» es decorativa, usar `alt=""` solo si no aporta información y no es necesaria para comprender el contenido; en caso informativo, describir que es una imagen simbólica/espacio creativo.
6. Incorporar atribución visible en el HTML cuando la licencia lo exija, con vínculo a la fuente/licencia si es requisito. Los créditos completos quedarán en `credits.md`.
7. No alterar composición, clases, estilos, contenido editorial o estructura ajenos a la sustitución, excepto correcciones justificadas y aprobadas en el plan/tareas.

**Control de salida:** ningún placeholder remoto queda en el documento; todos los nuevos `src` apuntan a archivos presentes.

### Fase E — Créditos y revisión final

1. Completar `specs/003-IMAGES/credits.md` en formato de tabla, con una fila por archivo utilizado y todos los campos requeridos.
2. Verificar las rutas desde la raíz del sitio y comprobar que los archivos están versionables y son imágenes válidas.
3. Auditar de nuevo `index.html` frente a criterios relevantes de `specs/001-HTML/spec.md`:
   - 14 secciones en orden y IDs únicos;
   - un solo `h1`, enlaces internos válidos;
   - 15 imágenes previstas, todos los `alt` presentes y coherentes;
   - cero `placehold.co` y cero `src` remotos;
   - FAQ con `details`/`summary`, Microdata de `Person` y seis `CreativeWork`;
   - cero scripts, CSS inline/embebido o tecnologías no permitidas.
4. Revisar el diff para confirmar que solo se cambiaron `index.html`, `images/` y `specs/003-IMAGES/credits.md` (además de los propios documentos de planificación ya autorizados).
5. Informar cualquier discrepancia HTML no relacionada que se haya detectado, sin ampliarla silenciosamente.

## 4. Matriz de imágenes y nombres objetivo

| # | Sección/elemento | Archivo objetivo (sin extensión) | Requisito de selección |
|---:|---|---|---|
| 1 | Hero | `ciudad-victoriana-postapocaliptica` | Vista amplia de ciudad/arquitectura histórica industrial con atmósfera de ruina o humo. |
| 2 | Sobre mí | `universo-artistico-damian-vesper` | Herramientas, escritorio creativo o imagen simbólica; nunca retrato atribuido al artista. |
| 3 | Gótico Neo-Victoriano | `gotico-neo-victoriano` | Arquitectura gótica o victoriana monumental. |
| 4 | Steampunk industrial | `steampunk-industrial` | Mecanismo, caldera, engranajes o maquinaria industrial. |
| 5 | Distopía urbana | `distopia-urbana` | Calle urbana nocturna/decadente, neón o grafiti. |
| 6 | Las Cenizas de Londres | `las-cenizas-de-londres` | Ciudad/arquitectura victoriana con atmósfera de ceniza; recurso ilustrativo, no obra atribuida a Damián. |
| 7 | El Corazón de Hierro | `el-corazon-de-hierro` | Máquina o mecanismo industrial monumental. |
| 8 | Crónicas del Último Imperio | `cronicas-del-ultimo-imperio` | Arquitectura/composición imperial ficticia, sin emblemas reales. |
| 9 | La Ciudad Sin Amanecer | `la-ciudad-sin-amanecer` | Ciudad nocturna con luces artificiales y tono distópico. |
| 10 | Los Hijos del Vapor | `los-hijos-del-vapor` | Maquinaria de vapor, fábrica o ciencia ficción industrial. |
| 11 | El Jardín de las Máquinas Muertas | `el-jardin-de-las-maquinas-muertas` | Vegetación y estructuras o máquinas abandonadas. |
| 12 | Archivo I: La Era del Óxido | `archivo-era-del-oxido` | Fábrica o estructura industrial envejecida. |
| 13 | Archivo II: Ciudades de Ceniza | `archivo-ciudades-de-ceniza` | Arquitectura monumental ruinosa o cubierta de bruma/ceniza. |
| 14 | Archivo III: El Nuevo Imperio | `archivo-el-nuevo-imperio` | Mezcla de arquitectura histórica e industrial sin símbolos nacionales reales. |
| 15 | Anatomía de una portada | `portada-conceptual-victoriana` | Imagen vertical como portada conceptual, sin falso texto final. |

La extensión y resolución final se definirán según las condiciones de licencia, el formato de origen y el uso; el nombre exacto deberá asentarse en los créditos.

## 5. Plan de contingencia y decisiones pendientes

- **Licencia no clara:** descartar el recurso y seguir buscando; nunca asumir permiso.
- **Atribución visible obligatoria:** añadir atribución accesible junto a la imagen o en un área de créditos enlazada si la licencia lo permite; documentar qué alternativa satisface los términos.
- **Recurso visual inadecuado:** no forzar su asociación con una obra o artista; reemplazarlo o consultar al usuario.
- **No se encuentran 15 recursos apropiados:** no rellenar con imágenes de baja pertinencia o licencia dudosa. Presentar las ubicaciones no resueltas y solicitar decisión; la especificación permite hasta 15, pero los criterios de aceptación deben revisarse con aprobación explícita si se reduce el total.
- **Fallo al acceder a internet o descargar:** registrar el bloqueo y no incorporar URL remota como sustituto final.
- **Defecto estructural ajeno a imágenes:** documentarlo y solicitar aprobación separada antes de corregirlo si amplía el alcance.

## 6. Validación prevista

Validación manual y con herramientas disponibles, sin instalar dependencias:

- Inspección de encabezados de archivo/tipo MIME y dimensiones.
- Verificación de todas las fuentes y licencias de las imágenes incorporadas.
- Auditoría Python estándar (`html.parser` y `pathlib`) para secciones, IDs, fragmentos, `img src`, rutas y atributos `alt`.
- Revisión visual local de los recursos para confirmar correspondencia y calidad. No se declarará que se ha validado visualmente una imagen si no pudo abrirse/revisarse.
- Comparación final de diff y lista de archivos afectados.

## 7. Gate de aprobación

Este plan no autoriza todavía a descargar recursos ni a editar el HTML. Tras la aprobación explícita del plan se elaborará `tasks.md`. La implementación solo comenzará después de que también se apruebe la lista de tareas.
