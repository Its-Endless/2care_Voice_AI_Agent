# 🏥 2Care.ai Voice Agent System

A fully automated, human-like **Medical Voice Assistant Suite** powered by AI. Our system manages the complete patient journey from initial contact to follow-up care through natural voice conversations, making healthcare more accessible and efficient.

## 📝 Start Here: Patient Intake Form

The patient journey begins with this **Tally.so form** where patients provide their initial details to kick off the workflow:

[Complete the Intake Form](https://tally.so/r/3q7NJO)

![Tally.so Intake Form](Screenshots/tallyform.png)

## 🎯 Our Agents

| Agent | Phone Number | Primary Role |
|-------|-------------|--------------|
| **Neha** | (+1 (239) 397 2143) | Patient Onboarding & Scheduling |
| **Priya** | (-) | Appointment Reminders & Rescheduling |
| **Anita** | (-) | Post-Visit Care & Health Check-ins |

## 🛠️ Tech Stack

[![Vapi.ai](https://img.shields.io/badge/Vapi.ai-Voice%20AI-blue)](https://www.vapi.ai)
[![n8n](https://img.shields.io/badge/n8n-Workflow%20Automation-orange)](https://n8n.io)
[![Twilio](https://img.shields.io/badge/Twilio-Communications-red)](https://www.twilio.com)
[![Airtable](https://img.shields.io/badge/Airtable-Database-green)](https://www.airtable.com)
[![Tally.so](https://img.shields.io/badge/Tally.so-Form%20Builder-brightgreen)](https://tally.so)

---

## 📊 System Architecture
![System Flowchart](Flowchart.png)

A brief Flowchart from initial contact to follow-up care.

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

**Prompt**: [`Neha Intro`](Agent%20Prompts/Neha%20Intro.txt)  
**Workflow**: [`Neha Workflow`](Screenshots/Neha%20Workflow.png)

---

### ⏰ Priya AI Agent – Appointment Reminder & Rescheduler

**Use Case**:
- Automatically calls patients **2 hours before** their scheduled appointment.
- Asks if they are still attending, gathers a brief health update, and offers to **reschedule** if needed.
- Handles appointment confirmation, rescheduling, or cancellation — based on live conversation.

**Prompt**: [`Priya Reminder`](Agent%20Prompts/Priya%20%20Reminder.txt)  
**Workflow**: [`Priya Workflow`](Screenshots/Priya%20Workflow.png)

---

### 📞 Anita AI Agent – Biweekly Check-In & Health-Based Upsell

**Use Case**:
- Conducts follow-up **health check-in calls 14 days after an appointment**.
- Reviews health trends, flags concerns, celebrates progress, and checks medication adherence.
- Introduces plan upgrades if they offer medical benefit (e.g., 24/7 support, better vitals tracking, family coordination).

**Prompt**: [`Anita 3-Week Report`](Agent%20Prompts/Anita%203_Week_Report.txt)  
**Workflow**: [`Anita Workflow`](Screenshots/Anita%20Workflow.png)

---

## 🤖 Agent Details

### 1. Neha - Patient Onboarding Specialist
- **Role**: Initial patient contact and scheduling
- **Use Cases**:
  - Patient information collection
  - Family member discovery calls
  - Appointment scheduling
  - General inquiries handling
- **Prompt**: [View Neha's Conversation Flow](Agent%20Prompts/Neha%20Intro.txt)
- **Active Hours**: 24/7

### 2. Priya - Appointment Manager
- **Role**: Appointment coordination and reminders
- **Use Cases**:
  - 2-hour appointment reminders
  - Rescheduling requests
  - Pre-visit instructions
  - Last-minute cancellations
- **Prompt**: [View Priya's Conversation Flow](Agent%20Prompts/Priya%20%20Reminder.txt)
- **Active Hours**: Based on appointment schedule

### 3. Anita - Follow-up Care Specialist
- **Role**: Post-appointment care and monitoring
- **Use Cases**:
  - 2-week health check-ins
  - Progress monitoring
  - Treatment adherence checks
  - Care plan upgrades
- **Prompt**: [View Anita's Conversation Flow](Agent%20Prompts/Anita%203_Week_Report.txt)
- **Active Hours**: Business hours only

## 🔄 Workflow Automation

### 1. Call Scheduling System
![Neha's Call Flow](Screenshots/Neha%20Workflow.png)
- **Workflow File**: [Call_Scheduling____2care_ai.json](n8n%20Workflows/Call_Scheduling____2care_ai.json)
- **Purpose**: Manages the entire scheduling pipeline from initial contact to appointment confirmation

### 2. Patient Reminder System
![Priya's Reminder Flow](Screenshots/Priya%20Workflow.png)
- **Workflow File**: [Patient_Reminder____2care_ai.json](n8n%20Workflows/Patient_Reminder____2care_ai.json)
- **Purpose**: Automates appointment reminders and handles rescheduling requests

### 3. Follow-up Care System
![Anita's Check-in Flow](Screenshots/Anita%20Workflow.png)
- **Workflow File**: [Two_Week_Checkup____2care_ai.json](n8n%20Workflows/Patient_Reminder____2care_ai.json)
- **Purpose**: Manages post-appointment follow-ups, tracks patient progress, and identifies upgrade opportunities

## 🛠️ Technical Implementation

- **Vapi.ai**: Powers our conversational AI with advanced speech recognition and natural language processing
- **n8n**: Orchestrates workflows and integrates various services
- **Twilio**: Handles voice calls and SMS communications
- **Airtable**: Stores patient data, appointment schedules, and interaction logs
- **Tally.so**: Collects initial patient intake data via easy-to-use forms

---

## ✅ Setup Instructions

### 1. Repository Setup
- Clone the repository: `git clone https://github.com/yourusername/2care_Voice_AI_Agent.git`
- Navigate to project directory: `cd 2care_Voice_AI_Agent`
- Check all required files and folders are present (workflows, prompts, screenshots)

### 2. n8n Configuration
- Import the following workflow files to your n8n instance:
  - `Call_Scheduling____2care_ai.json`
  - `Patient_Reminder____2care_ai.json`
- Setup required credentials:
  - Google Calendar API credentials
  - Gmail credentials
  - Airtable API key and base configuration
  - Twilio account SID and auth token

### 3. Vapi.ai Setup
- Create three agents in Vapi dashboard (Neha, Priya, Anita)
- Upload conversation prompts from [`Agent Prompts`](Agent%20Prompts) folder
- Configure agent functions:
  - [`Get-Slots()`](vapi_functions/Get-Slot.txt) - Calendar availability check
  - [`Book_Slot()`](vapi_functions/Book_Slot.txt) - Slot reservation
  - [`Cancel_Slot()`](vapi_functions/Cancel_Slot.txt)) - Appointment cancellation
- Test each agent's conversation flow

### 4. Integration Configuration
- Update webhook URLs in n8n workflows with your Vapi endpoints
- Configure Twilio phone numbers for each agent
- Setup Airtable base with required tables:
  - Patients
  - Appointments
  - Health Records
  - Follow-ups
- Test end-to-end workflow for each agent

### 5. Monitoring & Maintenance
- Setup monitoring dashboard for:
  - Call success rates
  - Conversation completion metrics
  - Appointment statistics
- Configure error notifications
- Regular backup of workflow configurations
- Monitor API usage and limits

### 6. Testing & Validation
- Perform test calls with each agent
- Verify data flow between systems
- Check appointment booking and reminder functionality
- Validate health check-in process
