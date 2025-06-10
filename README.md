# 🧠 2Care.ai Vapi Voice Agent System

A fully automated, human-like **Voice Agent Suite** for 2Care.ai — built using [Vapi](https://www.vapi.ai/) and [n8n](https://n8n.io). This system includes three specialized AI agents — **Neha**, **Priya**, and **Anita** — designed to manage the full lifecycle of patient engagement through natural, real-time voice conversations.

> From onboarding and appointment scheduling to reminders and post-care check-ins — everything is handled hands-free, using voice.

---

## 🚀 Overview

| Agent | Role | Timing |
|-------|------|--------|
| **Neha** | Patient Onboarding, Appointment Scheduling, Family Calls, Customer Support | Initial Engagement |
| **Priya** | Appointment Reminder, Confirmation & Rescheduling | 2 hours before appointment |
| **Anita** | Biweekly Health Check-In, Follow-up Review, and Upsell Conversations | 2 weeks after appointment |

---

## 🎙️ Agents & Use Cases

### 🩺 Neha AI Agent – Intelligent Intake & Scheduling

**Use Cases**:
- **Initial Patient Discovery** – Captures structured health data (name, age, symptoms, conditions, contact info).
- **Family Member Discovery** – Gathers care context, urgency, relation to patient, and visit reason.
- **Appointment Booking** – Schedules appointments, confirming date, time, patient info, and medical need.
- **Customer Support** – Answers general queries, redirects to support, or logs help requests.

**Prompt**: [`Neha Intro`](Agent Prompts/Neha%20Intro.txt)  
**Workflow**: ![Neha Workflow](images/neha-workflow.png)

---

### ⏰ Priya AI Agent – Appointment Reminder & Rescheduler

**Use Case**:
- Automatically calls patients **2 hours before** their scheduled appointment.
- Asks if they are still attending, gathers a brief health update, and offers to **reschedule** if needed.
- Handles appointment confirmation, rescheduling, or cancellation — based on live conversation.

**Prompt**: [`Priya Reminder`](Agent Prompts/Priya%20Reminder.txt)  
**Workflow**: ![Priya Workflow](images/priya-workflow.png)

---

### 📞 Anita AI Agent – Biweekly Check-In & Health-Based Upsell

**Use Case**:
- Conducts follow-up **health check-in calls 14 days after an appointment**.
- Reviews health trends, flags concerns, celebrates progress, and checks medication adherence.
- Introduces plan upgrades if they offer medical benefit (e.g., 24/7 support, better vitals tracking, family coordination).

**Prompt**: [`Anita 3-Week Report`](Agent Prompts/Anita%203%20week%20report.txt)  
**Workflow**: ![Anita Workflow](images/anita-workflow.png)

---

## 🧰 Tech Stack

- **Vapi** – Multimodal Voice AI Interface (STT + LLM + TTS)
- **n8n** – Low-code automation to manage data flow, webhooks, database actions
- **Supabase** – Patient records, slot management, and health data storage
- **OpenAI / Claude** – Language models for contextual awareness and summarization
- **Google Meet** – Used for all appointment consultations

---

## 📦 Folder Structure

/Agent Prompts → Vapi prompt files for each agent
/images → Workflow screenshots for each agent
/n8n-workflows → Flow exports (optional)
README.md


---

## ✅ Setup Instructions

1. Clone the repository
2. Set up Vapi agents and upload corresponding prompts
3. Import and configure n8n workflows
4. Connect to Supabase (or any DB of choice)
5. Integrate webhook URLs between Vapi <-> n8n
6. Monitor conversations and follow-up actions via dashboards

---
