# Agentic RAG with Web-Based Loader

A simple **Agentic RAG pipeline** that decides whether a question requires web-based knowledge retrieval before generating an answer.

## Workflow

```text
Question
   ↓
LLM Decision
   ↓
Web Retrieval? ── No ──→ Generate
   │
  Yes
   ↓
Chroma Retrieval
   ↓
Generate Answer
```

## Implementation

* Loads web content using `WebBaseLoader`
* Splits documents using `RecursiveCharacterTextSplitter`
* Generates embeddings with `all-MiniLM-L6-v2`
* Stores vectors in **ChromaDB**
* Uses Gemini to decide whether retrieval is required
* Retrieves top-4 relevant documents
* Generates an answer grounded in retrieved context
* Orchestrated using **LangGraph**

## Tech Stack

`Python` · `LangGraph` · `LangChain` · `Gemini` · `HuggingFace Embeddings` · `ChromaDB` · `BeautifulSoup`

## Example

**Input**

```text
What is artificial intelligence?
```

**Output**

```text
Answer generated using retrieved web context.
```

## Key Concepts

**Agentic Routing · RAG · Web-Based Retrieval · Vector Database · LLM Generation · LangGraph**
