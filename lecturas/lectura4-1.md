# Content-Based Recommendation Systems
> Pazzani, M. J., & Billsus, D. (2007). Content-Based Recommendation Systems. The Adaptive Web, 4321, 325–341. https://doi.org/10.1007/978-3-540-72079-9

Este capítulo del libro _The Adaptive Web_ del año 2007 presenta la recomendación basada en contenidos.
La describen como cualquier sistema donde se debe buscar una forma de describir los ítems, una forma de describir a los usuarios y por último una forma de decidir si un ítem debe o no ser recomendado al usuario.
Los autores primero explican qué es un user profile y describen varios algoritmos (Árboles de decisión, KNN, Rocchio, SVM, Naive Bayes) que se pueden para tomar la decisión de acuerdo a la representación utilizada.

El artículo hace un buen trabajo explicando en general cómo se realiza el procesamiento de texto y justifican porqué es necesario.
Ellos explican que algunas características de los ítems o de los usuarios puede ser del tipo texto y que para usarla efectivamente es necesario hacer un tratamiento.
Por ejemplo, un restaurante de BBQ puede describirse como "restaurant no vegetariano".
Si se generara una feature que indique que el restaurant es vegetariano o no, solo usando la presencia o ausencia de esta palabra, este restaurant sería clasificado como vegetariano cuando claramente no lo es.

Una cosa que sí le falta a este artículo es ir un paso más allá para explicar más en detalle cómo funcionaría el recomendador.
Explican los dos pasos de crear el ítem y user profile pero no explican en la práctica cómo utilizar los algoritmos para poder recomendar, por ejemplo, no queda claro si para cada usuario se debe generar un modelo de clasificación o es un modelo para todos los usuarios. 
