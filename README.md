# Walmart Sales Forecasting

## Descripción del proyecto

Este proyecto analiza el comportamiento de ventas semanales de Walmart a partir de información histórica por tienda, departamento, semanas festivas, promociones y variables económicas.

El objetivo es identificar patrones relevantes en las ventas y construir modelos predictivos que apoyen decisiones relacionadas con inventario, planificación comercial y desempeño por tienda/departamento.

## Datos utilizados

Los datos provienen de la competencia **Walmart Recruiting - Store Sales Forecasting** disponible en Kaggle.

Por restricciones de uso, los archivos originales no se incluyen en este repositorio. Para replicar el proyecto, se deben descargar desde Kaggle y ubicarlos en una carpeta `data/`.

Archivos utilizados:

- `train.csv`: ventas históricas por tienda, departamento y semana.
- `features.csv`: variables externas como temperatura, precio del combustible, CPI, desempleo, promociones y festivos.
- `stores.csv`: características de las tiendas, como tipo y tamaño.

## Metodología

El proyecto incluyó:

- Carga e integración de datos.
- Tratamiento de valores faltantes en variables promocionales.
- Análisis exploratorio de ventas.
- Análisis por tienda, departamento, tipo de tienda y semanas festivas.
- Análisis de correlación.
- Modelo SARIMA para ventas agregadas semanales.
- Modelo Random Forest para ventas a nivel tienda-departamento-semana.
- Evaluación mediante MAE, RMSE, MAPE y WMAE.

## Resultados principales

### SARIMA

Modelo aplicado sobre ventas semanales agregadas.

- MAE: 1,703,732.76
- RMSE: 2,129,751.12
- MAPE: 3.68%

### Random Forest

Modelo aplicado a nivel tienda-departamento-semana.

- MAE: 2,191.54
- RMSE: 4,259.74
- WMAE: 2,212.10

Las variables más importantes para el modelo Random Forest fueron:

- Departamento
- Tamaño de tienda
- Tienda
- Semana del año

## Conclusiones

El análisis mostró que las ventas no dependen de una única variable, sino de la interacción entre factores temporales, comerciales y operativos.

El modelo SARIMA permitió capturar patrones generales de tendencia y estacionalidad en las ventas agregadas, mientras que Random Forest permitió analizar el comportamiento a un nivel más detallado, incorporando variables como tienda, departamento, tamaño, promociones y semanas festivas.

Este tipo de análisis puede apoyar decisiones relacionadas con inventario, planificación comercial, evaluación de promociones, desempeño por tienda/departamento y construcción de reportes gerenciales.

## Herramientas utilizadas

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Statsmodels
- Scikit-learn

## Portafolio ejecutivo

El resumen visual del proyecto se encuentra en la carpeta `reports/`.
