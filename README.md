
# 📈 AI-Powered Financial Portfolio Rebalancer

This project is an intelligent assistant that analyzes stock portfolios, detects imbalances, and suggests rebalancing actions using real-time market data. It uses **LangChain agents** with integration of multiple LLMs (OpenAI, Groq with LLaMA models) to dynamically select and run financial tools.

---

## 🚀 Features

- 🔍 Rebalances stock portfolios using an equal-weight strategy
- 📈 Analyzes market trends using S&P 500, NASDAQ, and Dow Jones
- 📊 Fetches real-time stock data using Yahoo Finance
- 🤖 Integrates OpenAI and Groq LLMs via LangChain agents
- 🧠 Compares LLM performance in terms of accuracy, speed, and tool usage

---

## 🧱 Tools Implemented

- `StockPriceLookup`: Fetches current stock price and daily change
- `PortfolioRebalancer`: Suggests buy/sell actions to equalize portfolio weights
- `MarketTrendAnalyzer`: Summarizes weekly trends of major indices and sentiment

---

## 🛠️ Setup Instructions

### 1. ✅ Environment Setup

Ensure you're using Python **3.8 or later**.

Install dependencies:

```bash
pip install langchain langchain-openai langchain-groq langchain-community
pip install pandas requests yfinance python-dotenv
```

If using in **Google Colab**, also install:

```bash
!pip install --upgrade --quiet langchain langchain-openai langchain-groq yfinance
```

---

### 2. 🔐 API Key Configuration

Create a `.env` file in your project root:

```
OPENAI_API_KEY=your_openai_key_here
GROQ_API_KEY=your_groq_key_here
```

> 🔒 **Note:** Never commit `.env` files to GitHub.

---

### 3. ⚙️ File Structure

```
📁 your_project/
├── agai_hw3.py                 # Main script with LangChain agent + tools
├── .env                        # API keys (not tracked by Git)
├── llm_performance_comparison.md  # Generated output/report (optional)
├── README.md                   # This file
```

---

### 4. ▶️ Run the Script

```bash
python agai_hw3.py
```

If using in a notebook:

```python
from agai_hw3 import run_test_cases
run_test_cases()
```

---

### 5. 📄 Output

The script prints performance metrics and financial advice per portfolio for each LLM.

Optional: Save results to markdown:

```python
with open("/content/drive/MyDrive/llm_report.md", "w") as f:
    f.write(formatted_results)
```

---

## 📦 Tested With

- Python 3.11+
- LangChain 0.1.14+
- OpenAI GPT-4
- Groq LLaMA 3 8B / 70B models

---

## 👨‍💻 Authors

Developed for the **Applied Generative AI Assignment 3 (AgAI HW3)**.  
Contributions by: [Your Name]

---

## 📜 License

MIT License (if applicable)
