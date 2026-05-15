# 📧 AI Email Triage & Priority Digest Automation

AI-powered email management workflow built with **n8n**, **Groq Llama 3.1**, and **Gmail API**.

Automatically fetches unread emails, classifies priority using AI, applies Gmail labels, and sends digest summaries — reducing inbox clutter and surfacing important emails faster.

---

![n8n](https://img.shields.io/badge/Built%20with-n8n-orange)
![Groq](https://img.shields.io/badge/LLM-Groq-green)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## 🚀 Features

✔ Fetch unread Gmail messages automatically  
✔ AI-powered priority classification  
✔ Gmail label automation  
✔ Digest email generation  
✔ Spam & trash filtering  
✔ Duplicate digest prevention  
✔ JSON parsing pipeline  
✔ Configurable scheduling  

---

## 📌 Problem Statement

Important emails often get buried under newsletters, promotions, and notifications.

This workflow uses AI to automatically:

- Analyze incoming emails
- Detect urgency
- Categorize messages
- Apply Gmail labels
- Generate digest summaries

Result:

**Less inbox noise → Faster response → Better productivity**

---

## 🏗 Workflow Architecture

```text
Schedule Trigger
      ↓
Fetch Unread Emails
      ↓
Clean Email Data
      ↓
Groq Llama 3.1 Analysis
      ↓
Parse JSON Response
      ↓
Apply Gmail Labels
      ↓
Generate Digest
      ↓
Send Summary Email
```

---

## 📷 Workflow Screenshot

Add screenshots here:

```text
screenshots/
├── workflow-overview.png
├── digest-email.png
└── gmail-labels.png
```

Example:

```md
![Workflow](screenshots/workflow-overview.png)
```

---

## 🧠 AI Classification Categories

| Category | Description |
|----------|-------------|
| 🔴 Urgent | Security alerts, failed payments, escalations |
| 🟠 Follow-up | Transactions, invoices, pending replies |
| 🔵 FYI | Newsletters, promotions, updates |

---

## ⚙ Tech Stack

| Tool | Purpose |
|------|---------|
| n8n | Workflow orchestration |
| Groq API | AI inference |
| Llama 3.1 8B Instant | Email classification |
| Gmail API | Email actions |
| JavaScript | Parsing & digest generation |

---

## 📦 Repository Structure

```text
.
├── workflow/
│     email-triage-digest.json
│
├── screenshots/
│     workflow-overview.png
│     digest-email.png
│
├── .env.example
├── .gitignore
└── README.md
```

---

## 🔧 Prerequisites

Before setup ensure you have:

- n8n instance running
- Gmail OAuth configured
- Groq API credentials
- Gmail account

---

## 🚀 Installation

Clone repository:

```bash
git clone https://github.com/your-username/repo-name.git

cd repo-name
```

Create env:

```bash
cp .env.example .env
```

Fill credentials:

```env
GMAIL_CREDENTIAL_ID=
GROQ_CREDENTIAL_ID=
YOUR_EMAIL=
```

Import workflow:

1. Open n8n
2. Workflows → Import
3. Select JSON file
4. Reconnect credentials
5. Activate workflow

---

## 🤖 Sample AI Output

```json
{
  "category":"Urgent",
  "summary":"Failed payment detected",
  "priority_score":3
}
```

---

## 📩 Sample Digest

```text
📧 Email Digest

Urgent: 1
Follow-up: 3
FYI: 5

Urgent:
• Failed payment detected

Follow-up:
• Invoice awaiting approval

FYI:
• Weekly newsletter
```

---

## 🔒 Security

Never commit:

- Real credential IDs
- Gmail tokens
- API keys
- Personal emails

Use placeholders before pushing to GitHub.

---

## 🛣 Roadmap

- [ ] Slack alerts
- [ ] Telegram alerts
- [ ] HTML digest templates
- [ ] Multi-user support
- [ ] Dashboard analytics
- [ ] Attachment summarization

---

## 👨‍💻 Author

**Jagadeesh S**

Built using:

`n8n + Groq + Gmail API + JavaScript`

If you found this useful, consider starring ⭐ the repository.
