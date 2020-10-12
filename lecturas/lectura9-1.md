# Multi-armed recommender system bandit ensembles
> Cañamares, R., Redondo, M., & Castells, P. (2019). Multi-armed recommender system bandit ensembles. RecSys 2019 - 13th ACM Conference on Recommender Systems, 432–436. https://doi.org/10.1145/3298689.3346984

Este paper presenta el uso de [Multi-armed bandit](https://en.wikipedia.org/wiki/Multi-armed_bandit) para crear recomendadores híbridos. Esta técnica básicamente entrega criterios para seleccionar entre distintas alternativas que compiten entre sí. Cuando se elige una alternativa se calcula el valor ganado y de acuerdo a este se actualizan los criterios de selección para la siguiente iteración.
Los autores utilizan el data set de MovieLens 1M y tres algoritmos de recomendación tradicionales (KNN, Most popular y Factorización Matricial) para mostrar cómo dos tećnicas de Multi-armed badit pueden crear mejores recomendadores que los métodos híbridos que simplemente seleccionan el mejor y que los métodos individuales.

Un aspecto que me llama la atención es que el algoritmo _Most Popular_ es el que obtiene mejor performance de forma individual y obtiene mejor performance que el algoritmo híbrido tradicional.
Los autores lo tratan de explicar con la vulnerabilidad que tienen los KNN al fenómeno de data sparsity pero según lo que hemos leído no hay suficente evidencia de que esto sea así. El valor de sparsity de este dataset es de ~ 4.3% que no es tan bajo en comparación con otros datasets, por lo que debe haber otro aspecto de este dataset que hace que el algoritmo _Most Popular_ tenga mejor performance.

Otro aspecto que creo que faltó fue explicar mejor el resultado de analizar cómo seleccionaba un algoritmo el método de emsemble tradicional. La figura 3 se supone que apoya esta explicación pero no se entiende muy bien loo que quieren ilustrar. Se supone que deberíamos ver como en distintas oportunidades se escoje un algoritmo por sobre otro pero no veo eso en esa figura.
