Predecir la tasa de promocion efectiva escolar en TdF
==============================

Predecir la tasa de promocion escolar en TdF

Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>


++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++

Trabajo Practico de Aprendizaje Automático: Analizar y predecir las tasas de promoción efectiva, repitencia y abandono escolar en las escuelas de Tierra del Fuego. 
Gabriel García 
Descripción y Formulación del Objetivo Definición del Problema: El objetivo del proyecto es analizar y predecir las tasas de promoción efectiva, repitencia y abandono escolar en las escuelas de Tierra del Fuego. Se busca identificar los factores que influyen en estos indicadores educativos y utilizar esta información para mejorar las políticas y prácticas educativas. Recolección y Preparación de Datos Variables Relevantes: Dependientes: Tasa de promoción efectiva Tasa de repitencia Tasa de abandono interanual Independientes: Datos socioeconómicos de los estudiantes (ingresos familiares, nivel educativo de los padres, etc.) Características de las escuelas (ubicación, recursos, infraestructura, número de estudiantes, ratios alumno/profesor) Factores contextuales (desempleo en la región, acceso a servicios básicos, etc.) Acciones: Cargar los datos y revisar su estructura. Limpiar los datos, manejando valores faltantes y eliminando registros inconsistentes. Codificar variables categóricas si es necesario. Objetivo del Trabajo: El objetivo de este proyecto es analizar y predecir las tasas de promoción efectiva, repitencia y abandono escolar en las escuelas de Tierra del Fuego. Este análisis se enfocará en identificar los factores socioeconómicos, institucionales y contextuales que influyen significativamente en estos indicadores educativos. Problema Específico: El problema específico que se abordará con este modelo es la identificación y comprensión de los factores que afectan negativamente la continuidad educativa de los estudiantes en Tierra del Fuego. Al predecir las tasas de promoción, repitencia y abandono, se pretende: Identificar Variables Clave: Determinar cuáles son los factores más influyentes en las tasas de promoción, repitencia y abandono escolar. Esto incluye analizar variables como el nivel socioeconómico de los estudiantes, las características de las escuelas, y los factores regionales. Predecir Indicadores Educativos: Desarrollar modelos predictivos que permitan anticipar las tasas de promoción, repitencia y abandono en diferentes escuelas y regiones, facilitando la planificación y la intervención temprana. Proporcionar Recomendaciones: Basándose en los hallazgos del análisis, ofrecer recomendaciones específicas para mejorar las políticas educativas y las prácticas escolares, con el objetivo de aumentar la tasa de promoción efectiva y reducir las tasas de repitencia y abandono. Mejorar la Eficiencia de Recursos: Ayudar a las autoridades educativas a asignar recursos de manera más eficiente y dirigida, enfocándose en las áreas y grupos de estudiantes que más lo necesitan. Contexto del Problema Situación Educativa en Tierra del Fuego: En Tierra del Fuego, como en otras provincias de la Argentina, se enfrenta a desafíos significativos en su sistema educativo. Aunque ha habido avances en el acceso a la educación, persisten problemas relacionados con la calidad de la educación y la equidad en el acceso y los resultados educativos. Algunos de los principales indicadores que reflejan estos desafíos son las tasas de promoción efectiva, repitencia y abandono escolar.
Tasa de Promoción Efectiva: Mide el porcentaje de estudiantes que avanzan al siguiente nivel educativo sin repetir el grado. Una tasa alta de promoción efectiva indica un sistema educativo que apoya y retiene a sus estudiantes de manera efectiva. Tasa de Repitencia: Refleja el porcentaje de estudiantes que deben repetir el grado. Altas tasas de repitencia pueden ser indicativas de problemas en la calidad de la enseñanza, la relevancia del currículo, o de problemas socioeconómicos que afectan el rendimiento estudiantil. 
Tasa de Abandono Escolar: Representa el porcentaje de estudiantes que dejan la escuela antes de completar su educación. El abandono escolar es un problema crítico, ya que está asociado con peores resultados en términos de empleo, ingresos y bienestar social a largo plazo. Relevancia del Problema La educación es un pilar fundamental para el desarrollo económico y social de cualquier país. En el caso de Tierra del Fuego, mejorar las tasas de promoción efectiva, y reducir las tasas de repitencia y abandono escolar, es crucial por varias razones: 
Desarrollo Económico: Una población bien educada es más productiva y tiene mayores oportunidades de empleo. La educación mejora las habilidades y competencias, lo que a su vez impulsa la innovación y el crecimiento económico. 
Equidad Social: Las disparidades en los resultados educativos a menudo reflejan y perpetúan desigualdades sociales y económicas. Mejorar los resultados educativos puede ayudar a reducir estas brechas y promover una mayor equidad social. 
Calidad de Vida: La educación está estrechamente vinculada a una mejor calidad de vida. Las personas con niveles educativos más altos tienden a tener mejores resultados en términos de salud, participación cívica y bienestar general. Política Pública: Para los responsables de la formulación de políticas, tener una comprensión clara de los factores que influyen en la promoción, repitencia y abandono escolar es esencial para diseñar intervenciones efectivas. 
Esto permite una asignación más eficiente de los recursos y la implementación de estrategias dirigidas a los grupos y regiones más vulnerables. Relevancia del Proyecto El análisis y la predicción de las tasas de promoción efectiva, repitencia y abandono escolar en Tierra del Fuego no solo contribuirán a la comprensión de estos fenómenos, sino que también proporcionarán una base sólida para la toma de decisiones informadas. Al identificar los factores que afectan negativamente la continuidad educativa, se pueden diseñar políticas y programas que apoyen mejor a los estudiantes y mejoren los resultados educativos a nivel nacional. 
Preguntas de Investigación Para abordar el problema de las tasas de promoción efectiva, repitencia y abandono escolar en Tierra del Fuego mediante técnicas de aprendizaje automático, formularemos las siguientes preguntas de investigación: Preguntas de Investigación 
¿Cuáles son los principales factores socioeconómicos, demográficos y académicos que afectan la tasa de promoción efectiva en las escuelas de Tierra del Fuego? ¿Qué variables están más correlacionadas con las tasas de repitencia y abandono escolar? ¿Es posible predecir con precisión la tasa de promoción efectiva de un grupo de estudiantes en función de las características disponibles? ¿Qué tan preciso es el modelo de aprendizaje automático para predecir las tasas de repitencia y abandono escolar? ¿Qué tipo de intervenciones (por ejemplo, tutorías adicionales, programas de apoyo económico) podrían tener el mayor impacto en la reducción de las tasas de repitencia y abandono? 
Selección del Modelo Utilizare un modelo de regresión de Aprendizaje Supervisado, probare con un modelo de regresión lineal (LinearRegression), ya que intentaremos predecir valore en este caso precios a futuro de una o más variables. También desarrollaremos un modelo de Árbol de Decisión (RandomForestRegressor) para mejorar la precisión y la robustez de las predicciones Pasos a seguir Carga de Librerías necesarias Pandas, Numpy, Seaborn, Matplotlib, sklearn Exploración de Datos Análisis General del DataSet Análisis Descriptivo y Estadístico del DataSet Análisis de valores nulos y duplicados. Preprocesamiento Conversión de fechas a un formato adecuado Codificación de variables categóricas. Normalización o estandarización de precios. Modelado Definición del Problema Selección de algoritmos apropiados (Regresión, Clasificación). Entrenamiento y validación del Modelo. Evaluación Métricas de desempeño para evaluar la precisión del modelo. Interpretación de resultados y conclusiones.  
++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Descripcion del Dataset y Origen
El dataset contiene datos sobre la tasa de finalización, tasa de repitencia y tasa de abandono de diferentes niveles educativos en la argentina.
Cantidad de instancias: El dataset tiene información sobre distintas provincias de argentina. Cada fila representa una provincia específica y sus datos asociados.
Características (columnas):
Región: Nombre de la provincia dentro del país.
Niveles educativos: Los datos están divididos en tres niveles educativos principales: Primaria (6 años), Secundaria (6 años), y Secundaria - Ciclo Básico y Orientado. Cada nivel educativo tiene subcolumnas para cada año de estudio, desde el primer año hasta el último. Por ejemplo, para la Primaria (6 años), las subcolumnas serían 1°, 2°, 3°, 4°, 5°, y 6°
Tipos de datos: Los datos son porcentajes de finalización de cada nivel educativo por año de estudio en las diferentes provincias. Los porcentajes están expresados como números decimales (por ejemplo, 97,12%).
Información relevante:
El dataset proporciona una visión detallada de la finalización educativa en diferentes provincias del país a lo largo del año 2015.
Las provincias incluidas en el dataset abarcan a toda la Nación Argentina.
Los datos se dividen en diferentes niveles educativos y años de estudio dentro de cada nivel, lo que permite un análisis detallado de la progresión educativa en cada región.
El dataset contiene información detallada sobre la finalización educativa en diferentes provincias de argentina, los datos provienen del Ministerio de Educación, Secretaría de Innovación y Calidad Educativa, Dirección Nacional de Planeamiento de Políticas Educativas, Dirección de Información y Estadística Educativa, Red Federal de Información Educativa, por lo tanto, se corresponde con una información oficial que data del año 2015. Por lo cual contiene información relevante que garantizar la precisión y coherencia de los datos para de su análisis.