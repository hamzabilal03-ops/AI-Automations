# AI Lead Agent

An n8n workflow that automatically qualifies and scores inbound leads.

## What it does
- Triggered by a form submission (new lead)
- An AI step evaluates the lead against defined qualification criteria (e.g. budget, intent, fit)
- Sends a notification (Gmail) only when a lead crosses the qualification threshold — filters out low-quality leads instead of flagging everything

## Tools used
- n8n (orchestration)
- OpenAI (lead scoring)
- Gmail (conditional notification)

## Why this approach
Kept it as a single AI scoring step with structured output rather than a multi-agent setup — lead qualification is a defined evaluation task, not something that needs complex agent reasoning.

## How to adapt
- Update the scoring criteria in the AI prompt to match your own qualification rules
- Swap the form trigger for any other lead source (webhook, CRM, etc.)
- Change the notification threshold or destination (Slack, Sheets, CRM update) as needed
