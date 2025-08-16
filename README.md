# 🔬 TDS Proje### Key Capabilities
- 🤖 **AI-Powered Analysis**: Leverages Google's Gemini API for intelligent data interpretation
- 📊 **Advanced Visualizations**: Creates publication-ready charts using Matplotlib and Seaborn
- 🌐 **Web Scraping**: Fetches real-time data from external sources
- 📈 **Multi-Format Support**: Handles CSV, Excel, JSON, Parquet, and text files
- ⚡ **Batch Processing**: Executes multiple analytical queries simultaneously
- 🔒 **Enterprise Security**: Implements secure API key management and local data processing

---

## 🚀 Quick Start Guide

### Prerequisites
- Python 3.8 or higher
- Google Cloud Platform account (for Gemini API)
- Git (for version control)

### Installation Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/Simhadri123/data_analyst.git
   cd data_analyst/Data_Analyst/TDS-project-2-Sameer
   ```

2. **Create Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables**
   ```bash
   cp .env.template .env
   # Edit .env file with your API keys
   ```

5. **Launch Application**
   ```bash
   uvicorn app:app --reload --host 0.0.0.0 --port 8000
   ```

6. **Access the Interface**
   Open [http://localhost:8000](http://localhost:8000) in your browser

---

## 💡 Usage Examples

### Basic Data Analysis
Create a `questions.txt` file with queries like:
```
What is the correlation between sales and marketing spend?
Show me the top 5 performing products by revenue.
Create a time series plot of monthly growth.
```

### Advanced Queries
- **Statistical Analysis**: "Perform regression analysis on customer data"
- **Predictive Modeling**: "Forecast next quarter's sales based on trends"
- **Data Validation**: "Identify outliers and data quality issues"

---

## 🏗️ API Documentation

| Method | Endpoint | Description | Parameters |
|--------|----------|-------------|------------|
| `GET` | `/` | Main web interface | None |
| `POST` | `/api` | Submit analysis request | `file`, `questions` |
| `GET` | `/summary` | Application health check | None |

---

## 📊 Supported File Formats

| Format | Extensions | Description |
|--------|------------|-------------|
| **CSV** | `.csv` | Comma-separated values |
| **Excel** | `.xlsx`, `.xls` | Microsoft Excel files |
| **JSON** | `.json` | JavaScript Object Notation |
| **Parquet** | `.parquet` | Columnar storage format |
| **Text** | `.txt` | Plain text files |

---

## 🔧 Configuration

### Environment Variables
```env
# Google Gemini API Keys (multiple for load balancing)
gemini_api_1=your_primary_key
gemini_api_2=your_secondary_key
# ... up to gemini_api_10

# Application Settings
LLM_TIMEOUT_SECONDS=240
PORT=8000
```

### Security Configuration
- All data processing occurs locally
- API keys stored securely in environment variables
- CORS policies configurable for production deployment

---

## 🚀 Deployment Options

### Local Development
```bash
uvicorn app:app --reload --host 0.0.0.0 --port 8000
```

### Docker Deployment
```bash
docker build -t tds-data-analyst .
docker run -p 8000:8000 --env-file .env tds-data-analyst
```

### Production Deployment
See [DEPLOYMENT_GUIDE.md](./DEPLOYMENT_GUIDE.md) for detailed Railway deployment instructions.

---

## 🛠️ Development

### Project Structure
```
├── app.py                 # Main FastAPI application
├── requirements.txt       # Python dependencies
├── Dockerfile            # Container configuration
├── entrypoint.sh         # Docker entrypoint script
├── index.html           # Frontend interface
├── .env.template        # Environment variable template
└── DEPLOYMENT_GUIDE.md  # Deployment instructions
```

### Contributing
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

---

## 📈 Performance & Scalability

- **Async Processing**: FastAPI ensures high concurrency
- **Load Balancing**: Multiple API keys for rate limit distribution
- **Caching**: Intelligent caching of analysis results
- **Resource Management**: Optimized memory usage for large datasets

---

## 🔍 Troubleshooting

### Common Issues
- **API Key Errors**: Verify Gemini API keys in `.env` file
- **Memory Issues**: Reduce dataset size or increase system memory
- **Timeout Errors**: Adjust `LLM_TIMEOUT_SECONDS` value
- **Port Conflicts**: Change port in Docker run command

### Debugging
```bash
# View application logs
docker logs <container_id>

# Check API health
curl http://localhost:8000/summary
```

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **TDS Course Team** for project requirements and guidance
- **Google AI** for Gemini API access
- **LangChain** for LLM orchestration framework
- **FastAPI** for excellent web framework

---

## 📞 Support & Contact

- **Issues**: [GitHub Issues](https://github.com/Simhadri123/data_analyst/issues)
- **Documentation**: [Project Wiki](https://github.com/Simhadri123/data_analyst/wiki)
- **Author**: Sameer Simhadri

---

*Built with ❤️ for TDS Project 2*

---

## 🏗️ Architecture & Technology Stack

### Backend Infrastructure
| Component | Technology | Purpose |
|-----------|------------|---------|
| **Web Framework** | FastAPI | High-performance async API server |
| **AI Engine** | Google Generative AI (Gemini) | Natural language processing and insights |
| **Orchestration** | LangChain | LLM workflow management |
| **Data Processing** | Pandas, NumPy | Data manipulation and analysis |
| **Visualization** | Matplotlib, Seaborn | Statistical plotting and charts |
| **Network Analysis** | NetworkX | Graph-based data relationships |

### Frontend & Interface
- **HTML5/CSS3/JavaScript**: Modern responsive web interface
- **Bootstrap Components**: Professional UI elements
- **Real-time Updates**: Dynamic content renderingligent Data Analyst Agent

**An enterprise-grade AI-powered data analysis platform built with FastAPI, LangChain, and Google's Generative AI.**

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-green.svg)](https://fastapi.tiangolo.com)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 🎯 Project Overview

The **TDS Data Analyst Agent** is a sophisticated AI-driven platform that automates complex data analysis workflows. Built for the TDS (Tools in Data Science) Project 2, it combines cutting-edge machine learning with intuitive web interfaces to deliver professional-grade insights.

### Key Capabilities
- 🤖 **AI-Powered Analysis**: Leverages Google's Gemini API for intelligent data interpretation
- 📊 **Advanced Visualizations**: Creates publication-ready charts using Matplotlib and Seaborn
- 🌐 **Web Scraping**: Fetches real-time data from external sources
- 📈 **Multi-Format Support**: Handles CSV, Excel, JSON, Parquet, and text files
- ⚡ **Batch Processing**: Executes multiple analytical queries simultaneously
- � **Enterprise Security**: Implements secure API key management and local data processing  

---

## ✨ Key Highlights  

| Feature                  | Why It’s Awesome 🚀 |
|---------------------------|----------------------|
| 🤖 AI-Powered Insights    | Uses Google’s Generative AI to “understand” your data |
| 📊 Rich Visualizations    | Generates plots with **Seaborn & Matplotlib** |
| 🌍 Web Scraper Mode       | Fetch live data directly from URLs |
| 📂 Multi-Format Friendly  | Accepts CSV, Excel, JSON, Parquet, or TXT |
| 🔄 Ask Many at Once       | Batch processing for multiple questions |
| 🖥️ Simple-to-Use Interface | Beginner friendly, no steep learning curve |
| ⚡ Super-Fast Execution   | Optimized for speed + real-time feedback |

---

## 🚀 Getting Started  

### 1️⃣ Clone the Repo  - git clone https://github.com/your-username/data-analyst-agent.git
cd data-analyst-agent

### 2️⃣ Install Requirements  - pip install -r requirements.txt

### 3️⃣ Configure API Keys  
Create a `.env` file inside the root folder:  
GEMINI_API_KEY=your_google_api_key
LLM_TIMEOUT_SECONDS=240


### 4️⃣ Start the Application  - python -m uvicorn app:app --reload

Now open [**http://localhost:8000/**](http://localhost:8000/) in your browser 🌐  

## 🧑‍💻 How It Works  

1. **Write Your Questions**  
   Create a `.txt` file with queries like:  What’s the revenue growth month-over-month?, Find correlation between Age and Income, Show most profitable products...etc

2. **Upload Dataset + Questions File**  
- Dataset (optional) → CSV, Excel, JSON, Parquet, or TXT  
- Questions file (required) → Plain text  

3. **Voilà!**  
- AI processes the queries  
- Generates insights + summaries  
- Builds neat visualizations  

---

## 🛠 Tech Behind the Scenes  

### Backend  
- FastAPI ⚡ → High-performance web server  
- LangChain 🧠 → Orchestrates LLM interactions  
- Google Generative AI ✨ → Core AI engine  
- Pandas + NumPy 📊 → Data wrangling made smooth  
- Seaborn + Matplotlib 🎨 → Clean, insightful charts  

### Frontend  
- HTML5 + CSS + JavaScript  
- Bootstrap-inspired modern UI  

---

## 🔧 API Blueprint  

| Method | Endpoint  | Purpose |
|--------|-----------|----------|
| `GET`  | `/`       | Access web app |
| `POST` | `/api`    | Submit dataset + questions |
| `GET`  | `/summary`| App diagnostics & summaries |

---

## 📂 File Support  

| Format | Extensions |
|--------|------------|
| CSV    | `.csv`     |
| Excel  | `.xlsx`, `.xls` |
| JSON   | `.json`    |
| Parquet| `.parquet` |
| Text   | `.txt`     |

---

## 🎯 Where Can You Use This?  

- 📈 Business Strategy – Sales, KPIs, forecasts  
- 🔬 Research – Data exploration, hypothesis validation  
- 🤖 Data Science – Quick EDA, anomaly detection  
- 📊 Reporting – Automated dashboards  

---

## 🔒 Security First  
- ✅ No cloud storage → All data stays local  
- ✅ API keys kept safe via `.env`  
- ✅ Configurable CORS policy for production use  

---

## 📜 License  

Licensed under **MIT** – free for personal & commercial use. 





  
