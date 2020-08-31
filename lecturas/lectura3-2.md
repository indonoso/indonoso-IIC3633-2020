# Performance of Recommender Algorithms on Top-N Recommendation Tasks
> Cremonesi, P., Koren, Y., & Turrin, R. (2010). Performance of recommender algorithms on top-N recommendation tasks. RecSys’10 - Proceedings of the 4th ACM Conference on Recommender Systems, September, 39–46. https://doi.org/10.1145/1864708.1864721

En este paper los autores realizan un benchmark de algoritmos de recomendación para tareas de ranking.
Ellos buscan demostrar que los algoritmos que se pueden optimizar para reducir el RSME no tienen buena performance en tareas topN.
Además de esto, ellos también demuestran que la forma en que se arma el set de set influye en la evaluación del algoritmo en tareas tipo topN. El artículo describe en detalle cómo armar el dataset de test para tareas de ranking y luego explica en detalle los algoritmos que utiliza en este benchmark.

El aspecto que, creo que es el más rescatable, de este artículo es la metodología de evaluación.
En la mayoría de los papers se crean los set de test simplemente separando una parte del _dataset_ de forma aleatoria o de forma estratificada, y luego se calculan las métricas sobre esos datos.
En este paper se preocuparon de crear un _dataset de test_ con el objetivo de evaluar _ranking_.
Además realizan dos evaluaciones, a todo el dataset de test y a los ítems que quedan en el _long tail_.
Esto es poco habitual y es muy valioso a la hora de evaluar algoritmos, ya que permite entender para qué tipo de ítems sirve el algoritmo.

Un aspecto que podría mejorar del paper es mostrar un análisis un poco más profundo de los datasets que utilizaron. Solo muestran una tabla con algunas características básicas de ambos (número de usuarios, items, density, ..).

Un aspecto que es cuestionable es por qué se tunearon los algoritmos MovieAvg, CorNgbr, AsySVD y SVD++ usando el dataset de Netflix y no se crearon dos modelos, uno para cada dataset. Esto influye en los resultados que obtuviero, AsySVD y SDV++ son mejores que Top-Pop en el dataset de Netflix, a diferencia de MovieLens donde Top-Pop sí era mejor que  AsySVD y SDV++.
Una parte importante de la discusión es sobre la performance de Top-Pop, ellos dicen que hay casos en que este algoritmo muy simple mejora la performance. Sin embargo en el dataset donde los otros algoritmos fueron optimizados para esos datos, Top-Pop no es mejor. Claramente hay un problema con la metodología y las conclusiones que obtuvieron.
