# Interview Question Creator 🎯

An AI-powered application that generates **interview questions and answers** from uploaded documents (PDF, DOCX, TXT).  
Built using **LLMs + Retrieval-Augmented Generation (RAG)** to extract relevant context and produce accurate, role-focused interview content.

---

## 🚀 Features

- Upload documents (PDF, DOCX, TXT)
- Automatically extracts and understands document content
- Generates interview questions based on the uploaded material
- Provides well-structured answers using retrieved context
- Fast and scalable backend using FastAPI
- Semantic search powered by FAISS vector database

---

## 🛠 Tech Stack

- **Programming Language:** Python  
- **Backend Framework:** FastAPI  
- **LLM Orchestration:** LangChain  
- **Vector Database:** FAISS  
- **LLM Provider:** OpenAI  
- **Embeddings:** OpenAI Embeddings  
- **Document Processing:** LangChain Document Loaders  

---

## 🧩 Architecture Overview

1. User uploads a document  
2. Document is parsed and split into chunks  
3. Chunks are converted into embeddings  
4. Embeddings are stored in FAISS  
5. User query retrieves relevant chunks  
6. LLM generates interview questions and answers using retrieved context  

---

## 📂 Project Structure

```text
Interview-Question-Creator/
│
├── app.py                 
├── requirements.txt        
├── src/
│   └── __init__.py
│   └── helper.py
│   └── prompt.py
├── templates/
│   └── index.html
├── static/
│   └── docs/
│   └── output/
├── setup.py
├── .env                  
└── README.md
```
---
## ⚙️ How to Run?

### STEP 01- Create a conda environment after opening the repository

```bash
conda create -n llmapp python=3.8 -y
```

```bash
conda activate llmapp
```

### STEP 02- install the requirements
```bash
pip install -r requirements.txt
```

### Create a `.env` file in the root directory and add your OPENAI_API_KEY as follows:

```ini
OPENAI_API_KEY= "xxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```


```bash
# Finally run the following command
uvicorn app:app --reload
```

Now,
```bash
open up : http://localhost:8000
```
