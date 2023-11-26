# Proyecto_de_Investigacion_Analisls_de_algoritmos
Proyecto de investigación


OPTIMIZATION AND CHALLENGES IN THE IMPLEMENTATION OF THE VITERBI ALGORITHM FOR HIDDEN MARKOV MODELS IN NATURAL LANGUAGE PROCESSING


Mateo Fonseca, Andrés Hurtado, Manuel Castro


Universidad Sergio Arboleda


mateo.fonseca01@usa.edu.co, andres.hurtado03@usa.edu.co, manuel.castro01@usa.edu.co 


RESUMEN: El análisis de algoritmos es esencial en la ciencia de la computación debido a su impacto en la eficiencia y el rendimiento de los sistemas informáticos. Al evaluar el tiempo y los recursos que un algoritmo requiere, se pueden tomar decisiones certeras sobre su implementación en problemas dados. Este informe busca analizar el rendimiento del algoritmo de viterbi, utilizado para el procesamiento de lenguaje natural, concretamente la predicción de la palabra que seguirá a la palabra observada, en base a la teoría de los modelos ocultos de Márkov.



ABSTRACT: Algorithm analysis is essential in computer science because of its impact on the efficiency and performance of computer systems. By evaluating the time and resources that an algorithm requires, accurate decisions can be made about its implementation on given problems. This report seeks to analyze the performance of the viterbi algorithm, used for natural language processing, specifically the prediction of the word that will follow the observed word, based on the theory of Markov's hidden models.


I.	INTRODUCCIÓN


Este informe fue realizado con el objetivo de medir y analizar la eficiencia del algoritmo de viterbi aplicando los modelos ocultos de márkov como modelos predictivos en el procesamiento de lenguaje natural. En el contexto del procesamiento del lenguaje natural, los HMM modelan la estructura latente de secuencias de palabras en un texto, donde los estados ocultos representan categorías gramaticales. El algoritmo de Viterbi es una técnica eficiente para encontrar la secuencia más probable de estados ocultos dadas las observaciones. Utilizando programación dinámica, el algoritmo calcula recursivamente las probabilidades máximas de llegar a cada estado en cada paso de tiempo, permitiendo así la identificación de la secuencia óptima de estados ocultos, fundamental para tareas como la predicción de la siguiente palabra en modelos de lenguaje basados en HMM.



II.	OBJETIVOS 


•	Objetivo General


El propósito fundamental de este proyecto es realizar un análisis exhaustivo y optimización del desempeño del algoritmo de Viterbi, integrado con Modelos Ocultos de Markov (HMM), para el Procesamiento de Lenguaje Natural (PLN) en Python. El objetivo central es desarrollar un sistema eficaz capaz de generar, a partir de una cadena de entrada, las palabras con mayor probabilidad de ocurrencia.


•	Objetivos Específicos 



1.	Implementación Eficiente: Desarrollar e implementar el algoritmo de Viterbi en Python, asegurando su eficiencia y modularidad para facilitar la integración con los Modelos Ocultos de Markov seleccionados.

2.	Selección y Adaptación de Modelos HMM: Seleccionar modelos HMM adecuados y adaptarlos para el análisis de lenguaje natural, considerando la diversidad y complejidad inherente al texto.

3.	Conjunto de Datos Representativo: Crear un conjunto de datos que refleje la diversidad lingüística y contextual, proporcionando la base para el entrenamiento y evaluación del sistema.

4.	Evaluación Precisa: Realizar pruebas rigurosas para evaluar la precisión y eficiencia del sistema, empleando métricas estándar de PLN y tiempos de ejecución.

5.	Análisis de Complejidad: Analizar la complejidad temporal y espacial del algoritmo de Viterbi en el contexto de HMM, identificando áreas susceptibles de mejora y optimización.

6.	Optimización del Rendimiento: Mejorar la eficiencia del algoritmo mediante ajustes y optimizaciones en la implementación, buscando una ejecución más rápida y eficaz.



III.	METODOLOGÍA



En el marco de este laboratorio, se adoptó una metodología para examinar la complejidad del algoritmo de viterbi aplicando los modelos ocultos de Márkov como modelos predictivos en el procesamiento de lenguaje natural a la hora de entrenar el modelo en relación con la cantidad de datos. Las pruebas fueron realizadas con un computador de procesador Intel Core i7.



Para comenzar, se definieron claramente los objetivos del estudio, centrados en analizar el tiempo de ejecución y la utilización de memoria del algoritmo en diferentes escalas de datos en el momento en el que el modelo es entrenado. Una consideración crucial fue la selección de datos a utilizar, ya que en la primera prueba se utiliza el mismo conjunto datos, pero con cantidad de datos variable en cada ejecución. En la segunda prueba por otro lado, se utilizan diferentes conjuntos de datos, cada uno con el tamaño completo de palabras que contenía. Como ya se mencionó anteriormente, en ambas pruebas se realizó una comparación del tiempo de ejecución y gasto de memoria con respecto a la cantidad de cada conjunto de datos.



Para garantizar la objetividad y consistencia de los datos, se realizaron 5 ejecuciones con cada conjunto de datos y se promediaron todos los resultados obtenidos para tener una aproximación más precisa a la hora de analizar los datos.



Durante la implementación del algoritmo se utilizaron los decoradores de “%timeit” y “%memit”, funciones disponibles en el entorno de Google Colab, que permitieron obtener en microsegundos el tiempo y en megabytes el consumo de memoria respectivamente al momento de ejecutar el algoritmo de entrenamiento del modelo.



En resumen, esta metodología, que incluyó la definición precisa de objetivos, la selección meticulosa de conjuntos de datos diferentes, la implementación con adaptaciones necesarias, las ejecuciones experimentales y un análisis crítico, proporcionó una comprensión fundamental de la complejidad algorítmica del entrenamiento del algoritmo de viterbi aplicando los modelos ocultos de Márkov como modelos predictivos en el procesamiento de lenguaje natural en distintos entornos enfrentándose a datos que contienen variados contextos.



IV.	RESULTADOS


fetch_20newsgroups (Cartas)
Ejecution	Size (n)	Time (μs)	Memory (Mb)
1	81079	115000	1427.76
2	162158	199000	1427.92
3	243237	403000	1434.12
4	324316	459000	1445.47
5	405397	696000	1457.88
Tabla 1: Prueba de rendimiento con Dataset “fetch_20newsgroups”.

 
Grafica 1: Prueba de rendimiento con Dataset “fetch_20newsgroups” – Tamaño VS Tiempo de ejecución.

 
Grafica 2: Prueba de rendimiento con Dataset “fetch_20newsgroups” – Tamaño VS Gasto de memoria.

Name	Size (n)	Time (μs)	Memory (Mb)
austen-emma	192427	507000	1455.99
austen-persuasion	98171	252000	1455.99
austen-sense	141576	637000	1456.01
bible-kjv	1010654	2980000	1456.01
blake-poems	8354	24300	1456.03
bryant-stories	55563	171000	1456.03
burgess-busterbrown	18963	49500	1456.05
carroll-alice	34110	114000	1456.05
chesterton-ball	96996	415000	1456.05
chesterton-brown	86063	341000	1456.05
chesterton-Thursday	69213	190000	1456.05
edgeworth-parents	210663	541000	1456.06
melville-moby_dick	260819	762000	1456.07
milton-paradise	96825	275000	1456.07
shakespeare-caesar	25833	72900	1456.07
shakespeare-hamlet	37360	120000	1456.07
shakespeare-macbeth	23140	90600	1456.07
whitman-leaves	154883	615000	1456.07
Tabla 2: Prueba de rendimiento con Datasets de distintos tamaños.

 
Grafica 3: Prueba de rendimiento con Datasets de distintos tamaños. – Tamaño VS Tiempo de ejecución.

 
Grafica 4: Prueba de rendimiento con Datasets de distintos tamaños. – Tamaño VS Gasto de memoria.
