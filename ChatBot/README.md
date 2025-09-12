# 🤖 ChatBot – n8n Google Gemini Chatbot

A lightweight **n8n** workflow for creating an AI-powered chatbot using **Google Gemini (PaLM)**.  
It listens for chat messages, processes them with an AI Agent, and uses a memory buffer for context.

---

## ✨ Features
- 🔗 Integrates **Google Gemini (PaLM)** for natural conversations  
- 🧠 Uses **Simple Memory Buffer** for recent chat context  
- 🤖 AI Agent for handling conversation flow  
- ⚡ Quick to set up in any n8n instance  

---

## 🗂 Workflow Nodes
| Node                       | Purpose                               |
|----------------------------|---------------------------------------|
| When chat message received  | Triggers on new chat messages         |
| AI Agent                    | Handles processing and reasoning      |
| Google Gemini Chat Model    | Generates responses via Gemini API    |
| Simple Memory               | Stores recent chat context            |

---

## ▶️ Usage
1. Import the workflow into your **n8n** instance.  
2. Add your **Google Gemini (PaLM)** API key under **Credentials → GooglePalmApi**.  
3. Activate the workflow.  
4. Test by sending a chat message trigger.  

---

## 🧩 Customization
- Adjust memory window size for more/less context.  
- Tweak AI Agent settings (e.g., temperature, system prompt).  
- Extend with extra nodes for logging, notifications, or integrations.  

---

## 📄 License
Provided as-is under the **MIT License**.
