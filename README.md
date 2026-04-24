# 👋 Hi, I'm Parfait RAKOTOMALALA | Full-Stack Developer & AI Engineer

🎓 **Computer Science Student** at École Nationale d'Informatique (ENI), Madagascar  
💡 **Specialization:** Software Engineering & Databases | AI & Data Governance  
🚀 **Passionate about:** Building intelligent, scalable applications that solve real-world problems

---

## 🔧 Tech Stack

**Languages:**  
![TypeScript](https://img.shields.io/badge/-TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/-SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

**Frontend:**  
![React Native](https://img.shields.io/badge/-React_Native-61DAFB?style=flat&logo=react&logoColor=black)
![React](https://img.shields.io/badge/-React-61DAFB?style=flat&logo=react&logoColor=black)
![Expo](https://img.shields.io/badge/-Expo-000020?style=flat&logo=expo&logoColor=white)

**Backend:**  
![Node.js](https://img.shields.io/badge/-Node.js-339933?style=flat&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/-Express-000000?style=flat&logo=express&logoColor=white)
![Socket.io](https://img.shields.io/badge/-Socket.io-010101?style=flat&logo=socket.io&logoColor=white)

**Database & AI:**  
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?style=flat&logo=postgresql&logoColor=white)
![Supabase](https://img.shields.io/badge/-Supabase-3ECF8E?style=flat&logo=supabase&logoColor=white)
![pgvector](https://img.shields.io/badge/-pgvector-336791?style=flat&logo=postgresql&logoColor=white)
![Groq](https://img.shields.io/badge/-Groq_AI-000000?style=flat&logo=ai&logoColor=white)
![Gemini](https://img.shields.io/badge/-Gemini-4285F4?style=flat&logo=google&logoColor=white)

**DevOps & Tools:**  
![Git](https://img.shields.io/badge/-Git-F05032?style=flat&logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Render](https://img.shields.io/badge/-Render-46E3B7?style=flat&logo=render&logoColor=white)

---

## 🚀 Featured Project: StudyHub

**🎯 Academic Community Platform with AI Assistant**

A mobile-first platform transforming how students share knowledge and learn together, powered by RAG (Retrieval-Augmented Generation) AI.

### 🌟 Key Features:
- 🤖 **Intelligent AI Assistant** using vector search (pgvector) + LLM (Groq/Gemini)
- 💬 **Q&A System** with automatic AI suggestions and community voting
- 📚 **Knowledge Base** with semantic search across 120+ academic documents
- 🎥 **Video Monetization** system with revenue sharing (80/20 model)
- 📊 **Offline Math Solver** with LaTeX rendering
- ⚡ **Real-time Notifications** via WebSocket
- 🔐 **Secure Authentication** with role-based access control

### 🛠️ Tech Highlights:
```typescript
// RAG Pipeline: Embedding → Semantic Search → LLM Generation
const response = await aiService.ask({
  question: userQuery,
  vectorStore: pgvector,    // 384-dim embeddings
  llm: groqAPI,              // Llama 3.3 70B (250+ tokens/s)
  fallback: geminiAPI,       // Auto-failover
  topK: 3                    // Top 3 relevant documents
});
```

### 📊 Performance Metrics:
- ⚡ **Response Time:** 1.8s median (95th percentile: 2.9s)
- 🎯 **AI Accuracy:** 89% relevance score (tested on 100 queries)
- 📈 **Scalability:** Handles 100+ concurrent users
- 🔄 **Uptime:** 99.5% availability with auto-failover

### 🏗️ Architecture:
Mobile (React Native + Expo)
↓ HTTPS/WebSocket
Backend (Express.js + TypeScript)
↓ SQL + Vector Search
Database (PostgreSQL + pgvector)
↓ APIs
External Services (Groq, Gemini, HuggingFace)
