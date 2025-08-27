

# 📘 QueryPine

> ⚡️ A powerful **document-based question answering system** built with **Pinecone vector database**, **Google Generative AI embeddings**, and **Groq's Llama model**.
> Upload PDF documents and ask questions about their content using **advanced AI capabilities**.

---

## ✨ Features

 **PDF Document Processing** – Load and process multiple PDF documents from a directory
 **Text Chunking** – Intelligent text splitting with configurable chunk sizes and overlaps
 **Vector Embeddings** – Google Generative AI embedding model for high-quality vector representations
 **Vector Database** – Pinecone integration for efficient vector storage & similarity search
 **AI-Powered Q\&A** – Groq’s Llama 3.3 70B model for accurate question answering
 **Retry Mechanism** – Built-in retry logic for reliable Pinecone operations

---

## 🛠️ Prerequisites

*  Python **3.8+**
*  Pinecone account + API key
*  Google Generative AI API key
*  Groq API key

---

## ⚡ Installation

```bash
# Clone the repository
git clone <repository-url>
cd chatbot-pinecone

# Install dependencies
uv add -r requirements.txt
```

---

## ⚙️ Setup

1. Create a **`.env` file** in the root directory with your API keys:

```env
GOOGLE_API_KEY=your_google_api_key_here
PINECONE_API_KEY=your_pinecone_api_key_here
GROQ_API_KEY=your_groq_api_key_here
```

2. Place your **PDF documents** inside the `document/` directory
3. Update Pinecone configuration in `test.ipynb` if needed:

   * `index_name` → Name of your Pinecone index
   * `environment` → Your Pinecone environment
   * `region` → Your Pinecone region

---

## ▶️ Usage

### 📓 Running the Notebook

1. Open **`test.ipynb`** in Jupyter Notebook/Lab
2. Run cells sequentially to:

   * Load and process PDF documents
   * Create embeddings and store in Pinecone
   * Query the system with questions

#### 🔍 Example

```python
# Load documents
docs = read_doc('document/')

# Process and chunk documents
document = chuck_data(docs=docs)

# Create embeddings and store in Pinecone
embeddings = GoogleGenerativeAIEmbeddings(model="models/embedding-001")
index = PineconeVectorStore.from_documents(
    documents=docs,
    embedding=embeddings,
    index_name="my-embedding-index"
)

# Ask questions
query = "What is the shift of llms after the transformers rise ?"
answer = retrieve_answers(query)
print(answer)
```

---

### 💻 Running the Main Application

```bash
python main.py
```

---

## 📂 Project Structure

```
chatbot-pinecone/
├── document/              # PDF documents
├── test.ipynb             # Notebook with implementation
├── main.py                # Main application
├── requirements.txt       # Dependencies
├── pyproject.toml         # Project config
├── uv.lock                # Dependency lock
├── .python-version        # Python version
├── .gitignore             # Ignore rules
└── README.md              # This file
```

---

## 📦 Dependencies

*  **langchain** – LLM framework
*  **pinecone** – Vector database
*  **langchain-groq** – Groq’s LLM integration
*  **langchain-google-genai** – Google GenAI integration
*  **pypdf** – PDF document processing
*  **python-dotenv** – Manage environment variables

---

## 🔑 API Keys Required

1. **Google Generative AI** → For text embeddings
2. **Pinecone** → Vector database storage
3. **Groq** → LLM inference with Llama model

---

## ⚙️ Configuration

📌 **Pinecone Settings**

* Index Name: `my-embedding-index`
* Dimension: **768** (Google’s embedding-001 model)
* Metric: **Cosine similarity**
* Environment: `us-east-1` (adjust as needed)

📌 **Model Settings**

* Embedding Model: `models/embedding-001` (Google)
* LLM Model: `llama-3.3-70b-versatile` (Groq)
* Temperature: **0.5**

---

## 🐞 Troubleshooting

 **API Key Issues** → Ensure `.env` file has correct keys
 **Pinecone Index Errors** → Verify index name & environment
 **Document Not Loading** → Place PDFs in `document/` folder
 **Dependency Errors** → Run `pip install -r requirements.txt`

---

## 📜 License

Licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributions

Contributions are welcome 🎉!
Feel free to fork, open issues, and submit PRs 🚀

---

👉 Would you like me to also add **shields.io badges** (for Python version, license, dependencies) and a **demo screenshot/GIF section** to make it look even more professional?
=======


# 📘 QueryPine

> ⚡️ A powerful **document-based question answering system** built with **Pinecone vector database**, **Google Generative AI embeddings**, and **Groq's Llama model**.
> Upload PDF documents and ask questions about their content using **advanced AI capabilities**.

---

## ✨ Features

 **PDF Document Processing** – Load and process multiple PDF documents from a directory
 **Text Chunking** – Intelligent text splitting with configurable chunk sizes and overlaps
 **Vector Embeddings** – Google Generative AI embedding model for high-quality vector representations
 **Vector Database** – Pinecone integration for efficient vector storage & similarity search
 **AI-Powered Q\&A** – Groq’s Llama 3.3 70B model for accurate question answering
 **Retry Mechanism** – Built-in retry logic for reliable Pinecone operations

---

## 🛠️ Prerequisites

*  Python **3.8+**
*  Pinecone account + API key
*  Google Generative AI API key
*  Groq API key

---

## ⚡ Installation

```bash
# Clone the repository
git clone <repository-url>
cd chatbot-pinecone

# Install dependencies
uv add -r requirements.txt
```

---

## ⚙️ Setup

1. Create a **`.env` file** in the root directory with your API keys:

```env
GOOGLE_API_KEY=your_google_api_key_here
PINECONE_API_KEY=your_pinecone_api_key_here
GROQ_API_KEY=your_groq_api_key_here
```

2. Place your **PDF documents** inside the `document/` directory
3. Update Pinecone configuration in `test.ipynb` if needed:

   * `index_name` → Name of your Pinecone index
   * `environment` → Your Pinecone environment
   * `region` → Your Pinecone region

---

## ▶️ Usage

### 📓 Running the Notebook

1. Open **`test.ipynb`** in Jupyter Notebook/Lab
2. Run cells sequentially to:

   * Load and process PDF documents
   * Create embeddings and store in Pinecone
   * Query the system with questions

#### 🔍 Example

```python
# Load documents
docs = read_doc('document/')

# Process and chunk documents
document = chuck_data(docs=docs)

# Create embeddings and store in Pinecone
embeddings = GoogleGenerativeAIEmbeddings(model="models/embedding-001")
index = PineconeVectorStore.from_documents(
    documents=docs,
    embedding=embeddings,
    index_name="my-embedding-index"
)

# Ask questions
query = "What is the shift of llms after the transformers rise ?"
answer = retrieve_answers(query)
print(answer)
```

---

### 💻 Running the Main Application

```bash
python main.py
```

---

## 📂 Project Structure

```
chatbot-pinecone/
├── document/              # PDF documents
├── test.ipynb             # Notebook with implementation
├── main.py                # Main application
├── requirements.txt       # Dependencies
├── pyproject.toml         # Project config
├── uv.lock                # Dependency lock
├── .python-version        # Python version
├── .gitignore             # Ignore rules
└── README.md              # This file
```

---

## 📦 Dependencies

*  **langchain** – LLM framework
*  **pinecone** – Vector database
*  **langchain-groq** – Groq’s LLM integration
*  **langchain-google-genai** – Google GenAI integration
*  **pypdf** – PDF document processing
*  **python-dotenv** – Manage environment variables

---

## 🔑 API Keys Required

1. **Google Generative AI** → For text embeddings
2. **Pinecone** → Vector database storage
3. **Groq** → LLM inference with Llama model

---

## ⚙️ Configuration

📌 **Pinecone Settings**

* Index Name: `my-embedding-index`
* Dimension: **768** (Google’s embedding-001 model)
* Metric: **Cosine similarity**
* Environment: `us-east-1` (adjust as needed)

📌 **Model Settings**

* Embedding Model: `models/embedding-001` (Google)
* LLM Model: `llama-3.3-70b-versatile` (Groq)
* Temperature: **0.5**

---

## 🐞 Troubleshooting

 **API Key Issues** → Ensure `.env` file has correct keys
 **Pinecone Index Errors** → Verify index name & environment
 **Document Not Loading** → Place PDFs in `document/` folder
 **Dependency Errors** → Run `pip install -r requirements.txt`

---

## 📜 License

Licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 🤝 Contributions

Contributions are welcome 🎉!
Feel free to fork, open issues, and submit PRs 🚀

---

👉 Would you like me to also add **shields.io badges** (for Python version, license, dependencies) and a **demo screenshot/GIF section** to make it look even more professional?

