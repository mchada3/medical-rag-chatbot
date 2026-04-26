# Medical RAG Chatbot (LLaMA-2 + LangChain + FAISS)

## Overview

Developed an end-to-end Retrieval-Augmented Generation (RAG) chatbot for healthcare question answering, focused on diabetes-related queries. The system retrieves relevant information from medical PDF documents and generates context-aware responses using a large language model.

This project demonstrates a real-world RAG pipeline for domain-specific question answering using healthcare data.

## Problem Statement

Access to reliable and personalized healthcare information is limited, especially for chronic conditions like diabetes. This project addresses this gap by building a chatbot that can provide accurate, document-grounded responses using AI.

## Features

-   Semantic search over healthcare PDF documents
-   Context-aware question answering using retrieved knowledge
-   FAISS-based vector database for efficient retrieval
-   Interactive chatbot interface using Chainlit
-   Local LLM inference using LLaMA-2 (CTransformers)

## Architecture

1.  Load healthcare PDF documents
2.  Split text into smaller chunks
3.  Generate embeddings using HuggingFace models
4.  Store embeddings in FAISS vector database
5.  Retrieve relevant context based on user query
6.  Generate response using LLaMA-2

## Project Structure

-   `app.py` – main chatbot application and Chainlit interface
-   `ingest.py` – builds FAISS vector database from PDF documents
-   `requirements.txt` – dependencies
-   `chainlit.md` – UI configuration

## Tech Stack

-   Python
-   LangChain
-   FAISS
-   HuggingFace Embeddings
-   LLaMA-2 (CTransformers)
-   Chainlit

## Dataset

The chatbot uses healthcare-related PDF documents (clinical guidelines, research reports, and educational materials).
Due to size and licensing constraints, the dataset is not included in this repository.

## How to Run

1.  Install dependencies:

    ``` bash
    pip install -r requirements.txt
    ```

2.  Add PDF files to a local `data/` folder

3.  Build the vector store:

    ``` bash
    python ingest.py
    ```

4.  Run the chatbot:

    ``` bash
    chainlit run app.py
    ```
