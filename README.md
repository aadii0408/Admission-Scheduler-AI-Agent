# 🎓 DuckOps: AI Voice Admissions Assistant

Welcome to **DuckOps**, the first AI-powered voice agent designed specifically for university admissions scheduling and inquiry at Stevens Institute of Technology. Built during the VAPI Hackathon by Aditya and Rushi, DuckOps transforms how prospective students engage with admissions staff—making the process faster, friendlier, and fully automated.

---

## 🚀 Project Overview

DuckOps allows prospective students to:

* **🔹 Seamlessly schedule appointments** (application advising, campus tours, financial-aid consultations, visa guidance) via natural conversation.
* **🔹 Instantly answer FAQs** on deadlines, tuition & fees, scholarships, campus life, and visa procedures.
* **🔹 Reschedule or cancel** existing appointments with ease.
* **🔹 Receive multi-channel reminders** via Zoom calendar invites, email, and SMS.
* **🔹 Be transferred** to live Admissions Desk for complex or status-update queries.

It will be the *first* * AI assistant for the university for end-to-end admissions support—and can be extended to schools, coaching centers, healthcare clinics, and beyond.

---

## ✨ Key Features

1. **Natural Voice Conversation**: Powered by VAPI’s live call-control APIs, DuckOps understands intent and collects dynamic information in real time.
2. **Context-Aware Workflow**: Captures student type (domestic/international), program level, application status, urgency, and topics to cover.
3. **Warm Transfer**: Seamlessly hands off callers to human admissions specialists when deeper support is needed.
4. **Multi-Channel Confirmation**: Automatically generates Zoom invites, emails, and SMS reminders with customizable timing.
5. **Comprehensive Overview Module**: Provides on-the-spot summaries of deadlines, costs, scholarships, campus life, and next steps.

---

## 🏗 Architecture & Tech Stack

```mermaid
flowchart LR
  A[Caller] --> B[DuckOps (VAPI Voice Agent)]
  B --> C{Intent Router}
  C -->|Book| D[Appointment Scheduler]
  C -->|Info| E[Overview Module]
  C -->|Cancel| F[Cancellation Handler]
  C -->|Reschedule| G[Rescheduler]
  C -->|Status| H[Live Transfer]
  D --> I[Google Calendar API]
  D --> J[Email/SMS Gateway]
  H --> K[SIP: admissions-info@stevens.edu]
```

* **Voice Engine**: VAPI live call-control & speech-to-speech
* **Data Storage**: In-memory session store (demo), pluggable to Redis or database
* **Reminders**: Google Calendar API, Twilio (SMS), SendGrid (Email)
* **Deployment**: Dockerized microservices on Azure Container Instances

---

## 📺 Live Demo

Watch DuckOps in action: [YouTube Demo Video]([https://youtu.be/your-demo-link](https://youtu.be/fEOnXAHWh40))

---

## 💡 Use Cases & Extensions

* **Education**: Adaptable for high schools, coaching centers, graduate schools
* **Healthcare**: Clinic appointment scheduling, telemedicine intake
* **Services**: Customer support, reservation systems, and more

---

*Ready to bring AI voice Agents, Let’s duck in!*
