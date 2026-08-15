# Laboratorio No. 2 — Question Answering con Transformers y RAG

**Universidad de El Salvador**
Facultad de Ingeniería y Arquitectura
Escuela de Ingeniería de Sistemas Informáticos
Curso de Especialización de Machine Learning — Procesamiento del Lenguaje Natural

---

## Estudiante


| **Nombre** | *Mahalaleel Villalta Martínez* |
| **Carné** | *VM02009*|
| **Docente** | *Bladimir Diaz* |
| **Fecha de entrega** | *22/08/2026* |

## Objetivo

Implementar y evaluar sistemas de *Question Answering* extractivo en español utilizando
modelos Transformer preentrenados, y extender la solución a documentos extensos mediante
fragmentación (*chunking*), *embeddings*, indexación vectorial con FAISS y una arquitectura
**RAG** (*Retrieval-Augmented Generation*).

## Descripción del proyecto

El laboratorio recorre de forma progresiva las siguientes etapas:
    
1. **QA básico** — carga de tokenizer y modelo, pipeline de inferencia, interpretación de la respuesta y su *score*.
2. **Análisis de confianza** — comportamiento del `score`, uso de `top_k`, detección de respuestas de baja confianza y de preguntas sin respuesta en el contexto.
3. **Comparación de modelos** — tres modelos QA en español evaluados sobre los mismos contextos, midiendo respuesta, *score* y tiempo de inferencia.
4. **Documentos extensos** — superación del límite de 512 tokens mediante fragmentación, con comparación de estrategias con y sin solapamiento (*overlap*).
5. **Sistema RAG** — generación de *embeddings*, construcción del índice FAISS, búsqueda semántica, recuperación Top-K y QA sobre los fragmentos recuperados.
6. **Proyecto final** — asistente de consulta sobre normativa de la Universidad de El Salvador.

## Estructura del repositorio

```
LaboratorioML/
├── README.md
├── LaboratorioML.ipynb          Notebook completo y ejecutado
├── requirements.txt
├── .gitignore
│
├── data/                        Documentos fuente de los experimentos
│   └── README.md                Origen y licencia de cada documento
│
├── src/
│   └── funciones_qa.py          Funciones reutilizables extraídas del notebook
│
├── results/
│   ├── resultados_qa.csv
│   ├── comparacion_modelos.csv
│   └── graficos/
│
└── docs/
    └── informe.pdf              Informe técnico
```

## Cómo ejecutar el notebook

### Opción A — Google Colab (recomendada)

1. Abrir `LaboratorioML.ipynb` en [Google Colab](https://colab.research.google.com/).
2. Menú **Entorno de ejecución → Cambiar tipo de entorno de ejecución → T4 GPU**.
3. Ejecutar las celdas en orden (**Entorno de ejecución → Ejecutar todas**).

La primera ejecución descarga los modelos desde Hugging Face (~1.5 GB) y toma varios minutos.
Las descargas quedan en caché durante la sesión.

### Opción B — Local

```bash
python -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
jupyter notebook LaboratorioML.ipynb
```

> En CPU la comparación de modelos y la generación de *embeddings* son notablemente más lentas.

## Dependencias principales

| Librería | Uso |
|---|---|
| `transformers` | Modelos QA preentrenados y tokenizers |
| `torch` | Motor de inferencia |
| `sentence-transformers` | Generación de *embeddings* semánticos |
| `faiss-cpu` | Base vectorial e índice de búsqueda |
| `pymupdf` | Extracción de texto de los PDF fuente |
| `pandas` / `numpy` | Tablas de resultados y operaciones numéricas |
| `matplotlib` | Gráficos de *scores* y tiempos |

Versiones exactas en `requirements.txt`.

## Documentos utilizados

| Documento | Sección | Origen |
|---|---|---|
| *(pendiente)* | Documentos extensos, chunking y overlap | |
| *(pendiente)* | Proyecto final RAG | |
| *(pendiente)* | Artículo de Wikipedia en español | |

Detalle y enlaces en [`data/README.md`](data/README.md).

## Modelos utilizados

**Question Answering (extractivo, español)**

| Modelo | Arquitectura |
|---|---|
| *(pendiente)* | |
| *(pendiente)* | |
| *(pendiente)* | |

**Embeddings**

| Modelo | Dimensión |
|---|---|
| *(pendiente)* | |

> Los pesos de los modelos **no** se versionan en este repositorio: Hugging Face los descarga
> automáticamente en la primera ejecución.

## Resultados principales

*(Se completa al finalizar los experimentos.)*

## Conclusiones

*(Se completa al finalizar los experimentos.)*

## Enlaces

- **Notebook:** [`LaboratorioML.ipynb`](LaboratorioML.ipynb)
- **Informe técnico:** [`docs/informe.pdf`](docs/informe.pdf)
