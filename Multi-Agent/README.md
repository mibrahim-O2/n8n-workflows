# 🤖 Multi-Agent — README

## 🧠 Overview
**Multi-Agent** is an **interactive AI automation workflow** designed for **n8n**, enabling intelligent, multi-tool conversational capabilities through **Google Gemini (PaLM)** and integrated Google Workspace tools.  
It acts as a **smart assistant** that can **chat with users**, **remember context**, **retrieve data from Google Sheets**, and **manage events in Google Calendar** — all through a single conversational interface.

This workflow demonstrates how to build a **multi-agent AI system** inside n8n, where different “tools” (like calendar and sheet access) can be used automatically based on the user’s request.

---

## ⚙️ Workflow Summary

### **1. When Chat Message Received**
* **Node:** `When chat message received`
* **Type:** `@n8n/n8n-nodes-langchain.chatTrigger`
* **Purpose:** Triggers the workflow whenever a new chat message is received.
* **Usage:** Acts as the main entry point for user interactions in a chatbot or AI interface.

---

### **2. Google Gemini Chat Model**
* **Node:** `Google Gemini Chat Model`
* **Type:** `@n8n/n8n-nodes-langchain.lmChatGoogleGemini`
* **Purpose:** Provides the **AI language model** backbone that powers all conversational and reasoning abilities.
* **Credentials:** Uses the connected **Google Gemini (PaLM)** API account.
* **Function:** Generates intelligent, natural responses and can interpret multi-step instructions.

---

### **3. Simple Memory**
* **Node:** `Simple Memory`
* **Type:** `@n8n/n8n-nodes-langchain.memoryBufferWindow`
* **Purpose:** Enables **short-term memory** by storing the **last 10 messages** of conversation.
* **Function:** Helps maintain conversational context — so the AI can remember what was said earlier and respond accordingly.

---

### **4. AI Agent**
* **Node:** `AI Agent`
* **Type:** `@n8n/n8n-nodes-langchain.agent`
* **Purpose:** The central **multi-agent controller** that orchestrates all actions between chat input, memory, and external tools.
* **System Message:**  
  > “You are a helpful assistant!”
* **Functions:**
  - Processes incoming chat messages  
  - Maintains memory and context  
  - Calls appropriate tools dynamically based on user intent  
  - Returns a coherent, context-aware response

---

### **5. Get-Contact-Data (Google Sheets Tool)**
* **Node:** `Get-Contact-Data`
* **Type:** `n8n-nodes-base.googleSheetsTool`
* **Purpose:** Allows the AI Agent to **fetch specific data** (e.g., contact or patient info) from a connected Google Sheet.
* **Sheet Info:**
  - **Document ID:** `1zaLX0NAbyCctRppiRhrW0q8BRAPHEigtDDXsPK-6daA`
  - **Sheet Name:** `Contacts_CSV_template`
* **Use Case Example:**  
  “Find the record for patient *John Doe*” or “Check the contact details for *Client X*.”

---

### **6. Event-Manager (Google Calendar Tool)**
* **Node:** `Event-Manager`
* **Type:** `n8n-nodes-base.googleCalendarTool`
* **Purpose:** Allows the AI Agent to **create events** in Google Calendar automatically.
* **Description:** “Create an event in Google Calendar.”
* **Credentials:** Uses the connected **Google Calendar OAuth2** account.
* **Use Case Example:**  
  “Schedule a meeting for tomorrow at 10 AM” or “Add a reminder for next Friday.”

---

## 🧩 Node Connections

| From | To | Connection Type | Purpose |
|------|----|-----------------|----------|
| When chat message received | AI Agent | `main` | Sends the user’s message to the AI |
| Google Gemini Chat Model | AI Agent | `ai_languageModel` | Provides LLM capabilities |
| Simple Memory | AI Agent | `ai_memory` | Enables conversational memory |
| Event-Manager | AI Agent | `ai_tool` | Enables event scheduling via Calendar |
| Get-Contact-Data | AI Agent | `ai_tool` | Enables data lookup via Google Sheets |

---

## 🧱 How It Works

1. A user sends a **chat message** (via webhook or interface).  
2. The **AI Agent** receives it through the **Chat Trigger** node.  
3. The **Gemini model** interprets and reasons about the query.  
4. The **Memory** node provides previous conversation context.  
5. If the message requires data (e.g., contact info or scheduling), the agent:
   - Queries Google Sheets via **Get-Contact-Data**
   - Or creates events via **Event-Manager**
6. The **AI Agent** synthesizes the result and sends a **natural-language reply**.

---

## 🧠 Example Interactions

### 🔹 Retrieve Data
> **User:** “Show me the contact details for Sarah Parker.”  
> **AI Agent:** Retrieves the row from the Google Sheet and responds with relevant data.

### 🔹 Schedule an Event
> **User:** “Set a meeting with the design team on Monday at 3 PM.”  
> **AI Agent:** Automatically creates the event in Google Calendar and confirms.

### 🔹 Maintain Context
> **User:** “Add another reminder for the same day.”  
> **AI Agent:** Uses memory to recall the previous event and adds a new one accordingly.

---

## 🧠 Key Features
- **Conversational AI agent** powered by Google Gemini.  
- **Short-term memory** for contextual continuity.  
- **Multi-tool integration:** Google Sheets + Google Calendar.  
- **Fully automated chat interface** trigger via webhook.  
- **Flexible and scalable** for any business assistant use case.  

---

## ⚙️ Setup Instructions

1. **Import** `Multi-Agent.json` into your **n8n instance**.  
2. **Connect credentials**:
   - Google Gemini (PaLM)
   - Google Sheets OAuth2
   - Google Calendar OAuth2
3. **Activate the webhook trigger** (`When chat message received`).  
4. **Customize system message** in the **AI Agent** if needed.  
5. **Run the workflow** and test via your chat interface.  

---

## 🧾 Example Use Cases

- AI-powered **Customer Support Assistant**  
- **Internal company scheduler** (meetings, reminders)  
- **Patient management assistant** (fetching medical data from Sheets)  
- **Smart data assistant** for business analytics  

---

## 🧩 Core Technologies

| Component | Purpose |
|------------|----------|
| **n8n** | Orchestrates automation flow |
| **Google Gemini (PaLM)** | Natural language reasoning |
| **Google Sheets API** | Data retrieval |
| **Google Calendar API** | Event creation |
| **LangChain Integration** | Memory + multi-tool orchestration |

---

## 🧾 License
This workflow JSON is intended for **educational and internal automation** use.  
Ensure compliance with **Google API usage terms** for Sheets and Calendar integrations.

---
