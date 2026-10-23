# Plan de implementación: Landing page de Damián Vesper

- **Especificación de referencia:** [`spec.md`](./spec.md)
- **Identificador:** 001-HTML
- **Objetivo de este plan:** ordenar y verificar el trabajo requerido para implementar la fase HTML y dejar explícita la transición controlada a la futura fase CSS.
- **Estado:** planificación

## 1. Principios de ejecución

1. La especificación `spec.md` y las instrucciones permanentes de `AGENTS.md` son la fuente de verdad.
2. En esta fase se implementará únicamente `index.html`. No se creará `styles.css`, aunque el HTML lo referenciará para la fase posterior.
3. Se utilizará HTML5 únicamente. No se añadirán JavaScript, CSS embebido o inline, frameworks, librerías, dependencias ni otros tipos de archivo de implementación.
4. Se conservarán todos los textos solicitados y se respetará su intención, sin sumar afirmaciones profesionales o datos ficticios presentados como reales.
5. La página y sus ejemplos se identificarán claramente como conceptos ficticios/editables donde haga falta, especialmente en el portafolio y los eventos.
6. Las decisiones estructurales deben facilitar una fase visual responsive sin anticipar ni incluir estilos.
7. No se modificarán documentos existentes ni archivos ajenos al alcance de esta fase.

## 2. Entregables y límites

### Entregable de esta fase

- `index.html`: documento completo, semántico, accesible y con SEO/Microdata, que contenga las 14 secciones, la navegación y el pie de página definidos en `spec.md`.

### Referencias previstas, no entregables de esta fase

- `styles.css`: se enlazará en el `<head>` como archivo futuro, pero no se creará.
- `images/`: se utilizará como prefijo para rutas de imagen descriptivas, pero no se crearán carpetas ni archivos gráficos salvo petición posterior.

### Exclusiones

- No implementar diseño visual ni reglas CSS.
- No crear scripts, formularios interactivos o comportamientos que requieran JavaScript.
- No agregar nombres, años, premios, clientes, exposiciones confirmadas, perfiles sociales, fechas, lugares o credenciales no proporcionados.

## 3. Fases de trabajo

### Fase 0 — Preparación y control de alcance

**Acciones**

- Revisar `AGENTS.md` y `specs/001-HTML/spec.md` antes de comenzar.
- Confirmar los nombres de IDs, el orden de navegación principal, la lista de contenidos y las decisiones editables.
- Registrar las decisiones de contenido: Damián Vesper y las obras son ficticios/editables; los eventos son pendientes de confirmar; `contacto@ejemplo.com` es provisional; perfiles sociales no tendrán URL inventada.

**Salida**

- Lista de implementación definida y sin dudas que requieran cambiar el alcance.

**Control**

- Ninguna tarea de esta fase autoriza crear HTML/CSS antes de la solicitud de implementación.

### Fase 1 — Esqueleto de documento y encabezado

**Acciones**

- Crear `index.html` con `<!DOCTYPE html>`, `<html lang="es">`, `<head>` y `<body>`.
- Añadir `meta charset="UTF-8"` y `meta name="viewport"`.
- Definir un título de página breve y descriptivo, y una meta descripción única relacionada con ilustración editorial, Steampunk y mundos victorianos distópicos.
- Vincular `styles.css` mediante `<link rel="stylesheet" href="styles.css">`, sin crear el archivo ni incorporar estilos.
- Añadir enlace de salto al identificador del `main`.
- Crear `header` y `nav` con los siete enlaces principales y sus destinos estables.

**Verificación**

- El enlace de salto apunta a un elemento existente.
- Cada enlace del menú tiene destino válido.
- No se introduce ARIA redundante; si se etiqueta la navegación, su nombre aclara la región.

### Fase 2 — Contenedor principal y esquema de secciones

**Acciones**

- Crear un único `main` con ID estable, por ejemplo `contenido-principal`.
- Añadir en el orden indicado las 14 secciones principales y asignar los IDs definidos en `spec.md`:
  1. `inicio`
  2. `manifiesto`
  3. `sobre-mi`
  4. `universo-visual`
  5. `especialidades`
  6. `portafolio`
  7. `colecciones`
  8. `proceso`
  9. `anatomia-portada`
  10. `trayectoria`
  11. `colaboraciones`
  12. `presentaciones`
  13. `preguntas-frecuentes`
  14. `contacto`
- Cada sección tendrá su propio `h2`; los bloques internos utilizarán encabezados consecutivos según la estructura.
- Se añadirá una clase descriptiva en cada sección y en los elementos que requieran presentación propia en la fase CSS.

**Verificación**

- Hay exactamente 14 secciones principales y ningún `id` duplicado.
- Existe un único `h1` en el hero.
- La jerarquía de encabezados no salta niveles sin motivo.

### Fase 3 — Incorporación de contenido editorial

**Acciones**

- Distribuir sin omisiones sustanciales los textos y componentes especificados en cada sección.
- Utilizar párrafos para texto corrido, citas (`blockquote`) para frases destacadas cuando corresponda, listas para conjuntos de elementos y artículos para unidades de contenido autónomas.
- Construir especialidades, colecciones, componentes de portada y trayectoria con estructuras semánticas adecuadas.
- Representar los cinco pasos del proceso mediante `ol` y sus elementos en el orden indicado.
- Identificar el contenido del portafolio como obras conceptuales/proyectos imaginarios y los eventos como propuestas pendientes de confirmación.
- Añadir a las tarjetas de eventos el estado explícito de confirmación según el texto de la especificación.

**Verificación**

- Cada sección contiene su título y todo el contenido requerido.
- Los proyectos no se presentan como encargos reales.
- No aparecen años de trayectoria ni datos de eventos no especificados.

### Fase 4 — Imágenes y figuras

**Acciones**

- Añadir elementos `img` para el hero, el retrato/ilustración del artista, los tres mundos visuales, las seis obras, las tres colecciones y la portada conceptual.
- Elegir rutas bajo `images/` con nombres descriptivos, por ejemplo `images/ciudad-victoriana-postapocaliptica.jpg` o `images/las-cenizas-de-londres.jpg`.
- Usar `figure` y `figcaption` para representar cada obra donde resulte adecuado, integrando título, categoría y descripción sin duplicar información innecesariamente.
- Escribir `alt` que describa la información visual prevista, no texto de relleno. Usar `alt=""` solo para imágenes decorativas.

**Verificación**

- Toda imagen tiene `alt`.
- Todas las rutas comienzan bajo `images/` y tienen nombres significativos.
- Los archivos de imagen no se crean en esta fase y su ausencia no debe confundirse con un entregable omitido.

### Fase 5 — Microdata, FAQ y contacto

**Acciones**

- Asociar Microdata `https://schema.org/Person` al bloque del artista en «Sobre mí», utilizando solo nombre y ocupación confirmados por la especificación.
- Asociar Microdata `https://schema.org/CreativeWork` a cada uno de los seis proyectos conceptuales usando propiedades adecuadas a datos visibles, como nombre, imagen y descripción cuando correspondan.
- Añadir una indicación visible de que son conceptos ficticios/editoriales, para evitar interpretarlos como trabajos reales.
- Construir las cinco preguntas frecuentes como elementos `details` con `summary` y respuesta, sin scripts.
- Crear el enlace `mailto:contacto@ejemplo.com` con nombre accesible «Enviar un correo».
- Mostrar espacios para Behance, ArtStation e Instagram sin enlaces a perfiles no confirmados. Si no se dispone de URL real, mostrar el nombre como texto o marcador editorial no interactivo.

**Verificación**

- Microdata se expresa con `itemscope`, `itemtype` e `itemprop`; no se añade JSON-LD.
- No se marcan como conocidos datos que no lo sean.
- Las FAQ operan con el comportamiento nativo del navegador.
- No se construyen enlaces sociales rotos o ficticios.

### Fase 6 — Pie de página

**Acciones**

- Añadir el nombre artístico y la frase proporcionada.
- Incorporar enlaces internos principales a destinos existentes.
- Añadir una fórmula editable de derechos de autor sin inventar año o titular definitivo.
- Incluir un enlace de retorno a `#inicio`.

**Verificación**

- Todos los enlaces del footer tienen destinos válidos.
- El texto legal no afirma titularidad o fechas no confirmadas.

### Fase 7 — Revisión semántica, accesibilidad y SEO

**Acciones**

- Revisar landmarks: `header`, navegación, `main`, secciones y `footer`.
- Confirmar un único `h1`, encabezados lógicos, identificadores únicos, listas ordenadas/no ordenadas apropiadas y enlaces descriptivos.
- Revisar imágenes y alternativas; revisar el enlace de salto y la navegación por teclado desde la estructura nativa.
- Confirmar metadatos, idioma de documento y Microdata.
- Revisar clases descriptivas y vínculo al futuro CSS.

**Verificación**

- El contenido esencial no depende de color, imágenes, CSS o JavaScript para ser comprendido.
- ARIA se limita a los casos en que aporta una mejora necesaria.
- No se han incluido scripts, estilos o dependencias.

### Fase 8 — Validación final y control de cambios

**Acciones**

- Revisar el HTML como documento completo y comprobar manualmente todos los enlaces internos.
- Validar consistencia de `id`/`href`, estructura de secciones, `alt`, FAQ y Microdata.
- Revisar los cambios para confirmar que `index.html` es el único archivo de implementación creado en la fase.
- Comprobar que `styles.css` aparece únicamente como referencia y que no se generaron imágenes.

**Salida**

- `index.html` listo para la fase de diseño visual, sin CSS implementado.

## 4. Matriz de sección, estructura y verificación

| Orden | Sección | ID | Estructura HTML prevista | Puntos de control |
|---:|---|---|---|---|
| 1 | Inicio — Hero | `inicio` | `section`, un `h1`, textos, enlaces de acción, `figure`/`img` | Texto exacto, dos CTAs con destinos válidos, imagen y `alt` |
| 2 | Manifiesto | `manifiesto` | `section`, `h2`, párrafos, cita | Dos textos y frase destacada completos |
| 3 | Sobre mí | `sobre-mi` | `section`, `h2`, textos, imagen, Microdata `Person` | Perfil solo con datos permitidos, imagen alternativa |
| 4 | Mi universo visual | `universo-visual` | `section`, tres `article` con imagen, `h3` y descripción | Tres mundos con textos requeridos |
| 5 | Especialidades | `especialidades` | `section`, cuatro `article`, `h3` y párrafo | Cuatro servicios y descripciones completos |
| 6 | Portafolio | `portafolio` | `section`, seis `figure`/`figcaption`, Microdata `CreativeWork` | Título, categoría, descripción, imagen y naturaleza ficticia por obra |
| 7 | Colecciones | `colecciones` | `section`, tres `article` con imagen, título y párrafo | Tres archivos con sus descripciones |
| 8 | Proceso creativo | `proceso` | `section`, `ol` con cinco pasos | Orden y textos completos |
| 9 | Anatomía de una portada | `anatomia-portada` | `section`, lista/cuatro `article`, imagen conceptual | Cuatro componentes y gran imagen con `alt` |
| 10 | Trayectoria | `trayectoria` | `section`, textos y tres bloques/etapas | Sin fechas ni hitos verificables inventados |
| 11 | Colaboraciones | `colaboraciones` | `section`, textos, lista de destinatarios, enlace CTA | CTA lleva a `#contacto` |
| 12 | Próximas presentaciones | `presentaciones` | `section`, tres `article` de evento/actividad | Cada tarjeta pendiente, sin datos confirmados |
| 13 | Preguntas frecuentes | `preguntas-frecuentes` | `section`, cinco `details`/`summary` | Pregunta y respuesta exactas; sin JavaScript |
| 14 | Contacto | `contacto` | `section`, textos, `mailto`, espacios sociales, frase final | Correo provisional, sin perfiles inventados |
| — | Pie de página | — | `footer`, navegación secundaria y copyright editable | Nombre, lema, enlaces válidos y retorno a inicio |

## 5. Inventario de IDs y enlaces

### IDs de secciones

```text
inicio
manifiesto
sobre-mi
universo-visual
especialidades
portafolio
colecciones
proceso
anatomia-portada
trayectoria
colaboraciones
presentaciones
preguntas-frecuentes
contacto
```

### Enlaces de navegación principal

```text
Inicio          #inicio
Sobre mí        #sobre-mi
Especialidades  #especialidades
Portafolio      #portafolio
Trayectoria     #trayectoria
Presentaciones  #presentaciones
Contacto        #contacto
```

### Enlaces contextuales previstos

```text
Explorar mis obras       #portafolio
Hablemos de tu historia  #contacto
Cuéntame tu proyecto     #contacto
Volver al inicio         #inicio
Enviar un correo         mailto:contacto@ejemplo.com
```

El enlace de salto apuntará a `#contenido-principal` (o a un nombre equivalente, definido una sola vez en el `main`). Todo destino fragmentario debe aparecer exactamente una vez en el documento.

## 6. Estrategia de clases y preparación para CSS

- Usar nombres semánticos y predecibles, por ejemplo `site-header`, `primary-navigation`, `hero`, `section-heading`, `portfolio-grid`, `portfolio-card`, `creative-process`, `faq-list` y `site-footer`.
- Mantener clases separadas de los identificadores: los `id` sirven para navegación/fragmentos y las clases para el diseño futuro.
- Aplicar una clase a elementos repetidos para permitir su organización responsive sin recurrir a estilos inline.
- No crear utilidades visuales en HTML ni insertar caracteres decorativos como sustituto de información semántica.
- Las clases no deben alterar el orden de lectura ni sugerir que existe CSS implementado.

## 7. Política de contenido y datos

### Confirmado por la solicitud

- Nombre artístico ficticio y editable: Damián Vesper.
- Especialidad y estilos visuales descritos.
- Textos de presentación, secciones, servicios, proceso, etapas narrativas y FAQ.
- Seis proyectos conceptuales y tres colecciones imaginarias.
- Correo de ejemplo `contacto@ejemplo.com` explícitamente provisional.

### No confirmado; no inventar

- Años, duración de trayectoria, estudios, ubicación, tarifas, disponibilidad, premios o premios recibidos.
- Clientes, editoriales asociadas, ventas, testimonios o encargos reales.
- Exposiciones, ferias, encuentros, fechas, ubicaciones o programación confirmada.
- Direcciones URL o nombres de usuario de perfiles sociales.
- Derechos de titularidad definitivos de las ilustraciones o proyectos ficticios.

### Tratamiento

- Presentar los proyectos como imaginarios/conceptuales en el texto visible.
- Presentar las actividades del bloque de eventos como pendientes de confirmación.
- Mantener datos editables mediante contenido claro, no usando textos que aparenten ser información real.

## 8. Plan de pruebas y lista de aceptación

### Integridad del documento

- [ ] `index.html` contiene doctype, idioma `es`, `<head>` y `<body>`.
- [ ] Incluye codificación, viewport, título, descripción SEO y referencia a `styles.css`.
- [ ] No contiene CSS inline/embebido, JavaScript ni dependencias externas.
- [ ] Solo se creó o modificó el archivo de implementación autorizado en esta fase.

### Estructura y navegación

- [ ] Hay un solo `h1` con el texto del hero.
- [ ] Secciones principales en orden, todas con `id` único.
- [ ] `header`, `nav`, `main`, secciones y `footer` tienen uso semántico.
- [ ] El enlace de salto apunta a `main`.
- [ ] Cada fragmento interno de los menús y CTAs tiene un destino existente.
- [ ] No hay identificadores duplicados ni enlaces internos vacíos.

### Contenido

- [ ] Están presentes las 14 secciones y todos los textos requeridos.
- [ ] El portafolio muestra las seis obras con título, categoría y descripción.
- [ ] Colecciones, proceso, anatomía de portada y trayectoria contienen todos sus elementos.
- [ ] Las cinco preguntas/respuestas están completas y usan `details`/`summary`.
- [ ] Contacto y pie de página incluyen todos los componentes previstos.

### Accesibilidad y semántica

- [ ] Cada `<img>` dispone de un `alt` adecuado.
- [ ] Figuras y pies de imagen corresponden al contenido presentado.
- [ ] Enlaces tienen propósitos comprensibles.
- [ ] Listas numeradas y agrupaciones usan las etiquetas correspondientes.
- [ ] ARIA se usa solo cuando sea necesario y no duplica semántica nativa.

### SEO y datos estructurados

- [ ] Metadatos no afirman datos profesionales no confirmados.
- [ ] El artista utiliza Microdata `Person` con propiedades válidas y disponibles.
- [ ] Los seis trabajos usan Microdata `CreativeWork` basado solo en datos mostrados.
- [ ] No existe JSON-LD ni script de datos estructurados.

### Integridad factual

- [ ] Las obras se identifican como imaginarias o conceptuales.
- [ ] Las presentaciones no se presentan como eventos celebrados o confirmados.
- [ ] No aparecen fechas, lugares, clientes, premios, perfiles sociales o trayectoria verificable inventados.
- [ ] Correo provisional y copyright son claramente editables.

## 9. Riesgos y mitigaciones

| Riesgo | Mitigación |
|---|---|
| Confundir proyectos ficticios con trabajos reales | Añadir una indicación visible de proyectos conceptuales/imaginarios en la introducción o en cada ficha |
| Interpretar tarjetas de eventos como agenda confirmada | Etiquetar cada actividad como pendiente de confirmar e incluir solo estados suministrados |
| Enlaces a redes sociales rotos o inventados | Dejar los nombres como marcadores no interactivos hasta contar con URLs verificadas |
| Imágenes aún inexistentes | Mantener rutas descriptivas bajo `images/`; documentar que los recursos gráficos pertenecen a una etapa posterior |
| Alt text que describa una imagen inexistente como un hecho | Redactar descripciones como descripción del recurso previsto y reemplazarlas cuando se incorporen las imágenes definitivas |
| Secciones muy extensas difíciles de ajustar a una pantalla | Usar estructura flexible; el CSS futuro podrá aproximarse a `100vh` sin recortar ni ocultar contenido |
| Desajustes entre navegación e IDs | Mantener inventario de IDs y pasar la comprobación de enlaces internos en la revisión final |
| Microdata que estructure información inventada | Limitar `itemprop` a nombres, ocupación, títulos, imágenes y descripciones realmente presentes en el contenido |

## 10. Transición a la fase CSS

La fase HTML se considerará cerrada cuando todos los criterios anteriores estén verificados y no queden omisiones de contenido. Solo entonces podrá comenzar la fase visual:

1. Crear `styles.css` sin introducir tecnologías adicionales.
2. Mantener el orden de lectura y la semántica implementados en `index.html`.
3. Desarrollar diseño responsive oscuro, industrial y victoriano, incluyendo estados de foco, contraste suficiente y adaptación a movimiento reducido.
4. Permitir que las secciones se acerquen a `100vh` sin recortar contenido en pantallas pequeñas o ante texto extenso.
5. Evitar modificar el HTML validado salvo que sea imprescindible, explicando cada cambio necesario.

Este documento organiza el trabajo; no sustituye ni amplía los textos y requisitos normativos de `spec.md` y `AGENTS.md`.
