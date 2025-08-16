
# � Production Deployment Guide: TDS Data Analyst Agent

**Professional deployment guide for deploying the AI-powered Data Analyst Agent to Railway platform.**

[![Railway](https://img.shields.io/badge/Deploy-Railway-blueviolet)](https://railway.app)
[![Docker](https://img.shields.io/badge/Docker-Enabled-blue)](https://docker.com)
[![Production](https://img.shields.io/badge/Production-Ready-green)](https://github.com/Simhadri123/data_analyst)

---

## 📋 Overview

This guide provides step-by-step instructions for deploying the TDS Data Analyst Agent to Railway, a modern platform-as-a-service (PaaS) provider. The deployment includes automated container builds, environment variable management, and production-ready configurations.

### Deployment Features
- ✅ **Automated CI/CD**: Direct GitHub integration with automatic deployments
- ✅ **Container Support**: Docker-based deployment for consistency
- ✅ **Environment Management**: Secure API key and configuration handling
- ✅ **Load Balancing**: Multiple API key support for high availability
- ✅ **Monitoring**: Built-in logging and application monitoring

---

## 📁 Pre-configured Files

The repository includes production-ready configuration files:

| File | Purpose | Description |
|------|---------|-------------|
| `Dockerfile` | Container definition | Multi-stage build optimized for production |
| `Procfile` | Process specification | Defines how Railway starts the application |
| `runtime.txt` | Runtime version | Specifies Python version for deployment |
| `.dockerignore` | Build optimization | Excludes unnecessary files from container |
| `.env.template` | Configuration template | Template for environment variables |

---

## � Pre-deployment Setup

### 1. Environment Configuration

Create a `.env` file in your project root with the following structure:

```env
# Google Gemini API Keys (Production Setup)
# Recommendation: Use multiple keys for load balancing and redundancy
gemini_api_1=your_primary_gemini_api_key
gemini_api_2=your_secondary_gemini_api_key
gemini_api_3=your_tertiary_gemini_api_key
gemini_api_4=your_quaternary_gemini_api_key
gemini_api_5=your_backup_gemini_api_key
gemini_api_6=your_fallback_gemini_api_key
gemini_api_7=your_additional_gemini_api_key
gemini_api_8=your_redundant_gemini_api_key
gemini_api_9=your_extra_gemini_api_key
gemini_api_10=your_final_gemini_api_key

# Application Configuration
LLM_TIMEOUT_SECONDS=240
PORT=8000

# Production Settings (Optional)
DEBUG=false
LOG_LEVEL=INFO
```

> ⚠️ **Security Note**: 
> - Never commit `.env` files to version control
> - Use at least 2 different API keys for redundancy
> - If you only have one key, duplicate it across all variables for compatibility

### 2. Repository Preparation

Ensure your code is committed to GitHub:

```bash
# Initialize repository (if not already done)
git init

# Add all files
git add .

# Commit changes
git commit -m "Initial commit with Railway deployment config"

# Push to GitHub
git remote add origin https://github.com/your-username/your-repo.git
git push -u origin main
```

```bash
cd /path/to/project
git init
git add .
git commit -m "Initial commit with Railway deployment config"
git remote add origin https://github.com/your-username/your-repo.git
git push -u origin main
```

---

## 🚀 **3. Deploy to Railway**

### **Option A – Dashboard**

1. Visit [railway.app](https://railway.app)
2. Sign in with GitHub
3. **New Project → Deploy from GitHub**
4. Select your repo
5. Railway will auto-deploy

### **Option B – CLI**

```bash
npm install -g @railway/cli
railway login
railway init
railway link
railway up
```

---

## 🌍 **4. Add Environment Variables in Railway**

1. Go to your Railway project
2. Click **Variables**
3. Add your Gemini keys & settings exactly as in `.env`

---

## 🧪 **5. Test Locally**

```bash
source venv/bin/activate   # Windows: venv\Scripts\activate
uvicorn app:app --host 0.0.0.0 --port 8000
```

Visit: **[http://localhost:8000](http://localhost:8000)**

---

## 🐳 **6. (Optional) Test with Docker**

```bash
docker build -t tds-data-analyst .
docker run -p 8000:8000 --env-file .env tds-data-analyst
```

---

## ⚙ **Environment Variable Reference**

| Variable                       | Description            | Default          | Required       |
| ------------------------------ | ---------------------- | ---------------- | -------------- |
| `gemini_api_1`......`gemini_api_10` | Google Gemini API keys | —                | ✅ (at least 1 but make copy of it in all variable) |
| `LLM_TIMEOUT_SECONDS`          | LLM Max Time for task  | 240              | ❌              |
| `PORT`                         | App port               | 8000             | ❌              |

---

## 🛠 **Troubleshooting**

**Common Issues**

* `Module not found` → Check `requirements.txt`
* Port conflict → Use Railway’s `PORT` variable in architecture => project=> setting => networking => edit =>select default port (uvicorn)
* API key errors → Ensure keys are correct in Railway Variables
* Build fails → See Railway build logs

**View Logs**

```bash
railway logs
```

---

## 📚 **Helpful Links**

* 📖 [Railway Docs](https://docs.railway.app)
* 🤖 [Google AI Docs](https://ai.google.dev)

---

