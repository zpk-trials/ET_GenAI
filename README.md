<div align="center">
  <h1>🚀 NEXUS: Agentic Opportunity Radar</h1>
  <p><em>Institutional-Grade Statistical Validation for Retail Investors</em></p>
</div>

> **The Mission:** Democratizing Investment Intelligence by verifying whether a stock price breakout is backed by true institutional volume, protecting retail traders from the dreaded "Bull Trap."

---

## 🎯 Problem Statement

Retail investors often rely on lagging indicators or "noisy" price action, entering trades at the peak only to watch the momentum instantly reverse. This information asymmetry exists because institutional players use quantitative volume analysis, while retail relies on rumors.

**NEXUS** solves this by reframing market analysis as a **multi-agent statistical validation pipeline**.

### The Input
- Target Ticker Symbol (e.g., `RELIANCE.NS`)
- Live 20-day OHLCV Data (via yFinance)

### The Output
- **Statistically Validated Action:** `BUY`, `WATCH`, or `AVOID`
- **Agentic Rationale:** A human-readable breakdown of the underlying math and market narrative.

---

## 🧠 Core Methodology (The Math)

We discard standard volume bars in favor of **Volume Z-Score Analysis**. This acts as the unshakeable guardrail for our AI agents.

1. **Data Ingestion:** Fetch 20 days of historical volume.
2. **Statistical Modeling:** Calculate the rolling mean and standard deviation.
3. **Z-Score Calculation:** We measure how many standard deviations today's volume is from the average.
   * `Z > 2.0` → Top 2.5% volume day (High Institutional Conviction).
   * `Z < 0` → Below average volume (High Risk / Noise).
4. **Agentic Handoff:** The raw statistics are passed to our CrewAI orchestrator for narrative synthesis.

---

## 🤖 Architecture: The Multi-Agent Crew

Powered by **Llama 3.3 70B** running on **Groq** for sub-second inference, our pipeline utilizes two distinct AI personas:

<details>
  <summary style="list-style: none; cursor: pointer;">
    <b>🕵️‍♂️ Agent 1: The Lead Quant Researcher (Click to expand)</b>
  </summary>
  <p>This agent acts as the strict logical gatekeeper. It does not care about news; it only cares about the Z-Score and price momentum. If the math doesn't show a high-conviction breakout, this agent flags the asset as "Noisy."</p>
</details>

<details>
  <summary style="list-style: none; cursor: pointer;">
    <b>📈 Agent 2: The Indian Market Strategist (Click to expand)</b>
  </summary>
  <p>Takes the raw quantitative report from the Lead Quant and translates it into a risk-mitigated execution plan tailored for the volatile realities of the NSE/BSE markets.</p>
</details>

---

## 🛠️ Tech Stack

- **Orchestration:** CrewAI
- **LLM Engine:** Groq (Llama-3.3-70b-versatile)
- **Data Layer:** yFinance, Pandas, NumPy
- **Environment:** Python 3.11+

---

## ▶️ Quick Start Guide

**1. Clone the repository**
```bash
git clone https://github.com/Zapking-001/NEXUS_Opportunity_Radar.git
cd NEXUS_Opportunity_Radar
```

**2. Initialize the environment**
```bash
python -m venv venv
source venv/Scripts/activate  # On Windows Git Bash
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

**4. Configure Keys**
Create a `.env` file in the root directory and add your Groq API key:
```text
GROQ_API_KEY=your_key_here
```

**5. Launch the Radar**
```bash
python main.py
```

---

## 🏁 Submission Details

**Track:** Democratizing Investment Intelligence  
**Event:** ET GenAI Hackathon 2026

```text
  _   _ _______  ___    _  _____ 
 | \ | |  ___\ \/ / |  | |/ ____|
 |  \| | |__  \  /| |  | | (___  
 | . ` |  __| /  \| |  | |\___ \ 
 | |\  | |___/ /\ \ |__| |____) |
 |_| \_|____/_/  \_\____/|_____/ 
                                 
```
<br>

**| The Team |$|ians |**
| Name | Role |
|-----|-----|
| **Saurav Kumar** | Data Pipeline (yFinance) & Dependency Management |
| **Garg Parashar** | CrewAI Orchestration & LLM Prompt Engineering |
| **Pritham Prajwin V** | Lead Quant Logic , Systems Architecture , Technical Documentation & Product Strategy |
