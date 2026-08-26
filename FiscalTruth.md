# FiscalTruth  
**Truth in Every Transaction**
- HTML Mirror:  [https://roxanneardary.com/fiscaltruth-specification/](https://roxanneardary.com/fiscaltruth-specification/)  

---

FiscalTruth is an open-source civic watchdog and whistleblower intelligence platform designed to provide full transparency into how state and public funds are allocated, spent, and potentially mismanaged across the United States.

It aggregates budget data, contracts, and public financial records into a unified system that enables citizens, journalists, and researchers to track every dollar, detect anomalies, and investigate public spending with clarity and accountability.

---

## 🚨 Mission

To create a fully transparent, citizen-powered system that ensures **public money is visible, traceable, and accountable at every stage of its flow**.

---

## 🌟 Core Modules

### 🧭 1. Core Budget Transparency System
- State-by-state budget ingestion and normalization  
- Department-level spending breakdowns (education, healthcare, infrastructure, etc.)  
- Multi-year historical budget tracking  
- Revenue vs expenditure analysis  
- County and municipal expansion readiness  
- Drill-down from state → agency → line item  

---

### 📊 2. Advanced Visualization Layer
- Interactive charts (bar, pie, line, heatmaps)  
- Geospatial spending maps using PostGIS  
- Cross-state comparison dashboards  
- Department efficiency scoring views  
- Time-series budget evolution visualization  
- Exportable reports (CSV, JSON, PDF)  

---

### 🧠 3. AI Analytics & Intelligence Engine
- Anomaly detection in spending patterns  
- Budget spike and irregularity detection  
- Forecasting future budget trends  
- Natural language querying across datasets  
- Cross-state pattern recognition  
- Spending inefficiency classification  
- AI-generated explanations of financial anomalies  

---

### 🔍 4. Data Verification & Trust Layer
- Multi-source validation (state, federal, scraped data)  
- Source reliability scoring system  
- Cross-checking budgets vs actual expenditures  
- Confidence scoring for every data point  
- Conflict detection between sources  
- Verified vs unverified labeling  

---

### 🧾 5. Contract Intelligence Engine
- Public contract ingestion and parsing  
- Vendor clustering and identity resolution  
- Shell company detection patterns  
- Overpayment and inflated contract detection  
- Bid comparison analysis  
- Contract renewal risk alerts  
- Vendor dominance tracking  

---

### 🛰️ 6. Real-Time Monitoring System
- Live budget updates feed  
- New contract detection alerts  
- Spending spike detection  
- Department change tracking  
- Multi-channel alerts (email, Telegram, Signal, webhooks)  

---

### 🧩 7. Citizen Case Investigation System
- Convert anomalies into structured case files  
- Timeline-based investigative views  
- Evidence attachment system  
- Collaborative investigation threads  
- Case status tracking (open, verified, resolved)  
- Shareable investigation links  

---

### 🗳️ 8. Community Verification Layer
- Crowdsourced anomaly validation  
- Reputation scoring system  
- Journalist and auditor verification badges  
- Voting on flagged issues  
- Anti-brigading trust weighting  
- Public commentary on investigations  

---

### 🔐 9. Whistleblower Security System
- End-to-end encrypted submissions  
- Zero-knowledge architecture  
- Anonymous reporting system  
- Metadata stripping from uploads  
- Optional Tor/I2P submission support  
- Secure drop links  
- Time-delayed release options  

---

### 🧱 10. Immutable Audit & Data Integrity Layer
- Append-only audit logs  
- Git-style versioned financial datasets  
- Full change history tracking  
- Public dataset verification  
- Tamper-evident logging  
- Snapshot archival system  

---

### 🌐 11. Federation & Decentralization Layer
- Mirrorable deployments  
- Regional/state node support  
- Signed dataset synchronization  
- Offline archival mode  
- Distributed transparency network  

---

### 🧬 12. Data Lineage & Provenance Graph
- Full traceability of all data points  
- Visual data origin graphs  
- Transformation tracking pipeline  
- Source → processing → output mapping  
- Confidence propagation tracking  

---

### 🧭 13. Timeline Replay System
- Replay budget history over time  
- Animated financial evolution  
- Policy impact visualization  
- Department growth/shrink tracking  
- Event-linked spending changes  

---

### ⚖️ 14. Legal & Policy Mapping Engine
- Link spending to legal statutes  
- Compliance vs actual spending comparison  
- Required vs actual funding gaps  
- Legislative impact tracking  
- Policy change correlation  

---

### 📢 15. Alerting & Notification System
- Custom anomaly alerts  
- Budget threshold monitoring  
- Contract value change alerts  
- Real-time monitoring triggers  
- Multi-channel notification delivery  

---

### 🧠 16. AI Investigation Assistant
- Conversational data exploration  
- “Explain this anomaly” interface  
- Cross-state comparisons  
- Evidence summarization  
- Narrative generation of findings  
- Risk interpretation (non-accusatory framing)  

---

### 📁 17. Citizen Research & Journalism Toolkit
- Exportable investigative reports  
- Dataset downloads  
- Embeddable charts  
- Journalistic case sharing tools  
- Advanced filtering and querying  

---

### 🧭 18. Impact Layer
- Budget shift impact mapping  
- Spending redistribution visualization  
- Service-level correlation analysis  
- Infrastructure/education/health impact tracking  
- Priority change detection  

---

### 🧱 19. System Architecture
- Modular monorepo structure (GitLab-ready)  
- API-first backend design  
- Scalable ingestion pipelines  
- Dockerized deployment system  
- Microservice-ready architecture  

---

### 🔒 20. Safety & Integrity Layer
- Separation of raw data, AI interpretation, and verified cases  
- Non-accusatory anomaly labeling  
- Audit-safe logging  
- Provenance enforcement  
- Responsible disclosure workflows  

---

## ⚙️ Suggested Tech Stack

### Frontend
- React  
- TailwindCSS  
- D3.js / Chart.js  
- Mapbox (geospatial visualization)  

### Backend
- Python (FastAPI) or Node.js (Express)  
- REST + optional GraphQL API  

### Data & Storage
- PostgreSQL  
- PostGIS (geospatial queries)  
- Elasticsearch / OpenSearch  

### AI / Analytics
- Python  
- Pandas  
- Scikit-learn  
- PyTorch  

### Security
- AES-256 encryption  
- RSA hybrid encryption  
- Client-side encryption for whistleblower system  

### Infrastructure
- Docker  
- Kubernetes-ready deployment  
- GitLab CI/CD pipelines  
- S3-compatible object storage  
- Optional IPFS integration  


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
  - [https://roxanneardary.com/fiscaltruth/](https://roxanneardary.com/fiscaltruth/)  

---

## 📜 License & Notice Requirements

FiscalTruth is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- FiscalTruth specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
