# 🤖 AI Business Intelligence Agent

> An AI-powered business analysis agent built with Streamlit that transforms raw data into strategic insights and executive decisions — in seconds.

---

## 📌 Overview

**AI Business Intelligence Agent** is a multi-agent system that accepts CSV, Excel, or PDF files and uses a large language model (via Groq API) to automatically:
- Analyze sales and business data
- Detect anomalies using Z-score statistics
- Generate actionable business insights
- Produce executive-level decisions
- Export a downloadable PDF report

---

## 🚀 Getting Started

### 1️⃣ Install Dependencies

```bash
pip install streamlit pandas matplotlib plotly openai reportlab PyPDF2 openpyxl
```

### 2️⃣ Get Your Groq API Key

1. Go to [https://console.groq.com/](https://console.groq.com/)
2. Sign in or create a free account
3. Click on **API Keys** then **Create API Key**
4. Copy your key

### 3️⃣ Add Your API Key to the Code

Open `App.py` and find this line in **two places**:

```python
api_key=["GROQ_API_KEY"]
```

Replace it with your actual key:

```python
api_key="gsk_xxxxxxxxxxxxxxxx"  # ← Put your Groq API Key here
```

> ⚠️ **Warning:** Do not share your key or push it to GitHub

### 4️⃣ Run the App

```bash
streamlit run App.py
```

---

## 📂 Supported File Types

| Format | Analysis Type |
|---|---|
| `.csv` | Full data analysis + insights + decisions |
| `.xlsx` / `.xls` | Full data analysis + insights + decisions |
| `.pdf` | Document extraction + AI document analysis |

---

## ✨ Features

| Feature | Description |
|---|---|
| 📊 **Data Analysis** | Auto-summarizes CSV/Excel files |
| 🔍 **Anomaly Detection** | Flags unusual data points using Z-score |
| 🧠 **AI Insights** | LLM-generated business insights |
| ✅ **Decision Engine** | Executive-level action recommendations |
| 🗃️ **Memory System** | Remembers last 5 analysis sessions |
| 📄 **PDF Export** | Auto-generated business report |

---

## 🏗️ Architecture

```
User Input (file + query)
        │
        ▼
┌─────────────────┐
│  Planner Agent  │
└────────┬────────┘
         │
   ┌─────▼──────┐    ┌──────────────┐    ┌──────────────────┐
   │ Data Agent │───▶│   Analysis   │───▶│ Anomaly Detector │
   └────────────┘    └──────────────┘    └────────┬─────────┘
                                                  │
                                         ┌────────▼────────┐
                                         │  Insight Agent  │
                                         └────────┬────────┘
                                                  │
                                         ┌────────▼────────┐
                                         │ Decision Agent  │
                                         └────────┬────────┘
                                                  │
                                         ┌────────▼────────┐
                                         │   PDF Report    │
                                         └─────────────────┘
```

---

## 📦 Project Structure

```
ai-business-agent/
│
├── App.py              # Main application
├── memory.db           # Auto-created on first run
└── README.md
```

---

## 🤝 Contributing

Pull requests are welcome!

---
