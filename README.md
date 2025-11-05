ALGORITMO KNN

1.	OBJETIVOS
•	Conocer el funcionamiento del algoritmo KNN (K vecinos más próximos).
•	Analizar la utilidad de los algoritmos KNN.
 
2.	INTRODUCCIÓN
En computación y matemáticas un algoritmo de ordenamiento es un algoritmo que pone elementos de una lista o un vector en una secuencia dada por una relación de orden, es decir, el resultado de salida ha de ser una permutación, o reordenamiento, de la entrada que satisfaga la relación de orden dada. 

Un algoritmo de búsqueda es un conjunto de instrucciones que están diseñadas para localizar un elemento con ciertas propiedades dentro de una estructura de datos; por ejemplo, ubicar el registro correspondiente a cierta persona en una base de datos.

2.1.	 Algoritmo KNN
Las reglas de clasificación por vecindad están basadas en la búsqueda en un conjunto de prototipos de los k prototipos más cercanos al patrón a clasificar. No hay un modelo global asociado a los conceptos a aprender. Las predicciones se realizan basándose en los ejemplos más parecidos al que hay que predecir. El coste del aprendizaje es 0, todo el coste pasa al cálculo de la predicción. [1]

K-Nearest-Neighbor es un algoritmo basado en instancia de tipo supervisado de Machine Learning. Puede usarse para clasificar nuevas muestras (valores discretos) o para predecir (regresión, valores continuos). Al ser un método sencillo, es ideal para introducirse en el mundo del Aprendizaje Automático. Sirve esencialmente para clasificar valores buscando los puntos de datos “más similares” (por cercanía) aprendidos en la etapa de entrenamiento y haciendo conjeturas de nuevos puntos basado en esa clasificación. [2] A diferencia de K-means, que es un algoritmo no supervisado y donde la “K” significa la cantidad de “grupos” (clusters) que deseamos clasificar, en K-Nearest Neighbor la “K” significa la cantidad de “puntos vecinos” que tenemos en cuenta en las cercanías para clasificar los “n” grupos que ya se conocen de antemano, pues es un algoritmo supervisado.

En resumen, el objetivo del algoritmo del vecino más cercano es identificar los vecinos más cercanos de un punto de consulta dado, de modo que podamos asignar una etiqueta de clase a ese punto. [3] En la Figura 1 se muestra lo mencionado.
 
<img width="567" height="194" alt="image" src="https://github.com/user-attachments/assets/f6310635-3f3b-42b6-94e1-8e2fa0e271bc" />

Figura 1. Funcionamiento del KNN.

Para llevar a cabo el aprendizaje supervisado se necesita datos etiquetados. ¿Cómo se puede obtener datos etiquetados? Hay varias formas de obtener datos etiquetados: 
1.	Datos históricos etiquetados
2.	Experimentar para obtener datos: Se puede realizar experimentos para generar datos etiquetados como Pruebas A/B.
3.	Colaboración colectiva

3.	EJERCICIOS PLANTEADOS Y PROGRAMAS IMPLEMENTADOS
Para la implementación del algoritmo de KNN se utilizaron las librerías que se muestran en la Figura 2, estas librerías se encargan de realizar el proceso de aprendizaje y de graficar los datos necesarios.

<img width="393" height="249" alt="image" src="https://github.com/user-attachments/assets/d5b2605d-e8e2-45b8-b856-f3e619e14c05" />

Figura 2. Librerías usadas en KNN.
Se usó la librería de “warnings” para evitar alertas futuras, estas alertas presentan mensaje que podrían ser confundidos por mensajes de error.

3.1.	Implemente el algoritmo de KNN en Python para una tarea de clasificación. Utilice un dataset cuya variable dependiente sea categórica.
Diseño del Algoritmo
1.	En la Figura 3 se muestra la lectura del archivo en sus primeras 10 líneas.

<img width="559" height="240" alt="image" src="https://github.com/user-attachments/assets/3e0b3aac-197a-4231-8293-4eaeab9281ed" />
 
Figura 3. Lectura del dataset a utilizar.

2.	Con la lectura del dataset, se muestra información adicional del dataset mediante el método “describe”, como se muestra en la Figura 4. Como se aprecia se muestra información como: cantidad de elementos en el dataset, valores mínimo y máximo en el dataset, etc.

<img width="554" height="150" alt="image" src="https://github.com/user-attachments/assets/006dfc9c-aa4e-49b1-ab5e-4c7ca8e2ebf4" />
 
Figura 4. Información sobre el Dataset.
3.	A continuación, se muestra un histograma del dataset en el cual se muestra la distribución de los datos del dataset. Ver Figura 5.

<img width="567" height="305" alt="image" src="https://github.com/user-attachments/assets/f549a02d-dfdf-4ebd-9d7a-afe086e68ec9" />

Figura 5. Histograma del Dataset.

4.	En la Figura 6, se muestra el dataset filtrado y ordenado por una de sus variables. En este caso la variable es “Star Rating”, la cual muestra cuantos elementos del dataset tienen 5, 4, 3, 3 y 1 estrella.

<img width="567" height="183" alt="image" src="https://github.com/user-attachments/assets/75c40ffb-4a52-4364-9ab6-b167970cf8ef" />

Figura 6. Filtrado del Dataset.

5.	El siguiente paso es crear el modelo de aprendizaje del dataset. En la Figura 7 se muestra el código implementado.

<img width="567" height="133" alt="image" src="https://github.com/user-attachments/assets/86e066be-6982-415b-8f9b-eab773411781" />
 
Figura 7. Variables a usar del Dataset.
6.	Ahora se crea el modelo para el dataset. El modelo creado tendrá como valor de k = 7. Este valor permitirá un acierto entre 3l 86% y el 90%.

<img width="534" height="224" alt="image" src="https://github.com/user-attachments/assets/11176e8b-a15a-4d4d-873d-f0f803346175" />

Figura 8. Valores de entrenamiento para K = 7.
Análisis y Validación de Solución
1.	En la Figura 9, se muestra los resultados obtenidos para un valor de prueba.

<img width="469" height="334" alt="image" src="https://github.com/user-attachments/assets/874b1e34-3640-4b0f-8507-05ef411f632c" />

Figura 9. Funcionamiento del algoritmo KNN.

2.	En la Figura 10 se muestra la gráfica de los resultados.

<img width="567" height="324" alt="image" src="https://github.com/user-attachments/assets/d2a6cb69-64b7-401f-a808-6c2245b72344" />

Figura 10. Resultados gráficos tras aplicar KNN.
3.	Para mejor el rendimiento del algoritmo se puede calcular el mejor K con el cual trabajar. En este caso se realizó el cálculo para los K entre 1 y 20 como se muestra en la Figura 11. El cálculo demostró que los mejores K para trabajar están entre 7 y 14.

<img width="567" height="324" alt="image" src="https://github.com/user-attachments/assets/487b0b50-cd7d-4e1d-8364-e185a8fc41ff" />

Figura 11. Mejores K con los cuales trabajar.

REFERENCIAS BIBLIOGRÁFICAS
[1]	Cambronero, C. G., & Moreno, I. G. (2006). Algoritmos de aprendizaje: knn & kmeans. Inteligencia en Redes de Comunicación, Universidad Carlos III de Madrid, 23.
[2]	Aprende Machine Learning. (2023, febrero 18). “Clasificar con K-Nearest-Neighbor ejemplo en Python” [Online]. Disponible en: https://www.aprendemachinelearning.com/clasificar-con-k-nearest-neighbor-ejemplo-en-python/
[3]	IBM. (2023, febrero 18). “¿Qué es el algoritmo de k vecinos más cercanos?” [Online]. Disponible en: https://www.ibm.com/co-es/topics/knn
