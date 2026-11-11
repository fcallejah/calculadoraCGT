# Calculadora Concurso Traslados Andalucía 2026

Esta versión 2026 es una actualización de [MaestroRafa](https://github.com/rbuegon523/calculadoraCGT) al nuevo baremo y una **reescritura y modernización completa** de la herramienta de 2025. Se ha transformado una calculadora básica en una aplicación web (PWA) profesional, adaptada milimétricamente al [**BOJA n.º 210, de 29 de octubre de 2026**](https://www.juntadeandalucia.es/boja/2026/210/16).

✅ Accesible aquí (https://fcallejah.github.io/calculadoraCGT/) ✅


### 📋 1. Adaptación Normativa (baremo 2026)
*   **🗣️ Idiomas separados (3.3 y 5.5):** se ha creado una sección exclusiva para certificados internacionales (ACLES) en el 5.5, liberando el 3.3 para la Escuela Oficial de Idiomas (EOI). Se incluye un buscador dinámico de certificados ACLES.
*   **Catálogo ACLES revisado:** contrastado con las columnas del PDF oficial de **28/07/2025**. Corrige DLF/DS/DHEF, TestDaF, Pearson, Oxford, Anglia, LRN y CIC; incorpora entradas omitidas y certificados comunes. Respeta el nivel mínimo por destreza y, en Cambridge, el nivel del examen realizado. Al recuperar datos antiguos, actualiza los niveles inequívocos con aviso; la antigua opción agrupada de Anglia y TOEIC C2 requieren reselección y no generan puntos mientras tanto. Se mantienen los identificadores guardados y las filas manuales.
*   **Puestos bilingües:** comprobador opcional compartido entre 3.3 y 5.5, con resultado también en el resumen. Utiliza las especialidades de las bases 4.1.4, 4.2.1 y 4.6.6 y las acreditaciones del [anexo XVI del BOJA 2026](https://www.juntadeandalucia.es/boja/2026/210/BOJA26-210-00168-14181-01_00345411.pdf#page=166), no el listado de certificados baremables de ACLES. Reconoce EOI B2–C2 y coincidencias verificadas de certificados de 5.5 en el mismo idioma; las demás acreditaciones se eligen por idioma, nivel (B2/C1/C2) y certificado, con una opción aparte para titulaciones sin nivel MCER indicado. Comprueba fechas límite de versiones antiguas de Aptis y Pearson y pide confirmar puntuaciones, destrezas o documentación cuando el anexo lo exige. No garantiza adjudicación: deben cumplirse también la titularidad de la especialidad, el cuerpo habilitado y las restantes condiciones de participación.
*   **Idiomas conectados en ambos sentidos:** al activar el comprobador, los méritos compatibles de 3.3/5.5 preseleccionan el idioma si solo hay uno, además del nivel y certificado. Los cambios posteriores en esos méritos actualizan la comprobación sin cambiar la especialidad elegida. En sentido inverso, una acreditación bilingüe solo autocompleta 3.3 o 5.5 si tiene una correspondencia exacta de certificado y nivel, y tras confirmar sus requisitos específicos. No crea duplicados ni convierte Aptis, titulaciones universitarias o equivalencias ambiguas en puntos ACLES. Al cambiar la selección se sustituye únicamente la fila creada automáticamente; las filas introducidas o corregidas manualmente se conservan.
*   **Servicios de Religión (1.2.1):** no se incluyen servicios con contrato laboral como profesor/a de Religión ajeno a los cuerpos de funcionarios docentes ([RD 696/2007, artículos 1 y 2](https://www.boe.es/buscar/act.php?id=BOE-A-2007-11450#a1)). El baremo exige servicios como funcionario/a de carrera, en prácticas o interino/a en el cuerpo correspondiente ([anexo II, 1.2.1](https://www.juntadeandalucia.es/boja/2026/210/BOJA26-210-00168-14181-01_00345411.pdf#page=26)); no se excluyen otros periodos que sí cumplan esa condición.
*   **🇬🇧 Lista de idiomas EOI ampliada:** ahora incluye 22 idiomas oficiales, incorporando lenguas cooficiales (catalán, euskera, gallego y valenciano) según la disposición complementaria segunda del BOJA.
*   **🤟 Nuevo mérito DLSE (3.3):** añadida caja específica para los Diplomas de Lengua de Signos Española (B1–C2) con su puntuación correspondiente y enlace oficial al CNLSE.
*   **🎭 Sección 6.3 reescrita:** se ha desglosado completamente el apartado de méritos artísticos y deportivos (premios, espectáculos, composiciones, actuaciones, exposiciones, conservador-restaurador y deportistas).
*   **📚 Obras literarias (6.1):** nueva tabla específica para autor, coautor, 3+ autores e ilustrador/a.
*   **💜 Plan de Igualdad (6.2):** añadido como mérito específico (1,0 pto./curso).
*   **Subapartados 6.2.a y 6.2.b:** el formulario y el desglose siguen la nomenclatura de la hoja de méritos de la Junta y de la disposición complementaria quinta, puntos 3 y 4, del [BOJA (página 45)](https://www.juntadeandalucia.es/boja/2026/210/BOJA26-210-00168-14181-01_00345411.pdf#page=45). El 6.2.a recoge premios y participación en proyectos de investigación o innovación educativa (0,2 puntos por proyecto); el 6.2.b, coordinación y participación en planes y proyectos educativos aprobados por la Consejería. Ambos comparten el tope de 2,5 puntos del 6.2.
*   **🎓 Múltiples títulos (3.1 y 3.2):** los títulos de doctor, DEA y máster pasan de ser casillas únicas a contadores, permitiendo alegar varios títulos a la vez.

### 🧮 2. Correcciones críticas de cálculo
*   **📅 Fecha de corte exacta (26/11/2026):** el cálculo de antigüedad (1.1 y 1.2) ya no se detiene el 31 de octubre. Ahora computa hasta la fecha de fin de plazo de solicitudes, reflejando correctamente los dos meses (septiembre y octubre) del año en curso, 2026.
*   **⚖️ Bug del 6.2 solucionado:** se ha corregido el error que permitía superar el tope máximo de **2,5 ptos.** en premios y proyectos. Se ha aplicado un `Math.min` estricto en todos los apartados para garantizar que nunca se sobrepasen los límites legales.
*   **📊 Desglose del 4.3 (coordinación):** se ha dividido la caja genérica en **tres apartados independientes** (jefatura de departamento, coordinación de ciclo/EOE/CEP y tutoría LOE), cada uno con su propia caja de años/meses.
*   **👩‍🏫 Tutorización (6.6) diferenciada:** máster/grado (0,1 pto./curso) frente a fase de aspirantes (0,2 ptos./curso), con un aviso para los cursos anteriores a 2023/24.
*   **Controles de coherencia con 1.2.1:** los periodos de 4.1, 4.2 y 4.3 no superan los servicios del mismo cuerpo. Los cursos de proyectos de 6.2, las convocatorias de 6.5 y los cursos de 6.6 se limitan, como control de esta calculadora, a los años completos de 1.2.1; esto no convierte las convocatorias o cursos del BOJA en méritos por año de servicio. Se mantienen los topes de puntos y de tutorización desde 2023/24.
*   **Especial dificultad (1.1.3):** solo computa servicios como funcionario/a de carrera, dentro del periodo de destino definitivo o provisionalidad que corresponda y sin superar 1.2.1. En prácticas, todo 1.1 queda deshabilitado y no puntúa. Si se completó el cuestionario, también se utiliza la fecha de nombramiento de carrera para excluir prácticas e interinidad; si se rellena manualmente, deben excluirse esos periodos.
*   **Provisionalidad anterior (1.1.2):** puede sumarse a 1.1.1 cuando se participa voluntariamente desde el primer destino definitivo obtenido por concurso, según el BOJA. El cuestionario pregunta expresamente por este supuesto y recoge años y meses; también puede confirmarse y ajustarse en el formulario. No se limita a dos años, pero no incluye prácticas, interinidad ni tiempo ya computado en 1.1.1. Si constan las fechas, se limita al periodo entre el nombramiento de carrera y ese primer destino. Una vez obtenido otro destino definitivo, ya no se acumula; tampoco recupera la especial dificultad anterior en 1.1.3.
*   **Datos y desglose:** los excesos se conservan para su revisión, con avisos explícitos, pero no se suman. El desglose y el PDF muestran las cantidades efectivamente computadas. El resumen y la impresión incluyen un aviso de simulación no oficial.

### Comprobaciones locales

Sin instalar dependencias, ejecutar `python3 -m http.server 8011 --bind 127.0.0.1` y abrir `http://127.0.0.1:8011/tests/calculator.html`. Las pruebas ejercitan la aplicación real: niveles EOI/ACLES, límites, situaciones del cuestionario, avisos, desglose y anchos móviles de 320 a 430 píxeles. La página de pruebas no guarda cambios en los datos de la calculadora.

### 🧙‍♂️ 3. El nuevo cuestionario de Antigüedad
Se ha pasado de tener simples cajas de texto a un **asistente interactivo (Wizard)** de varios pasos:
*   **Tecla Enter:** con el cuestionario abierto, avanza desde los campos, las casillas o el título del paso, incluso si se pierde el foco al deshabilitar un campo. Usa las mismas validaciones que «Siguiente»; en el último paso aplica las respuestas. Los botones y desplegables conservan su manejo normal de teclado; las casillas siguen marcándose con Espacio.
*   **📅 Fechas por defecto:** los calendarios arrancan automáticamente en el 1 de septiembre más reciente.
*   **🛡️ Validación estricta:** el sistema bloquea fechas de carrera anteriores a las de prácticas o que superen un margen lógico de 2 años. Además, se ha implementado un campo de texto `dd/mm/aaaa` sincronizado con el calendario nativo.
*   **🔄 Casilla de estabilización:** nueva casilla para marcar «No realicé prácticas / Accedí por estabilización», que iguala automáticamente las fechas.
*   **⚠️ Avisos inteligentes:** se muestra un aviso si eres funcionario en prácticas (puntuación real 0), si la compensatoria no es del último destino, o si las tutorías son anteriores a 2007 o las tutorizaciones de funcionarios/as en prácticas a 2023/24.

### ✨ 4. Interfaz, Usabilidad y Accesibilidad
*   **🌙 Modo oscuro nativo:** con persistencia en `localStorage` y detección automática del tema del sistema. Se ha ajustado el contraste de todos los elementos para garantizar su legibilidad.
*   **👨‍💻 Diseño:** fondo dinámico de tonos verdosos con un movimiento ondulado. Se han añadido detalles estéticos en todos los iconos, botones y menús.
*   **Bienvenida sin barra lateral:** el bloqueo del fondo se aplica antes de cargar los recursos externos. La tarjeta oculta su barra, pero mantiene el desplazamiento táctil en pantallas pequeñas; al entrar, la calculadora recupera su scroll normal.
*   **📈 Barras de progreso:** cada apartado incluye una barra visual que se llena según los puntos obtenidos. Al llegar al tope, aparece una píldora verde de «Máximo alcanzado».
*   **🔢 Formato numérico profesional:** todas las cifras usan fuente monoespaciada y ceros tachados (`Ø`) para evitar confusiones con la letra "O". El resumen se ha rediseñado para albergar totales de 3 dígitos y 4 decimales.
*   **🔀 Selectores interactivos EOI/ACLES:** botones que atenúan la caja del idioma que no corresponde y muestran un aviso dinámico, evitando que se introduzcan méritos en el lugar equivocado.
*   **Certificados ordenados:** los desplegables de ACLES y de puestos bilingües presentan los títulos alfabéticamente por su denominación visible dentro del nivel elegido. Unifican entidad, nombre, siglas y nivel, respetando las mayúsculas de las siglas; 5.5 añade los puntos. El resumen y el PDF utilizan las mismas denominaciones sin cambiar los identificadores guardados.
*   **Aviso ACLES en bilingües:** al seleccionar una acreditación no reconocida en la tabla utilizada (rev. 28/07/2025), aparece un aviso rojo: puede acreditar el acceso bilingüe, pero no puntúa como idioma en 5.5. No se aplica a EOI, ni excluye posibles méritos académicos en el apartado 3. Las denominaciones o equivalencias pendientes se señalan para revisión, sin afirmar que estén excluidas.
*   **💾 Guardado automático:** el progreso se guarda automáticamente, aunque se refresque o se cierre la página.
*   **🗑️ Borrado seguro:** se ha añadido un modal de confirmación antes de borrar todos los datos.
*   **💡 _Feedback_ integrado:** botón de sugerencias que enlaza a un Google Forms, y botón directo de «Inscribirse en el concurso». 
*   **📱 PWA (Aplicación web instalable):** se ha añadido un `manifest.json` y un _Service Worker_ para que la calculadora se pueda instalar en Android/iOS como si fuera una _app_ nativa.
*   **🖨️ Informe de impresión rediseñado:** cabecera con total, desglose a dos columnas y marca temporal obtenida de un servidor horario web (con _fallback_ al reloj del dispositivo).
*   **♿ Accesibilidad:** uso de `aria-label`, `aria-current`, `aria-live`, `role="dialog"` y _focus rings_ visibles.

---

### ⚠️ Aviso
Herramienta **NO OFICIAL** de simulación. Los autores no se responsabilizan de posibles errores. Para el cálculo definitivo y vinculante, consultar siempre el **BOJA n.º 210, de 29/10/2026**:  
[https://www.juntadeandalucia.es/boja/2026/210/16](https://www.juntadeandalucia.es/boja/2026/210/16)

---

### 🙏 Créditos
*   Basada en el trabajo original de **MaestroRafa** — [https://github.com/rbuegon523/calculadoraCGT](https://github.com/rbuegon523/calculadoraCGT) (2025).
*   Adaptación al baremo 2026, rediseño de interfaz y nuevas funcionalidades: **fcallejah** — [https://github.com/fcallejah/calculadoraCGT](https://github.com/fcallejah/calculadoraCGT).
*   *Modificada con muchísimo cariño desde Cuevas Bajas (Málaga)* 🥕 💜 🫒 🏞️
