# ⚖️ JurisRAG

An AI-powered Legal Research Assistant built using **Retrieval-Augmented Generation (RAG)**, enabling intelligent legal document retrieval, semantic search, and context-aware question answering through large language models.

## 🚀 Overview

JurisRAG helps users explore and analyze legal documents using natural language queries. By combining vector search with LLM-powered reasoning, the system retrieves the most relevant legal references and generates accurate, context-aware responses.

The platform is designed to streamline legal research by reducing the time spent searching through lengthy documents and case records.

---

## ✨ Features

### 🔍 Intelligent Legal Search

* Semantic search across legal documents
* Context-aware retrieval using vector embeddings
* Fast similarity-based document matching

### 🤖 AI-Powered Legal Assistant

* Natural language legal queries
* Contextual response generation
* Source-backed answers

### 📚 Retrieval-Augmented Generation

* Document chunking and indexing
* Embedding generation
* Retrieval-based response enhancement

### ⚡ High Performance

* FastAPI backend architecture
* Optimized vector retrieval
* Concurrent request handling

### 🔐 Session Management

* Multi-user session support
* Query history tracking
* Session reset and cleanup functionality

---

## 🏗️ System Architecture

```text
Legal Documents
       │
       ▼
Document Processing
       │
       ▼
Vector Embeddings
       │
       ▼
Pinecone Vector Database
       │
       ▼
Relevant Context Retrieval
       │
       ▼
Llama 3.3 (Groq)
       │
       ▼
Context-Aware Legal Response
```

---

## 🛠️ Tech Stack

| Category         | Technology |
| ---------------- | ---------- |
| Backend          | FastAPI    |
| Vector Database  | Pinecone   |
| LLM              | Llama 3.3  |
| Inference Engine | Groq       |
| RAG Framework    | LangChain  |
| Frontend         | Streamlit  |
| Language         | Python     |

---

## 📂 Project Structure

```text
JurisRAG/
│
├── data/
├── src/
├── app.py
├── document_uploader.py
├── requirements.txt
├── README.md
└── LICENSE
```

---

## ⚙️ Installation

### Clone Repository

```bash
git clone https://github.com/pramodhvamshi/JurisRAG.git
cd JurisRAG
```

### Create Virtual Environment

```bash
python -m venv venv
```

### Activate Environment

Windows:

```bash
venv\Scripts\activate
```

Linux / macOS:

```bash
source venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file in the root directory.

```env
PINECONE_API_KEY=your_api_key
INDEX_NAME=your_index_name
GROQ_API_KEY=your_groq_api_key
```

---

## ▶️ Running the Application

### Start FastAPI Server

```bash
uvicorn app:app --reload
```

Server:

```text
http://localhost:8000
```

### Start Streamlit Interface

```bash
streamlit run app.py
```

Interface:

```text
http://localhost:8501
```

---

## 📡 API Endpoints

### Health Check

```http
GET /
```

### Ask Legal Questions

```http
POST /chat
```

Request:

```json
{
  "session_id": "user123",
  "query": "Explain the main points of this contract."
}
```

### Reset Session

```http
POST /session/reset/{session_id}
```

### Delete Session

```http
DELETE /session/{session_id}
```

### Active Session Count

```http
GET /sessions/count
```

### Retrieve Sources

```http
GET /sources/{session_id}
```

---

## 📈 Key Capabilities

* Retrieval-Augmented Generation (RAG)
* Semantic Search
* Vector Similarity Matching
* Context-Aware Question Answering
* Legal Knowledge Retrieval
* Multi-Session Support
* Fast API Responses

---

## 🔮 Future Enhancements

* PDF Upload Interface
* Citation Highlighting
* Legal Case Summarization
* Multi-Document Analysis
* Conversation Memory
* React Frontend
* Advanced Analytics Dashboard

---

## 📜 License

This project is licensed under the MIT License.

---

## 👨‍💻 Author

**Pramodh Vamshi**

Building intelligent AI systems with Retrieval-Augmented Generation, Large Language Models, and modern backend technologies.
