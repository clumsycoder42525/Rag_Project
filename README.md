

# 📄 README.md — RAG Internship Project

## 📌 Project Title

**Retrieval-Augmented Generation (RAG) Based Document Question Answering System**

---

## 🧠 Problem Statement

Organizations often struggle to extract meaningful, context-aware answers from large volumes of unstructured data such as company policies, FAQs, and documentation.
Traditional language models may generate incorrect or hallucinated responses because they rely only on pre-trained knowledge.

This project addresses the problem by building a **Retrieval-Augmented Generation (RAG)** system that retrieves relevant information from documents and generates accurate, context-aware answers.

---

## 🎯 Project Objective

* Build a simple RAG application using unstructured PDF data
* Retrieve relevant document chunks using vector similarity search
* Generate grounded answers using a Large Language Model
* Demonstrate a real-world enterprise use case for AI/ML internship

---

## 🗂️ Dataset

* Custom-created PDF document representing **company knowledge base**
* Includes:

  * HR policies (leave policy, working hours)
  * Product documentation
  * Organizational FAQs

The PDF simulates real organizational unstructured data.

---

## ⚙️ Tech Stack

### Language

* Python

### Libraries & Frameworks

* LangChain
* LangChain Community
* HuggingFace Transformers
* Sentence-Transformers
* ChromaDB
* PyPDF

### Model

* **FLAN-T5 Base** (Open-source LLM)

### Vector Database

* **ChromaDB** (local vector store)

---

## 🏗️ Architecture Overview

```
PDF Documents
      ↓
Text Chunking
      ↓
Embeddings (Sentence Transformer)
      ↓
Vector Database (ChromaDB)
      ↓
Retriever
      ↓
LLM (FLAN-T5)
      ↓
Final Answer
```

---

## 🔄 Workflow

1. **Document Ingestion**

   * Load PDF documents using LangChain PDF loader

2. **Text Preprocessing & Chunking**

   * Split documents into overlapping text chunks

3. **Embedding Generation**

   * Convert text chunks into vector embeddings

4. **Vector Storage**

   * Store embeddings in ChromaDB for similarity search

5. **Query Processing**

   * Convert user question into embedding
   * Retrieve most relevant document chunks

6. **Answer Generation**

   * Pass retrieved context to LLM
   * Generate context-aware answer

---

## 💡 Features

* Context-aware question answering
* Prevents hallucination using document grounding
* Interactive question input
* Clean output (only final answer shown)
* No external API keys required

---

## ▶️ How to Run

### 1️⃣ Install Dependencies

```bash
pip install langchain==0.1.16 langchain-community==0.0.36
pip install transformers sentence-transformers chromadb pypdf
```

---

### 2️⃣ Run the Notebook

* Upload the PDF dataset
* Run cells sequentially:

  * Load PDF
  * Chunk text
  * Create embeddings & vector store
  * Initialize LLM
  * Build RetrievalQA chain

---

### 3️⃣ Ask Questions

Interactive input example:

```python
query = input("Ask your question: ")
response = qa_chain(query)
print(response["result"])
```

---

## 🧪 Sample Questions

* What is the leave policy of the company?
* How many paid leaves are allowed per year?
* What are the working hours?
* What does the company product do?

---

## ✅ Sample Output

```
20 paid leaves per year
```

---

## 📊 Evaluation

* **Accuracy:** Answers strictly grounded in document content
* **Relevance:** Retrieved chunks match user query
* **Latency:** Fast retrieval using vector similarity

---

## 🧠 Learning Outcomes

* Understanding of RAG architecture
* Hands-on experience with vector databases
* Practical use of embeddings and LLMs
* End-to-end AI application development

---

## 🚀 Future Improvements

* Streamlit-based chatbot UI
* Support for multiple PDFs
* Source document highlighting
* Deployment using FastAPI

---

## 📌 Conclusion

This project demonstrates how Retrieval-Augmented Generation can effectively solve real-world information retrieval problems in organizations.
By combining vector search with language models, the system delivers accurate, reliable, and explainable AI-powered answers.

---

## 👨‍💻 Author

**AI/ML Internship Project**
Built as part of internship completion requirements.

---

## ⭐ One-Line Internship Summary

> *Developed a RAG-based document question-answering system using LangChain, ChromaDB, and open-source LLMs.*

---

