# RAG-pipleline-for-LLM
Simple RAG pipeline for LLMs
**RAG (Retrieval-Augmented Generation)** is a technique that enhances Large Language Models (LLMs) by giving them access to external knowledge at query time.  

It works by combining:
  - **Retriever**: Pulls relevant documents or data (e.g., from a knowledge base or vector store) based on the user's question.
  - **Generator**: Uses those retrieved documents as additional context to generate a response.

So instead of the LLM answering just from memory (training data), RAG gives it real-time knowledge to refer to.
For example:
Input: “What are the side effects of Drug X?”  
- Retriever pulls up the official documentation for Drug X.
- Generator reads it and answers:
“Common side effects of Drug X include dizziness, nausea, and dry mouth.”

**Why is RAG necessary?**
LLMs like GPT, Claude, or LLaMA are trained on large datasets, but they have key limitations:

1. Limited Knowledge Scope
- LLMs can only recall info they were trained on — which might be outdated or missing key details.
RAG fixes this as it lets the model pull in up-to-date or domain-specific knowledge from an external source (e.g., product manuals, research papers, private databases).

2. LLMs can sometimes make up facts when they don’t know the answer.
- RAG reduces this as it grounds the model’s response in retrieved, factual content, making answers more reliable.

3. It is not possible to train a model on everything. And training/fine-tuning is expensive.
- RAG is cheaper & more flexible: The knowledge base can be updated without retraining the model by simply changing the documents the retriever searches.
