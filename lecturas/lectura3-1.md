# Evaluating recommendation systems

> Guy, S., & Gunawardana, A.. (2011) “Evaluating recommendation systems.” In Recommender systems handbook, pp. 257-297. Springer US, 2011.

Este capítulo del libro _Recommender systems handbook_ describe varias propiedades de los recomendadores que, de acuerdo a los autores, deberíamos considerar al realizar un benchmark de recomendadores.
Parte explicando cuando realizar experimentos los distintos tipos de experimentos (offline, user study,A/B testing), cómo analizar los resultados y finalmente explica las propiedades o caracteristicas que podríamos querer en un sistema recomendador y cómo se pueden evaluar cada una de ellas en experimentos.

Hay varios aspectos del capítulo que son cuestionables. Primero, los autores dicen muchas cosas sobre el comportamiento de los usuarios pero sin fuentes que los respalden.
Son cuidadosos en ponerlos como ejemplo o casos hipotéticos pero sustentan varios de sus puntos en base a ellos sin tener certeza de que los usuarios realmente se comporten así.
Por ejemplo, cuando explican cómo los usuarios se pueden beneficiar de _confidence scores_:

> For example, if a system recommends a movie with very high confidence, and another movie with the same rating but a lower confidence, the user may add the first movie immediately to the watching queue, but may further read the plot synopsis for the second movie, and perhaps a few movie reviews before deciding to watch it

o cuando explican que para _user preference_ es mejor correr un estudio de usuarios y pedirles que elijan un algoritmo dicen:
> This evaluation does not restrict the subjects to specific properties, and it is generally easier for humans to make such judgments than to give scores for the experience.

esta declaración sustenta el punto de realizar un _user study_ pero no presentan evidencia de que los usuarios realmente se comporten así.

Me llama mucho la atención que todo lo de evaluación se define con respecto al algoritmo, tangencialmente mencionan la interfaz que se utiliza para recomendar.
Este handbook se publicó el 2011 pero ya en el 2003 habían papers que mostraban que la interfaz de recomendación influye en la opinión de los usuarios sobre los ítems, y por lo tanto en la performance del algoritmo ([Is seeing believing?: how recommender system interfaces affect users' opinions](https://dl.acm.org/doi/10.1145/642611.642713)).

En el handbook del 2015 (segunda edición de este mismo libro), agregan un capítulo  el capítulo de evaluación es básicamente SEM y evaluación de experiencia del usuario. En este capítulo solo mencionan la expeiencia de usuario, pero la tratan como algo muy independiente del sistema. cuando en verdad está relacionado ().



Por otro lado, me gustan las deficiones que hacen de las propiedades de los sistemas recomendadores. Algunas son muy cuestionables, _risk_ por ejemplo, pero en cada una definen una razón de existir y alguna forma de medirla.




- Describen varias métricas para medir ranking y prediction accuracy pero en verdad en todos estos años solo he visto que usen un puñado de ellas: ndcg, map, RSME, precision, recall, fscore, AUC. Se presentan varias métricas con variaciones pero en verdad esas se usan poco en general (varias eran nuevas para mí). De hecho me llama la atención que no citen papers que las utilicen. Supongo que no se usan porque son muy complejas de calcular.







- El paper asume que los usuarios son super complejos en su comportamiento con los sistemas
- Casi nadie usa ratings ahora y solo tienen un feedback binario
- Las métricas que describe son super complejas. Los researchers usan 2 o 3 y sería.
