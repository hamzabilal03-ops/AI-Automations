# n8n Workflow Examples

A collection of AI agents and automation workflows built with n8n, OpenAI, and supporting tools (vector databases, Telegram, Facebook API). Each folder contains an exported workflow JSON and a short README explaining what it does, why it was built that way, and how to adapt it.

## Projects

### [Jewellery Store RAG](./jewellery-store-rag)
A retrieval-augmented generation (RAG) chatbot integrated into a jewellery store's website. Answers customer questions about store timings, product details, and pricing by retrieving from the store's actual data rather than relying on general AI knowledge.

### [AI Lead Agent](./ai-lead-agent)
A lead qualification and scoring workflow. Triggered by a form submission, scores each lead against defined criteria using AI, and sends a notification only when a lead qualifies — filtering, not just flagging.

### [Email-SubWorkflows](./email-subworkflows)
An email-to-social-media pipeline. An email containing a post idea triggers an AI agent to write the post, which is then published directly to a Facebook Page, including support for multi-image posts.

### [Telegram Agent](./telegram-agent)
An AI agent connected to Telegram as a real-time chat interface, using Telegram's Bot API to receive messages and deliver AI-generated responses.

## Approach

Across these projects, the general philosophy is the same: use existing tools and APIs wherever they solve most of the problem, keep workflows as simple as the task allows (adding complexity like RAG or vector search only when the problem genuinely requires it), and prioritize workflows that are documented and easy to hand off or modify, not just functional.

## Stack

- **n8n** — workflow orchestration
- **OpenAI** — AI generation, scoring, and embeddings
- **Pinecone** — vector storage for semantic search (RAG use cases)
- **Telegram Bot API / Facebook Graph API** — delivery channels

## Note

Credentials and client-specific identifiers (API keys, webhook URLs, sheet/database IDs) have been removed or replaced with placeholders in all exported JSON files. You'll need to add your own credentials in n8n and update any placeholder values before importing.
