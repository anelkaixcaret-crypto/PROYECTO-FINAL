# PROYECTO-FINAL
ESTE ES MI RPOYECTO FINAL DE MI CLASE DE INTRODUCCION DE DATOS 
# Proyecto Final: Ciencia de Datos Aplicada al Consumo Energético de México

## 📌 Descripción General del Proyecto
Este proyecto consiste en el desarrollo de una aplicación móvil interactiva creada en la plataforma **MIT App Inventor**, como parte de la asignatura de **Introducción a la Ciencia de Datos**. 

El propósito principal de la aplicación es brindar una herramienta integral para el análisis de series temporales, centrándose específicamente en el estudio del **consumo de energía primaria en México a lo largo del periodo 2000-2023*. La plataforma combina la visualización interactiva de datos, la depuración de errores de medición, el modelado matemático mediante regresión lineal y la integración de Inteligencia Artificial para el análisis predictivo y contextual sobre el cambio climático global.

---

## 📊 Conjunto de Datos (Dataset)
La aplicación procesa un conjunto de datos histórico estructurado a partir de hojas de cálculo (Google Sheets / Microsoft Excel) con las siguientes características:

* **Variable Independiente ($X$):** Tiempo medido en **Años**, abarcando un rango continuo desde el año **2000 hasta el año 2023**[cite: .
* **Variable Dependiente ($Y$):** **Consumo Energético Anual de México**, expresado en **Teravatios-hora (TWh)**. Los registros muestran la evolución del consumo energético nacional desde aproximadamente 1,850 TWh en el año 2000 hasta superar los 2,690 TWh en 2023.
* **Flujo de Datos:** Los datos son importados y convertidos dinámicamente en coordenadas $(X, Y)$ para su representación gráfica dentro del componente `ChartData2D` de App Inventor.

---

## 🛠️ Arquitectura y Funcionalidades de la Aplicación

La aplicación está dividida en cuatro etapas principales de procesamiento de datos:

### 1. Visualización de Datos (`Show Data`)
* Permite cargar la serie de tiempo del consumo energético de México.
* Muestra gráficamente la trayectoria y tendencia general del uso de energía en el país durante las últimas dos décadas.

### 2. Detección y Limpieza de Anomalías (`Detect Anomalies` & `Data Cleaning`)
* **Identificación de Outliers:** Analiza la serie de tiempo en busca de anomalías, como valores nulos, registros en cero (`0`) o saltos atípicos provocados por errores de captura en la hoja de cálculo.
* **Depuración Interactiva:** Permite interactuar con los puntos de la gráfica para remover los datos anómalos, garantizando que el modelo matemático posterior se calcule únicamente con información limpia y coherente.

### 3. Ajuste del Modelo Matemático (`Draw Line of Best Fit`)
Mediante el uso del componente `Trendline`, la app traza automáticamente la **línea de mejor ajuste (regresión lineal)** sobre los datos depurados y calcula tres métricas estadísticas fundamentales:
* **$M$ (Linear Coefficient / Pendiente):** Representa la tasa de variación anual del consumo energético en México (TWh consumidos por año).
* **$B$ (Y-Intercept / Intersección con el Eje Y):** Indica el valor teórico base del consumo energético calculado al inicio de la serie.
* **$R$ (Correlation Coefficient / Coeficiente de Correlación):** Determina la fuerza y dirección de la relación lineal entre el paso de los años y el incremento en el consumo de energía.

### 4. Asistente Virtual e Inteligencia Artificial (`ChatBot`)
La aplicación integra un módulo de IA que utiliza el bloque `Conversar` alimentado por un prompt dinámico (`unir`)[cite: 1, 2]. El sistema compila automáticamente:
* Toda la secuencia de datos limpios (`ObtenerTodasEntradas`).
* Los parámetros matemáticos del modelo ($M$, $B$ y $R$).
* La consulta específica ingresada por el usuario en pantalla.

Con esta información, la IA realiza cálculos en tiempo real, genera predicciones sobre el comportamiento del consumo energético en el país y reflexiona sobre las implicaciones ambientales del uso de energía y el cambio climático, limitando sus respuestas a un formato conciso de 120 palabras.

---

## 💻 Tecnologías y Herramientas Utilizadas
* **Entorno de Desarrollo:** MIT App Inventor 2.
* **Fuentes de Datos:** Google Sheets / Microsoft Excel enlazados mediante URL pública.
* **Gráficos y Estadística:** Componentes `ChartData2D` y `Trendline`.
* **Procesamiento de Lenguaje Natural:** Componente `ChatBot` para consultas con Inteligencia Artificial.
