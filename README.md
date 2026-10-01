# analisis-sentimientos-modelos-huggingface
Comparación de modelos preentrenados para análisis de sentimientos en reseñas de productos.
Análisis comparativo de modelos de análisis de sentimientos
Descripción del proyecto

Este proyecto tiene como objetivo evaluar y comparar tres modelos preentrenados de procesamiento de lenguaje natural para la clasificación de sentimientos en reseñas de productos de comercio electrónico.

Se utilizaron modelos disponibles en Hugging Face y se evaluaron sobre una muestra reproducible de 1,000 reseñas del conjunto de datos Amazon Polarity, clasificadas como positivas o negativas.

Los modelos evaluados fueron:

TinyBERT IMDB
DistilBERT SST-2
DistilBERT Product Reviews

La comparación considera métricas de clasificación como Accuracy, Precision, Recall y F1-score, además del tiempo de inferencia y la latencia promedio por reseña.

El propósito del proyecto es analizar el equilibrio entre desempeño, eficiencia y recursos computacionales, identificando las características y compromisos de cada modelo para un posible escenario de análisis automatizado de opiniones de clientes.

Objetivo

Determinar el comportamiento de diferentes modelos preentrenados de análisis de sentimientos bajo las mismas condiciones de evaluación, utilizando métricas de desempeño y eficiencia que permitan realizar una comparación reproducible.

Dataset

Se utilizó el conjunto Amazon Polarity, obtenido mediante Hugging Face con el identificador:

mteb/amazon_polarity

Para el experimento se utilizó la partición test y una muestra de 1,000 registros seleccionada mediante la semilla 42.
