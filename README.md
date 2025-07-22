# 🔍 Multi-Source RAG Pipelines with LangChain

This project demonstrates the creation and deployment of three custom **Retrieval-Augmented Generation (RAG)** pipelines using the [LangChain API](https://www.langchain.com/). Each pipeline integrates a different type of document loader and vector database, showcasing the flexibility of RAG architectures in real-world use cases.

> **Tech Stack:** Python · LangChain · OpenAI · ChromaDB · Pinecone · Weaviate · Google Drive API · YouTube Transcript Loader

---

## 📦 Project Overview

Retrieval-Augmented Generation (RAG) combines LLMs with external knowledge bases to produce accurate, context-rich outputs. This project explores RAG across three distinct configurations, emphasizing diverse data sources and vector stores.

### 🧠 Objectives

- Build end-to-end RAG pipelines using LangChain.
- Integrate a variety of document loaders and vector databases.
- Handle unstructured data from sources like YouTube, Google Drive, and local directories.
- Compare and evaluate results from each setup.

---

## 📁 Pipeline Configurations

### 🚀 RAG 1 — YouTube + Weaviate

- **Document Loader:** `YouTubeLoader` (with transcript support)
- **Vector Store:** Weaviate
- **Use Case:** Answering questions about Durham College's AI program using a transcribed YouTube video.

**Sample Query:**  
> _"In which areas are students trained in the AI program at Durham College?"_  
**Answer:**  
> Topics include statistics, linear algebra, algorithms, computer systems, and more.

---

### ☁️ RAG 2 — Google Drive + Pinecone

- **Document Loader:** `GoogleDriveLoader`
- **Vector Store:** Pinecone
- **Use Case:** Ingesting and querying altered documents from Google Drive (e.g., fictionalized Wikipedia content).

**Sample Query:**  
> _"Who is Juano?"_  
**Answer:**  
> Juano is a robot alien superhero from Mars, a character from comic book Action's Comic #1. *(based on edited document content)*

---

### 🗂️ RAG 3 — Local File System + ChromaDB

- **Document Loader:** `DirectoryLoader` (Local `.txt` file)
- **Vector Store:** ChromaDB
- **Use Case:** Querying altered classic text (e.g., *Alice in Wonderland*) for retrieval testing.

**Sample Query:**  
> _"Who was Alice sitting beside?"_  
**Answer:**  
> Her brother *(modified from original source to validate RAG output accuracy)*

---

## 🛠️ Tech & Tools

- **LangChain**: RAG pipelines, chain construction, embeddings
- **OpenAI**: Embedding models
- **YouTube API**: Transcription via `YoutubeLoader`
- **Google Drive API**: Secure document loading from cloud
- **Vector Stores**: Weaviate, Pinecone, ChromaDB
- **Google Cloud Console**: API credential management

---

## 💡 Key Learnings

- Constructing modular, scalable RAG pipelines
- Integrating third-party APIs and handling secure credentials
- Comparing behavior across vector databases
- Fine-tuning chunking strategies and retrieval accuracy
