### 9.1 Redes de creencias bayesianas 
El Capítulo 8 introdujo el teorema de Bayes y la clasificación bayesiana ingenua. En este capítulo, describimos las redes de creencias bayesianas: modelos gráficos probabilísticos que, a diferencia de los clasificadores bayesianos ingenuos, permiten la representación de dependencias entre subconjuntos de atributos. Las redes de creencias bayesianas se pueden utilizar para la clasificación. La Sección 9.1.1 introduce los conceptos básicos de las redes de creencias bayesianas. En la Sección 9.1.2, aprenderá a entrenar dichos modelos.
### 9.1.1 Conceptos y mecanismos 
El clasificador bayesiano ingenuo asume la independencia condicional de clase, es decir, dada la etiqueta de clase de una tupla, se supone que los valores de los atributos son condicionalmente independientes entre sí. Esto simplifica el cálculo. Cuando la suposición es cierta, entonces el clasificador bayesiano ingenuo es el más preciso en comparación con todos los demás clasificadores. En la práctica, sin embargo, pueden existir dependencias entre variables. Las redes de creencias bayesianas especifican distribuciones de probabilidad condicional conjunta. Permiten definir independencias condicionales de clase entre subconjuntos de variables. Proporcionan un modelo gráfico de relaciones causales, sobre el cual se puede realizar el aprendizaje. Las redes de creencias bayesianas entrenadas se pueden utilizar para la clasificación. Las redes de creencias bayesianas también se conocen como redes de creencias, redes bayesianas y redes probabilísticas. Por brevedad, nos referiremos a ellos como redes de creencias. Una red de creencias está definida por dos componentes: un gráfico acíclico dirigido y un conjunto de tablas de probabilidad condicional (Figura 9.1). Cada nodo en el gráfico acíclico dirigido representa una variable aleatoria. Las variables pueden ser de valor discreto o continuo. Pueden corresponder a atributos reales dados en los datos o a “variables ocultas” que se cree que forman una relación (p. ej., en el caso de datos médicos, una variable oculta puede indicar un síndrome, representando una serie de síntomas que, juntos, caracterizan un enfermedad específica). Cada arco representa una dependencia probabilística. Si se dibuja un arco desde un nodo Y hasta un nodo Z, entonces Y es un padre o predecesor inmediato de Z, y Z es un descendiente