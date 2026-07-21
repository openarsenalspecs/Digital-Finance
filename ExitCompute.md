# ExitCompute  
### **Macro Signals and Risk Models—Combined for Your Exit Plan.**

ExitCompute is an open-source, RIA-style decision-support system designed to help retail investors determine **when and how to exit the stock market** with maximum capital preservation, minimized taxes, and personalized financial alignment.

Built on transparent models, macroeconomic indicators, scenario simulations, and structured best practices, ExitCompute empowers users to unwind market exposure safely, intelligently, and methodically.

---

## 🚀 **Purpose**

Retail investors often enter the market easily—but exiting safely is far more complex.  
ExitCompute addresses this by providing:

- **Personalized exit recommendations**, based on user financial needs  
- **Macro-informed modeling** using interest rates, inflation, liquidity data, and volatility regimes  
- **Tax-aware exit strategies**, including capital gains planning and loss harvesting windows  
- **Full scenario modeling**, showing outcomes under different:  
  - macroeconomic futures  
  - exit speeds  
  - drawdown conditions  
  - tax profiles  
  - risk preferences  

ExitCompute does **not** predict markets.  
It **models tradeoffs** and allows investors to exit with clarity instead of emotion.

---

## 🧠 Core Features

### **1. Personal Financial Alignment**
- Define time horizon, liquidity needs, retirement windows, income stability, and risk tolerance  
- AI aligns exit pace to user life constraints  

### **2. Macro Signal Engine**
Incorporates leading and lagging indicators including:
- Interest rate cycles  
- Yield curve shape  
- Volatility indices  
- Employment data  
- Money supply changes  
- Corporate credit stress  
- Asset correlation regimes  
- Momentum and liquidity measures  

### **3. Market Exit Scenario Simulator**
Runs multi-path simulations for:
- Slow exit (DCA out)  
- Fast exit (triggered risk-off)  
- Hybrid exit (macro + portfolio stress)  
- Profit-first exit  
- Tax-optimized exit  
- Scenario overlays including:  
  - recession onset  
  - inflation spikes  
  - liquidity crunches  
  - volatility breakouts  
  - bull continuation  

### **4. Tax Optimization Layer**
- Capital gains tax projection  
- Harvest timing optimizer  
- Holding period rebalancing  
- Long-term vs short-term gains difference modeling  
- State taxation overlays  

### **5. RIA-Style Risk & Disclosure Framework**
- Transparent assumptions  
- Adjustable risk factors  
- No black-box forecasting  
- Educational output instead of direct financial advice  

### **6. Web Service Architecture**
ExitCompute is designed to run as a full web service with:
- API layer for data ingestion  
- Scenario computation engine  
- Frontend dashboard  
- Audit logs  
- Model transparency panels  
- User-specific configuration  

---

## 📡 Tech Stack (Recommended)

- **Backend:** Python / FastAPI for service API  
- **Scenario Engine:** Python, NumPy, Pandas, statistical modeling, risk modules  
- **Macro Engine:** Scheduled fetchers + normalization pipelines  
- **Frontend:** Vue, React, or Svelte  
- **Data Storage:** Postgres  
- **CI/CD:** GitLab pipelines  
- **Containerization:** Docker  
- **Model Docs:** Markdown + OpenAPI spec  

---

## 📁 Repository Structure (Suggested)
```
/docs
/architecture
/scenarios
/api
/src
/backend
/frontend
/macro_engine
/risk_models
/scenario_engine
/tests
/config
License
notice.md
README.md
```

## Specification Branding License (SBL):  
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

Optional:
- Specification Branding License (SBL)
  - attribution-free commercial deployment
  - pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/exitcompute/](https://roxanneardary.com/exitcompute/)

---

## License & Notice Requirements

ExitCompute is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- ExitCompute specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---

## ⚠️ Financial Disclaimer

ExitCompute does **not** act as a financial advisor.  
It provides analytical tools only and does not guarantee any financial outcome.  
Users are responsible for their own investing decisions.

---

## 🤝 Contributions

Contributions are welcome!  
All contributions are accepted under the AGPL-3.0+ with Section 7 attribution requirement.
