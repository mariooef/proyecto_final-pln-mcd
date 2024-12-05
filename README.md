# Proyecto Final PLN

## Descripción del Proyecto
Este proyecto tiene como objetivo analizar las opiniones negativas de los usuarios de un servicio de alimentos en línea para priorizar su atención y mejorar la experiencia del cliente. Utilizamos técnicas avanzadas de Procesamiento de Lenguaje Natural (PLN) y aprendizaje automático para identificar automáticamente reviews con calificaciones bajas (1 y 2), explorar sus temas predominantes y ofrecer información que permita acciones correctivas.

## Objetivos Principales
1. **Identificación Automática de Reviews Negativas:** Clasificación de opiniones con calificaciones de 1 y 2 utilizando modelos de aprendizaje supervisado.
2. **Análisis de Tópicos Predominantes:** Uso de técnicas de modelado de tópicos para detectar las principales áreas de insatisfacción.
3. **Optimización del Modelo:** Evaluación del desempeño en un conjunto de prueba con métricas como precisión, recall, F1-score y curva ROC.

## Metodología
1. **Preprocesamiento de Datos:**
   - Limpieza del texto: eliminación de ruido, tokenización y normalización.
   - Conversión de texto en representaciones vectoriales usando TF-IDF y modelos preentrenados como BERT.

2. **Entrenamiento y Evaluación del Modelo:**
   - Implementación de modelos de clasificación como Logistic Regression.
   - Fine-tuning de modelos de lenguaje como BERT.

3. **Modelado de Tópicos:**
   - Análisis de temas predominantes en opiniones negativas utilizando técnicas como Latent Dirichlet Allocation (LDA) y visualización de los resultados con WordCloud.

## Resultados de los Modelos
### Modelos Supervisados
- **BERT Fine-tuning:**
  - **F1-score:** 96%.
  - **ROC AUC:** 97%.
  - Este modelo demostró ser el más robusto para identificar opiniones negativas, gracias al aprendizaje contextual de BERT.
  - 
- **Modelos Clásicos (Logistic Regression):**
  - **F1-score promedio:** 88%.
  - Aunque estos modelos lograron resultados decentes, fueron superados por los modelos de lenguaje preentrenados en términos de precisión y recall.
  - La gran diferencia es que este modelo no requiere de tanto poder de cómputo, por lo tanto, consideramos que es una buena opción cuando existen limitantes en este aspecto. 

### Modelado de Tópicos
El análisis de tópicos reveló los siguientes temas recurrentes en las opiniones negativas:
1. **Problemas de Entrega:** Retrasos frecuentes y paquetes dañados.
2. **Calidad del Producto:** Productos que no cumplen con las expectativas o llegaron en mal estado.
3. **Atención al Cliente:** Falta de respuesta rápida y resolución de problemas.
4. **Precios:** Percepción de altos costos en comparación con la calidad percibida.

La técnica de LDA permitió identificar estos tópicos y generó insights accionables para las áreas de mejora.

## Tecnologías Utilizadas
- Python (NLTK, scikit-learn, HuggingFace)
- Modelos preentrenados de BERT
- Herramientas de visualización como WordCloud y Matplotlib

## Contribuciones y opiniones finales
Este proyecto demuestra cómo las técnicas avanzadas de PLN pueden aplicarse para optimizar la experiencia del cliente en empresas de servicio. Los modelos desarrollados no solo permiten priorizar las opiniones negativas sino también identificar las causas principales de insatisfacción, proporcionando información valiosa para la toma de decisiones.
