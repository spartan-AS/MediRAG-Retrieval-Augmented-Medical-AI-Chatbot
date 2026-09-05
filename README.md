# 🩺 MediRAG — Retrieval-Augmented Medical AI Chatbot

> **Ask questions. Retrieve relevant knowledge. Get grounded answers.**

MediRAG is a **Retrieval-Augmented Generation (RAG) based medical chatbot** designed to provide conversational responses by combining **semantic search with Large Language Models (LLMs)**.

Instead of relying solely on an LLM's pre-trained knowledge, MediRAG first retrieves relevant information from a medical knowledge base and then uses that context to generate a more **relevant, grounded, and context-aware response**.

The project demonstrates an end-to-end **RAG pipeline** using open-source AI technologies:

**Medical Knowledge Base → Text Processing → HuggingFace Embeddings → FAISS Vector Search → Relevant Context → Mistral LLM → AI Response**

---

## 🧠 How MediRAG Works

When a user asks a question, the system follows a Retrieval-Augmented Generation pipeline:

```text
                 👤 USER
                    │
                    ▼
             💬 Medical Query
                    │
                    ▼
          🔍 Semantic Retrieval
                    │
                    ▼
       🤗 HuggingFace Embeddings
                    │
                    ▼
          🗂️ FAISS Vector Store
                    │
                    ▼
       📚 Relevant Medical Context
                    │
                    ▼
              🧠 Mistral LLM
                    │
                    ▼
           💬 Grounded Response
                    │
                    ▼
                 👤 USER
```

### 🔎 Retrieval

The user's question is converted into a vector representation using **HuggingFace embeddings**.

FAISS then performs similarity search against the indexed medical knowledge base to retrieve the most relevant information.

### 🧠 Generation

The retrieved context is provided to the **Mistral language model**, which uses that information to generate the final conversational response.

This approach helps reduce the dependency on the model's internal knowledge by grounding responses in the retrieved information.

---

## ✨ Key Features

* 🩺 **Medical Question Answering** — Conversational interface for medical-related queries
* 🔎 **Semantic Search** — Retrieves relevant information based on meaning rather than exact keyword matching
* 🤗 **HuggingFace Embeddings** — Converts medical knowledge and user queries into vector representations
* 🗂️ **FAISS Vector Database** — Enables efficient similarity-based document retrieval
* 🧠 **Mistral LLM** — Generates natural-language responses using retrieved context
* 🔗 **Retrieval-Augmented Generation** — Combines retrieval with LLM generation
* 💬 **Conversational Interface** — Interactive chatbot experience
* 🌐 **Streamlit UI** — Simple web interface for interacting with the system
* 🧩 **Open-Source Stack** — Built using accessible open-source AI technologies

---

## 🛠️ Tech Stack

### 🤖 AI & NLP

* **Mistral** — Large Language Model
* **HuggingFace** — Text embeddings
* **RAG** — Retrieval-Augmented Generation

### 🗂️ Vector Search

* **FAISS CPU** — Vector storage and similarity search

### 🖥️ Frontend

* **Streamlit** — Conversational web interface

### 🐍 Development

* Python

---

## 🎯 Why RAG?

A traditional chatbot can answer a question using only the knowledge stored within its language model.

```text
User Question
      │
      ▼
    LLM
      │
      ▼
   Answer
```

MediRAG introduces an additional retrieval layer:

```text
User Question
      │
      ▼
Create Embedding
      │
      ▼
Search Knowledge Base
      │
      ▼
Retrieve Relevant Context
      │
      ▼
      LLM
      │
      ▼
Grounded Answer
```

This architecture allows the chatbot to **retrieve relevant information before generating a response**, making it more suitable for knowledge-intensive question-answering applications.

---

## ⚙️ RAG Pipeline

The complete pipeline can be summarized as:

```text
        📚 Medical Documents
                │
                ▼
        ✂️ Text Chunking
                │
                ▼
      🤗 HuggingFace Embeddings
                │
                ▼
          🗂️ FAISS Index
                │
                │
                ▼
        👤 User Question
                │
                ▼
      🤗 Query Embedding
                │
                ▼
       🔍 Similarity Search
                │
                ▼
      📖 Relevant Documents
                │
                ▼
          🧠 Mistral LLM
                │
                ▼
        💬 Final Response
```

---

## 💡 Example

A user can ask a natural-language question such as:

```text
"What are the common symptoms associated with diabetes?"
```

The system:

1. Converts the question into an embedding.
2. Searches the FAISS vector store.
3. Retrieves relevant medical information.
4. Passes the retrieved context to Mistral.
5. Generates a conversational response based on the available context.

---

## 🚀 What This Project Demonstrates

MediRAG demonstrates practical implementation of:

* Retrieval-Augmented Generation (RAG)
* Vector embeddings
* Semantic similarity search
* FAISS vector databases
* HuggingFace models
* LLM-based question answering
* Context retrieval
* Prompt-based generation
* Conversational AI
* Streamlit application development
* End-to-end RAG pipeline design

---

## ⚠️ Medical Disclaimer

MediRAG is an **educational AI project** and is not intended to provide medical diagnosis, treatment, or professional medical advice.

Information generated by the system should not replace consultation with a qualified healthcare professional.

---

## ⭐ Why This Project?

MediRAG showcases how **retrieval systems and generative AI can work together** to build domain-specific conversational applications.

Rather than simply asking an LLM to generate an answer, the system introduces a knowledge-retrieval layer that connects the user's question with relevant information before generation.

This makes MediRAG a practical demonstration of how **RAG architectures can be applied to specialized domains such as healthcare**.
