# Troubleshooting

## Invalid SerpAPI Key

### Problem

Google Trends data cannot be retrieved.

### Solution

Verify that:

- Your SerpAPI key is valid.
- The key has not expired.
- Your API quota has not been exceeded.

---

## Telegram Bot Not Responding

### Problem

Approval messages are not delivered.

### Solution

- Verify the Bot Token.
- Confirm the Chat ID.
- Ensure the bot has permission to send messages.

---

## Missing Credentials

### Problem

Workflow stops during execution.

### Solution

Configure all required credentials before running the workflow.

Required credentials include:

- SerpAPI
- Groq
- Telegram

---

## LLM Errors

### Problem

Draft generation or classification fails.

### Solution

Verify:

- API key
- Model availability
- Token limits
- Provider status

---

## API Rate Limits

### Problem

External APIs reject requests.

### Solution

Retry after the rate limit resets or reduce request frequency.

---

## Workflow Stops Unexpectedly

### Problem

Execution terminates before completion.

### Solution

Check:

- Node configuration
- Conditional branches
- Error logs
- Credential configuration

Use n8n's execution history to identify the failing node.