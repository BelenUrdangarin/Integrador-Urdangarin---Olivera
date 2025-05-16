## **Análisis Global de Energía Renovable, Acceso a Electricidad y Condiciones Climáticas**

Este proyecto busca analizar el acceso a la electricidad, la producción de energía renovable y las condiciones climáticas,
con el fin de determinar qué fuentes de energía son más adecuadas para cada continente y región.
Para ello, se examinan tendencias de consumo, producción energética y factores ambientales, proponiendo estrategias para un desarrollo sostenible basado en datos.

### **Objetivo**

El análisis busca:
- Determinar la fuente de energía renovable más adecuada según clima, economía y población.
- Examinar la producción y consumo energético por país y continente. 
- Analizar el acceso a la electricidad en poblaciones urbanas y rurales.
- Detectar desigualdades en el acceso a energía y sus causas.
- Evaluar factores climáticos que afectan la viabilidad energética.
  
### **Datasets**

Banco Mundial: https://data.worldbank.org/

SE4ALL Dataset: https://data360.worldbank.org/en/dataset/WB_SE4ALL

Kaggle: Evolución de Energía Renovable: https://www.kaggle.com/code/mehmetisik/02-the-evolution-of-modern-renewable-energy/input?select=01+renewable-share-energy.csv

### **Principales descubrimientos del análisis exploratorio**

- Europa lidera en acceso a electricidad, con casi 100% de cobertura en zonas rurales y urbanas.
- Sudamérica tiene el mayor porcentaje de generación renovable respecto al total, alcanzando 59.4%, probablemente por sus recursos hídricos y políticas de incentivo.
- Oceanía es la región con menor producción proporcional de energía renovable (~16.3%), lo que sugiere un potencial de crecimiento.
- Oceania y África tienen las velocidades de viento más altas, lo que hace que la energía eólica sea una opción estratégica.
- África y Asia presentan los valores más altos de índice UV, lo que refuerza la viabilidad de energía solar en estos continentes.
- PM2.5 y PM10 están especialmente elevados en países en desarrollo, con variaciones por continente.

### **Resumen de los modelos aplicados**

- Limpieza y preprocesamiento de datos: Se eliminaron valores vacíos, se corrigieron datos faltantes y se ajustaron unidades para asegurar coherencia en las métricas.

- Normalización de datos: Se aplicó Min-Max Scaling en variables como producción y acceso a energía para facilitar comparaciones entre países.

- Clasificación por continente: Se usó pycountry_convert para asignar cada país a su continente.

- Detección y eliminación de outliers: Se utilizaron Z-Scores para identificar valores extremos en contaminación, temperatura y acceso energético, filtrando registros irreales.

- Análisis exploratorio con visualizaciones: Se crearon gráficos de distribución, boxplots, mapas y bar charts para entender tendencias por región.

- Agrupación y comparación de promedios: Se aplicó groupby() para analizar diferencias en producción energética y acceso a electricidad entre continentes.

### **librerias**

- pandas:  Manipulación de datasets

- numpy: Operaciones numéricas

- scipy.stats/zscore: Detección de outliers

- sklearn.preprocessing/MinMaxScaler: Escalado de valores

- matplotlib.pyplot: Creación de gráficos

- seaborn: Visualización avanzada con gráficos más estilizados

- pycountry_convert: Asignación de países a continentes
