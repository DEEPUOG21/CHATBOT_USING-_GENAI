# 🤖 GenAI RAG Chatbot (LangChain + Streamlit)

An AI-powered chatbot built using **Generative AI, Retrieval Augmented
Generation (RAG), and LangChain**. The chatbot can answer questions
using **local documents, web search, and multiple LLM providers**.

This project demonstrates a **production-style GenAI architecture**
combining vector search, embeddings, and LLM APIs.

https://chatbotusing-genai-fefavyopzw8vfcekzyrnlk.streamlit.app/
------------------------------------------------------------------------

## 🚀 Features

-   💬 Interactive chatbot UI using **Streamlit**
-   📚 Retrieval Augmented Generation (RAG)
-   🔎 **FAISS vector database** for semantic search
-   🧠 **Sentence Transformers embeddings**
-   🌐 Optional **Web Search using Tavily API**
-   🤖 Multi‑LLM support:
    -   OpenAI
    -   Groq
    -   Google Gemini
-   ⚡ Fast responses using Groq
-   🧩 Modular architecture

------------------------------------------------------------------------

## 🏗️ Project Architecture

chatbot_using_genai

├── app.py \# Streamlit chatbot interface\
├── models\
│ ├── llm.py \# LLM provider configuration\
│ └── embeddings.py \# Embedding model loader\
├── utils\
│ ├── rag_utils.py \# RAG pipeline + FAISS vector store\
│ └── search_utils.py \# Web search integration\
├── data\
│ └── rag_source.txt \# Knowledge base for RAG\
├── requirements.txt\
└── README.md

------------------------------------------------------------------------

## ⚙️ Installation

Clone the repository

``` bash
git clone https://github.com/DEEPUOG21/CHATBOT_USING-_GENAI.git
cd CHATBOT_USING-_GENAI
```

Create virtual environment

``` bash
python -m venv venv
source venv/bin/activate
```

Install dependencies

``` bash
pip install -r requirements.txt
```

------------------------------------------------------------------------

## 🔑 API Keys Setup

Create a `.streamlit/secrets.toml` file and add:

    OPENAI_API_KEY="your_openai_key"
    GROQ_API_KEY="your_groq_key"
    GOOGLE_API_KEY="your_gemini_key"
    TAVILY_API_KEY="your_tavily_key"

Recommended minimal setup:

    GROQ_API_KEY="your_groq_key"
    TAVILY_API_KEY="your_tavily_key"

------------------------------------------------------------------------

## ▶️ Run the Application

    streamlit run app.py

Open in browser:

    http://localhost:8501

------------------------------------------------------------------------

## 🧠 How It Works

1.  **Document Loading** -- Reads knowledge from local files.
2.  **Text Splitting** -- Breaks documents into chunks.
3.  **Embeddings** -- Converts text into vector embeddings.
4.  **Vector Search** -- FAISS retrieves relevant document chunks.
5.  **RAG Pipeline** -- Injects retrieved context into LLM prompts.
6.  **LLM Response** -- Generates final answer using the selected model.

------------------------------------------------------------------------

## 🛠️ Tech Stack

  Technology               Purpose
  ------------------------ -------------------
  Streamlit                UI
  LangChain                LLM orchestration
  FAISS                    Vector search
  Sentence Transformers    Embeddings
  Groq / OpenAI / Gemini   LLM providers
  Tavily                   Web search

------------------------------------------------------------------------

## 📌 Future Improvements

-   PDF document upload
-   Chat memory
-   Streaming responses
-   Multi‑document RAG
-   Agentic AI tools

------------------------------------------------------------------------

## 👨‍💻 Author

**Deepu Saideep**\
B.E -- Artificial Intelligence & Data Science

GitHub: https://github.com/DEEPUOG21

------------------------------------------------------------------------

⭐ If you like this project, consider giving the repo a star!
