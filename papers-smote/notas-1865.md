Batista et al. propusieron un metodo de mejora para SMOTE. El metodo utiliza TomekLink como metodo de limpieza de datos, que se aplica al conjunto de datos balanceado obtenido por SMOTE. 

la estrategia TomekLink es eliminar las muestras vecinas mas cercanas en pares. Hasta cierto punto, las muestras de error introducidas por SMOTE se pueden eliminar para mejorar el rendimiento del modelo de clasificacion posterior. Sin embargo este metodo puede eliminar muestras minoritarias representativas cerca del liminte de clasificacion del conjunto de datos original.

Para resolver los problemas anteriores, este documento propone un metodo de muetreo de decision de tres vías (CTD - Constructive Three way decision) basado en el algoritmo de cobertura constructiva (CCA). CTD primero usa el algoritmo de cobertura constructiva para construir la cobertura de los datos desequilibrados. Luego, las cubiertas de las muestras minoritarias se seleccionan y dividen en tres regiones segun la densidad de la cobertura. Finalmente, los umbrales correspondientes  α y β se obtienen en funcion de los patrones de distribución de cobertura y luego se pueden seleccionar muestras clave para el sobremuestreo SMOTE. 

Este articulo tiene en cuenta las incertidumbres causadas por CCA que eligen aleatoriamente el centro de cobertura, y propone un modelo de conjunto (CTDE) basado en CTD para mejorar la eficiencia del algoritmo. 

