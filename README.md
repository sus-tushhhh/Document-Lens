# 📚 Document Lens | RAG-Powered Document Assistant

**Document Lens** is an AI-powered document assistant that allows users to upload documents and interact with their content using natural language. Built with Python, Streamlit, LangChain, Gemini API and Retrieval-Augmented Generation (RAG), it retrieves relevant information from uploaded files to answer questions, summarize content, and analyze documents.

## ✨ Features

- 📁 **Multi-format Support** — Upload PDF, DOCX, and TXT files.
- 💬 **Ask Questions** — Query your documents using natural language.
- 🔍 **Context-Aware Answers** — Retrieve relevant document chunks to generate grounded responses.
- 📊 **Document Analysis** — Summarize, evaluate, and analyze document content, including resume ratings.
- 🧠 **Semantic Search** — Find relevant information using vector embeddings.
- ⚡ **Efficient Retrieval** — Use FAISS for similarity-based document search.
- 🌙 **Streamlit Interface** — Simple, interactive interface for document-based conversations.

## 🛠️ Tech Stack

- **Language:** Python
- **Frontend:** Streamlit
- **LLM Framework:** LangChain
- **Embeddings:** Hugging Face — `all-MiniLM-L6-v2`
- **Vector Database:** FAISS
- **Document Loaders:** PyPDFLoader, Docx2txtLoader, TextLoader
- **AI Model:** Gemini API

## ⚙️ How It Works

1. **Upload:** The user uploads a PDF, DOCX, or TXT document.
2. **Load:** The document loader extracts its text and metadata.
3. **Split:** The text is divided into smaller, overlapping chunks.
4. **Embed:** Hugging Face converts chunks into vector embeddings.
5. **Index:** FAISS stores the embeddings for similarity search.
6. **Retrieve:** Relevant chunks are retrieved based on the user's question.
7. **Generate:** The language model uses the retrieved context to generate an answer.

## 🔄 RAG Architecture

```text
Upload Document
      ↓
Extract Text
      ↓
Split into Chunks
      ↓
Generate Embeddings
      ↓
Store in FAISS
      ↓
User Question
      ↓
Retrieve Relevant Chunks
      ↓
LLM + Context
      ↓
Generated Answer
```

## 📂 Supported Documents

| Format         | Extension |
| -------------- | --------- |
| PDF            | `.pdf`    |
| Microsoft Word | `.docx`   |
| Plain Text     | `.txt`    |

## 💡 Example Use Cases

- Ask questions about lengthy documents.
- Summarize reports, notes, and study materials.
- Find specific facts in uploaded files.
- Review and rate resumes based on their content.
- Identify strengths, weaknesses, and areas for improvement in documents.

## 🔮 Future Enhancements

- [ ] Chat history and multi-turn conversations.
- [ ] Source citations with page numbers.
- [ ] Support for multiple documents in a single session.
- [ ] Downloadable summaries and analysis reports.
- [ ] Improved retrieval using hybrid search or reranking.
- [ ] More detailed resume evaluation criteria.
- [ ] Deployment with secure configuration and optimized resource usage.

## ⚠️ Limitations

- Answer quality depends on document quality, chunking, retrieval, and the selected language model.
- Resume ratings are AI-generated assessments and should not be treated as definitive hiring decisions.
- The assistant may miss relevant information if the retriever does not return the appropriate document chunks.

## 👨‍💻 Developer

**Tushant**  
🔗 GitHub: https://github.com/sus-tushhhh

---

⭐ If you found this project interesting, consider giving the repository a **star**!
