# Calculadora CGT Andalucía 2026

Calculadora para el **Concurso General de Traslados 2026** en **Andalucía** (Cuerpo de Maestros y Secundaria), basada en la calculadora original de [MaestroRafa](https://github.com/rbuegon523/calculadoraCGT) (2025) y adaptada al baremo publicado en el **BOJA n.º 210, de 29 de octubre de 2026**.

## 📋 Adaptación al baremo 2026

- 🗣️ **Idiomas separados EOI (3.3) y ACLES (5.5)**: nueva sección 5.5 para certificados internacionales (Cambridge, TOEFL, DELF, Goethe…). Los certificados EOI siguen puntuando en 3.3.
- 🎭 **Sección 6.3 completamente reescrita** conforme al BOJA (DC Quinta.5): premios internacionales/nacionales/autonómicos, espectáculos (gran formato y cámara), composiciones, actuaciones destacadas/secundarias, exposiciones, conservador-restaurador y deportista de alto nivel/rendimiento.
- 📚 **Nuevas obras literarias en 6.1** con su propia tabla (autor, coautor, 3+ autores e ilustrador/a a 0,2).
- 🏫 **Coordinación del Plan de Igualdad** como mérito específico en 6.2 (1,0 ptos./curso, frente a 0,5 del resto de proyectos).
- 🎓 **Múltiples títulos computables en 3.1**: Doctor, DEA y Máster pasan de casilla única a contador, permitiendo alegar varios títulos.
- 🎓 **Premio extraordinario** ampliado a doctorado **o grado**.
- 🏅 **Técnico Deportivo Superior y Técnico Superior de FP** incluidos junto a Artes Plásticas/Diseño en 3.3.
- 👩‍🏫 **Tutorización 6.6 diferenciada**: máster/grado (0,1/curso) vs. fase de aspirantes seleccionados desde 2023/24 (0,2/curso).
- 🧮 **Aclaraciones normativas** en 1.1 (solo último destino definitivo, excepciones por supresión/sentencia/excedencia forzosa), 1.2.1 (mismo cuerpo, cualquier especialidad) y 5.1 (equivalencia créditos: 1 crédito tradicional = 10 h; 1 ECTS = 25 h).
- 💻 **CDD** renombrada a "Competencia Digital Docente" con niveles A1–C2 sin cambios de puntuación.

## ✨ Mejoras de usabilidad

- 🌙 **Modo oscuro** con persistencia (`localStorage`) y detección automática del tema del sistema.
- 💾 **Guardado automático** del progreso en `localStorage` (`cgt2026_v1`).
- 🗑️ **Confirmación antes de borrar** todos los datos (modal accesible).
- 🧾 **Desglose de méritos** en la pestaña Resumen: tabla con el detalle bruto de cada mérito introducido antes de aplicar topes.
- 🖨️ **Informe de impresión rediseñado**: cabecera con total, desglose a dos columnas, y marca temporal obtenida de un **servidor horario web** (Europe/Madrid) con fallback al reloj del dispositivo.
- 📱 **Pestañas desplazables** con flechas en móvil y **navegación "Apartado previo / Siguiente"** al pie de cada sección.
- 🇪🇸 **Formato numérico español** (coma decimal, "ptos.").
- 🎨 **Favicon SVG** propio y branding revisado con enlace al repositorio y a la resolución del BOJA.
- ♿ **Accesibilidad**: `aria-label`, `aria-current`, `aria-live`, `role="dialog"`, focus rings visibles.

## ⚠️ Aviso

Herramienta **NO OFICIAL** de simulación. Los autores no se responsabilizan de posibles errores. Para el cálculo definitivo y vinculante, consultar siempre el **BOJA n.º 210, de 29/10/2026**: https://www.juntadeandalucia.es/boja/2026/210/16

## 🙏 Créditos

Basada en el trabajo original de **MaestroRafa** — https://github.com/rbuegon523/calculadoraCGT (2025).
Adaptación al baremo 2026: **fcallejah** — https://github.com/fcallejah/calculadoraCGT
