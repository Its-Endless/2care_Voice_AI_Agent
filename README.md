# 🧠 2Care Voice AI Agent (Vapi + n8n)

A fully automated, human-like Voice Agent for 2Care.ai — built using [Vapi](https://www.vapi.ai/) and [n8n](https://n8n.io/). These agent (Neha, Priya and Anita) handles medical appointment scheduling, patient onboarding, rescheduling, cancellations, customer support, appointment remainder and biweekly checkup — entirely through natural-sounding voice conversations.

## 🛠️ Features

- 🎙️ **Voice AI** powered by Vapi (LLM + TTS + STT)
- ⚙️ **n8n Automation** for scheduling logic, webhook handling, and database integration
- 🤖 **Context-aware Conversations** for new and returning patients
- 📆 **Appointment System Integration** with real-time availability checks and booking
- ❓ **FAQ Triage** using a dynamic knowledge base
- 📞 Handles full workflows: onboarding → booking → rescheduling → cancellation → support

## 📦 Tech Stack

- **Vapi.ai** – Voice AI orchestration
- **n8n.io** – Workflow automation + webhook routing
- **OpenAI / Claude** – Language model powering Assistant's brain (via Vapi)
- **Google Meet** – All consultations are scheduled as virtual calls

## 🚀 How It Works

1. User calls the AI agent.
2. Vapi processes speech and sends intents to n8n.
3. n8n routes the data (e.g., booking info) and handles webhook/API calls.
4. Confirmation and follow-ups are sent via WhatsApp/email.

## 🧰 Folder Structure
/n8n-workflows → All n8n flows used for appointment logic
/vapi-prompts → Voice agent prompt (Neha)
/docs → Architecture diagrams, notes
README.md


## 🔄 Flows Included

- Initial Patient Discovery
- Family Member Booking
- Appointment Scheduling (via `Get-Slot` + `Book_Slot`)
- Rescheduling 
- Cancellations (`Cancel_Slot`)
- FAQ support and fallback handling

## 🧪 Demo & Setup


To run this:
- Setup your agent on [Vapi.ai](https://vapi.ai/)
- Import n8n workflows
- Configure webhooks and environment variables
- Connect to a scheduling system 

