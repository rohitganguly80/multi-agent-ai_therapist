SafeSpace – AI Mental Health Therapist

SafeSpace is a multi-agent AI mental health system designed to provide empathetic conversation, mental health guidance, and emergency support. It uses a combination of Groq LLM routing, a specialized MedGemma model, and Twilio for emergency escalation to provide safe, intelligent, and human-like interactions.
Features

Empathetic AI Conversations

Uses the MedGemma model to respond to emotional user inputs in a supportive, therapeutic tone.

Multi-Agent Routing

Groq LLM classifies user messages into:

CASUAL → friendly small talk

EMOTIONAL → MedGemma responses

THERAPIST_LOOKUP → nearby therapist suggestions

Keyword-based emergency override for suicidal or self-harm messages → triggers Twilio call automatically.

Dark-themed professional chat interface with Streamlit.

Memory-aware context

Keeps last 10 messages for continuity

Maintains conversation context under 6000 token limit.

Optional mood selector for better user experience.

Architecture Overview
![WhatsApp Image 2026-02-26 at 1 44 26 AM](https://github.com/user-attachments/assets/8817844a-35df-4544-89f3-a17009b3192d)
Screenshots / Demo

SafeSpace Chat Interface:
<img width="1917" height="865" alt="Screenshot 2026-02-26 005129" src="https://github.com/user-attachments/assets/8b0f7685-1f54-41c0-a0ca-bf604bd7337f" />
<img width="1919" height="865" alt="Screenshot 2026-02-25 181238" src="https://github.com/user-attachments/assets/72a262bf-70e9-4538-859b-ca499c59acb4" />

Twilio Call Log
![WhatsApp Image 2026-02-26 at 2 14 23 AM](https://github.com/user-attachments/assets/221a2b69-ca67-43b4-8a97-2e32b01c7dba)
Note: Twilio calls are triggered only when serious keywords are detected (e.g., “I want to die”). These screenshots demonstrate the system functioning safely.

Requirements

Python 3.14+

Packages (install via pip install -r requirements.txt)

Setup Instructions

Clone the repository

Install dependencies

Configure API keys in config.py:

-GROQ_API_KEY = "your_groq_api_key_here"
-TWILIO_ACCOUNT_SID = "your_twilio_sid"
-TWILIO_AUTH_TOKEN = "your_twilio_auth_token"
-TWILIO_FROM_NUMBER = "+1234567890"
-EMERGENCY_CONTACT = "+919876543210"

Run backend

Run frontend

Open your browser at http://localhost:8501 to start chatting.

Usage

-Type messages in the chat box.

-The system will respond naturally using MedGemma for emotional support.

-Casual greetings are recognized and responded to.

-Serious messages trigger emergency calls via Twilio (safety feature).

-You can ask for local therapist suggestions using natural language.

Safety Notes

-SafeSpace is not a replacement for professional therapy.

-Emergency calls are triggered automatically for serious keywords.

-Keep user data secure; conversations are stored locally by default.

-Always verify emergency handling before deploying publicly.

Future Improvements

-Persistent user history (database storage)

-Sentiment analysis for more nuanced responses

-Quick-reply suggestions for easier interaction

-Real-time typing effect or streaming responses

Dynamic therapist search using free geolocation APIs

License

MIT License – free to use, modify, and distribute.
