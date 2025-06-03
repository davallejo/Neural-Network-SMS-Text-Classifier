# 📩 Clasificador de Mensajes SMS: Spam vs Ham

---

## 🎯 Objetivo del Proyecto

El objetivo principal de este proyecto es construir un modelo de aprendizaje profundo que permita clasificar mensajes SMS en dos categorías: **spam** (mensajes no deseados o publicitarios) y **ham** (mensajes legítimos). Esto facilita la detección automática de spam para mejorar la experiencia del usuario en aplicaciones de mensajería.

---

## 📖 Introducción

Los mensajes SMS son una forma común de comunicación, pero también un canal muy utilizado para el envío de mensajes no solicitados (spam). La detección automática de spam es un problema importante en procesamiento de lenguaje natural (NLP) y aprendizaje automático. En este proyecto, se desarrolla un modelo basado en redes neuronales recurrentes (LSTM bidireccionales) para clasificar con alta precisión mensajes de texto.

---

## 🛠️ Tecnologías Usadas

- 🐍 **Python 3** – Lenguaje de programación principal.  
- 🤖 **TensorFlow / Keras** – Frameworks para construir y entrenar el modelo de redes neuronales.  
- 🐼 **Pandas** – Para manipulación y análisis de datos.  
- ✂️ **Regex (Expresiones Regulares)** – Para limpieza y preprocesamiento del texto.  
- 🌐 **wget** – Para descargar los datasets públicos.  
- 💻 **Jupyter Notebook / Google Colab** – Entorno interactivo para desarrollo y experimentación.

---

## 🔍 Proceso del Proyecto

1. 📥 **Descarga de datos**  
   Se descargaron dos conjuntos de datos públicos en formato TSV, uno para entrenamiento (`train-data.tsv`) y otro para validación (`valid-data.tsv`).

2. 🧹 **Preprocesamiento del texto**  
   - 🔡 Conversión a minúsculas  
   - ❌ Eliminación de caracteres no alfabéticos  
   - 🔢 Tokenización y conversión a secuencias numéricas  
   - 🔲 Padding para igualar la longitud de secuencias

3. 🏗️ **Construcción del modelo**  
   Se definió una red neuronal secuencial con las siguientes capas:  
   - 🧮 Capa Embedding para vectores de palabras  
   - 🔄 Capas Bidireccionales LSTM para capturar contexto desde ambos lados del texto  
   - 🚫 Capas Dense con Dropout para evitar sobreajuste  
   - 🎯 Capa de salida con activación sigmoide para clasificación binaria

4. 🏋️‍♂️ **Entrenamiento**  
   El modelo fue entrenado por 5 épocas con EarlyStopping para evitar sobreajuste, utilizando `binary_crossentropy` como función de pérdida y `adam` como optimizador.

5. 🧪 **Evaluación y pruebas**  
   Se desarrolló una función `predict_message` para clasificar mensajes nuevos y una función `test_predictions` con ejemplos para validar que el modelo funcione correctamente.

---

## 📈 Resultados

- 📊 El modelo alcanzó una **precisión en validación superior al 97%** después de pocas épocas de entrenamiento.  
- ✔️ Pasó con éxito todas las pruebas de clasificación con mensajes reales de prueba, clasificando correctamente mensajes **spam** y **ham**.  
- 🤓 El uso de LSTM bidireccionales y Dropout mejoró la capacidad del modelo para entender el contexto y evitar sobreajuste.

---

## 📝 Conclusión

Este proyecto demuestra cómo aplicar técnicas de procesamiento de lenguaje natural y aprendizaje profundo para resolver un problema práctico como la detección de spam en mensajes SMS. El modelo entrenado puede integrarse en sistemas de mensajería para mejorar la experiencia del usuario y reducir la recepción de mensajes no deseados. Además, la metodología puede adaptarse para otros problemas de clasificación de texto con datos similares.

