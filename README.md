# WhatsApp Virtual Assistant – Calendar Scheduler

## 📌 Description
This project implements a **WhatsApp-based virtual assistant** using **n8n** to automate scheduling and calendar management with **Google Calendar**.  

Users can send text messages or voice notes through WhatsApp, and the assistant is able to:
- Transcribe voice notes using **OpenAI Whisper**.
- Interpret user requests with **AI (OpenAI GPT)**.
- Automatically create, reschedule, cancel, and query events in **Google Calendar**.
- Send back confirmations to the user via WhatsApp.

## 🚀 Technologies Used
- [n8n](https://n8n.io/) (workflow automation)
- [EvolutionAPI](https://github.com/) (WhatsApp integration)
- [OpenAI API](https://platform.openai.com/) (NLP and transcription)
- [Google Calendar API](https://developers.google.com/calendar)

## 📂 Key Features
- Receive messages (text or audio) from WhatsApp.
- Transcribe audio into text.
- Understand intent using AI.
- Manage calendar events automatically (create, update, delete, query).
- Send confirmation messages back to the user.

## ⚙️ Workflow Structure
1. **Webhook** → receives messages from EvolutionAPI (WhatsApp).
2. **Data Extraction** → extracts text or base64 audio.
3. **IF Node** → checks if the input is text or audio.
4. **Convert + Transcribe** → audio is converted and transcribed with OpenAI.
5. **AI Agent (OpenAI)** → interprets the user’s message.
6. **Google Calendar Nodes** → manage events (create, update, query, delete).
7. **HTTP Request** → sends confirmation to the user via WhatsApp.

## 📸 Workflow Example
![Calendar Workflow](./images/calendar-workflow.png)

## 📝 Conclusion
This assistant demonstrates how to combine **AI + messaging + automation** to build a powerful and practical tool for managing appointments in real time.
