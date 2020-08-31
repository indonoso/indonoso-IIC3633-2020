

- En el paper se dicen muchas cosas sobre el comportamiento de los usuarios pero sin fuentes que los respalden. Son cuidadosos en ponerlos como ejemplo o casos hipotéticos pero sustentan varios de sus puntos en base a ellos sin tener certeza de que los usuarios realmente se comporten así. Por ejemplo:

> For example, if a system recommends a movie with very high confidence, and another movie with the same rating but a lower confidence, the user may add the first movie immediately to the watching queue, but may further read the plot synopsis for the second movie, and perhaps a few movie reviews before deciding to watch it


> This evaluation does not restrict the subjects to specific properties, and it is generally easier for humans to make such judgments than to give scores for the experience. Then,



- Describen varias métricas para medir ranking y prediction accuracy pero en verdad en todos estos años solo he visto que usen un puñado de ellas: ndcg, map, RSME, precision, recall, fscore, AUC. Se presentan varias métricas con variaciones pero en verdad esas se usan poco en general (varias eran nuevas para mí). De hecho me llama la atención que no citen papers que las utilicen. Supongo que no se usan porque son muy complejas de calcular.

- Me gusta la deficiones que hacen de las propiedades de los recsys. Algunas son muy cuestionables pero en cada una definen una razón de existir y alguna forma de medirla. varias se podrían juntar en una misma, pero supongo que era mejor desagregar para mostrar los recsys como más complejos

- Me llama mucho la atención que todo lo de evaluación se define con respecto al algoritmo,tangencialmente mencionan la interfaz. En el handbook del 2015, el capítulo de evaluación es básicamente SEM y evaluación de experiencia del usuario. En este capítulo solo mencionan la expeiencia de usuario, pero la tratan como algo muy independiente del sistema. cuando en verdad está relacionado (https://dl.acm.org/doi/10.1145/642611.642713).




- El paper asume que los usuarios son super complejos en su comportamiento con los sistemas
- Casi nadie usa ratings ahora y solo tienen un feedback binario
- Las métricas que describe son super complejas. Los researchers usan 2 o 3 y sería.
