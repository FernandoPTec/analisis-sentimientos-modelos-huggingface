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

## Entorno de ejecución

El experimento fue desarrollado y ejecutado en **Google Colab**, utilizando una GPU **NVIDIA Tesla T4** para acelerar la inferencia de los modelos.

### Tecnologías utilizadas

* **Python 3**
* **Google Colab**
* **PyTorch**
* **Transformers**
* **Hugging Face Datasets**
* **Hugging Face Hub**
* **scikit-learn**
* **Pandas**

### Modelos evaluados

* `Harsha901/tinybert-imdb-sentiment-analysis-model`
* `distilbert/distilbert-base-uncased-finetuned-sst-2-english`
* `Floressek/sentiment_classification_from_distillbert`

### Dataset

* **Amazon Polarity**
* Identificador: `mteb/amazon_polarity`
* Partición utilizada: `test`
* Muestra evaluada: **1,000 reseñas**
* Semilla de reproducción: **42**

## Pasos de ejecución

1. Clonar o descargar el repositorio desde GitHub.
2. Instalar las dependencias indicadas en `requirements.txt`.
3. Abrir el notebook ubicado en la carpeta `notebooks/`.
4. Ejecutar el notebook en Google Colab o en un entorno compatible con Python y PyTorch.
5. Si es necesario, autenticar la cuenta de Hugging Face mediante `huggingface_hub`.
6. Cargar el dataset `mteb/amazon_polarity` y seleccionar la muestra reproducible de 1,000 reseñas utilizando la semilla `42`.
7. Cargar los tres modelos preentrenados y ejecutar la clasificación de las reseñas.
8. Calcular las métricas de evaluación: Accuracy, Precision, Recall y F1-score.
9. Medir la latencia de inferencia de cada modelo.
10. Consultar la tabla de resultados y las conclusiones generadas por el notebook.

## Conclusiones

La evaluación permitió comparar tres modelos preentrenados para clasificación de sentimientos sobre una muestra de 1,000 reseñas de Amazon Polarity.

Los resultados mostraron diferencias entre desempeño y eficiencia. **TinyBERT IMDB** presentó la menor latencia, con **2.24 ms por reseña**, mientras que **DistilBERT Product Reviews** obtuvo los valores más altos de Accuracy (**0.9090**) y F1-score (**0.9160**), además del mayor Recall (**0.9669**).

Para el caso de uso analizado se seleccionó **DistilBERT Product Reviews** debido a su desempeño y a su orientación hacia reseñas de productos, considerando aceptable su mayor latencia dentro de las condiciones del experimento.

Finalmente, los resultados corresponden a una evaluación sobre una muestra específica y no garantizan el mismo desempeño en datos reales. Antes de una implementación en producción sería necesario realizar pruebas adicionales con datos representativos del entorno objetivo.

