# Email-to-Social Media Pipeline

An n8n workflow that turns an email into a published Facebook post, using sub-workflows to keep the logic modular.

## What it does
- Triggered by an incoming email containing a post idea
- An AI agent writes the post content from the idea
- Publishes directly to a Facebook Page, including support for multi-image posts (uploads images unpublished, then creates one feed post with attached media)

## Tools used
- n8n (orchestration, sub-workflows)
- OpenAI (post writing)
- Facebook Graph API (publishing)
- Gmail/IMAP (email trigger)

## Why this approach
Split into sub-workflows so the email-parsing, content-generation, and publishing steps can be tested, reused, or modified independently.

## How to adapt
- Point the trigger at a different inbox or email format
- Adjust the AI prompt for tone/brand voice
- Swap the Facebook publish step for another platform's API
