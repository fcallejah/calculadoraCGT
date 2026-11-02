# Calculadora Concurso Traslados Andalucía 2026

Esta versión 2026 es una actualización de [MaestroRafa](https://github.com/rbuegon523/calculadoraCGT) al nuevo baremo y una **reescritura y modernización completa** de la herramienta de 2025. Se ha transformado una calculadora básica en una aplicación web (PWA) profesional, adaptada milimétricamente al [**BOJA n.º 210, de 29 de octubre de 2026**](https://www.juntadeandalucia.es/boja/2026/210/16).

✅ Accesible aquí (https://fcallejah.github.io/calculadoraCGT/) ✅


### 📋 1. Adaptación Normativa (baremo 2026)
*   **🗣️ Idiomas separados (3.3 y 5.5):** se ha creado una sección exclusiva para certificados internacionales (ACLES) en el 5.5, liberando el 3.3 para la Escuela Oficial de Idiomas (EOI). Se incluye un buscador dinámico de certificados ACLES.
*   **🇬🇧 Lista de idiomas EOI ampliada:** ahora incluye 22 idiomas oficiales, incorporando lenguas cooficiales (catalán, euskera, gallego y valenciano) según la disposición complementaria segunda del BOJA.
*   **🤟 Nuevo mérito DLSE (3.3):** añadida caja específica para los Diplomas de Lengua de Signos Española (B1–C2) con su puntuación correspondiente y enlace oficial al CNLSE.
*   **🎭 Sección 6.3 reescrita:** se ha desglosado completamente el apartado de méritos artísticos y deportivos (premios, espectáculos, composiciones, actuaciones, exposiciones, conservador-restaurador y deportistas).
*   **📚 Obras literarias (6.1):** nueva tabla específica para autor, coautor, 3+ autores e ilustrador/a.
*   **💜 Plan de Igualdad (6.2):** añadido como mérito específico (1,0 pto./curso).
*   **🎓 Múltiples títulos (3.1 y 3.2):** los títulos de doctor, DEA y máster pasan de ser casillas únicas a contadores, permitiendo alegar varios títulos a la vez.

### 🧮 2. Correcciones críticas de cálculo
*   **📅 Fecha de corte exacta (26/11/2026):** el cálculo de antigüedad (1.1 y 1.2) ya no se detiene el 31 de octubre. Ahora computa hasta la fecha de fin de plazo de solicitudes, reflejando correctamente los dos meses (septiembre y octubre) del año en curso, 2026.
*   **⚖️ Bug del 6.2 solucionado:** se ha corregido el error que permitía superar el tope máximo de **2,5 ptos.** en premios y proyectos. Se ha aplicado un `Math.min` estricto en todos los apartados para garantizar que nunca se sobrepasen los límites legales.
*   **📊 Desglose del 4.3 (coordinación):** se ha dividido la caja genérica en **tres apartados independientes** (jefatura de departamento, coordinación de ciclo/EOE/CEP y tutoría LOE), cada uno con su propia caja de años/meses.
*   **👩‍🏫 Tutorización (6.6) diferenciada:** máster/grado (0,1 pto./curso) frente a fase de aspirantes (0,2 ptos./curso), con un aviso para los cursos anteriores a 2023/24.

### 🧙‍♂️ 3. El nuevo cuestionario de Antigüedad
Se ha pasado de tener simples cajas de texto a un **asistente interactivo (Wizard)** de varios pasos:
*   **📅 Fechas por defecto:** los calendarios arrancan automáticamente en el 1 de septiembre más reciente.
*   **🛡️ Validación estricta:** el sistema bloquea fechas de carrera anteriores a las de prácticas o que superen un margen lógico de 2 años. Además, se ha implementado un campo de texto `dd/mm/aaaa` sincronizado con el calendario nativo.
*   **🔄 Casilla de estabilización:** nueva casilla para marcar «No realicé prácticas / Accedí por estabilización», que iguala automáticamente las fechas.
*   **⚠️ Avisos inteligentes:** se muestra un aviso si eres funcionario en prácticas (puntuación real 0), si la compensatoria no es del último destino, o si las tutorías son anteriores a 2007 o las tutorizaciones de funcionarios/as en prácticas a 2023/24.

### ✨ 4. Interfaz, Usabilidad y Accesibilidad
*   **🌙 Modo oscuro nativo:** con persistencia en `localStorage` y detección automática del tema del sistema. Se ha ajustado el contraste de todos los elementos para garantizar su legibilidad.
*   **👨‍💻 Diseño:** fondo dinámico de tonos verdosos con un movimiento ondulado. Se han añadido detalles estéticos en todos los iconos, botones y menús.
*   **📈 Barras de progreso:** cada apartado incluye una barra visual que se llena según los puntos obtenidos. Al llegar al tope, aparece una píldora verde de «Máximo alcanzado».
*   **🔢 Formato numérico profesional:** todas las cifras usan fuente monoespaciada y ceros tachados (`Ø`) para evitar confusiones con la letra "O". El resumen se ha rediseñado para albergar totales de 3 dígitos y 4 decimales.
*   **🔀 Selectores interactivos EOI/ACLES:** botones que atenúan la caja del idioma que no corresponde y muestran un aviso dinámico, evitando que se introduzcan méritos en el lugar equivocado.
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
