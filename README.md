# FUTURE_DS_02 — Customer Retention & Churn Analysis (Telco Churn)

## Objective
Analyze churn patterns, retention drivers, and customer lifetime (tenure) trends using the Telco Customer Churn dataset, then translate insights into practical actions a subscription business can take to reduce churn.

## Business Questions
1. Why are customers leaving the platform?
2. Which customer segments are most likely to churn?
3. How long do customers typically stay active?
4. What actions can improve customer retention?

## Dataset
Telco Customer Churn Dataset (Kaggle)  
https://www.kaggle.com/datasets/blastchar/telco-customer-churn  

See: `data/DATA_SOURCE.md`

## Tools
- **Google Colab (Python):** cleaning + analysis
- **Power BI Desktop:** interactive dashboard
- **GitHub:** documentation and deliverables

## Repository Structure
- `data/` — dataset link/instructions (raw dataset not stored in repo)
- `notebooks/` — Colab notebooks used for cleaning and analysis
- `dashboard/` — Power BI dashboard (`.pbix`)
- `reports/` — PDF export of dashboard and any report assets

## Work Completed (What’s inside the notebooks)
### Notebook 01 — Data Audit & Cleaning
- Validated dataset integrity (no duplicate customers / rows)
- Fixed `TotalCharges` type issue (converted to numeric; handled tenure=0 edge cases)
- Created dashboard-friendly fields (`SeniorCitizenFlag`, `HasInternet`, `HasPhone`)
- Exported the cleaned dataset for Power BI

### Notebook 02 — Churn Patterns, Drivers, and Lifetime
- Computed overall churn KPI and churn rates by segment
- Identified key churn drivers (Contract, Payment Method, Internet Service)
- Analyzed customer lifetime patterns using tenure buckets
- Identified highest-risk segment combinations (e.g., Contract × Payment, Contract × Internet)

> Notebooks are located in: `notebooks/`

## Key Results (Analysis + Dashboard)
- **Overall churn rate:** **26.54%**
- **Highest-risk contract type:** **Month-to-month — 42.71% churn**
- **Highest-risk payment method:** **Electronic check — 45.29% churn**
- **Highest-risk internet type:** **Fiber optic — 41.89% churn**
- **Lifetime pattern:** churn is highest in **0–6 months (52.94%)** and decreases steadily with tenure
- **Highest-risk pockets (from matrices):**
  - **Month-to-month × Electronic check**
  - **Month-to-month × Fiber optic**

## Recommendations (Business Actions)
- **Convert month-to-month customers** to longer contracts using targeted incentives.
- **Reduce payment friction** by migrating electronic-check customers to autopay (card/bank transfer).
- **Fiber retention program:** proactive support and service-quality focus for fiber customers.
- **Win early tenure (0–6 months):** stronger onboarding, first-bill clarity, and early customer success touchpoints.
- **Prioritize highest-risk pockets first** using the matrix visuals.

## Deliverables
- **Power BI dashboard:** `dashboard/telco_churn_dashboard.pbix`
- **PDF export (easy viewing):** `reports/telco_churn_dashboard.pdf`

## How to Reproduce
1. Download the dataset (see `data/DATA_SOURCE.md`) and place it locally if needed.
2. Run the notebooks in `notebooks/` (Google Colab recommended).
3. Open the Power BI dashboard in `dashboard/` to explore interactively.
4. View the PDF version in `reports/` for a static summary.

## How to View
- Open `reports/telco_churn_dashboard.pdf` for the static report
- Or open `dashboard/telco_churn_dashboard.pbix` in **Power BI Desktop** for full interactivity