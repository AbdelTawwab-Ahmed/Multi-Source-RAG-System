# 📚 Multi-Source RAG System

A conversational AI chatbot that ingests documents from multiple source types into a single ChromaDB collection, retrieves the most relevant context, maintains multi-turn conversation memory, cites sources in every response, and supports metadata-based retrieval filtering.

---

## ✨ Features

- 📄 Ingest data from multiple source types
  - PDF documents
  - Text files
  - Web pages
- 🧩 Store all documents in a single ChromaDB collection
- 💬 Multi-turn conversation with chat memory
- 🔎 Semantic search using vector embeddings
- 📌 Source citations included in every answer
- 🎯 Filter retrieval by source type (PDF / TXT / Web)
- ⚡ Built with LangChain, LangGraph and Gemini

---

## 🛠️ Tech Stack

- Python
- LangChain
- Google Gemini
- ChromaDB
- Sentence Transformers (Embeddings)
- Python Dotenv

---

## 📂 Project Structure

```text
multi-source-rag-system/
├── .env
├── .gitignore
├── requirements.txt
├── ingest.py
├── rag.py
├── app.py
├── data/
│   ├── document.pdf
│   └── notes.txt
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/multi-source-rag-system.git
cd multi-source-rag-system
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it:

**Windows**

```bash
.venv\Scripts\activate
```

**Linux / macOS**

```bash
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Create a `.env` file

```env
GOOGLE_API_KEY=your_api_key
```

### 5. Index the documents

```bash
python ingest.py
```

### 6. Start the chatbot

```bash
python app.py
```

---

## 🏗️ Architecture

```text
          PDF
            │
      Text File
            │
      Web Pages
            │
            ▼
      Document Loaders
            │
            ▼
      Text Splitter
            │
            ▼
      Embeddings
            │
            ▼
   ChromaDB Collection
            │
            ▼
       Retriever
            │
            ▼
 Conversational RAG Chain
            │
     Chat Memory
            │
            ▼
      Gemini LLM
            │
            ▼
 Answer + Source Citations
```

---

## 💬 Example Conversation

**User**

> What is Retrieval-Augmented Generation?

**Assistant**

> Retrieval-Augmented Generation (RAG) combines information retrieval with large language models to generate responses grounded in external knowledge.

**Sources**
- document.pdf (Page 3)

---

**User**

> Why is it useful?

**Assistant**

> It helps reduce hallucinations by retrieving relevant information before generating a response, improving factual accuracy.

**Sources**
- document.pdf (Page 4)

---

**User**

> Summarize it in one sentence.

**Assistant**

> RAG enhances language models by combining retrieval with generation to produce more reliable, context-aware responses.

**Sources**
- document.pdf (Page 3)
- notes.txt

---

## 📌 Future Improvements

- Hybrid Search (BM25 + Vector Search)
- Support additional document formats (DOCX, CSV, Markdown)
- Web interface with Streamlit
- Persistent chat history
- Advanced metadata filtering

---

## 👤 Author

**Abdeltawwab Ahmed**
AI Engineer passionate about LLMs, Agentic AI, RAG systems, and Voice AI.