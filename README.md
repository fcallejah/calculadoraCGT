# Calculadora CGT Andalucía 2026

Calculadora para el **Concurso General de Traslados 2026** en **Andalucía** (Cuerpo de Maestros y Secundaria), basada en la calculadora original de [MaestroRafa](https://github.com/rbuegon523/calculadoraCGT) (2025) y adaptada al baremo publicado en el **BOJA n.º 210, de 29 de octubre de 2026**.

✅ Accesible aquí (https://fcallejah.github.io/calculadoraCGT/) ✅


## 📋 Adaptación al baremo 2026

*   **🗣️ Idiomas separados EOI (3.3) y ACLES (5.5):** nueva sección 5.5 para certificados internacionales (Cambridge, TOEFL, DELF, Goethe…). Los certificados EOI siguen puntuando en 3.3.
*   **🎭 Sección 6.3 completamente reescrita** conforme al BOJA (DC Quinta.5): premios internacionales, nacionales y autonómicos; espectáculos (gran formato y cámara), composiciones, actuaciones destacadas y secundarias, exposiciones, conservador-restaurador y deportista de alto nivel o rendimiento.
*   **📚 Nuevas obras literarias en 6.1** con su propia tabla (autor, coautor, 3+ autores e ilustrador/a a 0,2 ptos.).
*   **🏫 Coordinación del Plan de Igualdad** como mérito específico en 6.2 (1,0 pto./curso, frente a 0,5 del resto de proyectos).
*   **🎓 Múltiples títulos computables en 3.1:** doctor, DEA y máster pasan de casilla única a contador, permitiendo alegar varios títulos.
*   **🎓 Premio extraordinario** ampliado a doctorado o grado.
*   **🏅 Técnico deportivo superior y técnico superior de FP** incluidos junto a Artes Plásticas/Diseño en 3.3.
*   **👩‍🏫 Tutorización 6.6 diferenciada:** máster/grado (0,1 pto./curso) frente a fase de aspirantes seleccionados desde 2023/24 (0,2 ptos./curso).
*   **🧮 Aclaraciones normativas** en 1.1 (solo último destino definitivo, excepciones por supresión, sentencia o excedencia forzosa), 1.2.1 (mismo cuerpo, cualquier especialidad) y 5.1 (equivalencia de créditos: 1 crédito tradicional = 10 h; 1 ECTS = 25 h).
*   **💻 CDD renombrada a "Competencia Digital Docente"** con niveles A1–C2 sin cambios de puntuación.


## 🧮 Mejoras en el cálculo y la baremación

*   **📅 Fecha de corte real (26/11/2026):** el cálculo de antigüedad y experiencia ya no se detiene el 31/10, sino en el fin del plazo de solicitudes, para que compute correctamente el segundo mes (septiembre/octubre) tal como exige la Junta.
*   **⚖️ Corrección del tope en 6.2:** solucionado el bug que permitía superar los 2,5 ptos. máximos en premios y proyectos. Ahora el sumatorio respeta el límite legal.
*   **📊 Desglose completo del 4.3 (Coordinación y tutoría):** se han creado cajas individuales para jefatura de departamento, coordinación de ciclo/EOE/CEP y tutoría, cada una con sus propios campos de años y meses, en lugar de una única caja genérica.
*   **🇪🇸 Lista de idiomas EOI ampliada:** ahora incluye 22 idiomas oficiales, incorporando lenguas cooficiales como el valenciano, catalán, euskera y gallego, tal como permite la disposición complementaria segunda del BOJA.


## ✨ Mejoras de usabilidad e interfaz

*   **🧙‍♂️ Cuestionario de antigüedad renovado:**
    *   **Fechas por defecto (1 de septiembre):** los calendarios arrancan en el 1 de septiembre más reciente para agilizar la introducción de datos.
    *   **Validación estricta de fechas:** el sistema impide que la fecha de nombramiento como funcionario de carrera sea anterior a la de prácticas o que supere un margen lógico de 2 años.
    *   **Checkbox de estabilización:** nueva casilla para marcar "No realicé prácticas / Accedí por estabilización", que iguala automáticamente las fechas y evita confusiones.
    *   **Textos más claros:** se ha reescrito la pregunta del destino definitivo para que no haya dudas: *"Destino definitivo actual, ¿desde cuándo estás en tu centro más reciente con plaza definitiva?"*.
*   **⚠️ Aviso para funcionarios en prácticas:** tanto en la pestaña de Antigüedad como en el resumen, se muestra un mensaje indicando que la puntuación real en el concurso será 0, ya que el proceso es exclusivo para funcionarios de carrera.
*   **🔀 Selector interactivo EOI / ACLES:** en los apartados 3.3 y 5.5 se han añadido botones para elegir el origen del título. Al seleccionar una opción, la caja contraria se atenúa y aparece un aviso con el icono SVG de advertencia, evitando que se introduzcan méritos en el lugar equivocado.
*   **📈 Barras de progreso y "Máximo alcanzado":** cada apartado del baremo cuenta ahora con una barra de progreso visual. Al llegar al tope de puntos, se muestra una píldora verde de "Máximo alcanzado".
*   **🔢 Formato numérico profesional:** todas las cifras usan fuente monoespaciada y ceros tachados (`Ø`) para distinguirlos de la letra "O". El resumen se ha rediseñado para que los totales de 3 dígitos (ej. 131,3666) tengan espacio suficiente.


## 🌙 Modo oscuro y accesibilidad

*   **Modo oscuro con persistencia** (localStorage) y detección automática del tema del sistema.
*   **Contraste mejorado en modo oscuro:** se han ajustado los colores de las pestañas, botones (BOJA, acceso al concurso) y puntuaciones para que se lean perfectamente sobre fondos oscuros.
*   **Guardado automático del progreso** en localStorage (`cgt2026_v1`).
*   **Confirmación antes de borrar** todos los datos (modal accesible).
*   **Desglose de méritos en el resumen:** tabla con el detalle bruto de cada mérito introducido antes de aplicar topes.
*   **Informe de impresión rediseñado:** cabecera con total, desglose a dos columnas y marca temporal obtenida de un servidor horario web (Europe/Madrid) con *fallback* al reloj del dispositivo.
*   **Pestañas desplazables** con flechas en móvil y navegación "Apartado previo / Siguiente" al pie de cada sección.
*   **Formato numérico español** (coma decimal, "ptos.").
*   **Favicon SVG propio** y *branding* revisado con enlace al repositorio y a la resolución del BOJA.
*   **Accesibilidad:** `aria-label`, `aria-current`, `aria-live`, `role="dialog"`, *focus rings* visibles.


## ⚠️ Aviso

Herramienta **NO OFICIAL** de simulación. Los autores no se responsabilizan de posibles errores. Para el cálculo definitivo y vinculante, consultar siempre el **BOJA n.º 210, de 29/10/2026**:  
[https://www.juntadeandalucia.es/boja/2026/210/16](https://www.juntadeandalucia.es/boja/2026/210/16)


## 🙏 Créditos

*   Basada en el trabajo original de **MaestroRafa** — [https://github.com/rbuegon523/calculadoraCGT](https://github.com/rbuegon523/calculadoraCGT) (2025).
*   Adaptación al baremo 2026 y mejoras de usabilidad: **fcallejah** — [https://github.com/fcallejah/calculadoraCGT/tree/fcallejah-boja-2026-updates](https://github.com/fcallejah/calculadoraCGT/tree/fcallejah-boja-2026-updates)
