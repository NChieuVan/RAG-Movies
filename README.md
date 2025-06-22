# RAG_Movies Pipeline

This project implements a **Retrieval-Augmented Generation (RAG)** pipeline to answer questions about a movie dataset using an LLM.

## Main Steps

1. **Load and Prepare Data**
    - Load movie data (Huggingface).
    - Prepare documents to be embedded and stored.

2. **Embedding Generation**
    - Use HuggingFace embeddings (sentence transformers) to convert documents to vector embeddings.

3. **VectorStore**
    - Store embeddings into FAISS VectorStore. (**MongoDB Atlat search vector**)

4. **Retriever**
    - Use retriever to find top-k relevant documents for a given user query. (**cosine highest**)

5. **LLM (RAG)**
    - Combine retrieved documents + user query, and pass to LLM for final answer generation.(**google/gemma-2-2b-it**)

## Main Libraries

- `
from huggingface_hub import login`
- `
from transformers import AutoTokenizer, AutoModelForCausalLM`
- `
import numpy`
- `
import pymongo`
- `from datasets import load_dataset`
- `from google.colab import userdata`
- `from sentence_transformers import SentenceTransformer`
- `import pandas`


## Pipeline Diagram demo
![alt text](<Screenshot 2025-06-23 011137.png>)
## How to Run

```bash


# Run the notebook colab
jupyter notebook RAG_Movies.ipynb
```
