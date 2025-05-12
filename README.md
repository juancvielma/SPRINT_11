# SPRINT_11
# Proyecto de Exploración de Pozos Petroleros - OilyGiant

Este proyecto simula el proceso de toma de decisiones de inversión para abrir 200 nuevos pozos petroleros, utilizando datos sintéticos de tres regiones diferentes. 

## Objetivo
Determinar en cuál de las tres regiones es más rentable invertir, evaluando la producción esperada, la ganancia estimada y el riesgo asociado.

## Pasos del análisis

1. **Carga y preparación de datos:**
   - Se cargan datos de tres archivos CSV (`geo_data_0.csv`, `geo_data_1.csv`, `geo_data_2.csv`).
   - Se examinan las características (`f0`, `f1`, `f2`) y el volumen real de reservas (`product`).

2. **Entrenamiento de modelos:**
   - Se entrena un modelo de regresión lineal por región para predecir el volumen de reservas.
   - Se evalúa el modelo con RMSE y el volumen promedio predicho.

3. **Cálculo de ganancias estimadas:**
   - Se seleccionan los 200 pozos con mayor predicción de reservas por región.
   - Se calcula el beneficio esperado con un ingreso de $4,500 por unidad de reserva y un presupuesto de $100M.

4. **Análisis de riesgo (bootstrapping):**
   - Se ejecuta una simulación de 1000 repeticiones para estimar la distribución de beneficios.
   - Se calcula el beneficio promedio, el intervalo de confianza del 95% y el riesgo de pérdida.

5. **Selección de región óptima:**
   - Se propone la mejor región basada en beneficio esperado y bajo riesgo.

## Resultados clave

- **Punto de equilibrio:** 111.1 unidades de producción promedio por pozo.
- **Región recomendada:** La región con mayor ganancia esperada y riesgo de pérdida inferior al 2.5%.

## Requisitos

- Python 3
- pandas, numpy, scikit-learn, matplotlib, seaborn

## Uso

1. Ejecuta el notebook `analisis_regiones_petroleo_actualizado.ipynb`.
2. Asegúrate de tener los archivos de datos en el mismo directorio:  
   - `geo_data_0.csv`
   - `geo_data_1.csv`
   - `geo_data_2.csv`

---

**Nota:** Todos los datos utilizados son sintéticos.
