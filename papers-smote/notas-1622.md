### Mejores prácticas 

Normalización/estandarización/escalado/selección de características 

La mayoría de las técnicas de sobremuestreo operan en el espacio euclidiano implícito en los atributos. Por lo tanto, es extremadamente importante normalizar/escalar los atributos apropiadamente. Sin conocimiento sobre la importancia de los atributos, la normalización/estandarización es un buen primer intento. Al tener algún conocimiento del dominio o la importancia de los atributos de la clasificación bootstrap, también es razonable escalar los rangos de atributos de acuerdo con sus importancias. Alternativamente, la selección de subconjuntos de características también podría mejorar los resultados al hacer que el sobremuestreo funcione en el subespacio más adecuado. Selección del modelo para el número de muestras a generar La clasificación después del sobremuestreo es muy sensible al número de muestras minoritarias que se generan. Equilibrar el conjunto de datos rara vez es la opción correcta, ya que la mayoría de los clasificadores funcionan de manera más eficiente si la densidad de muestras positivas y negativas cerca del límite de decisión es aproximadamente la misma. Si las variedades de las clases positivas y negativas no tienen aproximadamente el mismo tamaño, equilibrar el conjunto de datos no puede lograrlo. Además, en ciertas regiones puede incluso revertir la situación: si la variedad de la clase minoritaria es mucho menor que la de la clase mayoritaria, el equilibrio convertirá a la clase minoritaria en mayoritaria en los entornos locales a lo largo del límite de decisión. La solución es aplicar la selección del modelo para el número de muestras que se generan. Casi todas las técnicas implementadas en el paquete `smote-variants` tienen un parámetro llamado `proporción`. Este parámetro controla cuántas muestras generar, es decir, la cantidad de muestras minoritarias generadas es `proporción*(N_maj - N_min)`, es decir, establecer el parámetro de proporción en 1 equilibrará el conjunto de datos. Se recomienda encarecidamente llevar a cabo una selección de modelos con validación cruzada para un rango como `proporción` = 0,1, 0,2, 0,5, 1,0, 2,0, 5,0.

conclusiones: 
- la seleccion de subconjuntos de características tambien podria ayudar a mejorar los resultados al hacer que el sobremuestreo funcione en el subespacio mas adecuado.
- hay que lograr que la densidad de muestras positivas y negativas sean apropiadamente las mismas cerca del limite de decision.
- es extremadamente importante normalizar/ escalar los atributos apropiadamente.
- sino se conoce la importancia de los atributos, estandarizar/ escalar es un intento para aplicar el sobremuestreo.
- limite de decision
- espacio euclideano