# Comparación de Modelos NLP para Análisis de Sentimiento Financiero

## Descripción

Este proyecto compara tres modelos de Procesamiento de Lenguaje Natural (NLP) disponibles en Hugging Face para la tarea de clasificación de sentimiento financiero.

El objetivo es evaluar el desempeño y la eficiencia computacional de cada modelo utilizando un mismo conjunto de datos y métricas estandarizadas.

## Modelos Evaluados

* FinBERT
* RoBERTa-Financiera
* RoBERTa

## Dataset

Twitter Financial News Sentiment

Fuente:

https://huggingface.co/datasets/zeroshot/twitter-financial-news-sentiment

### Estructura

| Campo | Tipo    | Descripción                             |
| ----- | ------- | --------------------------------------- |
| text  | string  | Texto financiero utilizado como entrada |
| label | integer | Etiqueta de sentimiento                 |

Etiquetas:

* 0 = Bearish (Negativo)
* 1 = Bullish (Positivo)
* 2 = Neutral

## Entorno de Ejecución

* Python 3.11
* Google Colab
* GPU NVIDIA T4
* Hugging Face Transformers
* PyTorch

## Instalación

```bash
pip install transformers datasets evaluate accelerate scikit-learn pandas numpy tqdm huggingface_hub sentencepiece
```

## Ejecución

1. Configurar GPU en Google Colab.
2. Configurar token de Hugging Face.
3. Ejecutar todas las celdas del notebook.
4. Generar métricas y tablas comparativas.

## Resultados

| Modelo             | Accuracy | F1-Score |
| ------------------ | -------- | -------- |
| RoBERTa-Financiera | 0.750    | 0.758    |
| FinBERT            | 0.725    | 0.733    |
| RoBERTa            | 0.700    | 0.693    |

## Conclusiones

RoBERTa-Financiera presentó el mejor equilibrio entre precisión y latencia, obteniendo simultáneamente el mayor F1-Score y el menor tiempo promedio de inferencia.

## Estructura del Repositorio

```text
├── notebooks/
│   └── Actividad_4_Gestion_de_Proyectos_de_IA.ipynb
├── results/
│   └── model_comparison_results.csv
├── README.md
└── requirements.txt
```
