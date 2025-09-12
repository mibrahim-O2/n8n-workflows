# 📋 Airtable Example – n8n Workflow

This workflow demonstrates how to **create a new record in Airtable** using n8n.  
It includes a manual trigger, a field editor, and the Airtable node to insert data into your base.

---

## ✨ Features
- ▶️ **Manual Trigger** – Easily run the workflow on demand.  
- ✍ **Edit Fields** – Sets example values (`Name` and `User_Email`) before sending them to Airtable.  
- 📥 **Airtable Integration** – Creates a new record in your chosen base and table.  

---

## 🗂 Workflow Overview
| Node                          | Purpose                                        |
|-------------------------------|------------------------------------------------|
| When clicking ‘Execute workflow’ | Starts the workflow manually                  |
| Edit Fields                   | Assigns static values for Name and User_Email   |
| Create a record               | Sends the values to Airtable to create a record |

---

## ▶️ Usage
1. Import the `workflow.json` file into your **n8n** instance.  
2. Connect your **Airtable Personal Access Token** in the **Airtable** node credentials.  
3. Update:
   - **Base** – Select your Airtable base.  
   - **Table** – Choose the target table.  
   - **Fields** – Adjust field mappings if your Airtable schema differs.  
4. Click **Execute Workflow** to test.  
5. Verify the new record in your Airtable base.

---

## 🧩 Customization
- Replace static values in **Edit Fields** with dynamic data from another node or trigger.  
- Modify or expand field mappings to match your Airtable structure.  
- Schedule or automate the workflow with triggers like **Cron**, **Webhook**, or **Form submissions**.  

---

## 📄 License
Provided as-is under the **MIT License**.

