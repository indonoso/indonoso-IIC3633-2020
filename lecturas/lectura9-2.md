# Carousel Personalization in Music Streaming Apps with Contextual Bandits
> Bendada, W., Salha, G., & Bontempelli, T. (2020). Carousel Personalization in Music Streaming Apps with Contextual Bandits. 420–425. https://doi.org/10.1145/3383313.3412217

Este artículo presenta una evalución de distintos métodos de Multi-armed bandit para seleccionar los ítems que deben ir en la sección de recomendación de listas de reproducción de la aplicación [Deezer](https://www.deezer.com/es/). Estas recomendaciones tienen dos características: es una lista con un tamaño fijo (12 como máximo) y el feedback que dan los usuarios es implícito: se escuchó o no se escuchó la lista de reproducción.
Los autores testean varios métodos de recomendación con bandits (10 en total) con distintos niveles de personalización segmentada y muestran la evaluación de laboratorio y de _AB testing_ realizado en la plataforma.

Algo particular de este _paper_ es que es de industria, por lo que lo que buscan testear y probar está muy relacionado a cómo se maneja la aplicación en producción. Los tres aspectos que evalúan tienen relación con un aspecto de mantener una aplicación en producción:

1. Personalización, relacionado con la cantidad de parámetros a entrenar
2. Batch feedback, relacionado con cada cuánto se actualizan los algoritmos
3. Captura del feedback implícito, relacionado con la interfaz de recomendación

Estos aspectos son extremadamente importantes en cualquier sistema de _Machine  Learning_ que esté en producción y en papers de la academia no se toman mucho en cuenta porque no se considera que las métricas de _performance_ son lo único importante. En la industria, muchas veces se va a preferir algo un poco menos preciso en el corto plazo por apostar a tener mayor capacidad de ir mejorando semana a semana el modelo.

Un aspecto que creo que este artículo podría mejorar es el reporte de los resultados. Probaron muchos algoritmos y usaron colores para diferenciarlos en el gráfico pero el rango no hace posible diferenciarlos tan fácilmente. Habría sido mejor usar símbolos o líneas punteadas para diferenciar mejor algunos de ellos. En las figuras 3 y 4 los colores se repiten pero para otros algoritmos, lo que es super confuso. Si hubiesen usado otra marca visual para mostrar el tipo de algoritmo (forma o línea) habría sido más fácil entender los gráficos.
