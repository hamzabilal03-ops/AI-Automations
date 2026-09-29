# Telegram Agent

An n8n workflow that connects an AI agent to Telegram as the customer-facing chat interface.

## What it does
- Listens for incoming Telegram messages via a Telegram trigger
- Passes each message to an AI agent for a response
- Sends the AI's response back to the user in the same Telegram chat

## Tools used
- n8n (orchestration)
- Telegram Bot API (trigger + reply)
- OpenAI (response generation)

## Why this approach
Telegram's Bot API is simple to integrate and reliable for real-time chat delivery, making it a good lightweight front-end for an AI agent without building a custom chat UI.

## How to adapt
- Point it at any AI backend/knowledge base you want
- Add conversation memory/context handling if multi-turn context is needed
- Swap Telegram for another chat platform (WhatsApp, website widget) using the same underlying AI step
