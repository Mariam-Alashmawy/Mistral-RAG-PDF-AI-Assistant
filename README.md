# Mistral-RAG-Local-PDF-AI-Assistant

An efficient, fully local Retrieval-Augmented Generation (RAG) application that allows users to upload PDF documents and ask questions about their content. The system uses a fast FAISS vector index for document retrieval and the Mistral-Nemo-Instruct model for text generation, served via a FastAPI backend and a clean Streamlit user interface.

## Features
* **100% Local Execution**: Your data never leaves your machine. Processing, embedding, and generation happen entirely on local hardware.
* **Dynamic PDF Indexing**: Upload any PDF file on the fly; the backend automatically extracts text, chunks it, and builds an in-memory FAISS index instantly.
* **Persistent Session Q&A**: Submit multiple, consecutive questions about your uploaded document without losing state.
* **Clean & Uniform UI**: Streamlit interface designed with a focus on simplicity, removing visual clutter and maintaining uniform text sizes for readability.

## Architecture
* **Frontend**: Streamlit
* **Backend API**: FastAPI
* **Vector Database**: FAISS (IndexFlatL2)
* **Embedding Model**: `sentence-transformers/all-MiniLM-L6-v2`
* **Large Language Model**: Mistral-Nemo-Instruct (optimized with instruction-tuned templates)
