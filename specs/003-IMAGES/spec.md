# Especificación: revisión del HTML y selección de imágenes locales

- **Identificador:** 003-IMAGES
- **Fase:** revisión editorial y sustitución de imágenes provisionales
- **Estado:** pendiente de aprobación
- **Referencias:** [`BRIEFING.md`](../../BRIEFING.md), [`AGENTS.md`](../../AGENTS.md), [`specs/001-HTML/spec.md`](../001-HTML/spec.md)

## 1. Objetivo

Revisar `index.html` frente a la especificación 001 y `BRIEFING.md`, identificar desviaciones relevantes y reemplazar las imágenes provisionales por recursos visuales apropiados para la escena descrita en cada ubicación. Los recursos deben descargarse y quedar almacenados localmente bajo `images/`, con fuentes y licencias verificadas, para evitar depender de servicios remotos en tiempo de uso.

Esta especificación no autoriza todavía a modificar `index.html`, descargar imágenes ni crear archivos de implementación. La implementación solo comenzará después de aprobar esta especificación y los documentos posteriores `plan.md` y `tasks.md`, de acuerdo con `AGENTS.md`.

## 2. Alcance

Incluye:

1. Auditar el HTML existente contra los criterios aplicables de `specs/001-HTML/spec.md` y el briefing.
2. Conseguir hasta 15 imágenes adecuadas y descargables con licencia de uso clara, almacenarlas localmente en `images/` y reemplazar sus referencias provisionales en `index.html`.
3. Actualizar textos alternativos y pies de imagen para describir correctamente los recursos reales seleccionados, sin implicar que una fotografía de archivo sea una obra de Damián ni que retrate al artista.
4. Documentar fuente, autoría y licencia de cada recurso en `specs/003-IMAGES/credits.md` (o documento de créditos acordado en el plan), respetando los requisitos de atribución de cada licencia.
5. Ejecutar validaciones de rutas locales, atributos `alt`, enlaces internos y marcado HTML.

Queda fuera de alcance implementar estilos CSS, alterar textos editoriales no relacionados, rediseñar secciones, instalar dependencias, añadir JavaScript o usar URLs externas como `src` final.

## 3. Inventario y dirección visual requerida

Sustituir las 15 referencias actuales a `placehold.co`, si se encuentra una alternativa apropiada para cada una. Utilizar archivos locales y nombres descriptivos. Inventario:

| # | Ubicación | Nombre de archivo previsto | Contenido visual requerido |
|---:|---|---|---|
| 1 | Hero / ciudad victoriana postapocalíptica | `ciudad-victoriana-postapocaliptica` | Vista amplia y atmosférica de arquitectura histórica/industrial, ruinas o ciudad cubierta de humo; reservar espacio visual para el texto superpuesto si la composición lo requiere. |
| 2 | Sobre mí / imagen representativa | `universo-artistico-damian-vesper` | Naturaleza muerta de herramientas de ilustración, escritorio creativo o escena simbólica. No presentar a una persona desconocida como retrato real de Damián. |
| 3 | Gótico Neo-Victoriano | `gotico-neo-victoriano` | Arquitectura gótica/victoriana, catedral, filigrana o edificio monumental oscuro. |
| 4 | Steampunk industrial | `steampunk-industrial` | Engranajes, maquinaria, caldera o interior industrial con aspecto de vapor. |
| 5 | Distopía urbana | `distopia-urbana` | Calle urbana nocturna, arquitectura degradada, grafiti o neón, evitando atribuirla a un lugar real concreto. |
| 6 | Las Cenizas de Londres | `las-cenizas-de-londres` | Arquitectura urbana victoriana con humo/ceniza; obra de referencia conceptual, no portada real de libro. |
| 7 | El Corazón de Hierro | `el-corazon-de-hierro` | Máquina o mecanismo industrial de aspecto central/monumental. |
| 8 | Crónicas del Último Imperio | `cronicas-del-ultimo-imperio` | Arquitectura monumental o composición editorial de tono imperial ficticio, sin emblemas reales identificables. |
| 9 | La Ciudad Sin Amanecer | `la-ciudad-sin-amanecer` | Ciudad nocturna con luces artificiales, ambiente urbano distópico. |
| 10 | Los Hijos del Vapor | `los-hijos-del-vapor` | Máquina de vapor, fábrica o composición industrial con tono de ciencia ficción. |
| 11 | El Jardín de las Máquinas Muertas | `el-jardin-de-las-maquinas-muertas` | Vegetación recuperando estructuras o máquinas abandonadas. |
| 12 | Archivo I: La Era del Óxido | `archivo-era-del-oxido` | Fábrica, maquinaria o estructura industrial envejecida. |
| 13 | Archivo II: Ciudades de Ceniza | `archivo-ciudades-de-ceniza` | Arquitectura urbana monumental, ruinosa o cubierta de bruma/ceniza. |
| 14 | Archivo III: El Nuevo Imperio | `archivo-el-nuevo-imperio` | Arquitectura histórica e industrial combinada, sin símbolos de una nación real. |
| 15 | Anatomía de una portada | `portada-conceptual-victoriana` | Imagen vertical adecuada como portada conceptual victoriana/postapocalíptica, sin texto ficticio ilegible presentado como tipografía final. |

Los nombres son base para el inventario; la extensión (`.jpg`, `.png`, `.webp` u otra) se decidirá según el recurso original y la compatibilidad, y se registrará en el plan.

## 4. Requisitos de selección, licencias y archivos

- Preferir imágenes de dominio público o con licencia abierta que permita el uso previsto y la copia local. Verificar la licencia y atribución en la página del recurso original; no inferir permisos por el mero hecho de que una imagen sea visible o descargable.
- No usar recursos con licencia desconocida, restricciones incompatibles, marcas de agua o disponibilidad efímera.
- Conservar la atribución exigida y registrar, por recurso, título/descrición, autor, URL de fuente, licencia y URL de licencia en el documento de créditos.
- No seleccionar imágenes generadas o etiquetadas como arte de Damián Vesper; son referencias visuales para un sitio ficticio y deben identificarse como imágenes ilustrativas/conceptuales cuando corresponda.
- No usar una fotografía de una persona no identificada como si fuera el retrato de Damián. La imagen de la ubicación «Sobre mí» debe ser simbólica o representar herramientas/espacio de trabajo; si la selección final no permite esa interpretación honesta, proponer reemplazarla por una imagen decorativa de atmósfera y ajustar su `alt` en consecuencia.
- Descargar archivos a `images/` con nombres descriptivos, tamaño razonable y dimensiones suficientes para el uso previsto. No instalar herramientas o dependencias. No procesar ni modificar imágenes de forma que se infrinja su licencia.
- El HTML final no debe depender de servicios de imágenes externos. No añadir CSS ni estilos inline para forzar recortes; la composición visual queda para la fase CSS ya planificada.

## 5. Revisión del HTML existente

La auditoría debe comparar el documento con la especificación 001 y atender al menos:

- Las 14 secciones requeridas, orden, IDs, textos, navegación, encabezados, FAQ nativa y Microdata.
- Las rutas actuales de imágenes: sustituir los `src` remotos `placehold.co` por archivos locales seleccionados.
- Los `alt` y `figcaption`: retirar el texto «Imagen de prueba» cuando el archivo real lo sustituya, y describir con precisión la imagen elegida, sin duplicar el pie ni inventar contenido visual.
- Mantener la naturaleza ficticia de los seis proyectos y no transformar las imágenes seleccionadas en afirmaciones de autoría o encargos reales.
- Corregir únicamente desviaciones confirmadas por la spec/briefing que sean necesarias para completar esta solicitud. Cambios editoriales o estructurales de mayor alcance deberán proponerse aparte y no incluirse silenciosamente.

## 6. Criterios de aceptación

La fase se considerará conforme cuando:

1. `index.html` haya sido revisado contra `specs/001-HTML/spec.md` y `BRIEFING.md`, y cualquier desviación corregida esté dentro del alcance aprobado.
2. No queden referencias `https://placehold.co/` ni `src` remotos para las imágenes incluidas en el inventario.
3. Las imágenes utilizadas existan en `images/`, tengan nombres descriptivos y correspondan con el contenido de su sección.
4. Las licencias y atribuciones de todos los recursos incorporados estén comprobadas y registradas.
5. Todos los elementos `img` tengan `alt` adecuado al recurso real; las imágenes puramente decorativas usen `alt=""`.
6. La imagen del bloque «Sobre mí» no se haga pasar por una fotografía de Damián.
7. Las obras de ejemplo sigan identificadas como conceptos ficticios, sin insinuar que las imágenes de stock son encargos u obras creadas por el artista.
8. Se mantengan HTML5, accesibilidad, SEO, Microdata y tecnologías permitidas; no se agreguen CSS, JavaScript, dependencias ni frameworks.
9. Todos los enlaces internos continúen con destinos válidos y la revisión no introduzca IDs duplicados ni errores de marcado.
10. La lista final de archivos modificados se limite a `index.html`, los recursos gráficos autorizados bajo `images/` y el documento de créditos aprobado en `specs/003-IMAGES/`.

## 7. Aprobación requerida

Antes de continuar, aprobar explícitamente esta especificación. Tras su aprobación se preparará `plan.md`; el plan deberá aprobarse antes de elaborar `tasks.md`, y las tareas deberán aprobarse antes de descargar recursos o editar `index.html`.
