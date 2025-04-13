
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
pip install langchain-openai langchain-groq

```

---

### 2. 🔐 API Key Configuration

Create a `.env` file in your project root or add the following keys in Colab secrets:

```
OPENAI_API_KEY=your_openai_key_here
GROQ_API_KEY=your_groq_key_here
```

---


### 4. ▶️ Run the Script

- Use run_test_cases() function to run the script which gives a dictionary ouput for test cases.

- To generate performance report and write it to a file:
    Use generate_performance_report(metrics,fname) function 
    where metrics = 'output from run_test_cases()' and fname = 'File name for report'

- Additionally, use print_results(pmetrics) function to print performance metrics without writing to file.

  Example:

```
  if __name__ == "__main__":
    pmetrics = run_test_cases()
```

```
  generate_performance_report(pmetrics,'llm_performance_comparison2')
```
```
  print_results(pmetrics)
```

---

### 5. 📄 Output

The script prints performance metrics and financial advice per portfolio for each LLM.

Optional: Save results to markdown file .



---

## 📦 Tested With

- Python 3.11+
- LangChain 0.3.23
- OpenAI GPT-4
- Groq LLaMA 3 8B / 70B models

---

## 👨‍💻 Authors

Contributions by: Ashish Palli

---
