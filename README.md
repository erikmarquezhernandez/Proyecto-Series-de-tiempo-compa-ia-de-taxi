# Proyecto-Series-de-tiempo-compania-de-taxi
La compañía Sweet Lift Taxi ha recopilado datos históricos sobre pedidos de taxis en los aeropuertos. Para atraer a más conductores durante las horas pico, necesitamos predecir la cantidad de pedidos de taxis para la próxima hora.

**Objetivo:** Construye un modelo para dicha predicción; la métrica RECM en el conjunto de prueba no debe ser superior a 48.

Para lo anterior vamos a seguir estos pasos:

1.	Descargar los datos y remuestréalos de tal forma que cada punto de datos de los datos originales caigan dentro de intervalos de una hora.
2.	Analizar los datos.
3.	Entrenar diferentes modelos con diferentes hiperparámetros. La muestra de prueba debe ser el 10% del conjunto de datos inicial. Prueba los datos usando la muestra de prueba.
    - Vamos a usar los siguientes modelos: Regresión Lineal, LightGBM, XGBRegressor para este último vamos aplicar la validación cruzada a una serie de tiempo.
4.	Conclusión
