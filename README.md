<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=soft&color=0:0a0a0f,100:8B5CF6&height=300&section=header&text=🤖%20AI-Veltrix-App&fontSize=60&fontColor=white&animation=fadeIn&desc=The%20Ultimate%20AI%20Assistant%20%7C%20Groq%20120B%20%2B%20Local%20LLM&descSize=18" width="100%"/>
</div>

<br/>

<div align="center">
  
[![GitHub stars](https://img.shields.io/github/stars/harshiINF/AI-Veltrix-App?style=for-the-badge&logo=github&color=8B5CF6&labelColor=0a0a0f)](https://github.com/harshiINF/AI-Veltrix-App/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/harshiINF/AI-Veltrix-App?style=for-the-badge&logo=github&color=8B5CF6&labelColor=0a0a0f)](https://github.com/harshiINF/AI-Veltrix-App/network)
[![GitHub issues](https://img.shields.io/github/issues/harshiINF/AI-Veltrix-App?style=for-the-badge&logo=github&color=FF6B6B&labelColor=0a0a0f)](https://github.com/harshiINF/AI-Veltrix-App/issues)
[![License](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge&logo=opensourceinitiative&labelColor=0a0a0f)](LICENSE)

[![TypeScript](https://img.shields.io/badge/TypeScript-5.0-3178C6?style=for-the-badge&logo=typescript&logoColor=white&labelColor=0a0a0f)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-20.x-339933?style=for-the-badge&logo=nodedotjs&logoColor=white&labelColor=0a0a0f)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-4.18-000000?style=for-the-badge&logo=express&logoColor=white&labelColor=0a0a0f)](https://expressjs.com/)
[![Groq](https://img.shields.io/badge/Groq-API-FF6B6B?style=for-the-badge&logo=groq&logoColor=white&labelColor=0a0a0f)](https://console.groq.com)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=white&labelColor=0a0a0f)](https://reactjs.org/)
[![Tailwind](https://img.shields.io/badge/Tailwind-3.0-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white&labelColor=0a0a0f)](https://tailwindcss.com/)
[![SQLite](https://img.shields.io/badge/SQLite-3.x-003B57?style=for-the-badge&logo=sqlite&logoColor=white&labelColor=0a0a0f)](https://www.sqlite.org/)

</div>

<br/>

---

## 📋 **Daftar Isi**

<details open>
<summary><b>📑 Klik untuk ekspand (17 bagian utama)</b></summary>

| No | Section | Deskripsi |
|----|---------|-----------|
| 1 | [🚀 Tentang Project](#-tentang-project) | Latar belakang, tujuan, dan filosofi |
| 2 | [✨ Fitur Lengkap](#-fitur-lengkap) | Semua fitur dengan penjelasan detail |
| 3 | [🏗️ Arsitektur Sistem](#️-arsitektur-sistem) | Diagram, data flow, komponen |
| 4 | [🛠️ Technology Stack](#️-technology-stack) | Teknologi yang digunakan dengan versi |
| 5 | [📁 Struktur Project](#-struktur-project) | Tree lengkap dengan penjelasan |
| 6 | [⚙️ Cara Instalasi](#️-cara-instalasi) | Step-by-step dari awal |
| 7 | [🔧 Konfigurasi](#-konfigurasi) | Semua environment variables |
| 8 | [📡 Cara Pakai API](#-cara-pakai-api) | Contoh request response |
| 9 | [🎨 Cara Kerja UI](#-cara-kerja-ui) | Penjelasan komponen frontend |
| 10 | [🧠 Cara Kerja AI](#-cara-kerja-ai) | System prompt, reasoning, fallback |
| 11 | [🗄️ Cara Kerja Database](#️-cara-kerja-database) | Schema, query, memory |
| 12 | [🔄 Cara Fallback Logic](#-cara-fallback-logic) | Auto switch mechanism |
| 13 | [📊 Performance & Benchmark](#-performance--benchmark) | Data kecepatan dan limit |
| 14 | [❌ Cara Handling Error](#-cara-handling-error) | Error types & solutions |
| 15 | [🚀 Cara Deploy](#-cara-deploy) | Production deployment |
| 16 | [🤝 Cara Kontribusi](#-cara-kontribusi) | Guidelines for contributors |
| 17 | [❓ FAQ & Troubleshooting](#-faq--troubleshooting) | Masalah umum dan solusi |

</details>

<br/>

---

## 🚀 **Tentang Project**

### **Latar Belakang**

AI-Veltrix-App adalah asisten AI yang dirancang untuk **high availability** dengan menggabungkan dua model:

1. **Groq GPT-OSS 120B** — Model 120 miliar parameter dengan kemampuan reasoning setara GPT-4
2. **Local LLM 3B** — Backup andalan yang jalan di laptop biasa

### **Filosofi**

> *"Reliability through redundancy — never leave a user waiting."*

Sistem ini memastikan bahwa pengguna **selalu mendapatkan respons**, bahkan ketika Groq API sedang error atau kena rate limit.

### **Masalah yang Dipecahkan**

| Masalah | Solusi AI-Veltrix |
|---------|-------------------|
| Rate limit Groq (30 RPM, 8K TPM) | Auto fallback ke Local LLM |
| Groq API down | Switch otomatis dalam <500ms |
| Token limit 8,192 per response | Split response atau pakai local |
| Tidak ada internet | Local LLM tetap jalan |
| Mahalnya API | Local LLM gratis, Groq juga gratis |

---

## ✨ **Fitur Lengkap**

### **1. 🤖 Dual AI Models**

| Fitur | Groq 120B | Local 3B |
|-------|-----------|----------|
| **Model** | GPT-OSS 120B | Llama 3.2 3B |
| **Parameter** | 120 Miliar | 3 Miliar |
| **Context Window** | 128,000 token | 4,000 token |
| **Reasoning** | Chain of Thought, Tree of Thought | Basic reasoning |
| **Coding** | Full-stack, optimization, review | Simple functions |
| **Web Search** | ✅ Built-in | ✅ Tavily API |
| **Function Calling** | ✅ | ❌ |
| **Kecepatan** | 1.2-2.5s | 3-8s |
| **Biaya** | Gratis | Gratis |

### **2. 🌐 Web Search Integration**

```yaml
Groq:
  method: browser_search (built-in)
  verification: Multi-source
  cost: Free

Local:
  method: Tavily API
  verification: Single source
  cost: 1,000 free/month
```

3. 💾 Memory & Persistence

```sql
-- Data yang disimpan
messages     → Semua percakapan dengan timestamp
sessions     → Setiap sesi chat
users        → Profil dan preferensi
memories     → Pengetahuan jangka panjang
feedbacks    → Koreksi dan rating user
```

4. 🎨 User Interface

Komponen Fitur
Sidebar Collapse, history chat, settings
Chat Area Markdown, code highlight, tabel
Artifact Viewer Preview kode, copy, download
Input Area Auto-resize, send button, action buttons
Dark Mode Bisa toggle

---

🏗️ Arsitektur Sistem

Diagram Arsitektur Lengkap

```
┌─────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                         PRESENTATION LAYER                                      │
│  ┌───────────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                    React + Tailwind CSS                                   │  │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────────────┐  │  │
│  │  │  Sidebar    │ │  ChatArea   │ │   Message   │ │  InputArea  │ │   ArtifactViewer    │  │  │
│  │  │ • Logo      │ │ • Messages  │ │ • User      │ │ • Textarea  │ │ • Code Preview      │  │  │
│  │  │ • New Chat  │ │ • Scroll    │ │ • AI        │ │ • Send      │ │ • Copy Button       │  │  │
│  │  │ • History   │ │ • Auto      │ │ • Markdown  │ │ • Actions   │ │ • Download          │  │  │
│  │  │ • Settings  │ │             │ │ • Code      │ │             │ │                     │  │  │
│  │  └─────────────┘ └─────────────┘ └─────────────┘ └─────────────┘ └─────────────────────┘  │  │
│  └───────────────────────────────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────────────────────────────┘
                                                      │
                                                      ▼
┌─────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                          API GATEWAY                                            │
│  ┌───────────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                              Express.js + TypeScript                                      │  │
│  │  ┌─────────────────────────────────────────────────────────────────────────────────────┐  │  │
│  │  │  POST /api/chat  │  GET /api/health  │  Rate Limiter  │  CORS  │  Request Logger  │  │  │
│  │  └─────────────────────────────────────────────────────────────────────────────────────┘  │  │
│  └───────────────────────────────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────────────────────────────┘
                                                      │
                    ┌─────────────────────────────────┼─────────────────────────────────┐
                    ▼                                 ▼                                 ▼
┌───────────────────────────────────┐ ┌───────────────────────────────────┐ ┌───────────────────────────────────┐
│          GROQ SERVICE             │ │        LOCAL LLM SERVICE          │ │         MEMORY SERVICE            │
│  ┌─────────────────────────────┐  │ │  ┌─────────────────────────────┐  │ │  ┌─────────────────────────────┐  │
│  │ GPT-OSS 120B (120B params)  │  │ │  │ Llama 3.2 3B (3B params)   │  │ │  │ SQLite Database             │  │
│  │ browser_search (built-in)   │  │ │  │ Tavily API                  │  │ │  │ Vector Search               │  │
│  │ Function Calling            │  │ │  │ LM Studio / Ollama          │  │ │  │ Embedding Generation        │  │
│  │ 128K Context                │  │ │  │ 4K Context                  │  │ │  │ Session Management          │  │
│  │ 30 RPM / 8K TPM             │  │ │  │ Unlimited rate              │  │ │  │ User Preferences            │  │
│  └─────────────────────────────┘  │ │  └─────────────────────────────┘  │ │  └─────────────────────────────┘  │
└───────────────────────────────────┘ └───────────────────────────────────┘ └───────────────────────────────────┘
                                                      │
                                                      ▼
┌─────────────────────────────────────────────────────────────────────────────────────────────────┐
│                                          DATA LAYER                                             │
│  ┌───────────────────────────────────────────────────────────────────────────────────────────┐  │
│  │                                         SQLite                                           │  │
│  │  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────┐ ┌─────────────────────┐  │  │
│  │  │  messages   │ │  sessions   │ │    users    │ │  memories   │ │     feedbacks       │  │  │
│  │  │ • id        │ │ • id        │ │ • id        │ │ • id        │ │ • id                │  │  │
│  │  │ • session_id│ │ • user_id   │ │ • name      │ │ • user_id   │ │ • user_id           │  │  │
│  │  │ • role      │ │ • title     │ │ • email     │ │ • type      │ │ • message_id        │  │  │
│  │  │ • content   │ │ • summary   │ │ • prefs     │ │ • content   │ │ • rating            │  │  │
│  │  │ • embedding │ │ • created   │ │ • created   │ │ • embedding │ │ • feedback          │  │  │
│  │  └─────────────┘ └─────────────┘ └─────────────┘ └─────────────┘ └─────────────────────┘  │  │
│  └───────────────────────────────────────────────────────────────────────────────────────────┘  │
└─────────────────────────────────────────────────────────────────────────────────────────────────┘
```

Sequence Diagram: Request Flow

```
┌──────┐     ┌──────┐     ┌──────┐     ┌──────┐     ┌──────┐     ┌──────┐
│Client│     │Gateway│     │ Groq │     │Local │     │  DB  │     │Tavily│
└──┬───┘     └──┬───┘     └──┬───┘     └──┬───┘     └──┬───┘     └──┬───┘
   │            │            │            │            │            │
   │ POST /chat │            │            │            │            │
   │───────────>│            │            │            │            │
   │            │            │            │            │            │
   │            │ Save User Message        │            │            │
   │            │──────────────────────────────────────>│            │
   │            │            │            │            │            │
   │            │ Try Groq   │            │            │            │
   │            │───────────>│            │            │            │
   │            │            │            │            │            │
   │            │ [Success]  │            │            │            │
   │            │<───────────│            │            │            │
   │            │            │            │            │            │
   │            │ [Error/429]│            │            │            │
   │            │───────────>│            │            │            │
   │            │            │            │            │            │
   │            │            │ Retry 3x   │            │            │
   │            │            │ with backoff            │            │
   │            │            │            │            │            │
   │            │            │ Fallback   │            │            │
   │            │────────────────────────>│            │            │
   │            │            │            │            │            │
   │            │            │            │ Web Search │            │
   │            │            │            │ (if needed)│            │
   │            │            │            │────────────────────────>│
   │            │            │            │            │            │
   │            │            │            │ Results    │            │
   │            │            │            │<────────────────────────│
   │            │            │            │            │            │
   │            │            │ Response   │            │            │
   │            │<────────────────────────│            │            │
   │            │            │            │            │            │
   │            │ Save AI Response        │            │            │
   │            │──────────────────────────────────────>│            │
   │            │            │            │            │            │
   │ Response   │            │            │            │            │
   │<───────────│            │            │            │            │
   │            │            │            │            │            │
```

---

🛠️ Technology Stack

Backend

Technology Version Purpose Cara Install
Node.js 20.x Runtime nvm install 20
TypeScript 5.0 Language npm install -g typescript
Express 4.18 Framework npm install express
SQLite 3.x Database npm install better-sqlite3
dotenv 16.x Env vars npm install dotenv
cors 2.8 CORS npm install cors
helmet 7.1 Security npm install helmet
morgan 1.10 Logger npm install morgan

AI/ML

Service Model Cara Setup
Groq GPT-OSS 120B Daftar di console.groq.com, ambil API key
Local LLM Llama 3.2 3B Install Ollama: ollama pull llama3.2:3b
Tavily Web Search Daftar di app.tavily.com, ambil API key

Frontend

Technology Version Cara Install
React 18.2 npm install react react-dom
TypeScript 5.0 npm install -D typescript
Tailwind 3.4 npm install -D tailwindcss
Vite 5.0 npm install -D vite
Lucide React 0.294 npm install lucide-react
Marked 11.0 npm install marked

---

📁 Struktur Project

```
AI-Veltrix-App/
│
├── 📂 src/                                      # Source code utama
│   │
│   ├── 📂 prompts/                              # System prompts (OTAK AI)
│   │   ├── 📄 groqSystemPrompt.ts               # 1.577 baris - Primary AI
│   │   │   ├── Identity & Persona (200 lines)
│   │   │   ├── Reasoning Strategies (150 lines)
│   │   │   ├── Coding Guidelines (150 lines)
│   │   │   ├── Web Search Protocol (100 lines)
│   │   │   ├── Response Formats (200 lines)
│   │   │   ├── Memory Management (150 lines)
│   │   │   ├── Examples (300 lines)
│   │   │   ├── Meta-cognition (150 lines)
│   │   │   └── Safety & Ethics (100 lines)
│   │   └── 📄 localSystemPrompt.ts              # Versi ringan (300 lines)
│   │
│   ├── 📂 services/                             # Business logic
│   │   ├── 📄 groqService.ts                    # Groq API integration
│   │   │   ├── chat()                          # Kirim request ke Groq
│   │   │   ├── withWebSearch()                 # Browser search
│   │   │   └── handleRateLimit()               # Handle 429 error
│   │   ├── 📄 localLLMService.ts                # Local LLM integration
│   │   │   ├── chat()                          # Kirim ke LM Studio/Ollama
│   │   │   ├── withWebSearch()                 # Tavily API
│   │   │   └── simplifyHistory()               # Trim history untuk 4K context
│   │   ├── 📄 llmService.ts                     # Smart fallback routing
│   │   │   ├── chat()                          # Pilih Groq atau Local
│   │   │   ├── fallbackLogic()                 # Auto switch
│   │   │   └── resetFallback()                 # Reset after success
│   │   └── 📄 memoryService.ts                  # Database operations
│   │       ├── saveMessage()                   # Simpan ke SQLite
│   │       ├── getHistory()                    # Ambil percakapan
│   │       ├── saveMemory()                    # Simpan memori jangka panjang
│   │       └── getRelevantMemories()           # Semantic search
│   │
│   ├── 📂 components/                           # React UI components
│   │   ├── 📄 Sidebar.tsx                       # Navigation sidebar
│   │   │   ├── Logo & Brand
│   │   │   ├── NewChatButton
│   │   │   ├── HistoryList
│   │   │   └── SettingsFooter
│   │   ├── 📄 ChatArea.tsx                      # Main chat display
│   │   │   ├── Messages List
│   │   │   ├── Auto-scroll
│   │   │   └── Typing Indicator
│   │   ├── 📄 Message.tsx                       # Individual message
│   │   │   ├── User Message (right align)
│   │   │   ├── AI Message (left align, avatar)
│   │   │   └── Markdown Renderer
│   │   ├── 📄 InputArea.tsx                     # User input
│   │   │   ├── Textarea (auto-resize)
│   │   │   ├── Send Button
│   │   │   └── Action Buttons
│   │   ├── 📄 ArtifactViewer.tsx                # Code preview panel
│   │   │   ├── Code Preview
│   │   │   ├── Syntax Highlighter
│   │   │   └── Copy Button
│   │   └── 📄 TypingIndicator.tsx               # 3 dots animation
│   │
│   ├── 📂 hooks/                                # Custom React hooks
│   │   ├── 📄 useChat.ts                        # Chat state management
│   │   │   ├── messages state
│   │   │   ├── sendMessage()
│   │   │   └── clearMessages()
│   │   ├── 📄 useLocalStorage.ts                # Persistent storage
│   │   │   ├── getItem()
│   │   │   ├── setItem()
│   │   │   └── removeItem()
│   │   └── 📄 useWebSearch.ts                   # Web search toggle
│   │
│   ├── 📂 types/                                # TypeScript definitions
│   │   └── 📄 index.ts                          # All interfaces
│   │       ├── Message
│   │       ├── Session
│   │       ├── User
│   │       ├── Memory
│   │       └── Feedback
│   │
│   ├── 📂 utils/                                # Helper functions
│   │   ├── 📄 logger.ts                         # Logging utility
│   │   ├── 📄 tokenCounter.ts                   # Token estimation
│   │   ├── 📄 rateLimiter.ts                    # Rate limiting logic
│   │   └── 📄 validator.ts                      # Input validation
│   │
│   ├── 📄 db.ts                                 # SQLite database layer
│   │   ├── init()                              # Create tables
│   │   ├── query()                             # Execute query
│   │   └── close()                             # Close connection
│   │
│   ├── 📄 index.ts                              # Express server entry
│   │   ├── Middleware (cors, helmet, logger)
│   │   ├── Routes (POST /api/chat, GET /health)
│   │   └── Error Handler
│   │
│   ├── 📄 App.tsx                               # React root component
│   │   ├── State (sidebar open, artifacts open)
│   │   ├── useEffect (load history)
│   │   └── Render (Sidebar, ChatArea, ArtifactViewer)
│   │
│   └── 📄 main.tsx                              # Frontend entry point
│       ├── ReactDOM.render()
│       └── StrictMode
│
├── 📂 public/                                    # Static assets
│   ├── 📄 favicon.ico
│   └── 📄 robots.txt
│
├── 📄 .env.example                               # Environment template
├── 📄 .gitignore                                 # Git ignore rules
├── 📄 package.json                               # Dependencies and scripts
├── 📄 tsconfig.json                              # TypeScript configuration
├── 📄 vite.config.ts                             # Vite build configuration
├── 📄 tailwind.config.js                         # Tailwind CSS config
└── 📄 README.md                                  # This file
```

---

⚙️ Cara Instalasi

Prerequisites (Wajib)

Requirement Cara Install Check
Node.js 20+ nvm install 20 node --version
npm 9+ Install dengan Node.js npm --version
Git sudo apt install git (Linux) / Download dari git-scm.com git --version
Groq API Key Daftar di console.groq.com -

Step-by-Step Installation

<details>
<summary><b>📦 Klik untuk instruksi lengkap (Windows/Mac/Linux)</b></summary>

Windows

```powershell
# 1. Buka PowerShell atau Command Prompt sebagai Administrator

# 2. Clone repository
git clone https://github.com/harshiINF/AI-Veltrix-App.git
cd AI-Veltrix-App

# 3. Install Node.js (jika belum)
# Download dari https://nodejs.org/ (versi 20.x LTS)
# Install, restart terminal

# 4. Install dependencies
npm install

# 5. Copy .env.example ke .env
copy .env.example .env

# 6. Edit .env dengan notepad
notepad .env
# Ganti GROQ_API_KEY=your_groq_api_key_here dengan key asli

# 7. (Optional) Install Ollama untuk Local LLM
# Download dari https://ollama.com/download/windows
# Install, lalu jalankan:
ollama pull llama3.2:3b
ollama serve

# 8. Start development server
npm run dev

# 9. Buka browser di http://localhost:3005
```

MacOS/Linux (Ubuntu/Debian)

```bash
# 1. Buka terminal

# 2. Clone repository
git clone https://github.com/harshiINF/AI-Veltrix-App.git
cd AI-Veltrix-App

# 3. Install Node.js (pakai nvm)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
source ~/.bashrc
nvm install 20
nvm use 20

# 4. Install dependencies
npm install

# 5. Copy .env.example ke .env
cp .env.example .env

# 6. Edit .env
nano .env
# Ganti GROQ_API_KEY=your_groq_api_key_here dengan key asli
# Ctrl+X, Y, Enter

# 7. (Optional) Install Ollama untuk Local LLM
curl -fsSL https://ollama.com/install.sh | sh
ollama pull llama3.2:3b
ollama serve

# 8. Start development server
npm run dev

# 9. Buka browser di http://localhost:3005
```

</details>

---

🔧 Konfigurasi

Environment Variables (.env)

```env
# ==================== SERVER CONFIGURATION ====================
# Port yang digunakan server
PORT=3005
# Environment: development, production, test
NODE_ENV=development

# ==================== GROQ API CONFIGURATION ====================
# Dapatkan dari https://console.groq.com
GROQ_API_KEY=gsk_your_key_here
GROQ_BASE_URL=https://api.groq.com/openai/v1
GROQ_MODEL=openai/gpt-oss-120b
GROQ_FALLBACK_MODEL=llama-3.3-70b-versatile

# ==================== LOCAL LLM CONFIGURATION ====================
# URL LM Studio / Ollama
LLM_BASE_URL=http://127.0.0.1:1234/v1
# Nama model di LM Studio/Ollama
LLM_MODEL=llama-3.2-3b-instruct
# Enable fallback
LLM_FALLBACK_ENABLED=true

# ==================== WEB SEARCH CONFIGURATION ====================
# Tavily API (optional, untuk local LLM)
TAVILY_API_KEY=tvly_your_key_here

# ==================== MODEL PARAMETERS ====================
# Temperature (0-1): makin rendah makin deterministik
LLM_TEMPERATURE=0.6
# Top P: nucleus sampling
LLM_TOP_P=0.85
# Top K: batasi token
LLM_TOP_K=40
# Repeat penalty: kurangi pengulangan
LLM_REPETITION_PENALTY=1.15
# Max tokens per response
LLM_MAX_TOKENS=6000

# ==================== RATE LIMITING ====================
# Delay antar request (ms)
REQUEST_DELAY_MS=2000
# Maksimal retry
MAX_RETRIES=3
# Base delay untuk exponential backoff
RETRY_BASE_DELAY_MS=1000
# Window untuk rate limiting (ms)
RATE_LIMIT_WINDOW_MS=60000
# Maksimal request per window
RATE_LIMIT_MAX_REQUESTS=25

# ==================== TOKEN MANAGEMENT ====================
# Total token budget per request
MAX_TOTAL_TOKENS=15000
# System prompt token budget
SYSTEM_PROMPT_TOKEN_BUDGET=5000
# History token budget
HISTORY_TOKEN_BUDGET=2000
# Response token budget
RESPONSE_TOKEN_BUDGET=6000

# ==================== LOGGING ====================
# Log level: debug, info, warn, error
LOG_LEVEL=info
```

Cara Mendapatkan API Key

Groq API Key

1. Buka console.groq.com
2. Login dengan akun Google/GitHub
3. Klik "API Keys"
4. Klik "Create API Key"
5. Copy key (format: gsk_xxxxxxxxxxxxxxxx)

Tavily API Key (Optional)

1. Buka app.tavily.com
2. Daftar dengan email
3. Verifikasi email
4. Copy API key dari dashboard

---

📡 Cara Pakai API

Endpoint: POST /api/chat

Request:

```bash
curl -X POST http://localhost:3005/api/chat \
  -H "Content-Type: application/json" \
  -d '{
    "message": "Apa itu AI?",
    "useWebSearch": false,
    "forceLocal": false
  }'
```

Response Success:

```json
{
  "success": true,
  "data": {
    "content": "AI (Artificial Intelligence) adalah kecerdasan buatan...",
    "source": "groq",
    "model": "openai/gpt-oss-120b",
    "latency_ms": 1234,
    "usage": {
      "prompt_tokens": 150,
      "completion_tokens": 200,
      "total_tokens": 350
    }
  }
}
```

Response Rate Limit:

```json
{
  "success": false,
  "error": "Rate limit exceeded. Please wait 60 seconds.",
  "retryAfter": 60
}
```

Endpoint: GET /api/health

```bash
curl http://localhost:3005/api/health
```

Response:

```json
{
  "status": "ok",
  "timestamp": "2025-03-23T10:00:00.000Z",
  "config": {
    "groq_model": "openai/gpt-oss-120b",
    "local_model": "llama-3.2-3b-instruct",
    "environment": "development"
  }
}
```

---

🎨 Cara Kerja UI

Komponen Utama

1. Sidebar (Sidebar.tsx)

```tsx
// Cara kerja sidebar
- useState untuk open/close
- useEffect untuk load history dari localStorage
- map() untuk render history items
- onClick untuk switch session
- onDelete untuk hapus chat
```

2. ChatArea (ChatArea.tsx)

```tsx
// Cara kerja chat area
- useRef untuk scroll container
- useEffect untuk auto-scroll ke bawah
- map() untuk render messages
- conditional rendering untuk typing indicator
```

3. Message (Message.tsx)

```tsx
// Cara kerja message
- conditional class: user vs ai
- Markdown rendering pakai marked.js
- Code highlighting dengan Prism.js
- Copy button untuk code blocks
```

4. InputArea (InputArea.tsx)

```tsx
// Cara kerja input area
- useState untuk input value
- onChange untuk auto-resize height
- onKeyDown untuk Enter key
- onClick untuk send message
```

---

🧠 Cara Kerja AI

1. Groq Service (groqService.ts)

```typescript
// Cara kerja Groq service
1. Terima messages dari user
2. Tambah system prompt (1.577 baris)
3. Tambah browser_search tool jika enabled
4. Kirim request ke Groq API
5. Handle response
6. Return ke fallback logic
```

2. Local LLM Service (localLLMService.ts)

```typescript
// Cara kerja Local LLM service
1. Terima messages dari user
2. Sederhanakan history (max 10 pesan)
3. Tambah system prompt versi ringan
4. Kirim request ke LM Studio/Ollama
5. Jika butuh web search, panggil Tavily
6. Return ke fallback logic
```

3. System Prompt (groqSystemPrompt.ts)

```typescript
// Struktur system prompt (1.577 baris)
- Identity & Persona (200 lines)
- Capabilities (300 lines)
- Rules & Guidelines (400 lines)
- Examples (300 lines)
- Memory System (200 lines)
- Advanced Features (177 lines)
```

---

🗄️ Cara Kerja Database

Schema SQLite

```sql
-- messages table
CREATE TABLE messages (
    id TEXT PRIMARY KEY,
    session_id TEXT,
    role TEXT,
    content TEXT,
    embedding TEXT,
    created_at DATETIME
);

-- sessions table
CREATE TABLE sessions (
    id TEXT PRIMARY KEY,
    user_id TEXT,
    title TEXT,
    summary TEXT,
    created_at DATETIME
);

-- users table
CREATE TABLE users (
    id TEXT PRIMARY KEY,
    name TEXT,
    email TEXT,
    preferences TEXT
);

-- memories table
CREATE TABLE memories (
    id TEXT PRIMARY KEY,
    user_id TEXT,
    type TEXT,
    content TEXT,
    embedding TEXT,
    importance INTEGER
);

-- feedbacks table
CREATE TABLE feedbacks (
    id TEXT PRIMARY KEY,
    user_id TEXT,
    message_id TEXT,
    rating INTEGER,
    feedback_text TEXT
);
```

Query Examples

```typescript
// Simpan pesan
db.prepare(`
  INSERT INTO messages (id, session_id, role, content, created_at)
  VALUES (?, ?, ?, ?, ?)
`).run(id, sessionId, role, content, timestamp);

// Ambil history
db.prepare(`
  SELECT * FROM messages 
  WHERE session_id = ? 
  ORDER BY created_at DESC 
  LIMIT 20
`).all(sessionId);
```

---

🔄 Cara Fallback Logic

Algoritma Fallback

```typescript
// llmService.ts - Fallback logic
class LLMService {
  private consecutiveFailures = 0;
  private maxFailuresBeforeFallback = 2;

  async chat(messages: Message[], options?: ChatOptions) {
    // 1. Jika dipaksa pake local
    if (options?.forceLocal) {
      return await this.localLLM.chat(messages);
    }

    // 2. Jika gagal 2x berturut-turut
    if (this.consecutiveFailures >= this.maxFailuresBeforeFallback) {
      console.log('⚠️ Switching to local LLM due to consecutive failures');
      return await this.localLLM.chat(messages);
    }

    // 3. Coba Groq dulu
    try {
      const result = await this.groq.chat(messages, options);
      this.consecutiveFailures = 0; // Reset counter
      return result;
    } catch (error) {
      this.consecutiveFailures++;
      console.log(`🔄 Fallback triggered: ${error.message}`);
      return await this.localLLM.chat(messages);
    }
  }
}
```

Trigger Conditions

Condition Action
Groq API returns 429 Retry 3x with backoff, then fallback
Groq API returns 5xx Immediate fallback
Network timeout (>30s) Immediate fallback
2+ consecutive failures Force local until reset
forceLocal parameter Bypass Groq entirely

---

📊 Performance & Benchmark

Response Times

Operation Groq (p50) Groq (p99) Local (p50) Local (p99)
Simple Query 800ms 1.2s 1.5s 3s
Complex Reasoning 1.5s 2.5s 4s 8s
Code Generation 1.2s 2s 3s 6s
Web Search 1.8s 3s 2.5s 5s

Rate Limits

Model RPM TPM Reset
Groq GPT-OSS 120B 30 8,000 1 minute
Groq (with fallback) Unlimited Unlimited N/A
Local LLM Unlimited Unlimited N/A

Token Usage

Scenario Input Tokens Output Tokens Total
Simple Question 50-200 100-300 150-500
Code Generation 200-500 500-1,500 700-2,000
Document Analysis 1,000-5,000 500-1,000 1,500-6,000
Complex Reasoning 500-1,500 1,000-3,000 1,500-4,500

---

❌ Cara Handling Error

Error Types

Code Type Description Solution
400 Bad Request Message kosong Pastikan message tidak kosong
429 Rate Limit Terlalu banyak request Kurangi frekuensi, pakai fallback
500 Internal Error Server error Cek logs, restart server
503 Service Unavailable Groq down Auto fallback ke local
ECONNREFUSED Connection Failed Local LLM tidak jalan Start LM Studio/Ollama
ETIMEDOUT Timeout Request terlalu lama Cek koneksi internet

Logging

```typescript
// logger.ts
const log = {
  info: (msg) => console.log(`[INFO] ${new Date().toISOString()} ${msg}`),
  warn: (msg) => console.warn(`[WARN] ${new Date().toISOString()} ${msg}`),
  error: (msg) => console.error(`[ERROR] ${new Date().toISOString()} ${msg}`),
  debug: (msg) => process.env.LOG_LEVEL === 'debug' && console.debug(`[DEBUG] ${msg}`)
};
```

---

🚀 Cara Deploy

Production Build

```bash
# 1. Build TypeScript
npm run build

# 2. Start production server
npm start

# 3. Atau pakai PM2 untuk keep alive
npm install -g pm2
pm2 start dist/index.js --name ai-veltrix
pm2 save
pm2 startup
```

Docker Deployment

```dockerfile
# Dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY . .
EXPOSE 3005
CMD ["npm", "start"]
```

```bash
# Build image
docker build -t ai-veltrix .

# Run container
docker run -p 3005:3005 --env-file .env ai-veltrix
```

Vercel Deployment (Frontend)

```bash
# Install Vercel CLI
npm install -g vercel

# Deploy
vercel
```

---

🤝 Cara Kontribusi

Development Workflow

```bash
# 1. Fork repository
# 2. Clone fork
git clone https://github.com/username/AI-Veltrix-App.git
cd AI-Veltrix-App

# 3. Create branch
git checkout -b feature/amazing-feature

# 4. Make changes
# 5. Run tests
npm run test
npm run lint

# 6. Commit
git commit -m "feat: add amazing feature"

# 7. Push
git push origin feature/amazing-feature

# 8. Open Pull Request
```

Commit Convention

Type Description Example
feat New feature feat: add web search toggle
fix Bug fix fix: rate limit error handling
docs Documentation docs: update README
style Code style style: format code
refactor Refactoring refactor: simplify fallback logic
test Testing test: add unit tests
chore Maintenance chore: update dependencies

---

❓ FAQ & Troubleshooting

Q: Error "GROQ_API_KEY not found"

A: Pastikan file .env ada dan berisi GROQ_API_KEY=gsk_xxx. Copy .env.example ke .env.

Q: Error "Rate limit exceeded"

A: Groq punya limit 30 RPM, 8K TPM. Kurangi frekuensi request atau tunggu 1-2 menit.

Q: Local LLM tidak jalan

A:

1. Install LM Studio atau Ollama
2. Download model llama3.2:3b
3. Start server di port 1234
4. Cek dengan curl http://127.0.0.1:1234/v1/models

Q: Web search tidak jalan

A:

1. Untuk Groq: pastikan useWebSearch: true
2. Untuk Local: daftar Tavily API dan isi TAVILY_API_KEY

Q: Port 3005 sudah dipakai

A: Ganti PORT di .env ke port lain (misal 3006)

Q: Build error TypeScript

A:

```bash
npm run type-check
# Fix errors, then rebuild
npm run build
```

---

📝 License

```
MIT License

Copyright (c) 2025 Tegar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0a0f,100:8B5CF6&height=150&section=footer" width="100%"/>

  <br/>

Built with TypeScript, Node.js, and Groq API


  <br/>

“Reliability through redundancy — never leave a user waiting.”

  <br/>

⭐ Star this repository if you like it! ⭐

</div>
```

---
# 🚀 AI Veltrix

<p align="center">
  <img src="assets/logo.svg" width="150" alt="AI Veltrix Logo">
</p>

**AI Veltrix** is a powerful next-generation AI assistant platform built with a hybrid intelligence model. It seamlessly alternates between high-performance cloud reasoning (via Groq) and private, lightweight local execution (3B parameters) to ensure you always have access to intelligence, even when offline or rate-limited.

---

## 🖥️ UI Preview

![AI Veltrix UI Preview](assets/screenshot.png)

---

## ✨ Key Features

- ☁️ **Hybrid Cloud/Local Intelligence**: Uses `openai/gpt-oss-120b` for complex reasoning and automatically falls back to a 3B Local LLM if the cloud is unavailable.
- 🔍 **Real-time Web Search**: Integrated `browser_search` tool for both cloud and local models to fetch the latest information.
- 📊 **Source Tracking & Latency**: Every response includes metadata showing which model was used, the origin (Cloud/Local), and exact response latency in ms.
- 💾 **Persistent Memory**: Full conversation history stored in a local SQLite database with unique ID tracking.
- 📎 **File Integration**: Support for PDF and text file context injection directly into chat sessions.
- 🎨 **Premium Glassmorphism UI**: A stunning, modern React interface with dark/light modes and floating controls.

---

## 🛠️ Technology Stack

- **Backend**: Node.js, Express, TypeScript, SQLite
- **Frontend**: React 18, Vite, Tailwind CSS, Lucide Icons
- **AI Services**: Groq API, LM Studio / Ollama (Local)

---

## 🚀 Getting Started

### 1. Prerequisites
- Node.js (v18+)
- Local LLM Runner (e.g., LM Studio or Ollama) running on port `1234`

### 2. Installation
```bash
# Clone the repository
git clone https://github.com/harshiINF/AI-Veltrix-App.git
cd AI-Veltrix-App

# Install dependencies for both Backend & Frontend
npm install
cd frontend-claude-app && npm install
```

### 3. Configuration
Copy the `.env.example` file to `.env` and fill in your keys:
```bash
cp .env.example .env
```

### 4. Running the App
```bash
# Start Backend (from root)
npm run dev

# Start Frontend (from /frontend-claude-app)
npm run dev
```

---

## 🔒 Security & Privacy

- **Safe Dotenv**: All API keys are stored in `.env` and strictly ignored by Git.
- **Local Fallback**: Sensitive queries can be forced to run locally using the **Force Local** toggle in the UI.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

---

## 📄 License

MIT License - Copyright (c) 2026 harshiINF

---

<p align="center">
  <i>"Empowering Intelligence, Anywhere, Anytime."</i>
</p>
