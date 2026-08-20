<div align="center">

# 👋 Hi there, I'm Himanshu Pandey
### 🚀 Full-Stack Software Engineer & AI Systems Architect

[![GitHub Followers](https://img.shields.io/github/followers/HQHimanshu?label=Followers&logo=github&style=for-the-badge&color=181717)](https://github.com/HQHimanshu?tab=followers)
[![Repositories](https://img.shields.io/badge/Public_Repos-12%2B-6366F1?style=for-the-badge&logo=git&logoColor=white)](https://github.com/HQHimanshu?tab=repositories)
[![Team Hexagon](https://img.shields.io/badge/Hackathon_Squad-Team_Hexagon-FF6B6B?style=for-the-badge&logo=target&logoColor=white)](https://github.com/HQHimanshu)
[![Pronouns](https://img.shields.io/badge/Pronouns-he%2Fhim-8A2BE2?style=for-the-badge)](https://github.com/HQHimanshu)
[![Email](https://img.shields.io/badge/Contact-hhimanshuppandey%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hhimanshuppandey@gmail.com)

<br/>

```text
⚡ Full Stack Web (React, Node.js, Express, FastAPI)
🧠 Autonomous AI Agents & Persistent Memory (Groq LLMs, Breeth MCP, ChromaDB RAG)
🌾 IoT & Edge AI (Arduino, Real-Time Sensors, Multilingual Voice Alerts)
🏆 Hackathon Innovator @ Team Hexagon & Team Terminators
```

</div>

---

## 👨‍💻 About Me

```yaml
Name: Himanshu Pandey
GitHub: @HQHimanshu
Email: hhimanshuppandey@gmail.com
Role: Full-Stack Developer & AI Systems Engineer
Affiliations: 
  - Team Hexagon (Hackathon Innovation Squad)
  - Team Terminators
Core Expertise:
  - Agentic LLM Orchestration & Persistent Context (MCP)
  - Full-Stack Web Development (React 18, Express, FastAPI, Flask)
  - Local AI Inference & RAG Pipelines (Ollama Qwen 2.5, ChromaDB)
  - IoT Smart Systems & Multilingual Alert Pipelines (Arduino, Twilio, gTTS)
```

---

## 🌐 Live Production Deployments & Shipped Apps

<div align="center">

| Project | Live Demo | Repository | Core Stack |
| :--- | :---: | :---: | :--- |
| **Adaptive Interview Agent** | [🔗 **Live App**](https://adaptive-interview-agent.vercel.app/) | [📁 **GitHub**](https://github.com/HQHimanshu/adaptive-interview-agent) | React, Express, Groq LLM, Breeth MCP |
| **Smart Clinic Healthcare** | [🔗 **Live App**](https://smart-clinic-dusky.vercel.app) | [📁 **GitHub**](https://github.com/HQHimanshu/TECHBLITZ2026_TERMINATORS) | Client-Server Architecture, React, Vercel |
| **Komi Social Platform** | [🔗 **Live App**](https://hqhimanshu.github.io/komi-app/) | [📁 **GitHub**](https://github.com/HQHimanshu/komi-app) | Multi-page App, JavaScript, GitHub Pages |

</div>

---

## 🚀 Deep Dive: Star Projects & Technical Architecture

### 1️⃣ 🤖 [Adaptive Interview Agent](https://github.com/HQHimanshu/adaptive-interview-agent)
> **An AI-powered adaptive technical interview platform that turns a candidate's learning journey into a personalized, multi-turn technical interview.**  
> *Built for the **ABTalks Vibe Coding Hackathon** by **Team Hexagon**.*  
> 🔗 **Live Demo**: [https://adaptive-interview-agent.vercel.app/](https://adaptive-interview-agent.vercel.app/)

#### 🎯 Problem & Solution
- **The Problem**: Traditional technical interviews use static, rigid questionnaires that ignore the candidate’s actual background, projects, or dynamic progress.
- **The Solution**: The agent ingests candidate profiles and curriculum datasets (`candidates.json`, `curriculum.json`), dynamically formulating personalized technical questions, generating follow-ups in response to candidate answers, and maintaining memory across the multi-turn session.

#### 🏗️ Architecture & Component Flow
```text
                    React Frontend (Vercel)
                              │
                              │ HTTPS REST API
                              ▼
                    Express Backend (Render)
                              │
                    Interview Controller
                              │
          ┌───────────────────┼───────────────────┐
          ▼                   ▼                   ▼
   Session Manager      Prompt Builder       Data Layer
          │                   │          (candidates/curriculum)
          │                   ▼
          │           Groq LLM Service
          │                   │
          │                   ▼
          │               Groq API
          ▼
      Breeth MCP
  (Persistent Memory)
```

#### 🔄 Multi-Turn Interview Flow
```text
Select Candidate ──▶ Start Session ──▶ Generate Initial Question
                                               │
                                               ▼
Structured Feedback ◀── Final Evaluation ◀── Candidate Answers
       │                                       │
       ▼                                       ▼
Interview Completed ◀──────── (8+ Rounds) ◀── Record & Next Follow-up
```

#### ✨ Key Features
- **Adaptive Multi-Turn Dialogue**: Dynamically assesses answers and pivots questions based on candidate depth.
- **Breeth MCP Integration**: Model Context Protocol client for persistent session memory retrieval and writes.
- **Groq LLM Service**: Ultra-low latency inference for dynamic question generation and real-time evaluation.
- **Structured Final Feedback**: Outputs comprehensive evaluation with `Summary`, `Strengths`, `Knowledge Gaps`, and `Actionable Next Steps`.
- **API Endpoint**: Production REST endpoint `POST /api/interview` supporting session state and streaming evaluations.

---

### 2️⃣ 🌾 [KrishiDrishti (कृषिदृष्टि - "Farm Vision")](https://github.com/HQHimanshu/KrishiDrishti)
> **Complete IoT + Local AI Smart Agriculture System for Indian Farmers**  
> *Smart India Hackathon PS-301 & NeoFuture Hackathon (IEEE)*  
> 📁 **Repository**: [HQHimanshu/KrishiDrishti](https://github.com/HQHimanshu/KrishiDrishti)

```text
┌─────────────────────────────────────────────────────────────────┐
│                    Arduino Hardware + Sensors                   │
│        DHT22 (Temp/Humidity) | Soil Moisture | pH | Rain        │
└────────────────────────────────┬────────────────────────────────┘
                                 │ HTTP / Serial Bridge
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│                      FastAPI Async Backend                      │
│   ┌───────────────┐   ┌────────────────┐   ┌────────────────┐   │
│   │ Sensor Routes │   │ RAG Engine     │   │ Notifications  │   │
│   │ (Realtime)    │   │ (ChromaDB)     │   │ (Twilio/gTTS)  │   │
│   └───────┬───────┘   └────────┬───────┘   └────────┬───────┘   │
│           │                    │                    │           │
│           ▼                    ▼                    ▼           │
│   SQLite Database      Local Ollama LLM     WhatsApp/SMS/Voice  │
│   (Sensor History)     (Qwen 2.5:7b)        (Hindi/Marathi/Eng) │
└────────────────────────────────┬────────────────────────────────┘
                                 │ REST API
                                 ▼
┌─────────────────────────────────────────────────────────────────┐
│              React 18 + Vite PWA (Offline-First)                │
│    Realtime Dashboard  │  AI Farming Chat  │  Resource Analytics │
└─────────────────────────────────────────────────────────────────┘
```

#### ✨ Key Highlights
- **Local AI Inference**: Offline-capable AI advisory using **Ollama + Qwen 2.5:7b** with **ChromaDB RAG**.
- **IoT Sensor Monitoring**: Real-time soil moisture, temperature, pH levels, and rain detection.
- **Multilingual Alerts & Voice**: Automated notifications via **WhatsApp / SMS (Twilio)** and voice output via **gTTS** in **Hindi (हिंदी)**, **Marathi (मराठी)**, and **English**.
- **Offline-First PWA**: Built with Service Workers and local caching for rural environments with unstable connectivity.

---

### 3️⃣ 📄 [ResumeParser & OCR Extractor](https://github.com/HQHimanshu/resume_extracter)
> **Automated Talent Intelligence Pipeline with NLP & Computer Vision**  
> 📁 **Repository**: [HQHimanshu/resume_extracter](https://github.com/HQHimanshu/resume_extracter)

- **Multi-Format Ingestion**: Extracts text from PDF, DOCX, and scanned images (PNG/JPG) using **Tesseract OCR**, **pdfplumber**, and **PyMuPDF**.
- **Structured Schema**: Transforms unstructured resume text into standardized JSON schema (Contact info, Skills, Work History, Education, Certifications).
- **Production Ready**: Full Flask REST API (`POST /api/parse`) with Docker containerization support.

---

### 4️⃣ 🏥 [Smart Clinic](https://github.com/HQHimanshu/TECHBLITZ2026_TERMINATORS) & 💬 [Komi App](https://github.com/HQHimanshu/komi-app)
- **Smart Clinic** ([Live Demo](https://smart-clinic-dusky.vercel.app)): Full-stack medical operations and appointment scheduling system developed during TECHBLITZ 2026.
- **Komi App** ([Live Demo](https://hqhimanshu.github.io/komi-app/)): Real-time interactive communication hub with dashboards, messaging feeds, and custom profile interfaces.

---

## 🛠️ Technical Stack & Tooling

<div align="center">

| Domain | Technologies |
| :--- | :--- |
| **Languages** | ![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![C++](https://img.shields.io/badge/C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white) ![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white) |
| **Frontend** | ![React](https://img.shields.io/badge/React_18-20232A?style=for-the-badge&logo=react&logoColor=61DAFB) ![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white) ![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white) ![Bootstrap](https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white) |
| **Backend** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![Node.js](https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white) ![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge) ![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white) |
| **AI / ML & Agents** | ![Groq](https://img.shields.io/badge/Groq_LLM-F05032?style=for-the-badge) ![Ollama](https://img.shields.io/badge/Ollama_Qwen_2.5-000000?style=for-the-badge&logo=ollama&logoColor=white) ![MCP](https://img.shields.io/badge/Model_Context_Protocol-8A2BE2?style=for-the-badge) ![ChromaDB](https://img.shields.io/badge/ChromaDB_RAG-FC521F?style=for-the-badge) ![Tesseract OCR](https://img.shields.io/badge/Tesseract_OCR-5C93D4?style=for-the-badge) |
| **IoT & Hardware** | ![Arduino](https://img.shields.io/badge/Arduino_Hardware-00979D?style=for-the-badge&logo=arduino&logoColor=white) ![Sensors](https://img.shields.io/badge/DHT22_%7C_pH_%7C_Rain-4CAF50?style=for-the-badge) ![Twilio](https://img.shields.io/badge/Twilio_API-F22F46?style=for-the-badge&logo=twilio&logoColor=white) |
| **Cloud & DevOps** | ![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white) ![Render](https://img.shields.io/badge/Render-46E3B7?style=for-the-badge&logo=render&logoColor=black) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white) ![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white) |

</div>

---

## 🏆 Hackathon Achievements

```text
├── 🥇 ABTalks Vibe Coding Hackathon ────────── Built "Adaptive Interview Agent" (Team Hexagon)
├── 🌾 Smart India Hackathon & IEEE NeoFuture ─ Built "KrishiDrishti" (IoT + Local AI)
├── ⚡ TECHBLITZ 2026 ───────────────────────── Built "Smart Clinic" (Team Terminators)
├── 💬 Team Hexagon Initiatives ────────────── Built "Komi App" (Communication Platform)
└── 🚀 Aerospace Computing ─────────────────── Companion for Python for Aerospace Course
```

---

## 📬 Connect with Himanshu

<div align="center">

[![Email](https://img.shields.io/badge/Email_Me-hhimanshuppandey%40gmail.com-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:hhimanshuppandey@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-HQHimanshu-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/HQHimanshu)
[![Adaptive Interview Agent](https://img.shields.io/badge/Live-Adaptive_Interview_Agent-00C7B7?style=for-the-badge&logo=vercel&logoColor=white)](https://adaptive-interview-agent.vercel.app/)
[![Smart Clinic](https://img.shields.io/badge/Live-Smart_Clinic-0070F3?style=for-the-badge&logo=vercel&logoColor=white)](https://smart-clinic-dusky.vercel.app)
[![Komi App](https://img.shields.io/badge/Live-Komi_App-222222?style=for-the-badge&logo=githubpages&logoColor=white)](https://hqhimanshu.github.io/komi-app/)

</div>
