# Azerbaijani Legal RAG System

This project is a multilingual Retrieval-Augmented Generation (RAG) system built for Azerbaijani legal documents.  
It allows users to ask legal questions in Azerbaijani and receive context-aware answers generated from official legal texts.

The system uses LangChain, ChromaDB, Hugging Face embeddings, and GPT-4o-mini.


---
 # Architecture
 PDF Documents
     │
     ▼
PyPDFLoader → Load raw pages
     │
     ▼
Text Cleaning → Remove null bytes, filter short pages
     │
     ▼
RecursiveCharacterTextSplitter (chunk: 1500, overlap: 300)
     │
     ▼
multilingual-e5-base Embeddings (HuggingFace)
     │
     ▼
ChromaDB Vector Store
     │
     ▼
Retriever (similarity search, k=10)
     │
     ▼
RAG Chain → GPT-4o-mini → Answer in Azerbaijani

---

# Features

- Load and process Azerbaijani legal PDF documents
- Clean and split legal texts into chunks
- Generate multilingual embeddings
- Store embeddings in ChromaDB
- Semantic search for relevant legal context
- Azerbaijani question answering with LLMs
- Support for multiple legal domains

---
# Install dependencies
pip install -U langchain
pip install langchain-openai
pip install langchain-community
pip install langchain_text_splitters
pip install chromadb
pip install pypdf

---
