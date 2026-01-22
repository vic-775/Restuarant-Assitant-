# 🍽️ Platinum Restaurant Assistant

Platinum Restaurant Assistant is an **agentic AI system for restaurant operations** that combines modern LLM agents, workflow orchestration, and multi-channel communication to automate reservations, orders, and staff coordination.

The same AI agent can be triggered via **chat, voice calls, and WhatsApp**, providing a unified intelligence layer across all customer touchpoints.

---
![Platinum Restaurant Assistant](./Resturant%20Asistant%20image.png)

---

## ✨ Key Features

* 🤖 **Agentic AI (OpenAI)** for reasoning, intent detection, and decision-making
* 🧠 **n8n Orchestration** to coordinate tools, workflows, and integrations
* 🗄️ **Supabase Postgres** for transactional data and Natural Language → SQL (Text-to-SQL)
* 📚 **Supabase Vector Store (pgvector)** for Retrieval-Augmented Generation (RAG)
* 📞 **Voice Calling via Vapi** for phone-based reservations and inquiries
* 💬 **WhatsApp Messaging** for customer conversations and updates
* 📄 **Google Docs** as a live knowledge source (FAQs, policies)
* 📅 **Google Calendar** for reservations and availability management
* 📧 **Gmail Alerts** for real-time kitchen and staff notifications

---

## 🧩 Architecture Overview

Platinum Restaurant Assistant is designed around a **single AI agent** that can be triggered from multiple channels:

* Web / chat interfaces
* Voice calls (Vapi)
* WhatsApp messages

n8n acts as the **central orchestrator**, routing requests, invoking the AI agent, querying databases, retrieving knowledge via RAG, and triggering external actions such as emails or calendar updates.

**Supabase** is used as the unified data layer:

* **Postgres tables** store orders, menus, reservations, and operational data
* **pgvector** enables semantic search and RAG over unstructured knowledge

---

## 🔁 Supported Interaction Channels

### 💬 Chat & Messaging

* Natural language queries for menus, policies, and availability
* WhatsApp-based conversations for customer engagement
* Context-aware follow-ups using conversation memory

### 📞 Voice Calls (Vapi)

* AI-powered phone agent for:

  * Taking reservations
  * Answering common questions
  * Routing requests to staff when needed
* Uses the same backend agent and tools as chat

### 🏗️ Backend Automation (n8n)

* Workflow routing and state management
* Tool calling and conditional logic
* Event-based triggers (new reservation, new order, escalation)

---

## 🎯 Example Use Cases

* A customer calls the restaurant → AI answers via **Vapi** → books a table → updates **Google Calendar** → notifies staff via **Gmail**
* A customer messages on **WhatsApp** → asks about menu items → AI retrieves info from **RAG** (Google Docs)
* A customer places an order → AI converts intent to **SQL** → stores order in **Supabase Postgres** → alerts kitchen

---

## 🏗️ Design Principles

* **Single-agent, multi-channel** architecture
* **Loosely coupled services** for scalability and maintainability
* **Production-oriented** workflows (observability, retries, fallbacks)
* **Clear separation** between orchestration, intelligence, and storage layers

---

## 🚀 Tech Stack

* **LLM**: OpenAI
* **Orchestration**: n8n
* **Database**: Supabase (Postgres)
* **Vector Store**: Supabase pgvector
* **Voice AI**: Vapi
* **Messaging**: WhatsApp
* **Knowledge Source**: Google Docs
* **Scheduling**: Google Calendar
* **Notifications**: Gmail

---

## 📌 Status

This project is under active development and experimentation, focusing on agent reliability, prompt design, and real-world restaurant workflows.

---

