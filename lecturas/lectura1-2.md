# Netflix Update: Try This at Home
> Simon Funk, 2006. [Link](https://sifter.org/simon/journal/20061211.html)

Este artículo fue escrito por Simon Funk el 2006 en el contexto del [Netflix prize](https://www.netflixprize.com/index.html). Él fue uno de los primeros que abiertamente publicó sus métodos durante la competencia y llegó a estar tercero en la tabla de resultados. En este post él explica cómo utilizó la descomposición en valores singulares (SVD) para recomendación. Detalla cómo se realiza la descomposición en una matriz muy sparse y cómo resolvió varios problemas que fue encontrando en el camino.

El artículo es muy fácil de seguir y es hasta divertido en algunas partes. Da definiciones de conceptos complejos pero con palabras simples, algo que en general cuesta que ocurra en los papers más académicos. Un ejemplo de esto es cuando explica por qué una compresión de los datos (una factorización matricial) sí lograría representar los datos:

> For instance, any given movie can, to a rough degree of approximation, be described in terms of some basic attributes such as overall quality, whether it's an action movie or a comedy, what stars are in it, and so on. And every user's preferences can likewise be roughly described in terms of whether they tend to rate high or low, whether they prefer action movies or comedies, what stars they like, and so on. And if those basic assumptions are true, then a lot of the 8.5 billion ratings ought to be explainable by a lot less than 8.5 billion numbers, since, for instance, a single number specifying how much action a particular movie has may help explain why a few million action-buffs like that movie.

Lo que me hubiese gustado ver es cómo realiza la derivación del error aproximado. Es la parte más importante del artículo y no están las fórmulas y el paso a paso de cómo llegó a:

``` C
userValue[user] += lrate * err * movieValue[movie];
movieValue[movie] += lrate * err * userValue[user];
```

Lo que sigue en el artículo es basado en ese resultado, pero simplemente aparecen las ecuaciones (o código en verdad). Además de eso hubiese sido más ilustrativo un ejemplo con números de cómo se ejecutaría paso a paso el algoritmo para descomponer la matriz, tal y como lo hacen en [este post de medium](https://medium.com/datadriveninvestor/how-funk-singular-value-decomposition-algorithm-work-in-recommendation-engines-36f2fbf62cac).

Algo que me parece muy particular es que este algoritmo nunca fue presentado formalmente en una conferencia o journal. Solo se popularizó por este blog post. 
