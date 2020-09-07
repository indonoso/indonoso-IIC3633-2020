# Document clustering based on non-negative matrix factorization
> Xu, W., Liu, X., & Gong, Y. (2003). Document clustering based on non-negative matrix factorization. Proceedings of the 26th Annual International ACM SIGIR Conference on Research and Development in Informaion Retrieval - SIGIR ’03, 267. https://doi.org/10.1145/860435.860485

Este paper describe el método de factorización matricial no negativa que para clustering de documentos.
Básicamente es una descomposición matricial en donde los parámetros de las matrices son todos positivos y las direcciones del espacio latente no son necesariamente ortogonales.
Estas dos características hacen que se puedan obtener clusters directamente a partir del output de la factorización y no que se deba utilizar un método de clustering adicional sobre el espacio latente encontrado, como ocurre con SVD.

El paper explica el modelo muy bien pero me quedan dudas con la evaluación que realizan. Dicen:
> The testing data used for evaluating the proposed document clustering method are formed by mixing documents from multiple clusters randomly selected from the document corpus.
At each run of the test, documents from a selected number k of topics are mixed, and the mixed document set, along with the cluster number k, are provided to the clustering process.

De esto no queda claro si hubo reemplazo (¿un documento puede haber aparecido en varias rondas de test?). Más adelante explican que hicieron 50 tests, pero solo reportan la media y no la desviación estándar.

Otra cosa que no entiendo es por qué utilizaron `k=10` como máximo cuando en ambos datasets la cantidad de clusters es más de 50. Esto, sobre todo porque ellos mismos explican que los clusters que ellos encuentran se pueden superponer entre sí, por lo que es más probable que con un `k` igual al número de clusters real es menos probable encontrar los clusters reales.

Lo otro que faltó en este paper es cómo se comporta en clusters pequeños versus clusters enormes. Ellos mismos hacen hincapié en que hay clusters de 5 documentos y unos con más de mil. Hubiese sido interesante entender cómo se comporta el algoritmo en estos distintos escenarios para poder entender mejor en qué casos es conveniente usarlo.

Por último, y solo como algo anecdótico, es interesante que este método entrega como output algo muy parecido a lo que entrega LDA ([**L**atent **D**irichlet **A**llocation](https://www.jmlr.org/papers/volume3/blei03a/blei03a.pdf)): clusters que se pueden superponer entre sí, un score para cada documento que indica que tan probable es que el documento pertenezca a ese cluster, y clusters definidos con scores para cada feature del input. Estos dos papers fueron publicados el mismo año pero LDA se hizo muchísimo más conocido (33583 para LDA vs 2079 para NNMF). Supongo que el hecho de presentar el LDA en términos más cotidianos (tópicos de documentos) hizo que fuese más fácil entenderlo y usarlo. 
