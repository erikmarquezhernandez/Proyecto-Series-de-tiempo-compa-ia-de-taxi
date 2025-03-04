# **Predicción de demanda de taxis en aeropuertos**  

## **Situación**  
Sweet Lift Taxi enfrenta un desafío en la gestión de la demanda de taxis en aeropuertos. Durante las horas pico, la falta de conductores disponibles afecta la experiencia del cliente y la eficiencia del servicio. Para mitigar este problema, la empresa busca predecir la cantidad de pedidos de taxis en la próxima hora, permitiendo así ajustar la disponibilidad de conductores en tiempo real.  

## **Tarea**  
Desarrollar un modelo de Machine Learning que prediga la demanda de taxis en aeropuertos con una **Raíz del Error Cuadrático Medio (RMSE) no mayor a 48**, asegurando así una predicción precisa para mejorar la asignación de recursos.  

## **Acción**  
1. **Procesamiento y análisis de datos**:  
   - Se descargaron y remuestrearon los datos en intervalos de una hora.  
   - Se validó la calidad de los datos: no se encontraron valores negativos y se identificaron valores atípicos por encima de 200.  
   - Se detectó una tendencia creciente en la demanda de taxis, con un aumento significativo después de junio.  

2. **Entrenamiento y evaluación de modelos**:  
   - Se probaron tres modelos: **Regresión Lineal, LightGBM y XGBRegressor**.  
   - Se utilizó **validación cruzada para series de tiempo** en XGBRegressor, abordando el reto de particionar datos secuenciales sin sesgar el entrenamiento.  
   - La muestra de prueba representó el **10% del conjunto de datos**.  
   - Se compararon visualmente las predicciones de cada modelo con los valores reales, lo que permitió observar que la **Regresión Lineal se ajusta mejor a los picos de demanda** en comparación con los otros modelos.  

3. **Selección del mejor modelo**:  
   - Todos los modelos cumplieron con el objetivo de **RMSE < 48**.  
   - Sorprendentemente, **la Regresión Lineal superó a modelos más avanzados**, con un RMSE de **35.84**, siendo la mejor opción para la predicción.  

## **Resultado**  
- Se logró una predicción efectiva de la demanda de taxis, optimizando la planificación de recursos.  
- El modelo de **Regresión Lineal, con RMSE de 35.84**, ofreció la mejor combinación de simplicidad y precisión.  
- La visualización de las predicciones comparadas con los valores reales confirmó que la Regresión Lineal capta mejor los picos de demanda, lo que es clave para la toma de decisiones operativas.  
- La compañía ahora puede anticipar picos de demanda con mayor certeza, permitiendo estrategias proactivas como incentivos a conductores y ajustes en la distribución de unidades.  
