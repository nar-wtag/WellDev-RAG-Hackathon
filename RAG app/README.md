# Retrieval-Augmented Generation (RAG) System

## Overview
This project implements a **Retrieval-Augmented Generation (RAG)** system designed to enhance automated response generation by leveraging external knowledge sources. It extracts relevant information from documents (in this case, PDFs), stores them in a vector store, and uses a language model to generate responses based on the retrieved content. The system is built using Python and integrates several advanced libraries and models to process and generate accurate responses.

## Features
- **Document Chunking**: Breaks large documents into smaller, manageable chunks with token overlap for better context retention.
- **Similarity Search**: Uses FAISS to perform efficient similarity search on embeddings generated from document chunks.
- **Response Generation**: Utilizes the Ollama API and Llama model for generating human-like responses based on the retrieved context.
- **CSV Integration**: Handles user queries stored in a CSV file and generates responses with the retrieval context.
- **PDF Processing**: Extracts content from PDF documents for processing and embedding.
  
## Architecture
1. **Document Chunking**: Large PDF documents are split into smaller, overlapping chunks to make them manageable for embedding.
2. **Embedding & Vector Store**: Chunks are embedded into vectors using the **Sentence-BERT** model and stored in a FAISS index for fast similarity search.
3. **Query Processing**: When a query is received, a similarity search is performed in the vector store to retrieve the most relevant document chunks.
4. **Response Generation**: A context-based response is generated using the Ollama API, with the retrieved documents forming the context.

## Dependencies

Ensure you have the following dependencies installed:

- `pandas`: For reading and writing CSV files.
- `ollama`: For accessing Ollama models for response generation.
- `fitz` (PyMuPDF): For extracting text from PDF documents.
- `faiss`: For efficient similarity search using embeddings.
- `sentence-transformers`: For generating embeddings using pre-trained models.
- `numpy`: For numerical computations.
- `tiktoken`: For token counting and management.
- `re`: For regular expression-based text cleaning.
- `tqdm`: For displaying progress bars during document processing.


