<div align="center">

# ⚙️ VidyarthiCompanion — Backend (Production)

### Express 5 REST API — Cloud Deployment Build

[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-5-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB Atlas](https://img.shields.io/badge/MongoDB_Atlas-Cloud-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/atlas)
[![Gemini AI](https://img.shields.io/badge/Gemini_AI-2.5_Flash-4285F4?logo=google&logoColor=white)](https://ai.google.dev/)

</div>

---

## 📖 Overview

This is the **production-ready** variant of the VidyarthiCompanion backend, configured to connect to **MongoDB Atlas** (cloud database). The codebase is identical to VidyarthiCompanion-backend — the only difference is the environment configuration with a cloud MongoDB connection string.

> For comprehensive documentation on the project architecture, modules, API reference, shared models, and core services, refer to the **VidyarthiCompanion-backend README**.

---

## 🚀 Getting Started

```bash
# Navigate to this directory
cd github-backend

# Install dependencies
npm install

# Create your environment file (copy from example or create manually)
# Edit .env with your MongoDB Atlas URI and Gemini API key

# Start the development server (with hot-reload)
npm run dev
```

The API will be running at **http://localhost:5000**.

### Verify It's Running

```bash
curl http://localhost:5000/
# → { "status": "CampusOS API is running normally." }
```

---

## 🔐 Environment Variables

Create a `.env` file in the project root:

```env
MONGO_URI=mongodb+srv://<username>:<password>@<cluster>.mongodb.net/<database>
PORT=5000
GEMINI_API_KEY=your_gemini_api_key_here
```

| Variable | Required | Description |
|----------|----------|-------------|
| `MONGO_URI` | ✅ | MongoDB Atlas connection string (cloud) |
| `PORT` | ❌ | Server port (defaults to `5000`) |
| `GEMINI_API_KEY` | ✅ | Google Gemini API key for AI/OCR features |

> **⚠️ Security Note:** Never commit your `.env` file. The `.gitignore` is pre-configured to exclude it.

---

## 📜 Scripts

| Command | Description |
|---------|-------------|
| `npm run dev` | Start server with nodemon (hot-reload on file changes) |
| `npm start` | Start server in production mode |
| `npm test` | *(placeholder)* — Run tests |

---

## 🧪 Testing Bedrock Integration

```bash
# Activate and verify Bedrock model access
node activate-model.js

# Run a smoke test against Bedrock
node test-bedrock.js
```

---

## 🔗 Related

- **Root README** — Full project overview and architecture
- **VidyarthiCompanion-backend README** — Detailed backend documentation (identical codebase)
- **github-frontend README** — Production frontend

---

<div align="center">

**Part of the VidyarthiCompanion Campus OS**

*Built by Team QuantYap for HackOn with Amazon 2026*

</div>
