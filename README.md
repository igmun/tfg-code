


```

THESIS-ML-NASDAQ/
│
├── config/ # Configuración de parámetros y rutas
├── data/ # Datos en formato .csv (no es necesario replicar la descarga)
├── models/ # Modelos entrenados y/o scripts de entrenamiento
├── notebooks/ # Notebooks con todo el flujo de procesamiento
│ ├── 1. data_extraction.ipynb
│ ├── 2. data_join.ipynb
│ ├── 3. return_variable.ipynb
│ ├── 4. riskadjusted.ipynb
│ ├── 5. data_cleansing.ipynb
│ ├── 6. data_description copy.ipynb
│ ├── 7. feature engineering copy.ipynb
│ ├── 8. base_model.ipynb
│ ├── 10. XGBoost.ipynb
│ ├── 11. XGBoost-Probabilistic.ipynb
│ ├── en progreso.ipynb
│ └── prices.zip
├── others/ # Otros archivos y recursos útiles
├── test/ # Tests automáticos (si aplica)
├── .gitignore
└── README.md

```


---

## Descripción

Este repositorio contiene el código y los datos necesarios para reproducir los experimentos realizados en la tesis.  
El objetivo es aplicar técnicas de machine learning para la predicción de retornos de acciones estadounidenses, integrando variables técnicas, fundamentales y de valoración, así como diferentes enfoques de feature engineering.

---

## Carpetas principales

- **data/**: contiene los archivos `.csv` necesarios para replicar los modelos. No es necesario replicar la recuperación de datos desde cero.
- **notebooks/**: incluye el código para extraer datos, crear y transformar variables, limpiar datos, describir el dataset y construir modelos.
- **models/**: guarda modelos entrenados y scripts relacionados.
- **config/**: configuración del proyecto.
- **others/** y **test/**: recursos adicionales y tests.

---

## Requisitos

- Python 3+
- Recomendado: crear un entorno virtual (`venv` o `conda`)
- Instalar dependencias según el notebook a ejecutar

