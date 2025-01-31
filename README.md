# RAG Chatbot with Hugging Face and FAISS

This project is a **Retrieval-Augmented Generation (RAG) chatbot** built using **Flask**, **Hugging Face models**, and **FAISS** for efficient text retrieval. The chatbot retrieves relevant context from a document and generates answers using a language model.

## 🚀 Features
- **Flask-based Web Interface**: A simple web app for interaction.
- **RAG (Retrieval-Augmented Generation)**: Uses FAISS for vector retrieval and a Hugging Face model for generation.
- **Text Splitting & Embeddings**: Uses `CharacterTextSplitter` for document processing and `HuggingFaceEmbeddings` for vector embeddings.
- **FAISS for Efficient Search**: Stores and retrieves relevant document chunks for response generation.
- **Custom Prompting with LangChain**: Implements `ChatPromptTemplate` to structure model inputs.

---

## 📂 Project Structure

```
rag-app-main/
│── static/                # CSS, JavaScript files (if needed)
│── templates/             # HTML templates for Flask web app
│── doc_rag.txt            # Input document used for retrieval
│── app.py                 # Main Flask application
│── requirements.txt       # Dependencies list
│── README.md              # Project documentation
└── .gitignore             # Git ignored files
```

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```sh
git clone https://github.com/haritAhuja/rag-app-main.git
cd rag-app-main
```

### 2️⃣ Create a Virtual Environment (Recommended)

```sh
python -m venv env
source env/bin/activate  # On Windows use: env\Scripts\activate
```

### 3️⃣ Install Dependencies

```sh
pip install -r requirements.txt
```

---

## 🛠️ Usage

1. **Add your Hugging Face API key** in `app.py` (Replace `huggingfacehub_api_token=""` with your actual key).
2. **Run the Flask app**:

```sh
python app.py
```

3. Open `http://127.0.0.1:5000/` in your browser.

---

## 📜 Dependencies

Ensure the following Python libraries are installed:

```txt
Flask
openai
langchain
langchain_huggingface
langchain_community
faiss-cpu
re
```

To install missing dependencies:

```sh
pip install Flask openai langchain langchain_huggingface langchain_community faiss-cpu
```

---

## 📖 API Endpoints

- `GET /` - Returns the chatbot UI.
- `POST /chat` - Accepts a user query and returns the chatbot response.

---

## 🔧 Customization

- Modify `doc_rag.txt` to change the document context.
- Adjust `chunk_size` and `chunk_overlap` in `CharacterTextSplitter` for better retrieval.
- Change the Hugging Face model in `HuggingFaceHub` (default: `zephyr-7b-beta`).

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 🤝 Contributing

Feel free to submit issues or PRs on [GitHub](https://github.com/haritAhuja/rag-app-main).

Happy coding! 🚀
