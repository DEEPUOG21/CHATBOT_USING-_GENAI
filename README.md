# 🤖 GenAI RAG Chatbot (LangChain + Streamlit)

An AI-powered chatbot built using **Generative AI, Retrieval Augmented Generation (RAG), and LangChain**.  
The chatbot can answer questions using **local documents, web search, and multiple LLM providers**.

The project demonstrates a **production-style GenAI architecture** combining vector search, embeddings, and LLM APIs.

---

## 🚀 Features

- 💬 Interactive chatbot UI using **Streamlit**
- 📚 Retrieval Augmented Generation (RAG)
- 🔎 **FAISS vector database** for semantic search
- 🧠 **Sentence Transformers embeddings**
- 🌐 Optional **Web Search using Tavily API**
- 🤖 Multi-LLM support:
  - OpenAI
  - Groq
  - Google Gemini
- ⚡ Fast responses with Groq LLM
- 🧩 Modular architecture (LLM, RAG, Search utilities)

---

## 🏗️ Project Architecture
chatbot_using_genai
│
├── app.py # Streamlit chatbot interface
│
├── models
│ ├── llm.py # LLM provider configuration
│ └── embeddings.py # Embedding model loader
│
├── utils
│ ├── rag_utils.py # RAG pipeline + FAISS vector store
│ └── search_utils.py # Web search integration
│
├── data
│ └── rag_source.txt # Knowledge base for RAG
│
├── requirements.txt
└── README.md


---

# ⚙️ Installation

Clone the repository

```bash
git clone https://github.com/DEEPUOG21/CHATBOT_USING-_GENAI.git
cd CHATBOT_USING-_GENAI

Create virtual environment

python -m venv venv
source venv/bin/activate

Install dependencies

pip install -r requirements.txt
🔑 API Keys Setup

Create a .streamlit/secrets.toml file.

Example:

OPENAI_API_KEY="your_openai_key"
GROQ_API_KEY="your_groq_key"
GOOGLE_API_KEY="your_gemini_key"
TAVILY_API_KEY="your_tavily_key"

Recommended (fastest option):

GROQ_API_KEY="your_groq_key"
TAVILY_API_KEY="your_tavily_key"
▶️ Run the Application
streamlit run app.py

Then open:

http://localhost:8501

🧠 How It Works
1️⃣ Document Loading

The chatbot loads knowledge from:

data/rag_source.txt
2️⃣ Text Splitting

Documents are split using:

RecursiveCharacterTextSplitter
3️⃣ Embeddings

Text is converted into vector embeddings using:

sentence-transformers/all-MiniLM-L6-v2
4️⃣ Vector Search

FAISS stores embeddings for fast similarity search.

5️⃣ Retrieval Augmented Generation

Relevant document chunks are retrieved and injected into the LLM prompt.

6️⃣ LLM Response

The chatbot generates answers using:

OpenAI

Groq

Gemini

🌐 Optional Web Search

The chatbot can also augment responses using Tavily Web Search API.

This enables:

Real-time knowledge retrieval

More accurate responses

🧪 Example Capabilities

The chatbot can:

Answer questions from uploaded documents

Provide contextual answers

Combine RAG + web search

Generate explanations using LLMs

Example prompt:

Explain Retrieval Augmented Generation
🛠️ Tech Stack
Technology	Purpose
Streamlit	UI framework
LangChain	LLM orchestration
FAISS	Vector similarity search
Sentence Transformers	Embeddings
Groq / OpenAI / Gemini	LLM providers
Tavily API	Web search
📸 Future Improvements

PDF document upload

Chat memory

Streaming responses

Multi-document RAG

Agentic AI tools

Advanced UI

📌 Use Cases

AI knowledge assistants

Document Q&A systems

AI research assistants

Enterprise knowledge bots

👨‍💻 Author

Deepu Saideep

B.Tech in Artificial Intelligence & Data Science
Passionate about building intelligent systems using AI.

GitHub:
https://github.com/DEEPUOG21
