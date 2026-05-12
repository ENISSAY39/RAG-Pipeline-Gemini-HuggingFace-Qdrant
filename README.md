
# 🤖 RAG Pipeline – Gemini + HuggingFace + Qdrant

A Retrieval-Augmented Generation (RAG) pipeline built with:

- Google Gemini
- HuggingFace Sentence Transformers
- Qdrant Vector Database
- Python

This project demonstrates how to build a complete RAG workflow:
- embedding generation
- vector storage
- semantic retrieval
- LLM answer generation

The notebook was developed in Google Colab as part of an AI / Information Retrieval learning project.

---

# 🚀 Features

- 🔎 Semantic search using vector embeddings
- 🧠 Retrieval-Augmented Generation (RAG)
- 📦 Vector database integration with Qdrant Cloud
- 🤖 Gemini LLM response generation
- 📝 Markdown answer rendering
- 📊 Retrieved context visualization with Pandas
- ☁️ Secure API key management using Google Colab Secrets
- ⚡ Fast embedding generation with MiniLM
- 📚 Custom knowledge base ingestion

---

# 🛠 Tech Stack

## AI / LLM
![Gemini](https://img.shields.io/badge/Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)![Sentence Transformers](https://img.shields.io/badge/SentenceTransformers-FF6F00?style=for-the-badge)

## Vector Database
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge)

## Python Ecosystem
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas)![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy)

---

# 🧠 Project Overview

The goal of this project is to implement a complete Retrieval-Augmented Generation pipeline using modern AI tooling.

The workflow follows these steps:

1. Store a knowledge base as embeddings
2. Save vectors into Qdrant Cloud
3. Convert user questions into embeddings
4. Retrieve the most relevant context
5. Send retrieved context to Gemini
6. Generate a final natural-language answer

---

# ⚙️ Pipeline Architecture

## 1. Knowledge Base

A custom knowledge base containing information about:
- Institut Teknologi Sepuluh Nopember (ITS)
- FT-EIC Faculty
- Informatics Department
- Universiti Malaya (UM)

---

## 2. Embedding Generation

The project uses:

```python
all-MiniLM-L6-v2
````

from HuggingFace Sentence Transformers.

The embedding model converts text into dense semantic vectors.

---

## 3. Vector Storage with Qdrant

Embeddings are stored inside a Qdrant Cloud collection configured with:

* Cosine similarity
* Dynamic vector retrieval
* Payload storage for original texts

---

## 4. Retrieval

When a question is asked:

* the query is embedded
* Qdrant retrieves the most relevant vectors
* top-k matching documents are returned

Example:

```python
QUESTION = "What can you tell me about ITS?"
```

---

## 5. Generation with Gemini

Retrieved context is injected into a prompt sent to:

```python
gemini-2.5-flash
```

Gemini then generates a concise Markdown answer using the retrieved knowledge.

---

# 📂 Main Functions

| Function                    | Role                         |
| --------------------------- | ---------------------------- |
| `retrieve_context_qdrant()` | Semantic vector retrieval    |
| `generate_response()`       | Gemini answer generation     |
| `rag_with_gemini()`         | Full RAG orchestration       |
| `show_context_table()`      | Display retrieved results    |
| `show_markdown_answer()`    | Render final Markdown answer |

---

# 🔐 API Keys

The project uses Google Colab Secrets for secure credential management.

Required secrets:

* `QDRANT_URL`
* `QDRANT_API_KEY`
* `GOOGLE_API_KEY`

---

# 📦 Installation

Install dependencies:

```bash
pip install qdrant-client sentence-transformers google-generativeai
```

---

# ▶️ Usage

Run the notebook and execute:

```python
QUESTION = "What can you tell me about ITS?"
results = rag_with_gemini(QUESTION, top_k=5)
```

The pipeline will:

* retrieve relevant context
* display retrieved documents
* generate a final AI answer

---

# 📊 Example Workflow

User Question
↓
Embedding Generation
↓
Qdrant Vector Search
↓
Top-K Context Retrieval
↓
Gemini Prompt Construction
↓
Final AI Response

---

# 🎯 Learning Objectives

This project demonstrates:

* Vector embeddings
* Semantic similarity search
* Retrieval-Augmented Generation
* Prompt engineering
* Vector databases
* LLM orchestration
* AI pipeline integration

---

# 👨‍💻 Author

## Gharbi Yassine

EPF Engineering School – AI & Full-Stack Development

```
```
