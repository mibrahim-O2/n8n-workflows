# 🤖 ChatBot01 – n8n Google Gemini Chatbot

This repository contains an **n8n** workflow that creates an AI-powered chatbot using **Google Gemini (PaLM)** as the language model.  
It listens for incoming chat messages, processes them with an AI Agent, and retains conversation history using a memory buffer.

---

## ✨ Features

- 🔗 **Google Gemini (PaLM)** integration for natural language conversations  
- 🧠 **Simple Memory Buffer** to preserve recent chat context  
- 🤖 **AI Agent** node to handle reasoning and conversation flow  
- ⚡ Easily deployable in any n8n instance  

---

## 🗂 Workflow Overview

| Node                         | Purpose                                                                 |
|-------------------------------|-------------------------------------------------------------------------|
| **When chat message received** | Trigger: Activates when a new chat message is received                  |
| **AI Agent**                   | Processes input and communicates with the language model & memory       |
| **Google Gemini Chat Model**   | Provides responses using Google Gemini (PaLM) API                       |
| **Simple Memory**              | Stores recent chat history for contextual answers                       |

---

## ▶️ One-Click Import to n8n

[![Import to n8n](https://img.shields.io/badge/Import%20to-n8n-blue?logo=n8n&style=for-the-badge)](https://n8n.io/workflows/DMnsCrmf2mqHHLfw)

Alternatively, you can manually import:

1. **Open your n8n instance** (self-hosted or [n8n.cloud](https://n8n.io)).  
2. Click on **Import Workflow**.  
3. Paste the following **Import URL** to load the workflow directly:  https://n8n.io/workflows/DMnsCrmf2mqHHLfw

---

4. After import:
- Configure your **Google Gemini (PaLM) API** credentials in **Credentials → GooglePalmApi**.  
- Activate the workflow.  
- Test by sending a chat message trigger.

---

## 🔑 Required Credentials

- **Google Gemini (PaLM) API** → Add your API key in **Credentials → GooglePalmApi** within your n8n instance.

---

## 🧩 Customization

- Adjust **memory window size** in the **Simple Memory** node for more or less context retention.  
- Modify the **AI Agent’s settings** (temperature, system prompt, etc.) to match your use case.  
- Add additional nodes (e.g., database logging, notifications) to extend functionality.  
- Style or rename nodes for clearer workflow organization.

---

## 🖼 Preview

> *(Optional)* You can add a screenshot or diagram of the workflow here to show its layout in n8n.

---

## 📄 License

This workflow is provided as-is under the **MIT License**.



