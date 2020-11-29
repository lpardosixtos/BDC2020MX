# BDC2020MX
En este repositorio presentamos el trabajo de Luis Fernando Pardo Sixtos y Andrea Monserrat Ruiz Gómez para la Brewing Data Cup 2020

Nuestra solución principal, con la que alcanzamos nuestra mejor resultado, utiliza una versión modificada de k-medias con las siguientes particularidades:

* Acepta puntos repetidos, pero no permite que se encuentren en el mismo cluster.
* A partir de una iteración dada se balancea la cantidad de clientes por zona, dispersando el excedente de clientes de manera aleatoria, dando preferencia a los clusters con menos clientes.
* A partir de una iteración dada se balancea la cantidad de clientes por zona, dispersando el excedente de volumen (clientes) de manera aleatoria, dando preferencia a los clusters con menos volumen.
* Si no se ejectua balanceo, entonces se evalua las métricas de nodos y volumen, se construye un frente de pareto utilizando estas dos cantidades. Si el acomodo actual entra en el frente de pareto, se guarda para más tarde.
* Este algoritmo no ofrece una sola solución, sino un arreglo de soluciones con los mejores valores encontrados para las restricciones solicitadas.

El algoritmo está implementando utilizando la paquetería de pytorch, permitiendo una ejecución eficiente de operaciones matriciales y su uso en equipos con CUDA.
