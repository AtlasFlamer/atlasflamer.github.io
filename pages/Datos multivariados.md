## Tabla de contingencia
	- | id Pasajero | Clase | Satisfacción |
	  | --- | --- | --- |
	  | 1 | E | 2|
	  |2 | E | 4|
	  |3 | B | 1 |
	- Dos variables: Una ordinal y otra nominal (tratable como categórica)
	- Conteo de frecuencias
	- Múltiples clases que tienen distintos nivel de satisfacción. Se puede elaborar una matriz de correlación entre las clases y las variables presentes.
- Como armamos una tabla con variables continuas? Establecemos rangos.
- Por cada combinación de variables anotamos la cantidad de individuos que cumplen con esa condición.
- Cada una de las filas $x_1, ..., x_k$ La etiqueta de cada uno de los valores que toma la variable $x$, como puede ser la clase del vuelo. Se repite el mismo ejercicio con la variable $y$ que bien puede ser el rango. Se anota en esa columna la cantidad de individuos que cumple con esa combinación de variables.
- La última fila representa la suma de todos los elementos de la columna la cual se denota por $n_{1.}, ..., n_{K.}$
-
- ## Frecuencias absolutas marginales
- $$n = \sum _ {k=1} ^ {K} n_{k.} = \sum _{j=1}^j n_{.j} =\sum _ {k=1} ^ K \sum _{j=1}^Jn_{kj.}$$
- ## Frecuencias relativas marginales
- $$1 = \sum _ {k=1} ^ {K} n_{k.} = \sum _{j=1}^j n_{.j} =\sum _ {k=1} ^ K \sum _{j=1}^Jn_{kj.}$$
-
- ## Frecuencias condicionales
- La frecuencia condicional es una medida estadística que permite analizar la relación entre dos variables. Se refiere a la probabilidad de que ocurra un evento B, dado que ha ocurrido un evento A. En otras palabras, para calcular la frecuencia condicional se dividen los casos en los que se cumple tanto A como B, entre los casos en los que se cumple únicamente A. Esto permite entender cómo influye un evento en la ocurrencia de otro.
- $$f_{k|j} = \frac {f_{kj}} {f_{.j}} = \frac {n _{kj}} {n_{.j}}$$
- Tomo cualquiera de los valores $f_{kj}$ y lo divido por el total de la fila $f_{.j}$.
- A partir de una tabla con múltiples mediciones con variabilidad e incertidumbre. Podemos finalmente resumir esta tabla con un gráfico multivariable.
- *"Los pasajeros que tienen una clase económica tienen una satisfacción más baja que los que tienen una clase mayor"*. Es esto correcto? Puede eventualmente ser una tendencia. El problema es que las otras clases tienen muchos menos clientes que la clase económica así que no podemos comparar directamente los elementos.
- La clase *Bussiness* tiene una mayor cantidad que entregó una valoración 3.
- ### Considerando la frecuencias condicionales
- Mayoritariamente la experiencia de las otras clases es mejor que las del nivel economy
- ## Gráfico de frecuencia acumulada
- Resumen de los datos
-
-