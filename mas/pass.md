***James, G., Witten, D., Hastie, T. y Tibshirani, R. (2013). Una introducción al aprendizaje estadístico (p. 6). Nueva York: springer. [Cap 10: Aprendizaje no supervisado]***
[Una introducción al aprendizaje estadístico](https://hastie.su.domains/ISLR2/ISLRv2_website.pdf)

El aprendizaje estadístico se refiere a un conjunto de herramientas para dar sentido a conjuntos de datos complejos. En los últimos años, hemos visto un aumento asombroso en la escala y el alcance de la recopilación de datos en prácticamente todas las áreas de la ciencia y la industria. Como resultado, el aprendizaje estadístico se ha convertido en un conjunto de herramientas fundamental para cualquier persona que desee comprender los datos, y dado que cada vez más trabajos actuales involucran datos, esto significa que el aprendizaje estadístico se está convirtiendo rápidamente en un conjunto de herramientas fundamental para todos. Uno de los primeros libros sobre aprendizaje estadístico, The Elements of Statistical Learning (ESL, por Hastie, Tibshirani y Friedman), se publicó en 2001, con una segunda edición en 2009. ESL se ha convertido en un texto popular no solo en estadística sino también en en campos relacionados. Una de las razones de la popularidad de ESL es su estilo relativamente accesible. Pero ESL es más adecuado para personas con formación avanzada en ciencias matemáticas. Una Introducción al Aprendizaje Estadístico (ISL) surgió de la clara necesidad de un tratamiento más amplio y menos técnico de los temas clave en el aprendizaje estadístico. La intención detrás de ISL es concentrarse más en las aplicaciones de los métodos y menos en los detalles matemáticos. A partir del Capítulo 2, cada capítulo de ISL contiene un laboratorio que ilustra cómo implementar los métodos de aprendizaje estadístico vistos en ese capítulo utilizando el popular paquete de software estadístico R. Estos laboratorios brindan al lector una valiosa experiencia práctica. ISL es apropiado para estudiantes avanzados de pregrado o maestría en Estadística o campos cuantitativos relacionados, o para personas en otras disciplinas que deseen utilizar herramientas de aprendizaje estadístico para analizar sus datos. Se puede utilizar como libro de texto para un curso que abarque dos semestres.

#### CAP.10 Aprendizaje profundo

Este capítulo cubre el importante tema del aprendizaje profundo. En el momento de la escritura profunda (2020), es un área de investigación muy activa en las comunidades de aprendizaje automático e inteligencia artificial. La piedra angular del aprendizaje profundo es la red neuronal. Las redes neuronales saltaron a la fama a finales de la década de 1980. Hubo mucha emoción y cierto entusiasmo asociado con este enfoque, y fueron el ímpetu de las populares reuniones de Sistemas de procesamiento de información neuronal (NeurIPS, anteriormente NIPS) que se llevan a cabo todos los años, generalmente en lugares exóticos como estaciones de esquí. A esto le siguió una etapa de síntesis, en la que aprendices automáticos, matemáticos y estadísticos analizaron las propiedades de las redes neuronales; se mejoraron los algoritmos y se estabilizó la metodología. Luego llegaron las SVM, los boosting y los bosques aleatorios, y las redes neuronales cayeron un poco en desgracia. Parte de la razón fue que las redes neuronales requerían muchos retoques, mientras que los nuevos métodos eran más automáticos. Además, en muchos problemas, los nuevos métodos superaron a las redes neuronales mal entrenadas. Este fue el statu quo durante la primera década del nuevo milenio. Mientras tanto, sin embargo, un grupo central de entusiastas de las redes neuronales estaba impulsando su tecnología con más fuerza en arquitecturas informáticas y conjuntos de datos cada vez más grandes. Las redes neuronales resurgieron después de 2010 con el nuevo nombre de aprendizaje profundo, con nuevas arquitecturas, campanas y silbatos adicionales y una serie de historias de éxito en algunos problemas de nicho, como la clasificación de imágenes y videos, el modelado de voz y texto. Muchos en el campo creen que la razón principal de estos éxitos es la disponibilidad de conjuntos de datos de entrenamiento cada vez más grandes, que son posibles gracias al uso a gran escala de la digitalización en la ciencia y la industria.

En este capítulo, analizamos los conceptos básicos de las redes neuronales y el aprendizaje profundo, y luego analizamos algunas de las especializaciones para problemas específicos, como las redes neuronales convolucionales (CNN) para la clasificación de imágenes y las redes neuronales recurrentes (RNN) para series temporales y otros. secuencias. También demostraremos estos modelos utilizando el paquete R keras, que interactúa con el software de aprendizaje profundo tensorflow desarrollado en Google.1 El material de este capítulo es un poco más desafiante que en otras partes de este libro.

### 10.1 Redes neuronales de una sola capa

Una red neuronal toma un vector de entrada de p variables X = (X1, X2,...,Xp) y construye una función no lineal f(X) para predecir la respuesta Y . Hemos construido modelos de predicción no lineales en capítulos anteriores, usando árboles, potenciando y modelos aditivos generalizados. Lo que distingue a las redes neuronales de estos métodos es la estructura particular del modelo. La figura 10.1 muestra una red neuronal de avance simple para modelar una red neuronal de avance de respuesta cuantitativa usando p = 4 predictores. En la terminología de las redes neuronales, las cuatro características X1,...,X4 constituyen las unidades en la capa de entrada. Las flechas indican que cada una de las entradas de la capa de entrada alimenta cada una de las K unidades de la capa de entrada oculta (podemos elegir K; aquí elegimos 5). El modelo de red neuronal tiene unidades ocultas de la forma 