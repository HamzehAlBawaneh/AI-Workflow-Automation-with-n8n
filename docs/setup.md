# Setup Guide

This guide explains how to configure and run the AI Workflow Automation project in n8n.

## Prerequisites

Before importing the workflow, ensure you have:

- n8n (latest version recommended)
- A SerpAPI account and API key
- A Groq API key (or another supported LLM provider)
- A Telegram Bot Token
- A Telegram Chat ID

## Installation

1. Clone this repository:

```bash
git clone https://github.com/yourusername/AI-Workflow-Automation-with-n8n.git
```

2. Open your n8n instance.

3. Import one of the workflow JSON files from the `workflows/` folder.

## Configure Credentials

Replace the placeholder credentials with your own:

- SerpAPI API Key
- Groq API Key
- Telegram Bot Token
- Telegram Chat ID

Do not hardcode credentials inside the workflow.

## Running the Workflow

1. Activate the workflow.
2. Wait for the scheduled trigger or execute it manually.
3. The workflow will:
   - Retrieve AI-related trends.
   - Filter irrelevant topics.
   - Generate an AI draft.
   - Send the draft to Telegram for approval.
   - Log the approval decision.

## Workflow Outputs

After execution, approved drafts can be forwarded to downstream workflows such as:

- Social media publishing
- Editorial review
- Newsletter generation
- Knowledge management systems