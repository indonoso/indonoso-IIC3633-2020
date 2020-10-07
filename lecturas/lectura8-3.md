# Inspectability and control in social recommenders

> Knijnenburg, B. P., Bostandjiev, S., O’Donovan, J., & Kobsa, A. (2012). Inspectability and control in social recommenders. Proceedings of the Sixth ACM Conference on Recommender Systems - RecSys ’12, 43. https://doi.org/10.1145/2365952.2365966

Este artículo presenta una evaluación a un sistema de recomendación social. Estos sistemas de filtrado colaborativo son particulares porque la recomendación se hace en base a las acciones de personas que son conocidas para el usuario, por lo que puede ser natural para el usuario querer inspeccionar y controlar cómo se realiza la recomendación.

Los autores realizaron un estudio de usuarios (N=267) con una aplicación de facebook que recomienda bandas de música. El estudio es un 2x3 between subjects study donde hay tres condiciones de controlabilidad y dos de inspectabilidad. Los usuarios respondieron 2 encuestas, una antes del estudio y una post estudio. El objetivo de la primera encuesta era obtener características personales de los participantes y el de la segunda era evaluar la experiencia con el sistema.

Para analizar los resultados, los autores realizaron un análisis de factores latentes y ecuaciones estructurales. Este tipo de análisis se utiliza cuando se quiere medir algo que no es observable. Por ejemplo, la satisfacción con el sistema no se puede medir solo preguntando "¿Estás satisfecho con el sistema?", sino que se mide preguntando varias preguntas que están relacionadas con lo mismo. Con estas preguntas relacionadas se arma un factor latente que representa el constructo que queremos medir. Con este tipo de análisis se se disminuye el error al que pueden inducir las preguntas.

Los autores dicen que realizaron un CFA para confirmar los constructos de acuerdo a <a href="#note1red" id="note1">[1]</a> pero en ese paper no describen cómo realizar un CFA, describen como realizar un EFA y luego un SEM, que sí están relacionados pero no son lo mismo. No sé si esto fue un error conceptual o es solo una equivocación. Otra cosa que me llama la atención es que el diagrama que muestran en el paper (figura 3) no sigue con el estándar típico de SEM, donde:

- Lo observado se ponen en cuadrado (average rating, número de recomendaciones conocidas, etc)
- Lo latente en círculos o elipses (understandability, satisfaction, etc)

Aquí los autores utilizaron otra forma para dibujar el diagrama. Creo que dado que existen al menos dos áreas del conocimiento que ya usan factores latentes ampliamente (psicología y sociología) sería mejor subirse al carro de ellos y continuar con esos mismos estándares.

Por último, no entiendo la figura 4. No sé por qué no dejaron los puntajes escalados de todas las mediciones y no entiendo qué significan las pelotitas y las líneas en forma de cuadrados. Dado que CFA permite estandarizar los valores de todos los factores a una misma escala, se podría haber hecho una tabla con todos y simplemente mostrar los promedios y CI.


<small><a id="note1" href="#note1ref">[1]</a>Knijnenburg, B.P., Willemsen, M.C., Gantner, Z. et al. Explaining the user experience of recommender systems. User Model User-Adap Inter 22, 441–504 (2012). https://doi.org/10.1007/s11257-011-9118-4
