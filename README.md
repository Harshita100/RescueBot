# 🚨 Disaster Response RAG: Offline-First, Multilingual, Bluetooth-Enabled

> A **Retrieval-Augmented Generation (RAG)** assistant that delivers life-saving guidance during disasters, **without an internet connection**.

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![RAG](https://img.shields.io/badge/AI-RAG%20%7C%20LLM-purple)
![Offline](https://img.shields.io/badge/Mode-Offline--First-green)
![Bluetooth](https://img.shields.io/badge/Transport-Bluetooth-informational)
![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen)

---

## 📖 Overview

When networks go down, people still need answers. This project pairs a
**server** that continuously ingests real-time crisis data with lightweight
**client devices** that connect over **Bluetooth** to query a **RAG pipeline**.
Responses are grounded in the latest retrieved data, localized to the user's
position, and delivered in their own language.

**Keywords:** `RAG` · `LLM` · `Python` · `Bluetooth` · `Offline-First` ·
`Multilingual NLP` · `Retrieval` · `Real-Time Data` · `Client–Server` ·
`Location-Aware Alerts` · `Disaster Response`

---

## ✨ Key Features

| Feature | Description |
|---|---|
| 📡 **Real-Time Disaster Updates** | The server ingests live crisis data and indexes it for retrieval. |
| 📴 **Offline Accessibility** | Bluetooth pairing lets clients query the model with no network access. |
| 🧭 **Personalized Assistance** | Tailored guidance on first aid, evacuation routes, and emergency contacts. |
| 🌍 **Multilingual Support** | Queries and answers in multiple languages to reach wider audiences. |
| 📍 **Location-Based Alerts** | Localized warnings (e.g., flood alerts) that work even when offline. |

---

## 🏗️ How It Works

```
 ┌──────────────────┐   sync   ┌─────────────────────────┐
 │ Real-time crisis │ ───────▶ │  server.py              │
 │ data sources     │          │  • data ingestion       │
 └──────────────────┘          │  • retrieval index      │
                               │  • RAG / LLM responses  │
                               └───────────┬─────────────┘
                                           │ Bluetooth
                               ┌───────────▼─────────────┐
                               │  client.py              │
                               │  • offline queries      │
                               │  • location-aware       │
                               │    multilingual answers │
                               └─────────────────────────┘
```

1. **Ingest:** the server regularly pulls and stores fresh disaster data.
2. **Retrieve:** relevant context is fetched for each user query.
3. **Generate:** the LLM produces a grounded, localized answer.
4. **Deliver:** the answer reaches the client over Bluetooth, with no internet required.

---

## 🚀 Getting Started

### Prerequisites
- Python 3.9+
- A Bluetooth-capable device for both server and client

### Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/disaster-response-rag.git
cd disaster-response-rag

# Install dependencies
pip install -r requirements.txt
```

### Usage

**1. Start the server** (updates data regularly and stores it for offline access):
```bash
python server.py
```

**2. Start the client** (pairs over Bluetooth and retrieves data on demand):
```bash
python client.py
```

**3. Ask a question**, even with no connectivity. Answers are tailored to your
location and circumstances.

---

## 📂 Project Structure

| File | Purpose |
|---|---|
| `server.py` | Data updates, Bluetooth connections, and RAG model responses |
| `client.py` | User interface for querying the RAG model and receiving offline help |

---

## 🛣️ Roadmap

- [ ] Dashboard (Streamlit / Plotly / Grafana) for alert trends and query volume
- [ ] Slack or Telegram bot interface for coordinators and responders
- [ ] Tool-calling agent that routes queries to first-aid, evacuation, and contact tools
- [ ] MCP-based tool integration for orchestrating multiple data sources/APIs
- [ ] Logging and metrics (Prometheus-style) for monitoring server health

---

## 🤝 Contributing

Contributions are welcome!

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/your-idea`)
3. Commit your changes and open a **pull request** for review

---

## 📄 License

Add your license here (e.g., MIT).
