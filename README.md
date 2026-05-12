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
![Gemini](https://img.shields.io/badge/Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)
![Sentence Transformers](https://img.shields.io/badge/SentenceTransformers-FF6F00?style=for-the-badge)

## Vector Database
![Qdrant](https://img.shields.io/badge/Qdrant-DC244C?style=for-the-badge)

## Python Ecosystem
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy)

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
