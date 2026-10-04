#  FinanceAI — Personal Finance Assistant

<p align="center">
  <strong>Improved AI-powered Personal Finance Assistant — AI DataYard GenAI Bootcamp</strong>
</p>

<p align="center">
  Built with <b>Google Gemini 1.5 Flash</b> · <b>LangChain Agents</b> · <b>Streamlit</b> · <b>Plotly</b>
</p>

---

##  What's Improved Over the Original

| Feature | Original | FinanceAI (This Project) |
|---|---|---|
| AI Model | AWS Bedrock (Nova Lite) | Google Gemini 1.5 Flash (free tier) |
| LangChain Tools | 5 tools | **8 tools** |
| Budget Categories | 4 | **6** (+ health, utilities) |
| Currencies | 4 | **8** (+ AED, SAR, CAD, AUD) |
| Charts |  None | ** Donut, Bar, Gauge (Plotly)** |
| Dashboard Tab |  | ** Full financial dashboard** |
| Expense History |  | ** Persistent session log** |
| KPI Stat Cards |  | ** 4 live KPI cards** |
| Quick Prompts |  | ** 7 one-click prompts** |
| New Tools | — | **EMI Calculator, Spending Analysis** |
| Typography | Browser default | **Space Grotesk + Inter (Google Fonts)** |
| Theme | Basic Streamlit | **Custom dark glassmorphism** |
| Sidebar | Simple | **Live progress bars per category** |

---

##  Features

| Tool | Description |
|---|---|
|  `log_expense` | Log an expense with amount, category & description |
|  `get_budget_status` | Check budget for a single category |
|  `get_all_budget_summary` | Full overview of all 6 categories |
|  `convert_currency` | Convert between 8 currencies |
|  `calculate_savings_goal` | Project time to reach a savings target |
|  `get_financial_tips` | Personalised tips by topic |
|  `analyze_spending_pattern` | Detect overspending across categories |
|  `calculate_loan_emi` | Monthly EMI calculation with full breakdown |

---

##  Setup & Installation

### 1. Clone / Download this project

```bash
cd "c:\Users\Hammad\Desktop\ai datayard genai"
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Get a Google Gemini API Key

1. Visit [https://aistudio.google.com/app/apikey](https://aistudio.google.com/app/apikey)
2. Create a **free** API key
3. Copy it

### 4. Set your API key (choose one method)

**Option A — .env file (recommended)**
```bash
cp .env.example .env
# Edit .env and paste your key:
# GOOGLE_API_KEY=AIza...
```

**Option B — Streamlit Secrets (for deployment)**
Create `.streamlit/secrets.toml`:
```toml
GOOGLE_API_KEY = "AIza..."
```

**Option C — Enter in the sidebar**
Just run the app and paste the key in the sidebar.

### 5. Run the app

```bash
streamlit run app.py
```

---

##  Example Queries

```text
I spent PKR 3,500 on groceries today
What is my entertainment budget remaining?
Convert 200 USD to AED
How long to save PKR 1,000,000 if I save PKR 20,000/month?
Calculate EMI for PKR 2,000,000 at 20% annual rate for 5 years
Analyse my spending patterns and give me advice
Give me investing tips
Show me all my budget categories
```

---

##  Agent Architecture

```
User Query
    
    ▼
Gemini 1.5 Flash (LLM)
    
    ▼
ReAct Agent — Selects Tool(s)
    
     log_expense
     get_budget_status
     get_all_budget_summary
     convert_currency
     calculate_savings_goal
     get_financial_tips
     analyze_spending_pattern
     calculate_loan_emi
    
    ▼
Final Answer → Chat UI
```

---

##  Project Structure

```
ai datayard genai/
 app.py                  # Main Streamlit application
 requirements.txt        # Python dependencies
 .env.example            # API key template
 .streamlit/
    config.toml         # Streamlit dark theme config
 README.md               # This file
```

---

##  Tech Stack

- **Python 3.10+**
- **Streamlit** — Web UI framework
- **LangChain** — Agent & tool orchestration
- **langchain-google-genai** — Gemini integration
- **Google Gemini 1.5 Flash** — Language model
- **Plotly** — Interactive financial charts
- **Pandas** — Data tables
- **python-dotenv** — Environment management

---

> Built with  for AI DataYard Generative AI Bootcamp
