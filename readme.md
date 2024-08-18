# Análisis de Sentimientos y Categorización Temática en Documentos PDF

## Descripción del Proyecto

Este proyecto realiza un análisis de sentimientos y categorización temática en un conjunto de documentos PDF en español. Utiliza técnicas de lematización, análisis de frecuencia de palabras y modelos de clasificación para identificar temas relevantes en los documentos y clasificarlos según dichos temas.

### Funcionalidades Principales

1. **Extracción y Preprocesamiento de Texto:**

   - Extrae texto de archivos PDF ubicados en el directorio `Sources/`.
   - Lematiza el texto (reduce las palabras a su forma básica) utilizando un lematizador específico para el idioma español.
2. **Generación y Uso de un Léxico:**

   - Genera un léxico a partir de los documentos PDF que se utiliza para identificar la relevancia de los textos procesados.
   - Sólo los textos relacionados con este léxico son lematizados y guardados en la carpeta `lematizacion`.
3. **Análisis de Frecuencia de Palabras:**

   - Analiza las palabras más comunes en los textos lematizados y las utiliza para definir tres temas (`Tema 1`, `Tema 2`, `Tema 3`).
4. **Categorización Temática:**

   - Calcula puntuaciones para cada documento en función de la frecuencia de palabras relacionadas con los temas definidos.
   - Las puntuaciones se acumulan y se promedian para obtener una visión general del contenido temático.
5. **Clasificación de Documentos:**

   - Se entrenan modelos de clasificación utilizando TF-IDF y algoritmos de Naive Bayes y Random Forest para categorizar los documentos según los temas identificados.
   - Se evalúan los modelos utilizando métricas de precisión en conjunto de pruebas y validación cruzada.

## Estructura del Proyecto

- `Sources/`: Contiene los archivos PDF originales.
- `lematizacion/`: Almacena los textos lematizados que están relacionados con el léxico.
- `lexicon.txt`: Archivo generado que contiene el léxico utilizado para el análisis.
- `analyzer.ipynb`: Script principal que realiza el análisis completo de los documentos.
- `crear_lexicon.ipynb`: Script utilizado para generar el léxico a partir de los documentos PDF.

## Requisitos

- Python 3.x
- Bibliotecas:
  - PyPDF2
  - NLTK
  - scikit-learn
  - NumPy

## Ejecución del Proyecto

1. Coloca tus archivos PDF en la carpeta `Sources/`.
2. Ejecuta `crear_lexicon.ipynb` para generar el léxico basado en los documentos PDF.
3. Ejecuta `analyzer.ipynb` para realizar el análisis de sentimientos y categorización temática.
4. Los resultados se almacenarán en la carpeta `lematizacion/` y se mostrarán en la salida del notebook.

## Autor

Este proyecto fue desarrollado como parte de un trabajo universitario. Si tienes preguntas o deseas contribuir, no dudes en abrir un issue o enviar un pull request.
