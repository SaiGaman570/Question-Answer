# 📄 QNAdoc — Document QA Chatbot

A Streamlit-based chatbot that allows users to upload a PDF and ask natural language questions. Powered by LangChain, HuggingFace embeddings, Groq LLM, and Chroma vector store.

## ✨ Features

- 📥 Upload and process any PDF document
- 🧠 Contextual question answering using embedded document chunks
- 💬 Real-time responses via Groq's `llama3-70b-8192` model
- 🔍 Vector-based retrieval using HuggingFace + Chroma
- 🛠️ Modular architecture with customizable embedding, chunking, and model layers

## 📁 Project Structure

```text
├── app.py             # Streamlit interface for document upload and QA
├── docqa.py           # PDF loader, retriever setup, and QA logic
├── requirements.txt   # Python dependencies
├── .env               # Environment file with Groq API key and model info
```

## ⚙️ Setup Instructions

1. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

2. **Set environment variables**  
   Create a `.env` file:
   ```env
   GROQ_API_KEY=your_groq_api_key_here
   ```

3. **Run the Streamlit app**
   ```bash
   streamlit run app.py
   ```

## 📚 How It Works

1. User uploads a PDF file.
2. PDF is split into chunks using `CharacterTextSplitter`.
3. Chunks are embedded using `HuggingFaceEmbeddings`.
4. Chroma vector store retrieves relevant chunks based on user question.
5. A prompt is constructed with the question and context.
6. Groq’s LLM responds with an answer.

## 💡 Example Interaction

```
User: What are the key findings from the document?
🤖 AI: The document highlights three main findings...
```

## 🙌 Acknowledgments

Built with:
- [LangChain](https://www.langchain.com/)
- [HuggingFace Embeddings](https://www.sbert.net/)
- [Chroma](https://www.trychroma.com/)
- [Groq LLM](https://groq.com/)
- [Streamlit](https://streamlit.io/)
