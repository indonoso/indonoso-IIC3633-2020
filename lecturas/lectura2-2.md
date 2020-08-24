# Collaborative filtering for implicit feedback datasets
> Hu, Y., Koren, Y., & Volinsky, C. (2008). Collaborative filtering for implicit feedback datasets. In Data Mining, 2008. ICDM’08. Eighth IEEE International Conference on (pp. 263-272). IEEE.

- por qué no se comparan con MMMF? no entiendo por qué lo explican, y luego no evalúan con él
- La evaluación es extraña. Si estoy midiendo ranking, debo tener una lista que le mostré al usuario y medir con una métrica de ranking tipo ndcg o recall o precision@n

- es interesante notar que most popular es mejor que random.

En este paper los autores presentan un criterior de optimización de paramétros con el objetivo que entregar mejores ratings. Detallan el criterio de optimización y cómo se calculan los paramétrocps con el método descenso del gradiente estocástico para cualquier modelo. Realizan una evaluación comparando con dos modelos de factorización matricial, Cosine User KNN y most popular. Sus resultados muestran que consistentemente su metodología para encontrar paramétros es mejor en los dos datasets que evaluaron.

Algo que me parece particular de este artículo es la forma en que se realiza la evaluación. Ellos tomaron dos datasets, uno de ventas online que tiene historia de compra y quieren predecir la siguiente. El otro es un dataset de netflix donde tienen rankings y los transforman en implicit feedback eliminando el valor del ratings, dejando como tarea si el usuario va a rankear o no la película.

Estos dos datasets tienen problemas. El primero es un historial de compras, por lo tanto hay un componente prescendencia, hay items que fueron comprados antes y otros después por un mismo usuario, por lo que las entradas no son independientes entre sí. El segundo está tratando de predecir si el usuario va a rankear una película, pero el usuario puede no haberle gustado esa película, ¿qué utilidad tendría recomendarle cosas para que las evalúe si no le gustan? Además la métrica de evaluación es AUC, cuando en predicció de ranking ya existen métricas muy estudiadas que miden si una lista de items es apropiada o no para un usuario.




Este paper parte de la premisa que los algoritmos de recomendación están optimizados para precedir ratings y que esa optimización no es un buen criterio para armar rankings. Los autores plantean una forma de utilizar el feedback implícito para calcular los paramétros de un modelo cualquiera utilizando una formulación bayesiana.



En el caso de implicit feedback, ellos plantean que se pueden c describe un criterio para optimizar y el algoritmo para calcularlo,

La evaluación que se realiza no me parece tan correcta o al menos es cuestionable. Los autores están evaluando un algoritmo que optimiza ranking pero el dataset que tienen solo es de rankings.
