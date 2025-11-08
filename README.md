# 🏦 Financial Alert Agent  
### AI-Powered Financial Risk Analyzer with Interactive Q&A  
**Built using Gemini 2.5 Flash, FastAPI, Streamlit, and spaCy**

---

## 📘 Overview  
**Financial Alert Agent** is an AI-powered financial news analysis system that reads financial articles and automatically identifies:  
- Market sentiment (**Bullish / Bearish / Neutral**)  
- Primary financial risk (**Regulatory, Credit, Liquidity, etc.**)  
- Risk rationale and severity score (**1–5**)  
- Key entities like banks, people, or organizations involved  
- Supports **Q&A chat** to explore article implications interactively  

It leverages **Google Gemini 2.5 Flash**, **FastAPI**, and **Streamlit** to deliver real-time financial risk insights.

---

## 🧠 Key Features  
✅ Extracts organizations, people, and locations using **spaCy**  
✅ Analyzes sentiment and market implications using **Gemini 2.5**  
✅ Detects **risk types** (Regulatory, Liquidity, Credit, etc.)  
✅ Generates **risk score (1–5)** with clear reasoning  
✅ Provides **interactive Q&A** using Gemini’s context understanding  
✅ Modern, clean **Streamlit UI** for visualization  

---

## ⚙️ Tech Stack  
| Component | Technology Used |
|------------|------------------|
| **LLM** | Gemini 2.5 Flash (Google Generative AI) |
| **Backend** | FastAPI |
| **Frontend** | Streamlit |
| **NLP** | spaCy |
| **Language** | Python 3.10+ |
| **Deployment** | Localhost / Streamlit Cloud |

---

## 🧩 System Architecture  

### 🧭 Overview
Below is the workflow of the project:

![Architecture Diagram](architecture_diagram.png)

> **User → Streamlit → FastAPI → Gemini 2.5 Flash → spaCy → Streamlit Visualization**

---

## 📦 Setup & Installation  

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/hari30857/Financial_alert_agent.git
cd Financial_alert_agent
2️⃣ Create Virtual Environment
bash
Copy code
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
3️⃣ Install Requirements
bash
Copy code
pip install -r requirements.txt
4️⃣ Configure Gemini API Key
Create a .env file in the project root:

ini
Copy code
GEMINI_API_KEY=your_google_api_key_here
🔗 Get your API key from: https://aistudio.google.com/apikey

▶️ Run the Application
🧠 Start Backend (FastAPI)
bash
Copy code
uvicorn main:app --reload
Runs at: http://127.0.0.1:8000

💻 Start Frontend (Streamlit)
bash
Copy code
streamlit run app.py
Access at: http://localhost:8501

📰 Example Input
“The Reserve Bank of India fined ICICI Bank ₹5 crore for non-compliance with liquidity coverage ratio norms.”

🧾 Example Output
Field	Result
Summary	RBI fined ICICI Bank ₹5 crore for failing to comply with LCR norms.
Sentiment	Bearish
Risk Type	Regulatory
Risk Rationale	Penalty for regulatory non-adherence.
Risk Score	2 / 5 (Low Risk)
Entities	RBI, ICICI Bank

💬 Example Q&A
Question: What impact does this fine have on investors?
Answer: The fine highlights regulatory scrutiny on banking practices, which may cause short-term market caution but limited long-term investor impact.

⚠️ Risk Type Categories
Risk Type	Description
Regulatory Risk	Non-compliance with laws or government rules (e.g., RBI fines).
Credit Risk	When a borrower or company cannot repay loans.
Liquidity Risk	When a bank or firm cannot meet withdrawal or funding needs.
Market Risk	Losses due to stock, interest rate, or exchange rate fluctuations.
Operational Risk	Failures in internal systems or management processes.
Reputational Risk	Damage to brand trust due to scandals or bad publicity.

🧠 How It Works
1️⃣ User inputs a financial article.
2️⃣ FastAPI backend sends it to Gemini 2.5 Flash.
3️⃣ Gemini analyzes sentiment, risk, and rationale.
4️⃣ spaCy extracts key entities (ORG, PERSON, GPE).
5️⃣ Streamlit displays the results and allows follow-up Q&A.

👨‍💻 Developer
👤 Boddhapu Hareendra
B.Tech – Computer Science (AI & ML)
KL University

⭐ If you found this project useful, don’t forget to star the repo on GitHub! 🌟
