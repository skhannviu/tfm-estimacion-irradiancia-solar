# Registro de interacciones con Claude (Anthropic)
## TFM: Comparación entre modelos físicos y modelos de aprendizaje automático para la estimación de la irradiación solar

**Herramienta:** Claude Opus (Anthropic)
**Periodo:** Mayo – Julio 2026
**Total de conversaciones en el proyecto:** 4
**Propósito general:** Revisión del notebook experimental, redacción de secciones de la memoria, aplicación de correcciones del tutor, generación de diagramas conceptuales, verificación de coherencia y experimentos de robustez.

---

## Conversación 1: Diseño de la skill de redacción y redacción inicial (Mayo 2026)

### Prompt 1 — Creación de la skill de redacción
**Prompt:** "Necesito crear una skill personalizada para mi TFM que establezca las reglas de estilo, formato y terminología que debo seguir en toda la memoria."
**Respuesta (resumen):** Se creó un archivo `tfm-viu-redaccion_SKILL.md` con reglas de formato VIU (Arial 11pt, interlineado 1.15, márgenes específicos), estilo académico impersonal, terminología correcta (irradiancia vs irradiación, cenital vs zenital, componente en femenino), prohibición de rayas largas, y ejemplos de transformación de registro informal a académico.

### Prompt 2 — Redacción de la Introducción
**Prompt:** "Tienes mi bibliografía ya añadida a la memoria de este proyecto y siéntete libre de encontrar más si es preciso. [Se adjuntó el borrador de objetivos y el notebook]"
**Respuesta (resumen):** Se redactó la Introducción completa (~1.100 palabras) con la estructura: contexto energético → problema de descomposición → motivación Canarias → pregunta de investigación → estructura del documento. Se identificaron tres citas pendientes ([CITA]) que se resolvieron posteriormente con el Estado del Arte.

### Prompt 3 — Redacción del Estado del Arte
**Prompt:** "Corríjeme [borrador del Estado del Arte con secciones 3.1 a 3.7]"
**Respuesta (resumen):** Revisión completa del marco teórico. Correcciones principales: fecha de Kasten verificada como 1964, modelo de Perez identificado como versión simplificada de 1990 (no DIRINT 1992), adición de párrafos sobre fundamentos de ML (escalado, validación cruzada, hiperparámetros) al final de la sección 3.3, y formulación de hipótesis principal con dos secundarias en sección 3.7.

### Prompt 4 — Redacción de Metodología y Desarrollo
**Prompt:** "Corríjeme [borrador de Metodología] y lo ves bien? es corto? [borrador de Desarrollo]"
**Respuesta (resumen):** Revisión de las secciones 4 y 5. Se añadieron: justificación del enfoque en DNI vs DHI, nota sobre datos horarios ≠ series temporales, tabla de hiperparámetros (Tabla 5.1), párrafo de transparencia sobre implementaciones simplificadas de modelos físicos, y descripción expandida del modelo híbrido de dos etapas.

---

## Conversación 2: Finalización de la primera entrega al tutor (Junio 2026)

### Prompt 5 — Lista de referencias APA
**Prompt:** "Necesito compilar todas las referencias en APA 7ª edición."
**Respuesta (resumen):** Se generó la lista completa de 41 referencias en formato APA 7ª edición, verificando que cada referencia citada en el texto existiera en la lista y viceversa. Se corrigió la cita de Yang de "Yang en 2024" a "Yang et al. (2024)" y se añadió un espacio en la referencia de Maxwell antes de "(Informe técnico".

### Prompt 6 — Declaración de uso de IA (Anexo A)
**Prompt:** "Necesito redactar la declaración obligatoria de uso de IA generativa."
**Respuesta (resumen):** Redacción del Anexo A declarando el uso de Claude (búsqueda bibliográfica, revisión de código, redacción de borradores, verificación), Gemini (programación, revisión de código) y Consensus (localización de artículos). Se incluyó la frase de que el diseño, análisis, hipótesis y conclusiones son de elaboración propia.

### Prompt 7 — Lista de acrónimos
**Prompt:** "Necesito crear la lista de acrónimos."
**Respuesta (resumen):** Se generó una lista de 23 acrónimos (AOD, CSP, DHI, DNI, EDA, GBR, GHI, kNN, MAE, ML, MLP, NSRDB, REC, RF, RMSE, R², SVR, etc.) con sus significados en español e inglés.

### Prompt 8 — Expansión de la Discusión
**Prompt:** "La sección de Discusión es demasiado corta. Necesito expandirla con contraste con la literatura."
**Respuesta (resumen):** La Discusión se expandió de 685 a ~1.472 palabras añadiendo: convergencia con GISPLIT (Ruiz-Arias y Gueymard, 2024), comparación con Yang5, mecanismo de Galway como prueba de esfuerzo, asimetría DNI/DHI, mecanismo exacto del híbrido, e implicaciones prácticas. Cada párrafo se vinculó con una referencia del Estado del Arte.

### Prompt 9 — Correcciones de precisión
**Prompt:** "Revisa todo el documento y corrige errores de precisión."
**Respuesta (resumen):** Correcciones aplicadas: "DIRINT" eliminado (el notebook usa Perez 1990 simplificado), "alta resolución espectral" → "alta resolución temporal de un minuto" para Gueymard, MLP RMSE de 50,51 → 50,41, Grenoble MAE de 16,78 → 12,56, RF de 44,01 → 45,01 en conclusiones, "residencial" → "residual" (3 instancias), MLP corregido de "clasificador" a "regresor", R² por ciudad de 2 a 3 decimales (rango final 0,899–0,997).

### Prompt 10 — Correcciones terminológicas
**Prompt:** "Revisa la terminología no estándar."
**Respuesta (resumen):** Se corrigieron: "minutal" → "de un minuto", "subentrena/subentrenan" → "rinde por debajo de" / "muestran un acusado subajuste" (3 instancias), "subrendimiento" → "bajo rendimiento", "zenital" → "cenital" (consistencia en todo el documento), "intervalos probabilísticos de confianza" → "intervalos de predicción".

---

## Conversación 3: Aplicación de correcciones del tutor (Julio 2026)

### Prompt 11 — Corrección del Resumen: definir irradiancia
**Prompt:** "Mi tutor dice: 'Tienes que explicar qué es la irradiancia antes, para que se entienda por qué la DNI es importante.' [Se adjuntó el párrafo del Resumen]"
**Respuesta (resumen):** Se añadió una frase introductoria definiendo las tres componentes (GHI, DNI, DHI) antes de centrar el foco en la DNI.

### Prompt 12 — Corrección del Resumen: terminología de ensamble
**Prompt:** "El tutor dice: 'RF y GB ya son ensamble por ellos mismos (bagging y boosting).' [Se adjuntó el párrafo con 'ensamble por promedio']"
**Respuesta (resumen):** Se sustituyó "ensamble por promedio" por "combinador por promedio (Voting Regressor) que fusiona las salidas de los dos mejores regresores basados en árboles", distinguiéndolo del ensamble interno de RF y GB.

### Prompt 13 — Traducción del Abstract
**Prompt:** "El tutor dice que el Abstract debe ser la traducción fiel del Resumen final."
**Respuesta (resumen):** Se generó el Abstract completo como traducción fiel del Resumen corregido, manteniendo la misma estructura, cifras y matices.

### Prompt 14 — Figura de descomposición solar en Introducción
**Prompt:** "El tutor dice: 'Aquí es recomendable que pongas una figura para que se entienda esto a simple vista.' [Sobre el párrafo que define GHI, DNI, DHI]"
**Respuesta (resumen):** Se confirmó que la Figura 1.1 (diagrama de descomposición solar generado con Claude Design) corresponde a esta corrección. Se integró la referencia en el párrafo y se generó la nota APA.

### Prompt 15 — Declaración de IA movida a Anexo
**Prompt:** "El tutor dice: 'Esto debe ir en un apartado aparte, al final.' [Sobre el párrafo de uso de IA en la Introducción]"
**Respuesta (resumen):** Se eliminó el párrafo de la Introducción y se creó el Anexo A con la declaración completa, detallando el alcance de cada herramienta y las figuras generadas con asistencia de IA.

### Prompt 16 — Datos horarios ≠ series temporales
**Prompt:** "El tutor dice: 'Es importante que destaques que, aunque los datos sean horarios, no estamos hablando de modelos de series temporales.'"
**Respuesta (resumen):** Se añadió un párrafo en la sección 4.1 explicando que el enfoque es de regresión instantánea (cada registro es independiente), sin dependencia temporal, y que LSTM/GRU se proponen como línea futura.

### Prompt 17 — EDA previo al preprocesamiento
**Prompt:** "El tutor pregunta: '¿No hay un EDA previo?' [En la sección de Preprocesamiento]"
**Respuesta (resumen):** Se añadió un párrafo introductorio en 4.2 con referencia cruzada a la Sección 5.2 donde se detalla el EDA.

### Prompt 18 — Herramientas y tecnologías
**Prompt:** "El tutor dice: 'En algún lugar debes hablar de las herramientas que vas a usar (Python, qué librerías, etc.)'"
**Respuesta (resumen):** Se confirmó que la información ya existía en la Sección 5.1 y se añadió una referencia cruzada en la Sección 4.4.

### Prompt 19 — Fundamentos de ML en el marco teórico
**Prompt:** "El tutor dice: 'Hay que explicar qué es cada cosa y por qué se hace: escalado, validación cruzada, preprocesamiento.' [En la sección de Escalado]"
**Respuesta (resumen):** Se redactaron tres párrafos sobre estandarización, validación cruzada y optimización de hiperparámetros para insertar al final de la Sección 3.3 del Marco Teórico, con referencias a Arlot y Celisse (2010) y Bergstra y Bengio (2012).

### Prompt 20 — Justificación de cv=3
**Prompt:** "El tutor dice: 'Es raro usar 3 pliegues. Generalmente se toman 5 o 10.' ¿Significa que hemos hecho mal la validación?"
**Respuesta (resumen):** Se explicó que cv=3 se usa solo para optimización de hiperparámetros (no para evaluación final, que es el Spatial Split) y se redactó una justificación basada en dos razones: el entrenamiento proviene de solo 2 ciudades similares, y la prueba real de generalización es la división espacial.

### Prompt 21 — Métricas en afirmaciones comparativas
**Prompt:** "El tutor dice: 'Hay que intentar especificar en qué superan unos modelos a otros (usando alguna métrica).' ¿Dónde más aplica esto?"
**Respuesta (resumen):** Se identificaron 4 párrafos en la Sección 3.5 (Trabajos previos) donde faltaban métricas concretas. Se añadieron: MBD 0,96% y 0,03% para Ramadhan, R² > 0,97 para Bounoua, "RMSE y sesgo medio" para Lemos y Nunez Munoz, y "RMSE y R²" para Rajagukguk.

### Prompt 22 — Fusión de Resultados y Discusión
**Prompt:** "El tutor dice: 'Resultados y Discusión deben ir en el mismo apartado.' [Se adjuntaron las secciones 6 y 7 completas]"
**Respuesta (resumen):** Se proporcionó un mapa detallado de dónde mover cada párrafo de la antigua Sección 7 (Discusión) dentro de la Sección 6 (Resultados), subsección por subsección, sin perder ninguna frase. La Sección 7 se eliminó y las Conclusiones pasaron a ser Sección 7.

### Prompt 23 — Figuras del notebook: selección y ubicación
**Prompt:** "Indícame dónde van estas figuras en el documento, y si hay que cambiar algún párrafo para que encaje mejor la gráfica. [Se adjuntaron 10 figuras del notebook]"
**Respuesta (resumen):** Se creó un mapa completo de 14 figuras (10 del notebook + 4 conceptuales) con: ubicación exacta en el documento, pie de figura en formato APA, y párrafos de acompañamiento para cada una.

### Prompt 24 — Títulos y notas de tablas y figuras
**Prompt:** "¿Cómo van los títulos y los pies de tabla?"
**Respuesta (resumen):** Se explicó el formato APA 7ª: número en negrita encima, título en cursiva debajo del número, y nota con "Nota." en cursiva debajo del contenido. Se proporcionaron los 6 títulos de tablas y las 14 notas de figuras completas.

### Prompt 25 — Corrección del tutor sobre notas de figuras
**Prompt:** "El tutor dice: 'No me gusta que la descripción aparezca como pie de figura. Puedes poner que la fuente es elaboración mediante IA y describir la figura en el propio texto.'"
**Respuesta (resumen):** Se revisaron las 14 figuras, moviendo todas las descripciones de las notas al párrafo correspondiente del texto y dejando las notas solo con la fuente ("Nota. Elaboración propia.").

### Prompt 26 — Experimentos de robustez: código
**Prompt:** "Quiero probar a cambiar la validación cruzada en 3 pliegues. ¿Puedes darme código para probar 3, 5 y 10 pliegues, y también Leave-One-City-Out, sensibilidad del umbral y curvas de aprendizaje?"
**Respuesta (resumen):** Se generó el código completo de 4 experimentos de robustez: (1) sensibilidad al número de pliegues (versión rápida con cross_val_score), (2) Leave-One-City-Out, (3) sensibilidad del umbral del clasificador (7 valores), y (4) curvas de aprendizaje (5 fracciones). Incluía tablas, gráficos y conclusiones automáticas.

### Prompt 27 — Interpretación de resultados de robustez
**Prompt:** "Estos son los resultados de los 4 experimentos. ¿Puedes interpretarlos y decirme si son buenos o malos? [Se adjuntaron los outputs numéricos y las gráficas]"
**Respuesta (resumen):** Interpretación: (1) cv=3, 5 y 10 dan resultados idénticos en test → cv=3 justificado; (2) LOCO: entrenar con una sola ciudad da MEJOR rendimiento (RMSE 38,90) que con ambas (45,01) → la diversidad importa más que el volumen; (3) umbral del híbrido varía solo 0,42 W/m² en todo el rango → robusto; (4) curvas de aprendizaje planas desde el 10% de datos → un año es suficiente, el cuello de botella es la distancia climática. Se redactó el párrafo para la sección 6.7 de la memoria.

### Prompt 28 — Gráficas de paridad
**Prompt:** "El tutor sugiere: 'Puedes representar alguna gráfica de paridad (valores predichos vs valores reales).' ¿Puedes darme el código?"
**Respuesta (resumen):** Se generó el código para una figura con tres paneles (Erbs, Random Forest, Híbrido) con scatter de valores estimados vs observados, línea diagonal de ajuste perfecto, y métricas RMSE y R² incrustadas. Se proporcionó el título APA, la nota y el párrafo descriptivo para insertar en la sección 6.2.

### Prompt 29 — ODS y planificación temporal
**Prompt:** "¿Se pide algún apartado de organización del proyecto? Porque tengo un diagrama de Gantt sin usar."
**Respuesta (resumen):** Se verificó que el Gantt no es obligatorio pero sí lo es la vinculación con los ODS. Se redactó un párrafo sobre ODS 7 (Energía asequible) y ODS 13 (Acción por el clima) para incluir al final de la Introducción.

### Prompt 30 — Revisión final del documento
**Prompt:** "Te paso la última versión del TFM. Necesito que revises que cumple extensión, que tenga todos los apartados y que revises coherencia y fluidez, especialmente las conclusiones."
**Respuesta (resumen):** Revisión completa: 621 párrafos, 21.208 palabras, ~62 páginas de texto neto (cumple 40-80). Todas las secciones obligatorias presentes. Las 3 hipótesis recuperadas en conclusiones. Se detectaron 3 referencias cruzadas rotas, 1 URL pendiente, y 3 ajustes en conclusiones: faltaba mención a experimentos de robustez (añadida), el análisis de sensibilidad del umbral ya no era "no ejecutado" (corregido), y la línea futura de sensibilidad ya no procedía (reformulada).

---

## Conversación 4: Correcciones finales y preparación del repositorio (Julio 2026)

### Prompt 31 — Revisión de correcciones pendientes en PDF
**Prompt:** "Te envío mi última versión en PDF para que me lo corrijas y me digas cuáles de las 5 correcciones pendientes me quedan."
**Respuesta (resumen):** Las 5 correcciones pendientes (minutal, subentrena, zenital, R² rango, binariza) estaban todas resueltas. Se detectaron 2 nuevos pendientes: fecha de portada incompleta y URL del repositorio como placeholder en 3 sitios.

---

## Notas generales

- Las salidas generadas por Claude fueron en todos los casos revisadas, verificadas y adaptadas antes de su incorporación al proyecto.
- El diseño de la investigación, la selección de la metodología, la implementación del código experimental, el análisis e interpretación de los resultados, el planteamiento de las hipótesis y la formulación de las conclusiones son de elaboración propia.
- Claude Design (Anthropic) se empleó para el refinamiento visual de cuatro diagramas conceptuales: descomposición solar (Figura 1.1), flujo metodológico (Figura 4.1), Spatial Split (Figura 4.2) y arquitectura híbrida (Figura 5.6).
- Total de prompts documentados con Claude: 31 (selección representativa de interacciones más extensas).
