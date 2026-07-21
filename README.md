# 📧 AI Email Automation Agent

An AI-powered email automation workflow built with **n8n** that intelligently classifies incoming emails, sends instant WhatsApp notifications for high-priority emails, logs medium-priority emails into Google Sheets, and automatically organizes low-priority emails using Gmail labels.

---

## 🚀 Features

- 📥 Automatically monitors incoming Gmail emails.
- 🤖 Uses AI to classify emails into **High**, **Medium**, and **Low** priority.
- 📝 Generates a concise AI-powered summary for every email.
- 📱 Sends instant WhatsApp notifications for **High Priority** emails.
- 📊 Logs **Medium Priority** emails into Google Sheets for tracking.
- 🏷️ Labels **Low Priority** emails in Gmail and marks them as read to prevent duplicate processing.
- ⚡ Fully automated workflow built using n8n.

---

## 🛠️ Tech Stack

- **n8n**
- **Google Gemini AI**
- **Gmail API**
- **Google Sheets API**
- **WhatsApp Cloud API (Meta)**
- **JavaScript Expressions**

---

## 📂 Workflow Architecture

```text
Gmail Trigger
      │
      ▼
Get Email
      │
      ▼
AI Agent
(Classification + Summarization + Prioritization)
      │
      ▼
Switch
├───────────────┬─────────────────┬─────────────────┐
│               │                 │
▼               ▼                 ▼
HIGH         MEDIUM             LOW
│               │                 │
▼               ▼                 ▼
WhatsApp     Google Sheets     Gmail Label
Notification     Log           (AI-Low-Priority)
│                                 │
└───────────────┬─────────────────┘
                ▼
        Mark Email as Read
```

---

## 📌 Priority Classification

### 🔴 High Priority

Emails requiring immediate attention.

Examples:

- Job interviews
- Security alerts
- Password reset requests
- Payment overdue reminders
- Client escalations
- Critical account notifications

**Action Taken**

- AI Summary
- WhatsApp Notification

---

### 🟡 Medium Priority

Important emails that require action but are not urgent.

Examples:

- Team meetings
- Client meetings
- Project updates
- HR communications
- Performance reviews
- Document approval requests

**Action Taken**

- AI Summary
- Logged into Google Sheets

---

### 🟢 Low Priority

Informational or promotional emails.

Examples:

- Newsletters
- Promotional offers
- Marketing emails
- Blog updates
- Product announcements

**Action Taken**

- AI Summary
- Added Gmail Label
- Marked as Read

---

# 💡 Use Cases

- AI Email Management
- Smart Inbox Automation
- Business Email Prioritization
- Customer Support Automation
- Productivity Automation
- Workflow Automation

---

## ▶️ How to Use

1. Import `workflow.json` into n8n.
2. Configure your credentials:
   - Gmail OAuth
   - Google Gemini API
   - Google Sheets
   - WhatsApp Cloud API
3. Update the Google Sheet and Gmail Label according to your setup.
4. Activate the workflow.
5. Send test emails to verify each priority flow.

---

## 👩‍💻 Author

**Tisha Talati**

B.Tech Computer Science & Engineering

Passionate about AI Automation, Intelligent Agents, and Workflow Automation.

---

