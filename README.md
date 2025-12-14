# 🌦️ Weather-Aware Trail Recommendation AI Agent (n8n)

An autonomous AI agent built using **n8n** that recommends the best walking trail in **New Delhi** based on **real-time weather conditions**, schedules the walk, and sends a personalized email — fully automated.

---

## 🚀 Overview

This project demonstrates how to build a **production-ready AI agent** using workflow automation and LLM reasoning.

Once activated, the workflow:
1. Fetches current weather data
2. Reads trail information from Google Sheets
3. Uses an AI agent (Google Gemini) to select the best trail
4. Creates a Google Calendar event
5. Sends an email recommendation via Gmail

No manual intervention is required after setup.

---

## 🧠 AI Decision Logic

The AI agent evaluates trails using the following rules:

- Prefer **shady trails** on hot days
- Avoid **exposed trails** during high temperatures
- Choose **shorter routes** during rain
- Limit duration to under **2 hours on weekdays**
- Minimize elevation gain on extreme heat days

The agent always selects **exactly one** trail per run.

---

## 🛠️ Tech Stack

- **n8n** – Workflow automation
- **Google Gemini Chat Model** – AI reasoning
- **OpenWeatherMap API** – Weather data
- **Google Sheets API** – Trail dataset
- **Google Calendar API** – Event scheduling
- **Gmail API** – Email notifications

---

## 🔄 Workflow Architecture

Schedule Trigger  
↓  
AI Agent (Google Gemini)  
├── OpenWeatherMap → Fetch current weather  
├── Google Sheets → Read trail dataset  
├── Google Calendar → Create walk event  
└── Gmail → Send recommendation email  
