# ⚖️ Pak Justice AI Assistant

<div align="center">

**A State-of-the-Art RAG-based Legal Bot for Pakistani Criminal Law**

[![GitHub Stars](https://img.shields.io/github/stars/yourusername/pak-justice-ai?style=social)](https://github.com/yourusername/pak-justice-ai)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
[![Node.js](https://img.shields.io/badge/Node.js-16+-green.svg)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18+-61DAFB.svg)](https://reactjs.org/)

</div>

---

## 📖 Overview

**Pak Justice AI Assistant** is a cutting-edge **Retrieval-Augmented Generation (RAG)** platform designed to provide accurate, verified, and real-time legal assistance regarding Pakistani Criminal Law, specifically the **Pakistan Penal Code (PPC)** and the **Code of Criminal Procedure (CrPC)**.

The system leverages a modern **three-tier architecture** to deliver:
- ⚡ High-speed legal document retrieval
- 🔍 Hybrid search capabilities (BM25 + Vector Embeddings)
- 🌐 Intelligent web-fallback mechanism for comprehensive answers

---

## 🚀 Key Features

### 🔎 Hybrid Retrieval System
Combines semantic vector search (Cosine Similarity) with traditional keyword matching (BM25) for **98% accuracy**.

### 🤖 Legal AI Chatbot
Powered by **Llama-3.1-8b-instant** for reasoning and **gemini-embedding-001** for high-dimensional vector embeddings.

### 🌐 Web Fallback Mechanism
Integrated with **Serper API** to fetch real-time legal data when local database lacks relevant matches.

### 🛡️ Administrative Dashboard
Secure **React-based portal** for admins to manage legal blogs and document uploads.

### 💾 Dual-Database Architecture
Uses **MongoDB** for web/admin data and **ChromaDB** for efficient vector storage.

### ✅ Security & Validation
Custom Python-based query validator to filter out-of-scope or inappropriate prompts.

---

## 🏗️ System Architecture

The project is built using a decoupled **Three-Tier Architecture**:

| Layer | Technology | Purpose |
|-------|-----------|---------|
| **Frontend** | React.js (Vite + Tailwind CSS) | User Interface & Interaction |
| **Web Backend** | Node.js + Express | Admin Panel & Blog Management |
| **AI Engine** | Python FastAPI | RAG Pipeline & LLM Processing |

---

## 🛠️ Tech Stack

### Frontend
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)

### Backend
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

### AI/ML
![LangChain](https://img.shields.io/badge/LangChain-121212?style=for-the-badge&logo=chainlink&logoColor=white)
![Llama](https://img.shields.io/badge/Llama_3.1-0467DF?style=for-the-badge&logo=meta&logoColor=white)
![Google Gemini](https://img.shields.io/badge/Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)

### Databases
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6B6B?style=for-the-badge&logo=database&logoColor=white)

---

## 📋 Prerequisites

Before running the project, ensure you have:

- ✅ **Node.js** (v16 or higher)
- ✅ **Python** (v3.10 or higher)
- ✅ **MongoDB** (Local or Atlas)
- ✅ **Git**
- ✅ API Keys for Gemini, Llama (Groq), and Serper

---

## 💻 Installation & Setup

### 1️⃣ Clone the Repository

bash
git clone [https://github.com/yourusername/pak-justice-ai.git](https://github.com/yourusername/pak-justice-ai.git)
cd pak-justice-ai

2️⃣ Environment Configuration
Create .env files in both server and chatbot folders:

📁 server/.env
MONGO_URI=your_mongodb_uri
PORT=5000
NODE_ENV=development
📁 chatbot/.env
GEMINI_API_KEY=your_gemini_key
LLAMA_API_KEY=your_llama_key
SERPER_API_KEY=your_serper_key
CHROMA_DB_PATH=./chroma_db
🏃 How to Run the Project
Note: You need three separate terminals running simultaneously for the complete system to work.

🖥️ Terminal 1: MongoDB Web Server (Node.js)
This server manages the admin panel, authentication, and blog posts.
cd server
npm install
npm run dev
✅ Status: Manages admin panel, authentication, and blog posts

🤖 Terminal 2: Chatbot AI Engine (FastAPI)
This engine handles the RAG logic, embeddings, and LLM responses.
cd chatbot

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Start AI engine
python main.py
✅ Status: Handles RAG logic, embeddings, and LLM responses

🌐 Terminal 3: Frontend (React.js)
This is the main user interface
cd frontend
npm install
npm run dev
✅ Status: User interface accessible at http://localhost:5173

📊 Performance Metrics
Metric,Value
🎯 Accuracy,98% (at 0.27 similarity threshold)
⚡ Avg. Latency (Local),3.5s
🌐 Avg. Latency (Web Fallback),7.8s
📚 Vectorized Chunks,"3,237 legal segments"
🔍 Search Methods,Hybrid (BM25 + Cosine)
📸 Screenshots
🏠 Home Page

💬 Chat Interface

🛡️ Admin Dashboard

(Add your image links here)

🗂️ Project Structure
pak-justice-ai/
├── 📁 frontend/          # React.js application
│   ├── src/
│   ├── public/
│   └── package.json
├── 📁 server/            # Node.js backend
│   ├── routes/
│   ├── models/
│   └── package.json
├── 📁 chatbot/           # Python FastAPI engine
│   ├── main.py
│   ├── rag_pipeline.py
│   └── requirements.txt
└── README.md
👨‍💻 Developer
Muhammad Mahad Computer Science Student | KFUEIT

📜 License
This project is developed for academic purposes as a Final Year Project (FYP).
🙏 Acknowledgments
KFUEIT for academic support

LangChain for RAG framework

Google Gemini and Meta Llama for AI models

Serper API for web search integration
