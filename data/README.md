# Documentos fuente

Documentos utilizados como corpus en los experimentos del laboratorio.
Todos son de acceso público.

---

## 1. Código de Trabajo de la República de El Salvador

| | |
|---|---|
| **Archivo** | `codigo_trabajo_es.pdf` |
| **Usado en** | Sección 11 (documentos extensos) y Sección 12 (chunking vs. overlap) |
| **Fuente** | https://www.colsiba.org/wp-content/uploads/2021/09/Cod_Trab_ElSalv1.pdf |
| **Naturaleza** | Norma jurídica de dominio público |
| **Páginas** | *(completar)* |

**Justificación de la selección.** El texto está organizado en artículos breves que enuncian
valores concretos y verificables (plazos, jornadas, porcentajes, montos). Esa estructura es
especialmente adecuada para *Question Answering* extractivo, ya que la respuesta esperada es
un fragmento literal y corto, y permite contrastar objetivamente la salida del modelo contra
el artículo de origen.

---

## 2. Reglamento General de la Ley Orgánica de la Universidad de El Salvador

| | |
|---|---|
| **Archivo** | `reglamento_loues.pdf` |
| **Usado en** | Sección 13 (sistema RAG) y Sección 14 (proyecto final) |
| **Fuente** | https://academica.ues.edu.sv/storage/app/uploads/public/5b7/5b3/0e7/5b75b30e7a3aa989255098.pdf |
| **Naturaleza** | Normativa institucional pública |
| **Páginas** | *(completar)* |

**Justificación de la selección.** El enunciado del proyecto final solicita un asistente
inteligente capaz de responder consultas sobre la normativa de la Universidad de El Salvador.
Este reglamento es el documento base de esa normativa.

---

## 3. Artículo de Wikipedia en español

| | |
|---|---|
| **Archivo** | `wikipedia_articulo.txt` |
| **Usado en** | Sección 10 (comparación de modelos, segundo experimento) |
| **Fuente** | *(completar URL)* |
| **Licencia** | CC BY-SA 4.0 |

---

## Nota sobre el versionado

En este directorio se versionan únicamente los **documentos fuente**. Los artefactos derivados
—texto extraído, fragmentos, *embeddings* e índices FAISS— se regeneran al ejecutar el notebook
y están excluidos mediante `.gitignore`.
