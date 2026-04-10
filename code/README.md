# Documentación
Para la realizacion de este trabajo los algortimos QuickSort, MergueSort, naive y strassen se extragieron de las siguientes referencias
https://www.geeksforgeeks.org/dsa/quick-sort-algorithm
https://www.geeksforgeeks.org/dsa/merge-sort
https://www.geeksforgeeks.org/dsa/strassens-matrix-multiplication (Aqui se encuentra el naive y el strassen)

## Entrega

La entrega se realiza vía **aula.usm.cl** en formato `.zip`.
Para correr ambos main, make run en la carpeta respectiva.

Arturo Andres Almonacid Vargas
rol: 202373515-9

## Multiplicación de matrices
Naive
    Recorre filas de la primera matriz y columnas de la segunda,
    Calculando cada elemento como el producto punto entre fila y columna.

Strassen
    Primero ajusta las matrices a un tamaño potencia de 2 rellenando con ceros.
    Luego divide cada matriz en 4 submatrices y aplica recursión para
    Combinar sumas, restas y 7 multiplicaciones recursivas en vez de 8.
    Finalmente reconstruye la matriz resultado y recorta el padding extra.

### Programa principal

    Recorre los archivos de entrada de matrices y trabaja solo con aquellos
    que corresponden a la primera matriz de cada par (_1.txt).
    A partir de ese nombre busca automáticamente su archivo par (_2.txt)
    para poder multiplicar ambas matrices.

    Luego lee las dos matrices desde los archivos y ejecuta sobre ellas
    los algoritmos Naive y Strassen, midiendo en ambos casos el tiempo
    de ejecución y la memoria dinámica utilizada en el heap mediante
    una misma función de medición.

    Finalmente, guarda los resultados de tiempo y memoria en un archivo
    de mediciones y escribe en otro archivo la matriz resultado obtenida.
    
### Scripts

matrix_generator.py
    Genera los casos de prueba de las matrices con 2^4, 2^6, 2^8

plot_generator_matrices.py
    Se generaran gráficos de lineas que muestran el cambio a medida que crecen los datos,
    pero no fueron usados. Y graficos graficos de barras que comparan memoria y tiempo para 
    los 3 n, en total 6 graficos.

## Ordenamiento de arreglo unidimensional

MergeSort
    Recursivamente divide el arreglo en mitades hasta tener subarreglos de un solo elemento.
    Luego va combinando esas partes ordenándolas mediante una función merge que une dos subarreglos ordenados en uno solo.
QuickSort
    Selecciona un pivote y reorganiza el arreglo colocando los elementos menores a la izquierda y mayores a la derecha.
    Luego aplica el mismo proceso de forma recursiva en cada lado.
Sort
    Utiliza la función de ordenamiento de la STL, que internamente aplica un algoritmo optimizado para ordenar el arreglo directamente.

### Programa principal
    Recorre todos los archivos de entrada contenidos en la carpeta de arreglos.
    Cada archivo se lee y su contenido se transforma en un vector, que luego
    se usa como entrada para los distintos algoritmos de ordenamiento.

    Para cada método se trabaja sobre una copia del arreglo original, de modo
    que todos ordenen exactamente los mismos datos.

    El tiempo de ejecución y la memoria dinámica utilizada se miden mediante
    una única función de medición. En este caso, la memoria registrada
    corresponde al uso del heap durante la ejecución.

    Luego, los resultados de tiempo y memoria de cada algoritmo se guardan
    en un archivo de mediciones, y además se escribe en otro archivo
    el arreglo resultante ya ordenado.

### Scripts

array_generator.py
    Genera los casos de prueba de los arreglos 10^1, 10*^3, 10^5

plot_generator.py
    Se generaran gráficos de lineas que muestran el cambio a medida que crecen los datos,
    pero no fueron usados. Y graficos graficos de barras que comparan memoria y tiempo para 
    los 3 n, en total 6 graficos.