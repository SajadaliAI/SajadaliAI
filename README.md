
<div align="center">

# 📄 RAG AI Document Assistant

### Chat with Your Documents Using Generative AI

An AI-powered document question-answering application built with Python, LangChain, Google Gemini, Hugging Face embeddings, and FAISS.

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=for-the-badge)](https://www.langchain.com/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://streamlit.io/)
[![FAISS](https://img.shields.io/badge/FAISS-Vector_Search-0467DF?style=for-the-badge)](https://github.com/facebookresearch/faiss)

</div>

---

## 📌 Overview

The **RAG AI Document Assistant** is a Python-based application that allows users to ask natural-language questions about their documents.

It uses **Retrieval-Augmented Generation (RAG)** to retrieve relevant document content and provide context-based answers using a Large Language Model (LLM).

Instead of relying only on the model's general knowledge, the application uses document retrieval to help generate answers grounded in the uploaded content.

### 🎯 Problem Statement

Finding specific information in long documents can be time-consuming. This project explores how semantic search and generative AI can make document understanding faster and more accessible.

## ✨ Key Features

- 📁 **Document Upload:** Upload supported documents through a web interface.
- 🔍 **Semantic Search:** Retrieve relevant text using vector embeddings.
- 🧠 **RAG Pipeline:** Combine document retrieval with LLM-generated responses.
- 🤖 **LLM Integration:** Use Google Gemini through LangChain.
- 🗂️ **Vector Search:** Use FAISS to search document embeddings.
- 💬 **Natural-Language Q&A:** Ask questions about document content.
- 📚 **Document References:** Display source information where supported by the implementation.
- 🖥️ **Interactive Interface:** Access the application through Streamlit.

> Supported formats and individual features should match the current implementation. Verify them before publishing this README.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Application development |
| Streamlit | Web interface |
| LangChain | LLM and retrieval workflow |
| Google Gemini | Answer generation |
| Hugging Face | Text embedding models |
| FAISS | Vector similarity search |

## 🏗️ How It Works

```text
          Upload Document
                 |
                 v
        Extract Document Text
                 |
                 v
          Split into Chunks
                 |
                 v
        Generate Embeddings
                 |
                 v
         Store Vectors in FAISS
                 |
                 v
          User Asks a Question
                 |
                 v
       Retrieve Relevant Chunks
                 |
                 v
     Question + Context Sent to LLM
                 |
                 v
          Generate an Answer
                 |
                 v
          Display the Response
```

### RAG Workflow

1. **Document ingestion:** Extract text from the uploaded document.
2. **Text chunking:** Divide the extracted text into smaller sections.
3. **Embedding generation:** Convert chunks into numerical vector representations.
4. **Vector indexing:** Store the embeddings in FAISS.
5. **Retrieval:** Search for chunks relevant to the user's question.
6. **Answer generation:** Provide the question and retrieved context to the LLM.
7. **Response display:** Show the generated answer and available source references.

## 📂 Project Structure

The following is a suggested structure. Adjust filenames to match the actual repository.

```text
RAG-AI-Document-Assistant/
│
├── App.py
├── requirements.txt
├── .env.example
├── .gitignore
├── README.md
│
├── src/
│   ├── document_loader.py
│   ├── text_splitter.py
│   ├── embeddings.py
│   ├── vector_store.py
│   └── rag_pipeline.py
│
├── tests/
│   └── test_rag_pipeline.py
│
└── assets/
    ├── app_screenshot.png
    └── architecture.png
```

Only add files and folders that actually exist in your project.

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/SajadaliAI/RAG-AI-Document-Assistant.git
```

Navigate into the project directory:

```bash
cd RAG-AI-Document-Assistant
```

### 2. Create a Virtual Environment

**Windows:**

```bash
python -m venv .venv
.venv\Scripts\activate
```

**Linux / macOS:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Configure Your API Key

Create a `.env` file in the project root if the application uses environment variables.

Example:

```env
GEMINI_API_KEY=your_gemini_api_key_here
```

Use the exact variable name expected by your Python code. If your implementation uses `GOOGLE_API_KEY` instead, configure that name.

**Security:** Never upload your real API key or `.env` file to GitHub.

### 5. Run the Application

If the entry point is `App.py`:

```bash
streamlit run App.py
```

If your actual entry point is `app.py`, run:

```bash
streamlit run app.py
```

Open the local URL displayed in your terminal.

## 💡 How to Use

1. Start the Streamlit application.
2. Upload a supported document.
3. Wait for the document-processing and indexing steps to complete.
4. Enter a question related to the document.
5. Review the generated response.
6. Verify the answer against the original document and any available references.

## 🧪 Testing

Before sharing the project with recruiters, verify the following:

- [ ] The application starts successfully.
- [ ] Supported files upload and process correctly.
- [ ] Relevant questions retrieve appropriate document content.
- [ ] Missing API credentials produce a helpful error.
- [ ] Invalid or empty files are handled safely.
- [ ] Answers can be checked against the source document.
- [ ] The project runs in a clean virtual environment.
- [ ] No API keys or private documents are committed.

If you implement automated tests, document the actual test command and results here.

## ⚠️ Limitations

- AI-generated responses may contain incorrect or incomplete information.
- Retrieval quality depends on document extraction, chunking, and embedding quality.
- Scanned PDFs may require OCR.
- Model API usage may be subject to rate limits and costs.
- Large documents may require additional processing time and memory.
- Source references are only reliable when supported by the retrieval and citation implementation.

## 🚀 Future Improvements

Potential improvements include:

- Better PDF parsing and optional OCR.
- Page-level source citations.
- Automated RAG evaluation.
- Improved error handling and logging.
- Unit and integration tests.
- Docker-based deployment.
- Configurable chunk sizes and retrieval settings.
- Support for additional document formats.

These are proposed enhancements, not claims that they are already implemented.

## 👨‍💻 Author

**Sajad Ali**

AI Engineer | Python Developer | Generative AI | RAG & AI Agents

- GitHub: [@SajadaliAI](https://github.com/SajadaliAI)
- LinkedIn: [Sajad Ali](https://www.linkedin.com/in/sajad-ali-a3074b352)
- Fiverr: [sajad_tech](https://www.fiverr.com/sajad_tech)

---

<div align="center">

**Built with Python and Generative AI.**

Feedback and suggestions are welcome!

</div>
