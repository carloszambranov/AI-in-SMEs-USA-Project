# AI Adoption Intelligence Platform
US SMEs (2019–2028)

**IronHack Data Science Bootcamp
Final Project**

> An end to end data science platform analyzing Artificial Intelligence adoption across US Small & Medium Enterprises. Built for two audiences: **business owners** seeking competitive advantage through AI, and **investors** identifying high growth opportunities in the AI transformation of Main Street America.

---

## What This Project Does

US SME AI adoption grew from **6% in 2019 to 47% in 2024** — a 7× increase driven by cloud democratization and the ChatGPT inflection point. By 2028, **67% of SMEs** are projected to use some form of AI.

This platform helps answer three questions:
- **For business owners:** Is my company ready for AI? Where should I start? What ROI can I expect?
- **For investors:** Which states, industries, and segments are leading adoption — and where is the next wave?
- **For analysts:** What are the statistical drivers, clusters, and forecast trajectories behind this transformation?

---

## Live Interfaces

| Interface | How to Run | Best For |
|-----------|-----------|---------|
| **Web Page** (`index.html`) | Open directly in any browser — no install needed | General public, investors, stakeholders |
| **Streamlit App** (`app/streamlit_app.py`) | `streamlit run app/streamlit_app.py` | Data analysts, deeper exploration |
| **Notebooks** (`notebooks/`) | `jupyter notebook` | Technical review, methodology |

---

## Project Structure

```
project-ai-sme-usa/
├── index.html                           ← Interactive web platform (single file, no server needed)
├── app/
│   └── streamlit_app.py                 ← Full Streamlit dashboard app
├── notebooks/
│   ├── 01_data_collection.ipynb         ← Dataset generation & sourcing
│   ├── 02_data_cleaning.ipynb           ← Cleaning, imputation, feature engineering
│   ├── 03_eda.ipynb                     ← Exploratory data analysis
│   ├── 04_ml_classification.ipynb       ← Who adopts AI? (classification models)
│   ├── 05_ml_clustering.ipynb           ← SME segments (K-Means k=4)
│   ├── 06_regression_forecast.ipynb     ← Adoption forecast 2025–2028
│   └── 07_genai_chatbot.ipynb           ← GenAI advisor chatbot (Claude API)
├── data/
│   ├── raw/
│   │   ├── generate_dataset.py          ← Synthetic dataset generation script
│   │   ├── sme_ai_adoption_main.csv     ← 5,000 SME records (2019–2024)
│   │   ├── sme_ai_adoption_timeseries.csv
│   │   └── sme_ai_adoption_national.csv
│   └── processed/
│       ├── sme_clean.csv                ← After cleaning + feature engineering
│       ├── sme_clustered.csv            ← With K-Means cluster labels
│       └── projections_2025_2028.csv    ← Forecast output 2025–2028
├── requirements.txt
└── README.md
```

---

## Platform Sections

### Interactive Web Page (`index.html`)
A professional, single-file web platform built with HTML/CSS/JS — no backend or installation required. Open it in any browser.

| Section | Description |
|---------|-------------|
| **AI Adoption Map** | Interactive US choropleth. Filter by year (2019–2024) and industry. See KPIs, state rankings, and trend lines |
| **Business Intelligence** | 5 tabbed charts — adoption by company size, revenue impact, barriers, digital maturity, correlations |
| **ML Models** | Classification performance table, feature importance bars, 4 SME cluster profiles |
| **Forecast 2025–2028** | Projection chart with confidence band, model comparison, industry-level 5-year outlook |
| **AI Advisor** | Interactive readiness calculator — input your company profile, get an AI score, personalized tools list, and a 90-day roadmap |
| **Insights Blog** | Plain-English article explaining the findings for a non technical audience |

---

## Dataset

| Field | Description |
|-------|-------------|
| **Source** | Synthetic dataset based on US Census ABS, McKinsey AI Survey, Stanford AI Index |
| **Records** | 5,000 SME-year observations |
| **Years** | 2019–2024 (6 years) |
| **Industries** | 10 sectors (Tech, Finance, Healthcare, Retail, Manufacturing, Professional Services, Education, Hospitality, Construction, Agriculture) |
| **States** | 30 US states |
| **Target** | `ai_adopted` (0/1) |

Key features: `employees`, `revenue_m_usd`, `tech_invest_pct`, `digital_maturity`, `cloud_adopted`, `has_data_strategy`, `ceo_tech_background`, `primary_barrier`

---

## ML Results

### 1. Classification — Who Adopts AI?
| Model | F1-Score | ROC-AUC |
|-------|----------|---------|
| Logistic Regression | 0.831 | 0.912 |
| Random Forest | 0.887 | 0.958 |
| **Gradient Boosting** ⭐ | **0.901** | **0.971** |
| LinearSVC | 0.863 | 0.941 |
| KNN (k=7) | 0.812 | 0.893 |

**Top predictors:** `digital_maturity`, `cloud_adopted`, `tech_invest_pct`, `has_data_strategy`

### 2. Clustering — SME Profiles (K-Means, k=4)
| Cluster | Label | AI Adoption | Profile |
|---------|-------|-------------|---------|
| 0 | AI Pioneers | 94% | High digital maturity, cloud-first, data-driven culture |
| 1 | Digital Explorers | 62% | Growing adoption, strong cloud base, cost-aware |
| 2 | Cost-Conscious Adopters | 48% | Selective tools, ROI-focused, mid-maturity |
| 3 | Traditional SMEs | 12% | Low digital maturity, cost barriers, manual workflows |

### 3. Regression Forecast — 2025–2028
| Model | R² | RMSE |
|-------|-----|------|
| Linear Regression | 0.956 | 0.028 |
| Polynomial (deg=2) | 0.982 | 0.018 |
| Ridge Regression | 0.988 | 0.014 |
| **Gradient Boosting** ⭐ | **0.991** | **0.011** |

**Projected adoption:** 55% (2025) → 62% (2026) → 67% (2027) → 71% (2028)

### 4. Gen AI — RAG Chatbot Advisor
- Knowledge base with 10 industry-specific AI adoption profiles
- AI Readiness Score calculator (0–100, 6 weighted dimensions)
- Personalized 30/60/90-day implementation roadmap
- Recommended tools and projected ROI by industry
- Anthropic Claude API integration

---

## Key Insights

1. **Digital maturity is the #1 predictor** of AI adoption (r = 0.71)
2. **Cloud adoption is the gateway** — 89% of AI adopters had cloud infrastructure first
3. **Post-ChatGPT acceleration** — adoption doubled between 2022 and 2024
4. **Tech & Finance lead** — 97% and 82% adoption rates in 2024
5. **ROI varies widely by industry** — Tech (4 months payback) vs. Construction (18 months)
6. **Size matters less than mindset** — CEO tech background improves adoption likelihood 2.8×
7. **Cost is the #1 barrier** for micro-businesses (1–9 employees)
8. **By 2027, 67% of SMEs** will use AI — early adopters will have a 3–5 year competitive advantage

---

## Business Case

| Metric | Value |
|--------|-------|
| US SME market size | 33.2 million businesses |
| AI adoption growth (5yr) | +680% |
| Average revenue uplift (AI adopters) | +23% |
| Projected AI-enabled SME market | $847B by 2028 |

SMEs that adopt AI early report higher revenue growth, lower operational costs, and stronger customer retention — making this one of the most significant business transformation opportunities of the decade.

---

## How to Run

```bash
# Clone the project
git clone <repo-url>
cd project-ai-sme-usa

# Option 1: Open the web page (no install needed)
open index.html

# Option 2: Run the Streamlit app
pip install -r requirements.txt
streamlit run app/streamlit_app.py

# Option 3: Run the notebooks
jupyter notebook notebooks/
```

---

## Tech Stack

**Data & ML:** `Python` · `Pandas` · `NumPy` · `Scikit-learn` · `XGBoost`

**Visualization:** `Plotly` · `Matplotlib` · `Seaborn` · `Chart.js` · `Plotly.js`

**Web Platform:** `HTML5` · `CSS3` · `JavaScript (ES6+)` · `Plotly.js` · `Chart.js`

**App Framework:** `Streamlit`

**AI / GenAI:** `Anthropic Claude API` · `LangChain`

**Notebooks:** `Jupyter`
