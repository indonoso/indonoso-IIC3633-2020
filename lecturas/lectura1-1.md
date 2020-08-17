# Item-based collaborative filtering recommendation algorithms
> Sarwar, B., Karypis, G., Konstan, J., & Riedl, J. (2001). Item-based collaborative filtering recommendation algorithms. In Proceedings of the 10th international conference on World Wide Web (pp. 285-295).

Este paper propone un nuevo algoritmo basado en filtrado colaborativo, que en vez de usar `k` usuarios cercanos, utiliza los `k` items más similares para generar un espacio de búsqueda de recomendación. El paper describe varias técnicas para calcular la similaridad entre los items y dos formas distintas de hacer predicciones. Los autores realizan diferentes experimentos que los llevan a concluir que item-based CF es mucho mejor que user-based CF. El paper tiene varios problemas que describo a continuación.

La sección de resultados es muy confusa. En la sección 4.2.1 describen cuáles fueron los pasos para realizar los experimentos que básicamente fueron setear parámetros con el training set y luego evaluar el algoritmo y compararlo con otros métodos. Luego, en la sección 4.3 de presentación de resultados, donde uno esperaría que utilizaran los mismos pasos de antes para describir los resultados, describen dos tipos de resultados (quality y performance) que ni siquiera quedan claros. Esta sección está muy desorganizada, de hecho los títulos son los siguientes:

- 4.3 Experimental Results
  - 4.3.1 Effect of Similarity Algorithms
  - 4.3.2 Sensitivity of Training/Test Ratio
  - 4.3.3 Experiments with neighborhood size
  - 4.3.4 Quality Experiments
  - 4.3.5 Performance Results
- 4.4 Sensitivity of the Model size
  - 4.4.1 Impact of the model size on run-time and throughput

no queda claro por qué _Sensitivity of the Model size_ es una sección totalmente aparte y por qué _Impact of the model size on run-time and throughput_ no está en la sección de _Performance Results_. Por otro lado, en ambas secciones describen una forma distinta de setear los parámetros. En la 4.2.1 dicen que hacen 10-fold CV en el training set y en la 4.3 dicen que el training set lo subdividieron en training y test.

En la subseción 4.3.3 _Experiments with neighborhood size_ exponen los resultados de setear el tamaño del vecindario. Esto es muy extraño, porque según lo que dicen en la explicación del método el parámetro `k` _model size_ es el que define cuántos items similares se utilizan para predecir. Nunca hablan de vecindario, por lo que no entiendo a qué se refieren con ese valor. Más adelante en el paper exponen un análisis de sensitividad del _model size_ por lo que se generan aún más dudas.

Por último en la discusión los autores dicen que:

> Therefore, the item-item scheme is capable in addressing the two most important challenges ofrecommender systems for E-Commerce–quality of prediction and high performance.

pero en ninguna parte del paper comparan la performance (en tiempo y espacio) de user-based CF y item-based CF, solo comparan MAE para ambos casos.

Después de leer el paper me quedan muchas dudas sobre los resultados que se obtuvieron y de las conclusiones a las que llegan los autores.
