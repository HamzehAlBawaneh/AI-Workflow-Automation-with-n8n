# Workflow Overview

The workflow is designed to automate AI trend monitoring while ensuring human approval before any downstream action.

## Workflow Stages

### 1. Daily Trigger

Starts the workflow on a predefined schedule.

---

### 2. Google Trends Retrieval

Retrieves AI-related trending topics using the Google Trends API.

Collected information includes:

- Keyword
- Region
- Trend score
- Time window

---

### 3. Trend Normalization

Transforms raw API responses into a standardized format used throughout the workflow.

---

### 4. Rule-Based Noise Filtering

Removes topics unrelated to the workflow objectives.

Examples:

- Celebrity news
- Entertainment
- Viral memes
- Social media trends

---

### 5. AI Relevance Classification

An LLM evaluates each trend and determines whether it is relevant to one of the supported domains:

- AI Governance
- AI Regulation
- AI Security
- AI Education

The classifier also assigns:

- Risk label
- Category
- Relevance explanation

---

### 6. Insight Draft Generation

For relevant trends, an LLM generates an analytical draft explaining:

- Why the trend matters
- Potential impact
- Institutional relevance

Drafts are marked as **Not Approved**.

---

### 7. Telegram Approval

The generated draft is sent to Telegram.

The reviewer can choose:

- Approve
- Request Changes
- Reject

---

### 8. Decision Routing

The workflow behaves differently depending on the decision.

#### Approve

- Continue downstream
- Log approval

#### Request Changes

- Regenerate draft
- Return for another approval cycle

#### Reject

- Stop workflow
- Prevent downstream execution

---

### 9. Audit Logging

Every decision is recorded, including:

- Trend keyword
- Draft version
- Reviewer
- Timestamp
- Decision
- Feedback
- Risk label