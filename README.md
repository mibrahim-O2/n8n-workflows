<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1a1a,50:2ea44f,100:1a1a1a&height=160&section=header&text=n8n%20Workflows%20Collection&fontSize=38&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Automation%20Workflows%20Built%20With%20n8n&descAlignY=62&descSize=15&descColor=eab308"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=17&duration=2800&pause=1000&color=2ea44f&center=true&vCenter=true&width=650&lines=Order+Automation+%C2%B7+AI+Chatbots+%C2%B7+Data+Ops;Newsletter+Generation+%C2%B7+Multi-Agent+Assistant" alt="Typing SVG"/>

<br/>

<img src="https://img.shields.io/badge/n8n-1a1a1a?style=for-the-badge&logo=n8n&logoColor=eab308&labelColor=1a1a1a">
<img src="https://img.shields.io/badge/License-MIT-2ea44f?style=for-the-badge&labelColor=1a1a1a">
<img src="https://img.shields.io/badge/Workflows-6-eab308?style=for-the-badge&labelColor=1a1a1a">

</div>

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:1a1a1a,50:2ea44f,100:1a1a1a&height=2" width="100%"/>

<div align="center">
 
## Overview

</div>

This repository contains **automation workflows** built with [n8n](https://n8n.io), an open-source workflow automation platform. Each workflow lives in its own folder with a dedicated README and JSON file for easy import into your own n8n instance.

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:1a1a1a,50:eab308,100:1a1a1a&height=2" width="100%"/>

<div align="center">

## Table of Contents

| Workflow | Description |
|---|---|
| [Order Automation](#order-automation) | Order processing and team notifications |
| [ChatBot — Gemini](#chatbot--google-gemini-chatbot) | Conversational AI chatbot with memory |
| [Airtable Integration](#airtable-integration) | Automated record creation in Airtable |
| [Data Operations](#data-operations) | Customer data retrieval and messaging |
| [Newsletter Agent](#newsletter-agent) | Automated AI-curated weekly newsletter |
| [Multi-Agent Assistant](#multi-agent-assistant) | AI assistant with Sheets and Calendar integration |

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:1a1a1a,50:2ea44f,100:1a1a1a&height=2" width="100%"/>

</div>


## Getting Started

**Clone or Download**

```bash
git clone https://github.com/mibrahim-O2/n8n-workflows.git
cd n8n-workflows
```

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:1a1a1a,50:eab308,100:1a1a1a&height=2" width="100%"/>

## Available Workflows

### Order Automation

**Project Name:** Real World Case

<p>
<img src="https://img.shields.io/badge/n8n-1a1a1a?style=flat-square&logo=n8n&logoColor=eab308&labelColor=1a1a1a">
<img src="https://img.shields.io/badge/Automation-1a1a1a?style=flat-square&labelColor=1a1a1a&color=2ea44f">
</p>

- Automates order processing and team notifications.
- Retrieves, filters, calculates totals, stores data, and sends summaries — no manual effort required.
- [View Details](Order-Automation/README.md)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:1a1a1a,50:2ea44f,100:1a1a1a&height=1" width="100%"/>

### ChatBot — Google Gemini Chatbot

**Project Name:** AI Chatbot with Memory

<p>
<img src="https://img.shields.io/badge/Google_Gemini-1a1a1a?style=flat-square&logo=googlegemini&logoColor=eab308&labelColor=1a1a1a">
<img src="https://img.shields.io/badge/Memory_Buffer-1a1a1a?style=flat-square&labelColor=1a1a1a&color=2ea44f">
<img src="https://img.shields.io/badge/AI_Agent-1a1a1a?style=flat-square&labelColor=1a1a1a&color=2ea44f">
</p>

- Google Gemini (PaLM)–powered conversational bot.
- Retains recent chat context using Simple Memory Buffer.
- AI Agent processes and responds intelligently.
- [View Details](./ChatBot/README.md)

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:1a1a1a,50:eab308,100:1a1a1a&height=1" width="100%"/>

 
 
 
  
 

 
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

