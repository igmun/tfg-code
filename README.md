# TFG – Machine Learning aplicado a la selección de acciones del S&P 500

Este trabajo explora la posibilidad de generar *outperformance* mediante el uso de modelos de aprendizaje automático aplicados a la selección de acciones. En particular, se evalúa el desempeño de tres enfoques: **Ridge Classifier, XGBoost y una red neuronal profunda (DNN)**, en la tarea de clasificar empresas del índice **S&P 500** según su retorno futuro a un año.  

El objetivo es construir carteras formadas por las 20 compañías con mayor probabilidad estimada de pertenecer a la clase de máximo retorno, definida como el percentil 80 dentro de cada ventana de predicción.  

La metodología implementa un pipeline de *machine learning* que parte de la construcción de datos históricos en formato panel, enfrentando desafíos como:  
- la variabilidad de los constituyentes a lo largo del tiempo,  
- la necesidad de esquemas de validación temporal que eviten *data leakage*.  

Las variables predictoras se seleccionan a partir de la literatura sobre factores de inversión y estrategias con respaldo empírico. Los datos provienen de **LSEG** y **Nasdaq Data Link**.  

Los resultados muestran que los tres modelos superan sistemáticamente al índice S&P 500, con las redes neuronales profundas destacando como el mejor modelo (retorno anual compuesto del **16.79%** en 2004–2025), aunque con mayor exposición a la volatilidad.

---

## 📂 Estructura del repositorio


```

TFG-CODE/
│
├── config/ # Configuración de parámetros y rutas
│ └── config_user/ # Configuración personalizada (API Keys, paths locales)
│
├── data/ # Datos en formato .csv (excepto precios diarios por tamaño)
│ └── largefiles/ # Archivos de gran tamaño (excluidos del repo)
│
├── notebooks/ # Notebooks con el flujo completo de procesamiento
│ ├── 1. data_extraction.ipynb
│ ├── 2. data_join.ipynb
│ ├── 3. return_variable.ipynb
│ ├── 4. risk_adjusted.ipynb
│ ├── 5. data_cleansing.ipynb
│ ├── 8. base_model.ipynb
│ ├── 9. XGBoost.ipynb
│ ├── 10. DNN.ipynb
│ └── 11. evaluation.ipynb
│
├── result_metrics/ # Resultados de métricas y evaluaciones
│
├── others/ # Recursos adicionales y documentos auxiliares
│
├── .gitignore
├── requirements.txt
└── README.md

```

---

## Api KEY

Este repositorio contiene el código y los datos necesarios (Salvo datos de precios de cotización diario para los contituyentes que se han evitado subir debido a su gran peso) para reproducir los experimentos realizados en la tesis. En caso de que el lector quiera reproducir el proyecto completo debe Contratar la Base de datos US CORE EQUITY Bundle ofrecida por Nasdaq Data Link, haciendo uso en este proyecto específicamente de las tablas SF1, SEP y S&P500.



---

## ⚙️ Requisitos

- **Python 3+**  
- Se recomienda crear un entorno virtual (`venv` o `conda`).  
- Instalar dependencias según requirements.txt

Ejemplo de instalación básica:

```bash
pip install -r requirements.txt




