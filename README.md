# AI LLM RAG Project

A Retrieval-Augmented Generation (RAG) application built with Large Language Models (LLMs) to provide accurate, context-aware responses by combining semantic document retrieval with generative AI.

## Features

* Upload and process documents
* Semantic search using vector embeddings
* LLM-powered question answering
* Retrieval-Augmented Generation (RAG)
* <img width="981" height="607" alt="image" src="https://github.com/user-attachments/assets/811c45c8-02a1-404a-94be-b36d310bef97" />

* Fast and scalable document retrieval
* Interactive chat interface
* Context-aware responses based on uploaded knowledge

---

## 🏗️ Architecture

```text
          User Query
               │
               ▼
       Embedding Model
               │
               ▼
        Vector Database
               │
     Retrieve Relevant Chunks
               │
               ▼
      Prompt + Retrieved Context
               │
               ▼
          Large Language Model
               │
               ▼
        Generated Response
```

---

## 🛠️ Tech Stack

* Python
* LangChain
* OpenAI / LLM API
* Vector Database (ChromaDB)
* HuggingFace Embeddings
* Git

---

## 📂 Project Structure

```text
ai-llm-rag-project/
│
├── data/                  # Source documents
├── vectorstore/           # Stored embeddings
├── app.py                 # Main application
├── requirements.txt       # Dependencies
├── .env                   # API keys
├── utils.py               # Helper functions
└── README.md
```

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/Dhruvpatel1509/ai-llm-rag-project.git

cd ai-llm-rag-project
```

### 2. Create a virtual environment

Windows

```bash
python -m venv venv

venv\Scripts\activate
```

Linux / macOS

```bash
python3 -m venv venv

source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure environment variables

Create a `.env` file and add your API key.

```env
GROQ_API_KEY=your_api_key_here
```

---

## Run the Application

```bash
python app.py
```


---

## How It Works

1. Add one or more documents.
2. Documents are split into smaller chunks.
3. Chunks are converted into embeddings.
4. Embeddings are stored in a vector database.
5. When a user asks a question:

   * The query is embedded.
   * Similar document chunks are retrieved.
   * Retrieved context is combined with the prompt.
   * The LLM generates a grounded response.
  
<img width="1617" height="535" alt="image" src="https://github.com/user-attachments/assets/0ba6e17d-5aa8-427f-a292-7af0540fce0f" />


| Component                 | Library / Model                                 | Purpose                                                              |
| ------------------------- | ----------------------------------------------- | -------------------------------------------------------------------- |
| **LLM**                   | `langchain-groq` + `llama-3.3-70b-versatile`    | Generates accurate, context-aware answers with low latency.          |
| **Embeddings**            | `langchain-google-genai` + `gemini-embedding-2` | Converts document chunks into vector embeddings for semantic search. |
| **Document Loader**       | `PyPDFLoader`                                   | Loads PDF documents into LangChain.                                  |
| **Text Splitter**         | `RecursiveCharacterTextSplitter`                | Splits large documents into overlapping chunks for better retrieval. |
| **Vector Database**       | ChromaDB                                        | Stores document embeddings and performs similarity search.           |
| **Environment Variables** | `python-dotenv`                                 | Securely loads API keys from a `.env` file.                          |


---

## Example

**Question**

> What are the admission requirements?

**Retrieved Context**

> Admission requires a bachelor's degree, English proficiency, and supporting documents.

**LLM Response**

> Based on the uploaded documents, applicants must have a bachelor's degree, demonstrate English proficiency, and submit the required supporting documents.

---

## Requirements

* Python 3.10+
* Groq API Key (or compatible LLM)
* Gemini API

---

## Future Improvements

* Multi-document support
* Conversation memory
* Source citation in responses
* PDF, DOCX, and TXT support
* Hybrid search (keyword + semantic)
* Docker deployment
* Authentication
* Cloud vector database integration

---

## Contributing

Contributions are welcome!

1. Fork the repository.
2. Create a feature branch.

```bash
git checkout -b feature/new-feature
```

3. Commit your changes.

```bash
git commit -m "Add new feature"
```

4. Push the branch.

```bash
git push origin feature/new-feature
```

5. Open a Pull Request.

---


---

## 👨‍💻 Author

**Dhruv Patel**

* GitHub: https://github.com/Dhruvpatel1509

---

⭐ If you found this project useful, consider giving it a star!
