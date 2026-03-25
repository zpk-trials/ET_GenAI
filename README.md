<div align="center">
  <img src="https://capsule-render.vercel.app/render?type=soft&color=auto&height=200&section=header&text=|$|ians%20NEXUS&fontSize=80" width="100%" />

  ![Python](https://img.shields.io/badge/python-3.11+-blue.svg)
  ![CrewAI](https://img.shields.io/badge/Framework-CrewAI-red.svg)
  ![Groq](https://img.shields.io/badge/Inference-Groq_LPU-orange.svg)
  ![ISI](https://img.shields.io/badge/Institute-ISI_Bangalore-green.svg)

  <h3>🚀 NEXUS: Agentic Opportunity Radar</h3>
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
2. **Statistical Modeling:** Calculate the rolling mean ($\mu$) and standard deviation ($\sigma$).
3. **Z-Score Calculation:** We measure how many standard deviations today's volume is from the average.
   
   $$Z = \\frac{{V_{{today}} - \\mu_{{20day}}}}{{\\sigma_{{20day}}}}$$

   * `Z > 2.0` → Top 2.5% volume day (**High Institutional Conviction**).
   * `Z < 0` → Below average volume (**High Risk / Noise**).

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

**4. Launch the Radar**
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
| **Pritham Prajwin V** | Lead Quant Logic, Systems Architecture, Technical Documentation & Product Strategy |
| **Garg Parashar** | CrewAI Orchestration & LLM Prompt Engineering |
| **Saurav Kumar** | Data Pipeline (yFinance) & Dependency Management |

---

<div align="center">
  <img src="https://forthebadge.com/images/featured/featured-built-with-love.svg" height="25">
  <img src="https://forthebadge.com/images/featured/featured-cyber-punk.svg" height="25">
</div>
