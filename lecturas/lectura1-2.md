# Netflix Update: Try This at Home

Este artículo fue escrito por Simon Funk (no es su nombre real) el 2006 en el contexto del [Netflix prize](https://www.netflixprize.com/index.html) el 2006. Él fue uno de los primeros que abiertamente publicó sus métodos durante la competencia y llegó a estar tercero en la tabla de resultados.

Este post explica cómo utilizó la descomposición en valores singulares (SVD) para recomendación. Detalla cómo se realiza la descomposición en una matriz muy sparse y cómo resolvió varios problemas que fue encontrando en el camino.

Hay dos cosas que rescato de este artículo. Primero la forma fácil y concreta de explicar los conceptos. Cuando explica por qué una compresión de los datos sí lograría representar los datos dice lo siguiente:

> For instance, any given movie can, to a rough degree of approximation, be described in terms of some basic attributes such as overall quality, whether it's an action movie or a comedy, what stars are in it, and so on. And every user's preferences can likewise be roughly described in terms of whether they tend to rate high or low, whether they prefer action movies or comedies, what stars they like, and so on. And if those basic assumptions are true, then a lot of the 8.5 billion ratings ought to be explainable by a lot less than 8.5 billion numbers, since, for instance, a single number specifying how much action a particular movie has may help explain why a few million action-buffs like that movie.

> A fun property of machine learning is that this reasoning works in reverse too: **If meaningful generalities can help you represent your data with fewer numbers, finding a way to represent your data in fewer numbers can often help you find meaningful generalities.** Compression is akin to understanding and all that.


Por último, creo que es muy admirable que él nunca haya escrito un paper sobre este método
