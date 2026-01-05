# 📩 AI-Powered CRM Qualification from Email Replies (n8n)

This **n8n workflow** automatically analyzes replies from cold email campaigns, determines lead interest using **AI**, and creates deals in **Pipedrive CRM** when a prospect shows intent to meet.

The goal is to eliminate manual lead qualification and ensure that sales teams focus only on high-intent conversations.

---

## 🚀 What This Workflow Does

1. Monitors one or multiple **Gmail inboxes**
2. Captures replies from cold email campaigns
3. Matches the sender to an existing **Pipedrive person**
4. Checks whether the person belongs to an active campaign
5. Uses **AI (OpenAI)** to determine if the reply shows interest
6. Automatically creates a **deal in Pipedrive** if interest is detected

---

## 🧠 Use Case

- SDR / Sales teams running outbound campaigns  
- Founders handling cold outreach themselves  
- Agencies managing multiple inboxes and pipelines  
- Teams looking to reduce manual CRM updates  

---

## 🛠️ Tech Stack

- **n8n**
- **Gmail Trigger**
- **OpenAI (GPT-4)**
- **Pipedrive CRM**
- JavaScript (Code Node)

---

## ⚙️ Workflow Logic

- Gmail Trigger listens for incoming replies  
- Email content is extracted and normalized  
- Contact is searched and fetched from Pipedrive  
- Custom field `in_campaign` is validated  
- AI evaluates the reply for meeting intent  
- Positive replies automatically generate a CRM deal  

---

## 🔧 Setup Instructions

### 1. Import the Workflow
- Import the JSON file into n8n

### 2. Configure Credentials

You’ll need credentials for:
- Gmail
- OpenAI
- Pipedrive

> ⚠️ **Do not commit credentials or API keys to GitHub**

---

### 3. Configure Pipedrive Custom Field

Create a custom field for **Person** in Pipedrive:

- **Field name:** `in_campaign`
- **Type:** Single option
- **Values:** `TRUE` / `FALSE`

This field ensures only leads from active campaigns are evaluated.

---

### 4. Gmail Node Configuration

- Select **Inbox** as the label
- Disable **Simplify**
- Duplicate Gmail nodes to monitor multiple inboxes

---

## 📌 Key Features

- AI-based intent detection (not keyword-based)
- Multi-inbox support
- Automatic CRM deal creation
- Modular and extensible workflow
- Easy to adapt to other CRMs or email providers

---

## 🔮 Possible Extensions

- Add sentiment or confidence scoring  
- Send qualified leads to Slack or Notion  
- Update existing deals instead of creating new ones  
- Store AI reasoning for reporting and analytics  
- Support other CRMs (HubSpot, Salesforce)

---

## 🧩 Why This Matters

This workflow bridges the gap between **unstructured email replies** and **structured CRM actions**, saving time and improving sales efficiency through automation and AI-driven decision making.
