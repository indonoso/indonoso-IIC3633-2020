# Deep Learning Based Recommender Systems
> Ouhbi, B., Frikh, B., Zemmouri, E., & Abbad, A. (2018). Deep Learning Based Recommender Systems. Colloquium in Information Science and Technology, CIST, 2018-Octob(1), 161–166. https://doi.org/10.1109/CIST.2018.8596492


Este es el review de la segunda parte de este survey. El primer review (hasta la sección 3.4) está en este [link](https://github.com/indonoso/indonoso-IIC3633-2020/blob/master/lecturas/lectura10-1.md).

En la sección 3.5 describen la utilización de RNN en recomendación. Básicamente le han dado tres usos: recomendación durante una sesión sin un identificador, recomendación durante una sesión con identificador y como feature representation. Me llamó la atención que no se mencionara el bias que existe en este tipo de recomendación: el usuario hará click en lo que tenga disponible en la pantalla y eso depende de las recomendaciones que se hayan realizado con anterioridad. No me queda claro si estos algoritmos que mencionan se hacen cargo de este aspecto o simplemente es ignorado.

Un aspecto que los autores no abordan es el tema de la eficiencia de estos métodos. Hay veces en que modelos más simples logran igual o mejores resultados que modelos de redes neuronales que son muy costosos de entrenar. En los artículos que se menciona la eficiencia siempre es solo desde el punto de vista computacional, como mencionan en la sección 3.5 del survey:

> Jannach and Ludewig [68] indicated that some trivial methods (e.g., simple neighbourhood approach) could achieve the same or even better accuracy results as GRU4Rec while being computationally much more efficient.

El tema medioambiental nunca es considerado, a pesar de que la huella de carbono es enorme. Este [artículo](https://www.technologyreview.com/2019/06/06/239031/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/) es un resumen de [este paper](https://arxiv.org/abs/1906.02243) que indica que entrenar un modelo de 213 millones de parámetros genera una huella de carbono igual que la que 4 autos producirán durante toda su vida útil. Por esta razón es tan importante entender la mejora marginal que pueda tener algún modelo de DNN. Si un modelo mejorará solo en un 1% el estado del arte, pero para lograrlo generó una huella de carbono del orden de 4 autos, entonces la mejora no es necesariamente significativa desde el punto de vista práctico.

Un último aspecto que me gustaría mencionar es uno de los desafíos futuros. Los autores mencionan el de realizar _Cross Domain recommendation_, lo plantean como un desafío muy interesante que podría eliminar el problema del cold start y generar mejores recomendaciones. El problema es que no toman en cuenta la privacidad de los usuarios ¿Por qué Google tendría que saber lo que escucho en Spotify? Este desafío puede ser muy interesante desde el punto de vista técnico pero tiene problemas de base que son difíciles de solucionar.
