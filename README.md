# Análisis Visual de Distribuciones Categóricas y Outliers

## Origen de los datos
- **Dataset:** `tips` (Propinas), cargado directamente desde la librería `seaborn` en Python.
- **Contenido:** Registros de cuentas y propinas en un restaurante, con variables numéricas (como `total_bill` y `tip`) y categóricas (como `day`, `time`, `sex` y `smoker`).

## Contenido del análisis (analisis_distribuciones_outliers.ipynb)
- Exploración inicial y verificación de valores faltantes.
- Gráfico de barras (`countplot` / barplot) sobre variables categóricas.
- Cálculo e interpretación de **asimetría (`skewness`)** y **curtosis** para `total_bill`.
- Visualización de distribuciones y valores extremos mediante **Boxplot** y **Violin Plot**.
- Identificación y listado de registros atípicos (*outliers*) mediante la regla del **Rango Intercuartílico (IQR)**.

## Decisión sobre los outliers
- Al tratarse de montos reales de consumo (`total_bill`) con asimetría positiva (cola hacia valores altos), los registros por encima del límite superior del IQR representan cuentas elevadas reales y no necesariamente errores de carga.
- Como decisión inicial, conviene **conservarlos y documentarlos** durante el análisis exploratorio, y evaluar transformaciones (como logarítmica) o tratamiento específico recién en la etapa de modelado según el algoritmo utilizado.
