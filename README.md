Detección de Anomalías en Transacciones Financieras con Autoencoders y Random Forest
Este repositorio contiene un proyecto enfocado en la detección de fraudes en transacciones financieras, combinando técnicas de aprendizaje no supervisado (Autoencoders) y supervisado (Random Forest). La solución busca identificar comportamientos anómalos en los datos transaccionales, maximizando la detección de fraudes y minimizando los falsos positivos.

📌 Contexto
El crecimiento del comercio electrónico ha transformado radicalmente los hábitos de consumo. Con este cambio, también ha aumentado el riesgo de fraudes digitales, lo que exige herramientas avanzadas para proteger tanto a consumidores como a empresas.

A pesar del avance en sistemas de seguridad, los atacantes han perfeccionado técnicas como el carding, phishing, fraude por identidad sintética y apropiación de cuentas, entre otros. En este contexto, la detección proactiva de anomalías se vuelve crítica.

🎯 Objetivo
Desarrollar un sistema de detección de fraude capaz de:

Identificar transacciones sospechosas mediante un autoencoder entrenado solo con datos legítimos.

Utilizar el error de reconstrucción como feature para un clasificador Random Forest.

Minimizar falsos positivos sin sacrificar la capacidad de detección.

🧠 Metodología
El proyecto sigue la metodología CRISP-DM, que incluye:

Comprensión del negocio

Comprensión de los datos

Preparación de los datos

Modelado

Evaluación

La etapa de despliegue no se aborda, por estar fuera del alcance de este trabajo.

🔍 Enfoque Técnico
Autoencoder: entrenado exclusivamente con transacciones legítimas. Al no haber sido expuesto a fraudes, se espera que tenga dificultades para reconstruir anomalías, generando errores significativos.

Random Forest: se entrena con las transacciones etiquetadas, incluyendo como feature principal el error de reconstrucción del autoencoder.

Desbalanceo de clases: se manejan técnicas específicas para contrarrestar el efecto de clases desbalanceadas en el rendimiento del modelo.

📊 Herramientas y Tecnologías
Python

Pandas, NumPy, Matplotlib, Seaborn

Scikit-learn

TensorFlow / Keras

🗂️ Estructura del repositorio
bash
Copiar
Editar
├── data/                  # Datos de entrada (protegidos o con ejemplo sintético)
├── notebooks/             # Jupyter Notebooks con el desarrollo paso a paso
├── src/                   # Código fuente del modelo y funciones auxiliares
├── outputs/               # Gráficos y métricas generadas
├── README.md              # Este archivo
└── requirements.txt       # Dependencias del proyecto
📈 Resultados esperados
Reducción de falsos positivos.

Interpretabilidad de los factores más relevantes para la clasificación.

Visualizaciones que expliquen el comportamiento anómalo de las transacciones.

⚠️ Consideraciones
Este proyecto no utiliza datos reales confidenciales.

Su propósito es demostrar una estrategia efectiva de detección combinada.

Se recomienda aplicar validaciones adicionales en entornos reales antes de su uso operativo.
