📄 RAG Document Q&A Chatbot with Groq & LLaMA3

This project is a Retrieval-Augmented Generation (RAG) application built using Streamlit, LangChain, Groq (LLaMA3), and FAISS.
It allows users to upload and query PDF research papers and get accurate answers based only on the document context.

🚀 Features

🔍 Ask questions from PDF research papers

🧠 LLaMA3 (via Groq API) for fast inference

📚 FAISS vector database for similarity search

✂️ Recursive text splitting for better retrieval

🧩 Context-aware answers using RAG

🖥️ Interactive Streamlit UI

🛠️ Tech Stack

Python

Streamlit

LangChain

Groq API (LLaMA3-8B)

OpenAI Embeddings

FAISS

PyPDF

dotenv

📂 Project Structure
.
├── app.py
├── requirements.txt
├── .env
├── research_papers/
│   ├── paper1.pdf
│   ├── paper2.pdf
│   └── ...
└── README.md

📦 Installation
1️⃣ Clone the repository
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name

2️⃣ Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate   # Linux / Mac
venv\Scripts\activate      # Windows

3️⃣ Install dependencies
pip install -r requirements.txt

🔑 Environment Variables

Create a .env file in the root directory:

OPENAI_API_KEY=your_openai_api_key
GROQ_API_KEY=your_groq_api_key


⚠️ Do not push .env to GitHub
Add this to .gitignore:

.env

📄 Add Your Documents

Place your PDF files inside the research_papers/ folder.

Example:

research_papers/
├── ai_paper.pdf
├── ml_survey.pdf

▶️ Run the Application
streamlit run app.py


Then open the URL shown in the terminal (usually http://localhost:8501).

🧠 How It Works (RAG Pipeline)

PDF Loading – Documents are loaded from research_papers/

Text Splitting – Large documents are split into chunks

Embedding – Text chunks converted into vector embeddings

Vector Storage – Stored using FAISS

Retrieval – Relevant chunks retrieved for a query

Generation – LLaMA3 generates answers using retrieved context

📌 Usage

Click "Document Embedding" to create the vector database

Enter a question related to the research papers

View:

📖 Answer

🔎 Similar document chunks (inside expander)

☁️ Deployment (Streamlit Cloud)

Upload code without .env

Add secrets in Streamlit → App Settings → Secrets:

OPENAI_API_KEY="your_openai_api_key"
GROQ_API_KEY="your_groq_api_key"

⚠️ Notes

Ensure PDFs are text-readable (not scanned images)

Groq API is very fast but has usage limits

Embeddings use OpenAI — requires valid API key

📜 License

This project is for educational purposes.
Feel free to modify and extend.

🙌 Acknowledgements

LangChain

Groq

OpenAI

Streamlit

FAISS
