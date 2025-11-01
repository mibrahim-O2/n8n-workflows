# ⚙️ n8n Workflows Collection

This repository contains **automation workflows** built with [n8n](https://n8n.io), an open-source workflow automation platform.  
Each workflow lives in its own folder with a dedicated README and JSON file for easy import into your own n8n instance.

---

## 📂 Available Workflows

### 🔸 [Order Automation](./Order-Automation)
**Project Name:** Real World Case  
- 📦 Automates order processing and team notifications.  
- 🧮 Retrieves, filters, calculates totals, stores data, and sends summaries—no manual effort required.  
- 📄 [View Details](Order-Automation/README.md)  

---

## 🚀 Getting Started

### 1️⃣ Clone or Download
```bash
 ```markdown
### 1️⃣ Clone or Download
```bash
git clone https://github.com/mibrahim-O2/n8n-workflows.git
cd n8n-workflows
```
----
### 🤖 [ChatBot – Google Gemini Chatbot](./ChatBot01)
**Project Name:** AI Chatbot with Memory  
- 🔗 Google Gemini (PaLM)–powered conversational bot.  
- 🧠 Retains recent chat context using Simple Memory Buffer.  
- 🤖 AI Agent processes and responds intelligently.  
- 📄 [View Details](./ChatBot/README.md)

----
### 📋 [Air-Table-Integration](./Airtable_Example)  
**Project Name:** Airtable Record Creator  
- ▶️ Manually triggered workflow for quick testing.  
- ✍ Sets example fields (`Name`, `User_Email`) before sending.  
- 📥 Creates a new record in your chosen Airtable base.  
- 📄 [View Details](./Air-Table-Integration/README.md)
----

### 📊 [Data-Operations](./Data_Retrival)  
**Project Name:** Customer Data Messenger  
- 📥 Retrieves customer records from the training datastore.  
- ✍ Maps fields like ID, Name, Email, and Notes.  
- 📤 Sends formatted messages to customers.  
- 📄 [View Details](./Data-Operations/README.md)
----

### 📰 [News-Letter-Agent](./News-Letter-Agent)

**Project Name:** Automated AI Newsletter Generator

* 🧠 Uses **Google Gemini (PaLM)** and **Tavily API** to curate weekly business news.
* 🕒 Runs automatically every Monday at 9 AM via **Schedule Trigger**.
* ✍️ Generates structured content, converts it into an HTML newsletter, and saves a **Gmail draft** for review.
* 📄 [View Details](https://github.com/mibrahim-O2/n8n-workflows/blob/main/News-Letter-Agent/README.md)
----
### 🤖 [Multi-Agent](./Multi-Agent)

**Project Name:** AI Multi-Tool Assistant

* 💬 Chat-triggered workflow that responds intelligently using **Google Gemini (PaLM)**.
* 🧠 Includes short-term **memory** for contextual conversations.
* 🗓️ Integrates with **Google Sheets** for data lookup and **Google Calendar** for event scheduling.
* ⚡ Demonstrates a **multi-agent architecture** inside n8n for dynamic task handling.
* 📄 [View Details](https://github.com/mibrahim-O2/n8n-workflows/blob/main/Multi-Agent/README.md)
----



----

## 🧾 License

This repository is licensed under the **MIT License**.

You are free to use, modify, and distribute these workflow examples for both personal and commercial purposes, provided that you include the original copyright notice and this permission notice in all copies or substantial portions of the software.

> ⚠️ **Disclaimer:**
>
> * All workflows are provided **“as is”**, without warranty of any kind.
> * These examples are for **educational and internal automation** purposes.
> * Users are responsible for ensuring compliance with **third-party API terms** (e.g., Google, Tavily, Airtable).
> * OpenAI, Google Gemini, and other APIs used in these workflows may have their own usage restrictions and rate limits.
----

