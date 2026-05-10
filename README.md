# AI Email Triage & Priority Digest Automation

An AI-powered email management workflow built using n8n, Groq Llama 3.1, and Gmail APIs.
The system automatically fetches unread emails, classifies them by priority, applies Gmail labels, and generates a clean digest email twice daily.

---

# Overview

Managing large volumes of emails can cause important messages to get buried under newsletters, promotions, and notifications.

This workflow solves that problem by using AI to automatically:

* Analyze incoming emails
* Detect priority levels
* Organize inboxes with Gmail labels
* Generate readable digest summaries

---

# Features

* Automatic unread email fetching
* AI-powered email classification
* Gmail label automation
* Priority-based email digest
* Spam and trash filtering
* Duplicate digest prevention
* Clean JSON parsing pipeline
* Scheduled automation every 12 hours

---

# Email Categories

## Urgent

Used for:

* Security alerts
* Fraud warnings
* Failed payments
* Important escalations

## Follow-up

Used for:

* Transaction notifications
* Invoices
* Pending responses
* Important communication threads

## FYI

Used for:

* Promotions
* Newsletters
* Informational updates

---

# Workflow Architecture

```text
Schedule Trigger
    ↓
Get Emails (Unread Gmail Messages)
    ↓
Clean Email Data
    ↓
AI Agent (Groq Llama 3.1)
    ↓
Parse AI JSON Response
    ↓
Add Gmail Labels
    ↓
Create Priority Digest
    ↓
Send Digest Email
```

---

# Technologies Used

* n8n
* Groq API
* Llama 3.1 8B Instant
* Gmail API
* JavaScript

---

# AI Processing

The workflow uses Groq's Llama 3.1 model to:

* classify emails
* generate short summaries
* assign priority scores
* organize inboxes automatically

The AI returns structured JSON responses which are parsed inside the workflow for reliable automation.

---

# Gmail Automation

The workflow automatically creates inbox organization by applying labels such as:

* Urgent
* Follow-up
* FYI

This helps keep important emails visible and easier to manage.

---

# Digest Generation

At the end of each run, the system creates a summarized digest email containing:

* total urgent emails
* follow-up emails
* FYI emails
* AI-generated summaries

The digest is automatically sent to the configured Gmail account.

---

# Automation Logic

* Fetch only unread emails
* Ignore spam and trash
* Ignore previously generated digest emails
* Process emails using AI
* Sort emails by priority
* Generate readable summaries
* Deliver digest automatically

---

# Future Improvements

* Slack/Telegram urgent alerts
* HTML digest templates
* Multi-user support
* Dashboard analytics
* Sentiment analysis
* Attachment summarization

---

# Author

Jagadeesh S
