# BDC2020MX
En este repositorio presentamos el trabajo de Luis Fernando Pardo Sixtos y Andrea Monserrat Ruiz Gómez para la Brewing Data Cup 2020

Nuestra solución principal, con la que alcanzamos nuestra mejor resultado, utiliza una versión modificada de k-medias con las siguientes particularidades:

* Acepta puntos repetidos, pero no permite que se encuentren en el mismo cluster.
* A partir de una iteración dada se balancea la cantidad de clientes por zona, dispersando el excedente de clientes de manera aleatoria, dando preferencia a los clusters con menos clientes.
* A partir de una iteración dada se balancea la cantidad de clientes por zona, dispersando el excedente de volumen (clientes) de manera aleatoria, dando preferencia a los clusters con menos volumen.

El algoritmo está implementando utilizando la paquetería de pytorch, permitiendo una ejecución eficiente de operaciones matriciales y su uso en equipos con CUDA.
