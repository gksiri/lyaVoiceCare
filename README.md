# LyaVoiceCare

# Lya VoiceCare – Voice-first Ecosystem for Reminders and Emergencies

Lya VoiceCare is an intelligent voice-powered ecosystem designed to support older adults, individuals with Alzheimer’s, or anyone living alone. It delivers scheduled voice reminders, responds to emergencies through automation, and offers meaningful companionship using natural voice calls.

⚠️ This is a demo project. All data and interactions are fictitious and intended for demonstration purposes only.

---

🧠 What Does It Do?

Lya VoiceCare consists of 3 independent, integrable modules:

✅ 1. Voice Reminders  
Family members can schedule reminders through a Tally form. These are stored in Supabase and automatically trigger a call via Vapi’s API.  
If the user says a keyword like “help” during the call, the system transfers the call to a configured emergency contact.

🔥 2. Emergency Trigger via NFC, Alexa, or Physical Button  
Emergencies can be triggered by:  
- NFC tags (e.g., clothing pin, fridge magnet, bracelet)  
- Alexa voice command  
- Bluetooth physical button (e.g., Flic)  

Once activated, the system places a call to the emergency contact and shares critical info: blood type, allergies, medications, address, doctor contact, and GPS location—retrieved in real time from Supabase.

🧑‍🤝‍🧑 3. Conversational Memory Bot  
A personalized voice assistant that talks about the person’s favorite music, family stories, and memories—ideal for those experiencing cognitive decline. All topics are uploaded by loved ones beforehand.

---

🧰 Tech Stack

| Technology     | Purpose                              |
|----------------|----------------------------------------|
| Supabase       | Store and query medical info & reminders |
| Tally.so       | Collect reminders from family         |
| Make.com       | Automate workflow logic                |
| Vapi.ai        | Execute real-time voice calls          |
| HTML           | Emergency confirmation landing page    |
| Telegram Bot   | Alert emergency contacts               |

---

📁 Project Structure

📁 blueprints/  
├── ADD Supabase.blueprint.json         # Tally form → Supabase insert  
├── Recordatorios.blueprint.json       # Supabase → Vapi call for reminders  
├── Integration Webhooks.blueprint.json # Emergency trigger (NFC/Alexa/Flic)  
📄 index.html                           # Confirmation landing page (Make response)

---

🚀 How It Works (Demo Flow)

1. A family member submits a reminder via Tally  
2. Supabase stores the record. Make detects it and calls Vapi’s API  
3. Vapi makes the voice call with the personalized message  
4. If the person says the keyword, the call is transferred to an emergency contact  
5. Alternatively, the emergency can be triggered directly via NFC, Alexa, or button  
6. The emergency call includes real-time medical info pulled from Supabase  
7. An HTML confirmation page is shown, and a Telegram alert is sent

---

📊 Analytics (Optional Integration)

While not included in this repo, all events can be sent to Elasticsearch + Kibana to monitor:
- Reminders sent
- Emergency triggers
- Call durations
- Keyword frequency
- Module usage

---

❤️ Why It Matters

This project was built for the Vapi Challenge with one goal:

“To step away from screens and build something real that can positively impact lives.”

---

📌 Disclaimer

This is a demonstration only. No real patient data is used. No actual emergency services are contacted.

