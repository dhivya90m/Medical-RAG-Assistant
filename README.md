# Medical RAG Assistant

A Retrieval-Augmented Generation (RAG) AI solution for healthcare professionals, enabling fast, accurate, and explainable answers to clinical questions using trusted medical manuals (e.g., Merck Manual) and Large Language Models (LLMs).

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Sample Use Cases](#sample-use-cases)
- [Architecture](#architecture)
- [How It Works](#how-it-works)
- [Tech Stack](#tech-stack)
- [Project Status](#project-status)
- [License](#license)
- [Contact](#contact)

---

## Overview

Healthcare professionals face information overload and time pressure when making critical decisions. This project addresses those challenges by combining retrieval from trusted medical sources with generative AI, providing clinicians with real-time, evidence-based, and context-aware answers to diagnostic, treatment, and protocol questions.

---

## Features

- **Retrieval-Augmented Generation (RAG):** Combines semantic search over medical manuals with LLMs for grounded, explainable answers.
- **Trusted Medical Sources:** Uses authoritative content (e.g., Merck Manual PDF, >4,000 pages) as the knowledge base.
- **Natural Language Q&A:** Supports conversational queries on diagnostics, drug info, protocols, and more.
- **Prompt Engineering:** Ensures responses are clear, factual, and aligned with medical best practices.
- **Explainability:** Returns both the answer and the source context for clinical auditability.
- **Scalable Pipeline:** Efficient PDF ingestion, chunking, embedding, and vector search for large documents.

---

## Sample Use Cases

- **Diagnostic Assistance:**  
  “What are the common symptoms and treatments for pulmonary embolism?”

- **Drug Information:**  
  “Can you provide the trade names of medications used for treating hypertension?”

- **Critical Care Protocols:**  
  “What is the protocol for managing sepsis in a critical care unit?”

- **Treatment Planning:**  
  “What are the first-line options for managing rheumatoid arthritis?”

- **Specialty Knowledge:**  
  “What are the diagnostic steps for suspected endocrine disorders?”

---

## Architecture

graph TD
A[User Query] --> B[Prompt Engineering]
B --> C[Semantic Search (Vector DB)]
C --> D[Retrieve Relevant Chunks]
D --> E[LLM (e.g., Mistral, Gemini)]
E --> F[Generated, Contextual Answer]
F --> G[Display with Source Reference]


- **PDF Loader:** Loads and splits the medical manual into manageable text chunks.
- **Embedding & Vector DB:** Converts chunks to embeddings and stores them for fast semantic retrieval.
- **Retriever:** Finds the most relevant chunks for a user query.
- **LLM:** Generates an answer using both the user query and retrieved context.
- **Prompt Engineering:** Guides the LLM to provide clear, clinically reliable responses.

---

## How It Works

- **Data Ingestion:** Loads the medical manual PDF and splits it into overlapping text chunks.
- **Embedding:** Each chunk is embedded using a SentenceTransformer model and stored in a vector database (ChromaDB).
- **Query Handling:** User queries are embedded and used to retrieve the most relevant chunks.
- **LLM Generation:** The LLM (e.g., Mistral, Gemini, or OpenAI) receives the query and retrieved context, generating a grounded, explainable answer.
- **Prompt Engineering:** Ensures the LLM stays factual and provides references to the medical source.

---

## Tech Stack

- **Python:** Core language
- **LangChain:** Orchestration and RAG pipeline
- **Sentence Transformers:** Embeddings
- **ChromaDB:** Vector database for semantic search
- **PyMuPDF:** PDF loading and chunking
- **LLMs:** Mistral, Gemini, or OpenAI (configurable)
- **Streamlit (optional):** Interactive UI

---

## Project Status

- ✅ End-to-end RAG pipeline implemented and tested
- ✅ Supports PDF ingestion, chunking, embedding, and retrieval
- ✅ Prompt engineering for reliable, explainable clinical answers
- ⏳ UI and API endpoints (in progress)
- ⏳ Expansion to additional medical sources (planned)

---

## License

This project is for educational and research purposes only. Not for clinical use without validation.

---

## Contact

Dhivya Marimuthu  
[LinkedIn](https://www.linkedin.com/in/dhivya-marimuthu/) | [GitHub](https://github.com/yourusername)

---

*For questions or collaboration, please open an issue or contact via LinkedIn.*

