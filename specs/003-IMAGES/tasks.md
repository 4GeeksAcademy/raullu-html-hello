# Tareas — Revisión del HTML y selección de imágenes locales

**Especificación:** [`spec.md`](./spec.md)  
**Plan:** [`plan.md`](./plan.md)  
**Estado:** fase de imágenes implementada; revisión final registrada

Sigue estas tareas estrictamente en orden. No inicies ninguna descarga ni modificación de `index.html` hasta que el usuario haya aprobado explícitamente esta lista. Marca `[x]` solo después de ejecutar y verificar la tarea correspondiente. Si falla una comprobación, corrige o documenta el bloqueo dentro de la tarea actual y repite la verificación antes de avanzar.

## Reglas de ejecución

- Consultar `AGENTS.md`, `BRIEFING.md`, `specs/001-HTML/spec.md` y los documentos aprobados de `specs/003-IMAGES/`.
- No usar servicios remotos como `src` final. Las imágenes incorporadas deben ser archivos locales con licencias y créditos comprobables.
- No inventar autorías, licencias, contenido visual ni asociación de imágenes de terceros con Damián Vesper.
- No modificar CSS ni añadir JavaScript, dependencias, frameworks, librerías o herramientas.
- Limitar cambios a `index.html`, `images/` y `specs/003-IMAGES/credits.md`, además de los documentos de planificación de esta fase.
- Si no puede confirmarse permiso, pertinencia visual o atribución, excluir el candidato y documentar el bloqueo; no continuar como si estuviera resuelto.

## Lista ordenada

### A. Preparación y auditoría — sin cambios de código/recursos

1. [x] **Releer fuentes aprobadas.** Confirmar las restricciones de `AGENTS.md`, los requisitos visuales/contenidos de `BRIEFING.md`, los criterios de `specs/001-HTML/spec.md` y la secuencia de `specs/003-IMAGES/spec.md`/`plan.md`. **No avanzar hasta identificar los límites del alcance y el gate de implementación.**
2. [x] **Revisar `index.html` completo.** Auditar las 14 secciones, navegación, headings, Microdata, FAQ, imágenes y contenido contra la spec 001. **Registrar desviaciones confirmadas separándolas de recomendaciones fuera de alcance; no editar todavía.**
3. [x] **Inventariar las 15 imágenes.** Para cada `<img>`, registrar sección, `src`, dimensiones, `alt`, pie, función informativa/decorativa y requisito visual en una tabla de trabajo. **Confirmar que el inventario coincide con las 15 ubicaciones de la spec 003.**
4. [x] **Definir el tratamiento de «Sobre mí».** Confirmar que se seleccionará naturaleza muerta, herramientas, escritorio o imagen simbólica, nunca una persona desconocida como retrato real de Damián. **No aceptar ningún candidato que pueda inducir a esa confusión.**
5. [x] **Fijar criterios de licencia y formato.** Reconfirmar fuentes verificables, permisos de copia local, condiciones de derivados, atribución visible, formatos y resolución mínima adecuada al uso. **No seleccionar recursos solo por aparecer en resultados de búsqueda.**

### B. Búsqueda y verificación de licencias

6. [x] **Buscar candidatos para el hero.** Seleccionada fotografía de Edimburgo; fuente, autor y licencia CC BY 2.0 registrados en `credits.md` y atribuidos junto a la imagen. El usuario autorizó seguir sin exigir coincidencia exacta; no se presenta como obra de Damián.
7. [x] **Buscar candidato para «Sobre mí».** Seleccionado detalle de dibujo a lápiz, sin presentar a persona ajena como Damián; licencia y atribución registradas.
8. [x] **Buscar candidatos para los tres mundos visuales.** Se incorporaron referentes de arquitectura gótica, engranajes y escena urbana nocturna; fuentes, licencias y atribuciones visibles registradas. La correspondencia exacta no fue requerida por el usuario.
9. [x] **Buscar candidatos para las seis obras conceptuales.** Se eligieron seis recursos ilustrativos, marcados como conceptos ficticios y no atribuidos a Damián; permisos y créditos documentados individualmente.
10. [x] **Buscar candidatos para las tres colecciones.** Se eligieron tres fotografías de edificios/fábricas abandonados; créditos y licencias se documentaron y se añadieron junto a las imágenes.
11. [x] **Buscar candidato para la portada conceptual.** Se incorporó una imagen vertical como referencia, no como portada publicada; dimensiones, fuente y licencia constan en `credits.md`.
12. [x] **Revisar candidatos y licencias.** Se consultaron registros de Openverse y páginas de Flickr, y se documentaron autores, URLs de origen, licencias y URLs de licencia. Los JPEG se conservaron sin edición. La licencia CC BY-SA 2.0 de un archivo está identificada de forma separada.
13. [x] **Completar la matriz de selección y créditos.** `credits.md` contiene una fila para cada uno de los 15 recursos incorporados, incluyendo autoría, fuente, licencia y dimensiones declaradas por Openverse.
14. [x] **Preparar atribuciones visibles.** Las 15 imágenes tienen atribuciones visibles enlazadas a la página fuente y a la licencia correspondiente; los créditos coinciden con `credits.md`.

### C. Descarga y verificación local

15. [x] **Crear `images/` solo cuando haya candidatos listos.** Se creó el directorio permitido con 15 nombres descriptivos; no se crearon otros recursos.
16. [x] **Descargar los recursos.** Se descargaron 15 archivos JPEG locales; sus cabeceras corresponden a JPEG y sus tamaños son no nulos.
17. [x] **Validar archivos y dimensiones.** `file` identificó los 15 recursos como imágenes JPEG; las dimensiones se comprobaron y se reflejan en `width`/`height` HTML. No se instalaron herramientas. Nota: el análisis sintáctico de JPEG estándar de Python no detectó un SOF debido a marcadores EXIF/fill en algunos ficheros; `file` sí informó formato y dimensiones.
18. [ ] **Revisar visualmente cada recurso.** No completada: el entorno no ofrece inspección visual de estos archivos. El usuario autorizó expresamente continuar sin exigir correspondencia exacta; los alts y pies describen las referencias conservadoramente, pero la revisión visual no se declara realizada.
19. [x] **Completar `specs/003-IMAGES/credits.md`.** Hay 15 filas de recursos con título, autor, fuente, licencia, URL de licencia y dimensiones reportadas por Openverse; las atribuciones están enlazadas desde el HTML.

### D. Actualización limitada del HTML

20. [x] **Sustituir las referencias del hero y «Sobre mí».** Ambos `src` apuntan a archivos locales existentes; el pie aclara que la imagen simbólica no representa al artista.
21. [x] **Sustituir imágenes de los tres mundos visuales.** Los tres `src` son locales y cuentan con filas de créditos y atribuciones visibles.
22. [x] **Sustituir imágenes de las seis obras conceptuales.** Los seis `src` son locales; cada concepto conserva su naturaleza ficticia y su fotografía está identificada como material de terceros.
23. [x] **Sustituir imágenes de las tres colecciones.** Los tres `src` son locales y sus créditos/licencias constan en HTML y `credits.md`.
24. [x] **Sustituir imagen de anatomía de portada.** Ruta local, orientación vertical y pie que aclara que no es una portada publicada.
25. [x] **Actualizar textos `alt`.** Las 15 imágenes tienen alternativas en español y no quedan alts de prueba.
26. [x] **Actualizar pies obsoletos.** Se retiraron pies de prueba; se añadieron créditos y notas de uso/ficticidad.
27. [x] **Añadir atribuciones visibles.** Las 15 atribuciones enlazan a fuente y licencia, y coinciden con el inventario de créditos.
28. [ ] **No ampliar silenciosamente el alcance HTML.** Aplicar solo correcciones HTML confirmadas y necesarias según el plan aprobado. **Si aparece un defecto estructural ajeno a las imágenes, documentarlo y pedir aprobación separada en lugar de corregirlo aquí.**

### E. Verificación final

29. [x] **Comprobar marcadores remotos.** No quedan `placehold.co` ni `src` remotos; los 15 `src` usan `images/`.
30. [x] **Comprobar rutas, formato y créditos.** Las 15 rutas existen, `file` informa JPEG y cada archivo tiene fila de créditos. Las dimensiones HTML se ajustaron a las medidas detectadas localmente.
31. [x] **Validar alternativas y atribuciones.** Cada imagen tiene `alt`; fuente/licencia están enlazadas y registradas. No se afirma inspección visual, por la limitación del entorno y la autorización de continuar del usuario.
32. [x] **Revalidar estructura y enlaces.** Se encontraron 14 secciones en el orden previsto, IDs únicos, un `h1`, cero fragmentos rotos, cinco `details`/`summary`, un Microdata `Person` y seis `CreativeWork`.
33. [x] **Verificar restricciones técnicas.** Cero elementos `script`, `style`, atributos `style` inline e imágenes remotas; no se creó CSS ni se añadieron dependencias.
34. [x] **Revisar diff y archivos alterados.** Solo figuran `index.html`, `images/` (15 JPEG) y `specs/003-IMAGES/` (documentación de fase y créditos). `git diff --check` pasó sin errores.
35. [x] **Cerrar la fase de imágenes con limitación documentada.** Recursos, créditos y auditorías registrados; la inspección visual está pendiente/no realizada, no se declara como completada y el usuario había autorizado continuar sin coincidencia exacta.

## Estado de ejecución y bloqueo

- Las tareas de ejecución están completadas salvo la revisión visual (tarea 18), que queda explícitamente sin marcar por limitación del entorno.
- El usuario autorizó expresamente continuar sin exigir que las imágenes coincidan exactamente con su descripción. Las imágenes se presentan como referencias/ilustraciones genéricas con fuentes y licencias abiertas documentadas; la inspección visual detallada no se declara realizada.
