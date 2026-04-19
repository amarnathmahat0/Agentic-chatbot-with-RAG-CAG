# 🤖 Agentic Chatbot with CAG (Cache-Augmented Generation)

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python&logoColor=white)](https://www.python.org/)
[![Ollama](https://img.shields.io/badge/LLM-Llama%203.2-orange?logo=ollama&logoColor=white)](https://ollama.com/)
[![Framework](https://img.shields.io/badge/Architecture-RAG%20%2F%20CAG-green?style=flat-square)](#-features)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A high-performance, **offline AI assistant** featuring Cache-Augmented Generation (CAG), real-time weather integration, smart route planning, and seamless voice interaction. Built for privacy and speed.

---

## 🌟 Key Features

- **📂 Cache-Augmented Generation (CAG):** Preload PDF, DOCX, or TXT files using KV cache for near-instant document-based Q&A without repeated processing.
- **☁️ Weather Forecasting:** Real-time weather updates and 5-day forecasts via [OpenWeatherMap](https://openweathermap.org/).
- **🗺️ Smart Navigation:** Advanced route planning and distance calculation using [OpenRouteService](https://openrouteservice.org/).
- **🎙️ Voice-Activated Interface:** Hands-free operation with wake-word detection ("Jarvis") and text-to-speech (gTTS).
- **🧠 Local Intelligence:** Fully offline LLM processing using **Llama 3.2:3b** via [Ollama](https://ollama.com/).
- **🎭 Mood Awareness:** Facial emotion detection for a more personalized interaction (via `main.py`).
- **🗄️ Context Retention:** Integration with [Qdrant](https://qdrant.tech/) vector database for long-term memory.

---

## 🛠️ Tech Stack

| Component | Technology |
| :--- | :--- |
| **LLM Engine** | Llama 3.2 (via Ollama) |
| **Backend** | Python, Express (Local Server) |
| **GUI** | Tkinter |
| **Vector DB** | Qdrant |
| **APIs** | OpenWeather, OpenRouteService |
| **NLP** | spaCy (en_core_web_sm) |

---

## ⚙️ Setup & Installation

### 1. Clone & Environment
```bash
git clone [https://github.com/amarnathmahat0/Agentic-chatbot-with-RAG-CAG.git](https://github.com/amarnathmahat0/Agentic-chatbot-with-RAG-CAG.git)
cd Agentic-chatbot-with-RAG-CAG
python -m venv venv
# Activate:
# Windows: venv\Scripts\activate | Mac/Linux: source venv/bin/activate
2. Dependencies
Bash
pip install -r requirements.txt
python -m spacy download en_core_web_sm
3. External Services
Ollama: Install and run ollama pull llama3.2:3b.

Qdrant: Run via Docker: docker run -p 6333:6333 qdrant/qdrant.

API Keys: Rename .env.example to .env and add your keys:

Code snippet
OPENWEATHER_API_KEY=your_key_here
OPENROUTESERVICE_API_KEY=your_key_here
🚀 How to Run
Start the Ollama server: ollama serve

Run the main application:

Bash
python test.py
Using the Bot:

Upload Documents: Use the "Upload (CAG)" button to feed data.

Voice Mode: Click "Enable Voice" and say "Jarvis" to start talking.

Commands: Try "What is the weather in Delhi?" or "Route from Mumbai to Pune."

🔍 Advanced: Inspecting KV Cache
To verify how your documents are stored and optimized in the cache:

Bash
python kv_cache.py
🤝 Contributing
Contributions make the open-source community amazing!

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📜 License
Distributed under the MIT License. See LICENSE for more information.

Developed by Amarnath Mahato
