# Context-aware recommender systems
> Adomavicius, G., & Tuzhilin, A. (2015). Context-aware recommender syst                                         ems. Recommender Systems Handbook, Second Edition, 191–226. https://doi.org/10.1007/978-1-4899-7637-6_6

Este artículo explica el uso de información contextual en sistemas de recomendación. Los autores proponen 3  aspectos para entender los _CARS_.
Primero explican que el contexto en que se da una recomendación está definido por factores y proponen una clasificación de los contextos posibles usando dos dimensiones: conocimiento de los factores y cómo cambian los factores.
A partir de esto se generan 6 clasificaciones de contexto.
Después describen 3 formas en que se incorpora el contexto en el proceso de recomendación: prefiltrado, antes de correr el algoritmo de recomendación, postfiltrado, después de correr el algoritmo y modelamiento, donde el contexto se utiliza como una _feature_ adicional.
Finalmente describen los factores que se consideran de acuerdo a 4 contextos: físico, social, interacción con medios y modal.
El _paper_ termina con la presentación varios ejemplos del uso de contexto en diferentes dominios.

Hay varias cosas del artículo que no me cuadran del todo.
Los autores presentan esta tabla con los diferentes contextos de acuerdo a los dos criterios (conocimiento y tipo de cambio) pero las explicaciones que hacen de cada uno no quedan claras.
No presentan ejemplos para todos los posibles casos y terminan el artículo planteando que esas otras formas de contexto deben ser exploradas.
Básicamente presentan un concepto que todavía no ha sido aplicado y para el cual no son capaces de pensar en un uso posible.
Tampoco utilizan los 3 aspectos que definieron para describir los ejemplos, solo utilizan el último, los tipos de contextos de acuerdo a los factores. Creo que eso le quita debilidad a las definiciones que realizan.

Otro punto que creo que es relevante y que no se aborda en el artículo es cuándo es importante utilizar información contextual. En el trabajo futuro mencionan que hay que explorar cómo y qué información contextual se debería utilizar, pero ¿no se debería partir por entender en qué casos o dominios el contexto es relevante en la recomendación? Hay casos que presentan los autores (en los recomendadores musicales) para los que, en mi opinión, utilizar el contexto es solo por agregar algo a la recomendación pero en realidad no ayuda a mejorar la predicción ni la experiencia de usuario. De hecho los autores prácticamente no hablan de _benchmark_ entre recomendadores con y sin contexto.
