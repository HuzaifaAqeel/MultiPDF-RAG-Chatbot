# MultiPDF RAG Chatbot

Chat with multiple PDF documents using Retrieval-Augmented Generation (RAG) — upload your PDFs, and ask questions in plain English. Built with Streamlit, LangChain, FAISS, and Google Gemini.

## How it works

1. **Upload** one or more PDF files in the sidebar
2. **Processing** — text is extracted (PyPDF2), split into chunks, embedded with Gemini embeddings, and indexed in a FAISS vector store
3. **Chat** — your question is embedded, the most relevant chunks are retrieved, and Gemini generates an answer grounded in your documents

## Features

- Upload and process multiple PDFs at once
- Semantic search over your documents (FAISS vector index)
- Conversational chat interface with history
- Answers strictly from your documents — says so when the answer isn't in the context

## Getting started

1. Get a free API key from [Google AI Studio](https://aistudio.google.com/apikey) and put it in a `.env` file:

   ```env
   GOOGLE_API_KEY=your_key_here
   ```

2. Install and run:

   ```bash
   pip install -r requirements.txt
   streamlit run app.py
   ```

3. Open http://localhost:8501, upload PDFs, click **Submit & Process**, and start chatting.

## Tech stack

Python · Streamlit · LangChain · FAISS · Google Gemini (embeddings + chat)

## Credits

Based on [gemini_multipdf_chat](https://github.com/kaifcoder/gemini_multipdf_chat) by [kaifcoder](https://github.com/kaifcoder) (MIT License — see `LICENSE`). Extended and maintained by [Muhammad Huzaifa Aqeel](https://github.com/HuzaifaAqeel).
