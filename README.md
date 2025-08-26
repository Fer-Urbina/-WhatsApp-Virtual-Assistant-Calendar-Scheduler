# WhatsApp Virtual Assistant – Calendar Scheduler

## 📌 Descripción
Este proyecto implementa un asistente virtual conectado a **WhatsApp** que utiliza **n8n** como orquestador para automatizar la gestión de citas en **Google Calendar**.  

Los usuarios pueden enviar mensajes de texto o notas de voz a través de WhatsApp, y el asistente es capaz de:
- Transcribir notas de voz usando **OpenAI Whisper**.
- Interpretar solicitudes con **IA (OpenAI GPT)**.
- Crear, reprogramar, cancelar y consultar citas en **Google Calendar** automáticamente.
- Responder al usuario por WhatsApp con confirmaciones.

## 🚀 Tecnologías utilizadas
- [n8n](https://n8n.io/) (automatización de flujos de trabajo)
- [EvolutionAPI](https://github.com/)** (puente para WhatsApp)
- [OpenAI API](https://platform.openai.com/) (procesamiento de lenguaje natural y transcripción)
- [Google Calendar API](https://developers.google.com/calendar)

## 📂 Funcionalidades principales
- Recepción de mensajes (texto o voz) desde WhatsApp.
- Transcripción de audios a texto.
- Interpretación y gestión de citas mediante IA.
- Creación, reprogramación, cancelación y consulta de eventos en Google Calendar.
- Respuesta automática al usuario vía WhatsApp.

## ⚙️ Estructura del Workflow
1. **Webhook** → recibe mensajes de EvolutionAPI (WhatsApp).
2. **Data Extraction** → extrae texto o base64 de audio.
3. **IF Node** → determina si es texto o audio.
4. **Convert + Transcribe** → si es audio, convierte y transcribe con OpenAI.
5. **AI Agent (OpenAI)** → interpreta el mensaje.
6. **Google Calendar Nodes** → agenda, consulta, cancela o reprograma eventos.
7. **HTTP Request** → envía la confirmación al usuario vía WhatsApp.

## 📸 Ejemplo de flujo
![Workflow Calendar](./images/calendar-workflow.png)

## 📝 Conclusión
Este asistente demuestra cómo integrar **IA + mensajería + automatización** para resolver problemas reales de gestión de citas de manera automática.
