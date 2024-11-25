# Detector de comentarios toxicos en redes sociales
Introducción
La toxicidad en redes sociales es un problema global que afecta tanto a usuarios como a creadores de contenido. Comentarios maliciosos, insultos, y lenguaje dañino han generado un ambiente virtual hostil que impacta la salud mental y el bienestar emocional de muchas personas, especialmente adolescentes y jóvenes.

Este proyecto se centra en el desarrollo de un sistema de detección automática de comentarios tóxicos utilizando Procesamiento del Lenguaje Natural (NLP) y modelos de aprendizaje automático. Nuestro objetivo es proporcionar una herramienta eficaz para identificar y mitigar la exposición a contenido dañino, promoviendo así interacciones en línea más saludables.

Estructura del Proyecto
El repositorio incluye las siguientes carpetas:

-Notebooks de modelos: Contiene todos los notebooks utilizados para entrenar los modelos de clasificación, desde enfoques tradicionales hasta redes neuronales avanzadas.
-Preprocesamiento de la base de datos: Incluye los pasos y scripts utilizados para procesar y limpiar los datos antes del entrenamiento de los modelos.
-Base de datos: Debido al tamaño de los datos, encontrarás un archivo .txt con un enlace para acceder a la base utilizada en este proyecto.

Requisitos
Este proyecto está diseñado para ejecutarse directamente en Google Colab, sin necesidad de instalar recursos adicionales. Asegúrate de importar las bibliotecas mencionadas en los notebooks para un funcionamiento correcto.

Desarrollo del Proyecto
El sistema utiliza un ensamble de modelos que combina diferentes enfoques para maximizar la precisión:

-Naive Bayes: Detecta rápidamente insultos y palabras ofensivas explícitas.
-LSTM: Analiza el contexto y detecta toxicidad implícita en comentarios más largos y complejos.
-Análisis de Sentimientos (VADER): Complementa la detección al identificar tonos negativos y emociones maliciosas.

El flujo del modelo sigue los pasos de preprocesamiento, evaluación individual y combinación ponderada para clasificar los comentarios en categorías: No Tóxico, Posiblemente Tóxico y Tóxico.

Resultados del Ensamble Final
El modelo ensamblado, que combina las fortalezas de Naive Bayes, LSTM y el Análisis de Sentimientos (VADER), demostró un rendimiento sobresaliente, logrando una precisión global del 91% en pruebas con nuevos comentarios.

Principales Métricas del Ensamble:
-Precisión en comentarios no tóxicos: 89%.
-Precisión en comentarios posiblemente tóxicos: 85%.
-Precisión en comentarios tóxicos: 94%.

El enfoque integrado permitió cubrir una amplia variedad de patrones lingüísticos y matices emocionales, destacándose en la detección de toxicidad implícita y explícita. Además, este sistema es capaz de:

Identificar rápidamente insultos y palabras ofensivas (Naive Bayes).
Capturar contextos complejos y matices semánticos en comentarios largos (LSTM).
Detectar tonos negativos y maliciosos en textos con poca o ninguna toxicidad explícita (VADER).
El modelo ensamblado es una solución robusta y versátil para abordar la toxicidad en redes sociales, demostrando su potencial para aplicaciones reales en moderación de contenido.

Problemas y Desafíos Abordados
El desarrollo de un detector de comentarios tóxicos enfrenta diversos problemas y desafíos, muchos de los cuales aún están en proceso de resolverse:

-Diferencias lingüísticas y culturales: La percepción de toxicidad varía según el idioma y el contexto cultural. Esto hace necesario ajustar los modelos para que sean inclusivos y justos en diferentes escenarios.
-Sarcasmo e implicaciones sutiles: Detectar toxicidad implícita o sarcasmo sigue siendo complejo, ya que los comentarios pueden carecer de insultos directos, pero contener un tono malicioso o dañino.
-Lenguaje informal y abreviaturas: En redes sociales, el lenguaje suele estar lleno de jerga, errores ortográficos o abreviaturas que complican el análisis tradicional.
-Desequilibrio en los datos: La mayoría de los comentarios son no tóxicos, lo que genera un sesgo hacia esta clase. Este desequilibrio se abordó ajustando los pesos de las clases y aplicando técnicas de sobremuestreo y submuestreo.
-Limitaciones computacionales: Implementar modelos más avanzados como BERT no fue viable debido a la alta demanda de recursos de hardware, limitando las opciones exploradas.
-Sesgos inherentes a los datos: Los modelos pueden reflejar prejuicios presentes en las bases de datos de entrenamiento, lo que podría afectar la equidad en la clasificación de comentarios de ciertos grupos o culturas.

A pesar de estos desafíos, se adoptaron estrategias para mitigar varios de estos problemas, incluyendo el uso de técnicas como embeddings avanzados (GloVe y FastText) y un ensamble de modelos para aumentar la precisión y robustez del sistema.

Conclusión y Futuras Líneas de Trabajo
Este proyecto demuestra cómo las técnicas de NLP y machine learning pueden abordar problemas críticos en el entorno digital. Las futuras mejoras incluirán:

-Ampliación del conjunto de datos con múltiples idiomas y dialectos.
-Incorporación de modelos más avanzados y ligeros como DistilBERT.
-Optimización del sistema para su implementación en tiempo real.
