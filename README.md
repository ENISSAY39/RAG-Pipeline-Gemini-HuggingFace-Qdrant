
# 🤖 RAG Pipeline – Gemini + HuggingFace + Qdrant

A complete Retrieval-Augmented Generation (RAG) pipeline built with:

- Google Gemini
- HuggingFace Sentence Transformers
- Qdrant Vector Database
- Python

This project demonstrates how to build a modern AI retrieval workflow including:
- embedding generation
- semantic vector search
- context retrieval
- LLM-powered answer generation

The project was developed in Google Colab as part of an AI / Information Retrieval learning project.

---

# 🚀 Features

- 🔎 Semantic similarity search using embeddings
- 🧠 Retrieval-Augmented Generation (RAG)
- 📦 Qdrant Cloud vector database integration
- 🤖 Gemini-based answer generation
- 📊 Retrieved context visualization with Pandas
- 📝 Markdown answer rendering
- ☁️ Secure API key management using Google Colab Secrets
- ⚡ Fast embedding generation with MiniLM
- 📚 Custom knowledge base ingestion
- 🔄 End-to-end retrieval and generation pipeline

---

# 🛠 Tech Stack

## 🤖 AI / LLM

![Gemini](https://img.shields.io/badge/Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)![Sentence Transformers](https://img.shields.io/badge/SentenceTransformers-FF6F00?style=for-the-badge)![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black)![Scikit-Learn](https://img.shields.io/badge/ScikitLearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)

## 📦 Vector Database

![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge)

## 🐍 Python Ecosystem

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas)![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy)![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch)![Scikit-Learn](https://img.shields.io/badge/ScikitLearn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)

---

# 🧠 Project Overview

The objective of this project is to implement a complete Retrieval-Augmented Generation pipeline using modern AI tooling.

The workflow follows these steps:

1. Create embeddings from a custom knowledge base
2. Store vectors inside Qdrant Cloud
3. Convert user questions into embeddings
4. Retrieve the most relevant context
5. Inject retrieved context into Gemini prompts
6. Generate a final natural-language answer

---

# ⚙️ Pipeline Architecture

## 1. Knowledge Base

The project uses a custom knowledge base containing information about:

- Institut Teknologi Sepuluh Nopember (ITS)
- FT-EIC Faculty
- Informatics Department
- Universiti Malaya (UM)

---

## 2. Embedding Generation

The embedding model used is:

```python
all-MiniLM-L6-v2
````

from HuggingFace Sentence Transformers.

The model converts textual information into dense semantic vectors.

---

## 3. Vector Storage with Qdrant

Embeddings are stored in a Qdrant Cloud collection configured with:

* Cosine similarity
* Semantic vector retrieval
* Payload storage for original documents

---


When a user asks a question:

* the query is converted into an embedding
* Qdrant searches for similar vectors
* the top-k most relevant documents are retrieved

Example query:

```python
QUESTION = "What can you tell me about ITS?"
```

---

## 5. Generation with Gemini

Retrieved context is injected into a prompt sent to:

```python
gemini-2.5-flash
```

Gemini then generates a concise Markdown answer using the retrieved information.

---

# 📂 Main Functions

| Function                    | Role                            |
| --------------------------- | ------------------------------- |
| `retrieve_context_qdrant()` | Semantic vector retrieval       |
| `generate_response()`       | Gemini response generation      |
| `rag_with_gemini()`         | Full RAG pipeline orchestration |
| `show_context_table()`      | Display retrieved context       |
| `show_markdown_answer()`    | Render final Markdown answer    |

---

# 🔐 API Keys

The project uses Google Colab Secrets for secure credential management.

Required secrets:

* `QDRANT_URL`
* `QDRANT_API_KEY`
* `GOOGLE_API_KEY`

---

# 📦 Installation

Clone the repository:

```bash
git clone <repository_url>
cd <repository_name>
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

# 📋 Requirements

```txt
qdrant-client
sentence-transformers
google-generativeai
numpy
pandas
ipython
torch
transformers
scikit-learn
```

---

# ▶️ Usage

Run the notebook and execute:

```python
QUESTION = "What can you tell me about ITS?"
results = rag_with_gemini(QUESTION, top_k=5)
```

The pipeline will:

* retrieve the most relevant context
* display retrieved documents
* generate a final AI answer using Gemini

---

# 📊 Example Workflow

```text
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
```

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

# 📁 Project Structure

```text
rag-gemini-qdrant/
│
├── notebook/
│   └── rag_pipeline.ipynb
│
├── requirements.txt
├── README.md
└── .gitignore
```

---

# 👨‍💻 Author

## Gharbi Yassine

EPF Engineering School – AI & Full-Stack Development

