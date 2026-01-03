# AI Daily News Automation (n8n Workflow)

This project is an **n8n workflow** that automatically fetches the latest **Tech News** and **World News**, summarizes them using OpenAI, and sends a daily email summary.

---

## 🚀 Features

- Fetches news from:
  - [The Verge RSS](https://www.theverge.com/rss/index.xml)
  - [BBC World RSS](https://feeds.bbci.co.uk/news/world/rss.xml)
- Summarizes news with **OpenAI GPT-4.1-mini**.
- Sends the summary via **Gmail**.
- Scheduled to run **daily at 7 AM**.
- Simple and secure workflow with credentials hidden.

---

## 🛠 Installation

1. Install [n8n](https://docs.n8n.io/getting-started/installation/).
2. Import the workflow JSON file (`ai_daily_news_workflow.json`) into n8n.
3. Configure credentials:
   - **OpenAI API key**
   - **Gmail OAuth2**
4. Set the recipient email in the **Send summary by email** node.

---

## ⚙️ Workflow Nodes

1. **Get Tech News** – Fetches tech news RSS feed.
2. **Get World News** – Fetches world news RSS feed.
3. **AI Summary Agent** – Uses OpenAI to summarize the news.
4. **Output** – Stores summary for email.
5. **Send summary by email** – Sends the summary to your inbox.
6. **Schedule Trigger** – Runs the workflow every day at 7 AM.

---

## 🔒 Security Tips

- **Do not share** your workflow with credentials included.
- Replace sensitive fields before sharing:
  - OpenAI API key → `"REPLACE_WITH_YOUR_OPENAI_KEY"`
  - Gmail OAuth2 → `"REPLACE_WITH_YOUR_GMAIL_OAUTH2_ID"`
  - Recipient email → `"YOUR_EMAIL@example.com"`
- Remove `instanceId` and `webhookId`.

---

## 📂 Files

- `ai_daily_news_workflow.json` – n8n workflow JSON file (with credentials removed).

---

## 📧 Usage

1. Import the workflow JSON into n8n.
2. Set your OpenAI and Gmail credentials.
3. Execute manually or wait for the scheduled trigger.
4. Check your inbox for daily news summary.

---

## 🔗 References

- [n8n Docs](https://docs.n8n.io/)
- [OpenAI API](https://platform.openai.com/docs/)
- [Gmail OAuth2 Setup](https://developers.google.com/identity/protocols/oauth2)
