# Mistral-RAG-PDF-AI-Assistant

An efficient, fully local Retrieval-Augmented Generation (RAG) application that allows users to upload PDF documents and ask questions about their content. The system uses the all-MiniLM-L6-v2 model from sentence-transformers to generate text embeddings, a fast FAISS vector index for document retrieval, and the Mistral-Nemo-Instruct model for text generation, served via a FastAPI backend and a clean Streamlit user interface.

## Features
* **Dynamic PDF Indexing**: Upload any PDF file on the fly; the backend automatically extracts text, chunks it, and builds an in-memory FAISS index instantly.
* **Persistent Session Q&A**: Submit multiple, consecutive questions about your uploaded document.
* **Clean & Uniform UI**: Streamlit interface designed with a focus on simplicity, removing visual clutter and maintaining uniform text sizes for readability.

## Architecture
* **Frontend**: Streamlit
* **Backend API**: FastAPI
* **Vector Database**: FAISS (IndexFlatL2)
* **Embedding Model**: `sentence-transformers/all-MiniLM-L6-v2`
* **Large Language Model**: Mistral-Nemo-Instruct 

## Quick Start 

Because this project uses a heavy, running it locally requires a high-end GPU. We recommend using the provided notebook on Google Colab or Kaggle.

1. **Open the Notebook**: 
   [![Kaggle](https://kaggle.com/static/images/open-in-kaggle.svg)](https://www.kaggle.com/kernels/welcome?src=https://raw.githubusercontent.com/Mariam-Alashmawy/Mistral-RAG-PDF-AI-Assistant/main/custom-pdf-ai-assistant.ipynb)
2. **Set Hardware**: Ensure the environment is set to **GPU (T4 or higher)**.
3. **Configure**: Insert your `NGROK_TOKEN` when prompted in the code.
4. **Run All**: Execute all cells to launch the FastAPI backend and the Streamlit frontend.
