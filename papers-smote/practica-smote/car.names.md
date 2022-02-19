1. Title: Car Evaluation Database

2. Sources:
   (a) Creator: Marko Bohanec
   (b) Donors: Marko Bohanec   (marko.bohanec@ijs.si)
               Blaz Zupan      (blaz.zupan@ijs.si)
   (c) Date: June, 1997

3. Uso pasado:

   El modelo de decisión jerárquico, del que se deriva este conjunto de 
   datos, se presentó por primera vez en 

   M. Bohanec y V. Rajkovic: Adquisición de conocimiento y explicación 
   para la toma de decisiones de atributos múltiples. En el 8º Taller 
   Internacional sobre Sistemas Expertos y sus Aplicaciones, Avignon, 
   Francia. páginas 59-78, 1988. 

   Dentro del aprendizaje automático, este conjunto de datos se utilizó 
   para la evaluación de HINT (herramienta de inducción de jerarquía), 
   que demostró ser capaz de reconstruir completamente el modelo jerárquico
   original. Esto, junto con una comparación con C4.5, se presenta en 

   B. Zupan, M. Bohanec, I. Bratko, J. Demsar: Machine learning by function
   decomposition. ICML-97, Nashville, Tennessee. 1997 (por aparecer)

4. Relevant Information Paragraph:

   Car Evaluation Database was derived from a simple hierarchical
   decision model originally developed for the demonstration of DEX
   (M. Bohanec, V. Rajkovic: Expert system for decision
   making. Sistemica 1(1), pp. 145-157, 1990.). The model evaluates
   cars according to the following concept structure:

   CAR                      aceptabilidad del coche
   . PRICE                  Precio total
   . . buying               precio de compra
   . . maint                precio del mantenimiento
   . TECH                   características técnicas
   . . COMFORT              comodidad
   . . . doors              número de puertas
   . . . persons            capacidad en términos de personas para transportar
   . . . lug_boot           el tamaño del maletero
   . . safety               seguridad estimada del coche

   Los atributos de entrada se imprimen en minúsculas. Además del concepto objetivo (CAR), 
   el modelo incluye tres conceptos intermedios: PRECIO, TECNOLOGÍA, CONFORT. 
   En el modelo original, cada concepto está relacionado con sus descendientes de nivel inferior 
   mediante un conjunto de ejemplos (para ver estos conjuntos de ejemplos, consulte http://www-ai.ijs.si/BlazZupan/car.html).

   La base de datos de evaluación de automóviles contiene ejemplos con la información estructural eliminada, es decir, relaciona directamente el CAR con los seis atributos de entrada: compra, mantenimiento, puertas, personas, lug_boot, seguridad.

   Debido a la estructura conceptual subyacente conocida, esta base de datos puede ser particularmente útil para probar métodos de inducción constructiva y descubrimiento de estructuras.

5. Número de instancias: 1728
    (las instancias cubren completamente el espacio de atributos)

6. Número de atributos: 6

7. Valores de atributo:

   buying       v-high, high, med, low
   maint        v-high, high, med, low
   doors        2, 3, 4, 5-more
   persons      2, 4, more
   lug_boot     small, med, big
   safety       low, med, high

8. Valores de atributos faltantes: ninguno

9. Distribución de clases (número de instancias por clase)

   class      N          N[%]
   -----------------------------
   unacc     1210     (70.023 %) 
   acc        384     (22.222 %) 
   good        69     ( 3.993 %) 
   v-good      65     ( 3.762 %) 

la distribución de clases habla sobre si el modelo de automovil es 

   unacc (inaceptable)
   acc (aceptable)
   good (bueno)
   v-good (muy bueno)