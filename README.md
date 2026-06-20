Markdown# 🔗 Smart URL Answer Bot

A Retrieval-Augmented Generation (RAG) application that allows users to provide website URLs, automatically extract and index their content, and then ask questions based on that content using an LLM.

Built with Streamlit, LangChain, ChromaDB, Hugging Face Embeddings, and Groq Llama 3.3.

---

## 🚀 Features

- Process up to 3 URLs simultaneously
- Extract content directly from web pages
- Automatically split content into chunks
- Generate vector embeddings using Hugging Face models
- Store embeddings in Chroma Vector Database
- Ask natural language questions about the processed content
- Retrieve source references along with answers
- Interactive Streamlit UI

---

## 🏗️ Architecture

```text
User URLs
    │
    ▼
UnstructuredURLLoader
    │
    ▼
Text Splitter
    │
    ▼
Hugging Face Embeddings
    │
    ▼
Chroma Vector Store
    │
    ▼
Retriever
    │
    ▼
Groq Llama 3.3
    │
    ▼
Answer + Sources
🛠️ Tech StackFrontendStreamlitLLMGroqLlama 3.3 70B VersatileEmbeddingsAlibaba-NLP/gte-base-en-v1.5Vector DatabaseChromaDBFrameworksLangChainData LoadingUnstructuredURLLoader📂 Project StructurePlaintextGen_AI/
└── RAG_app/
    ├── main.py
    ├── rag.py
    ├── requirements.txt
    ├── README.md
    └── .env
⚙️ Installation & Setup1. Clone RepositoryBashgit clone [https://github.com/rohanssharrma/New_Rag_App.git](https://github.com/rohanssharrma/New_Rag_App.git)
cd New_Rag_App
2. Activate Virtual EnvironmentWindows:Bash.\venv\Scripts\activate
Linux/Mac:Bashsource venv/bin/activate
3. Navigate to App Folder & Install DependenciesBashcd Gen_AI/RAG_app
pip install -r requirements.txt
🔑 Environment VariablesCreate a .env file inside the Gen_AI/RAG_app/ directory.Code snippetGROQ_API_KEY=your_groq_api_key
HUGGINGFACEHUB_API_TOKEN=your_huggingface_token
Get API KeysGroqhttps://console.groq.comHugging Facehttps://huggingface.co/settings/tokens▶️ Run ApplicationBashstreamlit run main.py
Application will launch at:Plaintexthttp://localhost:8501
📖 How to UseStep 1Enter one or more URLs in the sidebar.Example:Plaintext[https://example.com/article1](https://example.com/article1)
[https://example.com/article2](https://example.com/article2)
Step 2Click:Plaintext🚀 Process URLs
The application will:Load webpage contentSplit content into chunksGenerate embeddingsStore vectors in ChromaDBStep 3Ask questions in the chat box.Example:PlaintextWhat is the main topic discussed?
PlaintextSummarize the article in 5 points.
🧠 Model DetailsComponentModelLLMLlama 3.3 70B VersatileProviderGroqEmbedding ModelAlibaba-NLP/gte-base-en-v1.5Vector DBChromaDB🚧 Future EnhancementsUpload PDF supportUpload DOCX supportMulti-document chatConversation memoryStreaming responsesCitation highlighting👨‍💻 AuthorRohan SharmaGitHub: @rohanssharrma📄 LicenseThis project is licensed under the MIT License.
---

### Push your final changes to GitHub:
Once you save the file, update your online repository by running these commands in your VS Code terminal:

```bash
git add README.md
git commit -m "docs: customize readme with my information"
git push