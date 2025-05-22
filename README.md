# 🧠 Detección de Ansiedad a partir de Señales Fisiológicas usando CNN  
**Proyecto de Investigación – Inteligencia Artificial y Salud Mental**

---

## 📌 Descripción del proyecto

Este trabajo de investigación explora el uso de **Redes Neuronales Convolucionales (CNN)** para la **detección de ansiedad** a partir de señales fisiológicas captadas por dispositivos wearables (relojes inteligentes o bandas biométricas). El objetivo es automatizar la clasificación de estados ansiosos en tiempo real mediante aprendizaje profundo.

---

## 📊 Dataset

- Señales fisiológicas empleadas:
  - 💓 **Frecuencia cardíaca (HR)**
  - 💡 **Variabilidad cardíaca (HRV)**
  - 📉 **Nivel de estrés estimado**
  - 🌡️ **Temperatura corporal**
  - 💧 **Respuesta galvánica de la piel (GSR)**
  - 🫁 **Frecuencia respiratoria**
- Origen: Dispositivos portables (ej. Empatica E4, Xiaomi Smart Band, etc.)
- Etiquetas: Estado emocional auto-reportado (ansiedad / no ansiedad)

---

## ⚙️ Arquitectura del modelo CNN

- Capas convolucionales para extracción automática de patrones temporales
- `Conv1D` + `MaxPooling` + `Dropout`
- Capas `Dense` para la clasificación binaria
- Activación: `ReLU` + `Sigmoid`
- Pérdida: `binary_crossentropy`
- Optimización: `Adam`

---

## 🏗️ Flujo del proyecto

1. **Preprocesamiento de señales** (normalización, padding, sliding windows)
2. **Diseño del modelo CNN** (entrada multicanal)
3. **Entrenamiento y validación cruzada**
4. **Evaluación** con métricas: *Accuracy, F1-Score, Recall*
5. **Predicción en tiempo real** desde dispositivo wearable (en desarrollo)

---

## 📈 Resultados esperados

- Accuracy > 85% en detección binaria (Ansiedad vs. No Ansiedad)
- F1-Score balanceado para evitar sesgo de clase
- Potencial para implementación en **sistemas de monitoreo continuo en salud mental**

---

## 📎 Herramientas utilizadas

- Python 3.9
- TensorFlow / Keras
- NumPy, Pandas, Matplotlib
- Scikit-learn
- Dispositivo wearable con exportación de datos crudos (CSV / API)

---

## 📂 Estructura del proyecto

```bash
Anxiety_detection_CNN/
├── README.md                        # Documentación del proyecto
├── analisis_exploratorio.ipynb     # Análisis estadístico y visualización de datos
├── desarrollo_modelos_comparacion.ipynb  # Implementación de modelos CNN y pruebas
├── preprocesamiento_datos.py       # Limpieza, normalización y segmentación de señales
