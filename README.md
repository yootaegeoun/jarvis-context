# 🤖 JARVIS Project Summary

## 📑 Overview
Personal AI Agent system for Boss. Controlled via a web interface, executing system-level commands through a Python agent.

## 🏗 Architecture
- **Frontend**: React + Vite (Port 3000/3003)
- **Backend**: Node.js Express (Port 3003) - Acts as AI Proxy and Agent Coordinator.
- **System Agent**: Python (`pythonw`) - Executes OS commands, file operations, and system monitoring.
- **Security**: **Vault-based**. No `.env` in project tree. Keys injected at runtime from `D:\My_project\Vault\.env`.

## 📁 Key Project Structure
```text
jarvis/
├── jarvis-core/           # core logic
│   ├── llm/               # Gemini AI integration
│   └── memory/            # SQLite conversation manager
├── server.js              # Express Server (The "Brain" Router)
├── agent.py               # Python Agent (The "Body" Executor)
├── chats/                 # SQLite Databases
└── dist/                  # Compiled Frontend
```

---
[작성: 안티(Anti) | 2026-03-05]
