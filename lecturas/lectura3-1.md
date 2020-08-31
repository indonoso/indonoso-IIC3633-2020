# Evaluating recommendation systems

> Guy, S., & Gunawardana, A.. (2011) “Evaluating recommendation systems.” In Recommender systems handbook, pp. 257-297. Springer US, 2011.

Este capítulo del libro _Recommender systems handbook_ describe varias propiedades de los recomendadores que, de acuerdo a los autores, deberíamos considerar al realizar un benchmark.
Parte explicando cuando realizar los distintos tipos de experimentos (_offline_, _user study_, _A/B testing_), cómo analizar los resultados y finalmente explica las propiedades o características que podríamos querer en un sistema recomendador y cómo se pueden evaluar cada una de ellas en experimentos.

Hay varios aspectos del capítulo que son cuestionables. Primero, los autores dicen muchas cosas sobre el comportamiento de los usuarios pero sin fuentes que los respalden.
Son cuidadosos en ponerlos como ejemplo o casos hipotéticos pero sustentan varios de sus puntos en base a ellos sin tener certeza de que los usuarios realmente se comporten así.
Por ejemplo, cuando explican cómo los usuarios se pueden beneficiar de _confidence scores_ dicen:

> For example, if a system recommends a movie with very high confidence, and another movie with the same rating but a lower confidence, the user may add the first movie immediately to the watching queue, but may further read the plot synopsis for the second movie, and perhaps a few movie reviews before deciding to watch it

o cuando explican que para _user preference_ es mejor correr un estudio de usuarios y pedirles que elijan un algoritmo dicen:

> This evaluation does not restrict the subjects to specific properties, and it is generally easier for humans to make such judgments than to give scores for the experience.

En ninguno de estos casos presentan evidencia (cita a algún paper) de que los usuarios realmente se comporten así. A pesar de que son ejemplos creo que hay formas de presentar estos casos con más cuidado o con mayor evidencia.

Me llama mucho la atención que todo lo de evaluación se define con respecto al algoritmo, y solo mencionan tangencialmente la interfaz que se utiliza para recomendar.
Este handbook se publicó el 2011 pero ya en el 2003 habían papers que mostraban que la interfaz de recomendación influye en la opinión de los usuarios sobre los ítems, y por lo tanto podría influir en la performance del algoritmo ([Is seeing believing?: how recommender system interfaces affect users' opinions](https://dl.acm.org/doi/10.1145/642611.642713)). En este capítulo solo mencionan la experiencia de usuario, pero la tratan como algo muy independiente del sistema. cuando en verdad está relacionado.
Es interesante que en el handbook del 2015 (segunda edición de este mismo libro), crean una sección para evaluación con varios capítulos (en el 2011 la sección es evaluación y aplicaciones) y agregan uno evaluación de experiencia de usuario.


Algo que me llama la atención es que describen varias métricas para medir ranking y prediction accuracy pero en verdad en todo el tiempo que llevo leyendo papers del área (varios años ya) solo he visto que usen un puñado de ellas: ndcg, map, RSME, precision, recall, fscore, AUC. Los autores presentan varias métricas con variaciones pero no citan papers que las utilicen en sus evaluaciones. 
