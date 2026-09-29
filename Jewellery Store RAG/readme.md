# Jewellery Store RAG Chatbot

A retrieval-augmented generation (RAG) chatbot integrated into a jewellery store's website to handle customer queries.

## What it does
- Answers questions about store timings, product details, and pricing
- Retrieves relevant information from a vector store of the store's data rather than relying on the AI's general knowledge, so answers stay accurate and store-specific
- Deployed as a chat widget on the client's own website

## Tools used
- n8n (orchestration)
- OpenAI (embeddings + response generation)
- Vector store (e.g. Pinecone) for semantic search over store data

## Why this approach
RAG is the right fit here because the knowledge base (product catalog, store info) is unstructured and needs semantic search — a plain scripted bot couldn't handle varied customer phrasing well.

## How to adapt
- Replace the source data with your own product catalog / store info to re-embed
- Adjust the system prompt to control tone and what the bot will/won't answer
- Swap the vector store provider if preferred, or connect the same backend to a different front-end (Telegram, WhatsApp, etc.)
