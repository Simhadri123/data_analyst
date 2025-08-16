# Data Analyst Agent

An **enterprise-grade AI-powered data analysis platform** built with **FastAPI, LangChain, and Google Generative AI (Gemini)**. Designed for **TDS Project 2**, it enables automated insights, visualization, and reporting with an intuitive web interface.

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)](https://fastapi.tiangolo.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## 🚀 Key Features

- 🤖 **AI-Powered Analysis** – Uses Google Gemini API for natural language data interpretation  
- 📊 **Advanced Visualizations** – Publication-ready charts via Matplotlib & Seaborn  
- 🌐 **Web Scraping** – Fetches and analyzes real-time data  
- 📈 **Multi-Format Support** – Works with CSV, Excel, JSON, Parquet & TXT  
- ⚡ **Batch Processing** – Handle multiple queries in one go  
- 🔒 **Secure by Design** – Local data processing & secure API key management  

---

## 📦 Quick Start

### Prerequisites
- Python **3.8+**
- Google Cloud account (for Gemini API)
- Git

### Installation

```bash
# Clone repository
git clone https://github.com/Simhadri123/data_analyst.git
cd data_analyst/Data_Analyst/TDS-project-2-Sameer

# Create virtual environment
python -m venv venv
source venv/bin/activate   # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Configure environment
cp .env.template .env
# Edit .env with your API keys

# Start server
uvicorn app:app --reload --host 0.0.0.0 --port 8000
````

Visit: [http://localhost:8000](http://localhost:8000) 🎉

---

## 💡 Usage

### Example Queries (`questions.txt`)

```
What is the correlation between sales and marketing spend?
Show the top 5 products by revenue.
Plot a time series of monthly growth.
```

Supports:

* 📈 Statistical Analysis → regression, correlations
* 🔮 Forecasting → predict sales, growth trends
* 🛠 Data Quality → detect outliers, anomalies

---

## 🛠 Architecture

### Backend

| Component       | Technology                    |
| --------------- | ----------------------------- |
| API Framework   | FastAPI                       |
| AI Engine       | Google Generative AI (Gemini) |
| Orchestration   | LangChain                     |
| Data Processing | Pandas, NumPy                 |
| Visualization   | Matplotlib, Seaborn           |
| Graph Analysis  | NetworkX                      |

### Frontend

* HTML5, CSS, JavaScript
* Bootstrap components
* Interactive real-time updates

---

## 📊 Supported File Formats

| Format  | Extensions      |
| ------- | --------------- |
| CSV     | `.csv`          |
| Excel   | `.xlsx`, `.xls` |
| JSON    | `.json`         |
| Parquet | `.parquet`      |
| Text    | `.txt`          |

---

## 🔧 Configuration

### Environment Variables

```env
# Google Gemini API Keys (supports multiple keys for load balancing)
gemini_api_1=your_primary_key
gemini_api_2=your_secondary_key
# ... up to gemini_api_10

# App Settings
LLM_TIMEOUT_SECONDS=240
PORT=8000
```

Security:

* ✅ Data stays local
* ✅ API keys stored securely
* ✅ Configurable CORS for production

---

## 🚀 Deployment

### Local

```bash
uvicorn app:app --reload --host 0.0.0.0 --port 8000
```

### Docker

```bash
docker build -t tds-data-analyst .
docker run -p 8000:8000 --env-file .env tds-data-analyst
```

### Production

See [DEPLOYMENT\_GUIDE.md](DEPLOYMENT_GUIDE.md)

---

## 📂 Project Structure

```
├── app.py               # FastAPI app
├── requirements.txt      # Dependencies
├── Dockerfile            # Container setup
├── entrypoint.sh         # Docker entry script
├── index.html            # Frontend
├── .env.template         # Env template
└── DEPLOYMENT_GUIDE.md   # Deployment instructions
```

---

## 📈 Performance & Scalability

* ⚡ Async processing with FastAPI
* 🔑 API key load balancing
* 🗄️ Caching for repeated queries
* 🧠 Optimized memory use for large datasets

---

## 🔍 Troubleshooting

* **API Key Errors** → check `.env`
* **Memory Issues** → reduce dataset or increase system resources
* **Port in Use** → change `PORT` in `.env` or Docker run
* **Timeouts** → raise `LLM_TIMEOUT_SECONDS`

Logs:

```bash
docker logs <container_id>
```

Health check:

```bash
curl http://localhost:8000/summary
```

---

## 🤝 Contributing

1. Fork repo
2. Create a feature branch
3. Commit changes + add tests
4. Open a PR

---

## 📜 License

MIT License – see [LICENSE](LICENSE)

---



Do you want me to also **add shields.io badges** for things like Docker, Pandas, NumPy, Seaborn, etc., to make it look even more polished?
```
