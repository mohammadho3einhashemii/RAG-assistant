# RAG assistant
Large Language Models have limited knowledge of domain-specific documents and may generate hallucinations.
This project demonstrates how Retrieval-Augmented Generation (RAG) can generate responses from external knowledge sources.

## Overview
When we want to use a AI assistant in a specific job or topic (like law or medicine) that the model doesn't know the techniqal and deep subjects, we use RAG.

This project provides an AI assistant

In this project, i am using one of my chapters of Operating system lesson booklet in my university, you can use any another resource!

This assistant uses "llama-3.1-8b-instant" model from groq's api as main LLM, and uses "sentence-transformers/all-MiniLM-L6-v2" model as embed model from HuggingFace and FAISS vectore database which all of the are free!

## Key Features
- Langchain Framework
- Groq's API
- Large Language Model
- Embed Model
- FAISS vectore database

## How it works
You can run the cells sequentialy and see the results and testing by yourself.
- Architecture flow:
- Data collection → Chunking → Embedding → Storing in Vector Database → Retrieval → Generation

## Example 
Question:
```
Explain Banker’s Algorithm.
```
Answer:
```
Banker’s Algorithm is a resource allocation and deadlock avoidance algorithm. It is used to manage multiple threads (processes) that require multiple instances of ...
```

## Project Structure
```
RAG/
├── data
|    └── Chapter 3 - Deadlock.pdf
├── notebook
|    └── RAG_assistant.ipynb
├── .gitignore
├── requirements.txt
└── README.md
```

## Installation
- Clone the repository
```
git clone <your-repository-url>
cd RAG
```
- Install dependencies
```
pip install -r requirements.txt
```
- run RAG_assistant.ipynb

## Limitations and Future work
- There is no score for retieving best relavant chunks!
- Chunks have metadata(page, source) but we don't use them in LLM's prompt yet, LLM can reason and answer better with them. 
- There is no reranking for retrieval chunks, in the most of the real RAG projects, we have to use them
- Using better and larger Embed models
- We can add a conversation memory to LLM
- Citation, LLM can mention that its answer in based on wich page of pdf(or ant another source)
- adding a UI (like gradio)


## Tech Stack
- Python
- Langchain
- Groq
- Colab
- Auto Regressive model
- Embed model
- FAISS 
