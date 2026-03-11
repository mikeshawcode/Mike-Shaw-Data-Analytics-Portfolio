# Data Analytics Portfolio
**Mike Shaw**  
[LinkedIn](https://www.linkedin.com/in/michael-shaw-95111a254/) | michaelwshaw2@gmail.com

---

## Portfolio Overview
Two end-to-end analytics projects demonstrating Python, SQL, time series forecasting, and data storytelling skills.

| Project | Skills | Tools | Business Impact |
|---------|--------|-------|-----------------|
| [Sales Forecasting](#1-superstore-sales-forecasting) | Time Series, Forecasting, EDA | Python, Prophet, Pandas | Predicted $12K weekly revenue with validated 90-day holdout |
| [Fitness Tracker Analysis](#2-fitbit-activity-analysis) | SQL, Statistical Analysis, Segmentation | Python, SQLite, Seaborn | Quantified steps-to-calories relationship across 30+ users 

---

## 1. Superstore Sales Forecasting

**Problem:** Predict the next 7 days of retail sales for inventory and staffing optimization.

**Approach:**
- Analyzed 4 years (9,800 transactions) of retail sales data
- Identified weekly and yearly seasonality (Nov peak +90%, Saturday +35%)
- Built a Facebook Prophet model with US holiday effects and multiplicative seasonality
- Validated on a 90-day holdout set using MAE, RMSE, and MAPE before forecasting forward

**Results:**
- **7-day forecast:** $12,012 total (Dec 31 – Jan 6)
- **Model validated:** Out-of-sample error metrics confirm forecast reliability
- **Key insight:** Business grew ~60% YoY (2015–2018) — trend component captures compounding growth
- **Recommendations:** Reduce Jan 3–4 staffing (predicted $400–$1,178/day); maximize weekend resources

**Tools:** Python, Pandas, Prophet, Matplotlib, Seaborn

[View Code](https://github.com/mikeshawcode/Mike-Shaw-Data-Analytics-Portfolio/blob/main/Superstore_Dataset_v2.ipynb)

---

## 2. FitBit Activity Analysis

**Problem:** What behavioral patterns drive calorie burn, and how do users differ from one another?

**Approach:**
- Loaded raw FitBit CSV data into an **in-memory SQLite database** and ran all analysis through SQL
- Used `CASE WHEN` segmentation to classify days by CDC step guidelines
- Profiled individual users with **CTEs** and classified them into behavioral archetypes
- Applied **window functions** (`RANK() OVER`, `NTILE()`) to identify top vs. bottom performers
- Quantified the steps–calories relationship with Pearson r and R²

**SQL Concepts Demonstrated:**

| Concept | Used For |
|---------|----------|
| `SELECT`, `COUNT`, `MIN/MAX`, `AVG` | Data validation & summary stats |
| `CASE WHEN` | Activity segmentation, step bucketing |
| `GROUP BY`, `HAVING`, `ORDER BY` | Aggregations across segments and days |
| `WITH` (CTEs) | Multi-step user profiling |
| `RANK() OVER (PARTITION BY ...)` | Ranking each user's best days |
| `NTILE()` | Top 10% vs. bottom 10% decile analysis |

**Results:**
- **Strong positive correlation** between steps and calories (r and R² reported in notebook)
- **Very Active Minutes** shows a comparable or stronger relationship to calorie burn than step count alone — intensity matters as much as volume
- Top 10% step days burn significantly more calories and log far fewer sedentary minutes than the bottom 10%
- Most users fall into the Sedentary or Casual Walker archetype — light walking alone does not meaningfully reduce sitting time

**Tools:** Python, SQLite (`sqlite3`), Pandas, Seaborn, SciPy

[View Code](https://github.com/mikeshawcode/Data_Analytics_Portfolio/blob/main/FitBit_Data_Analysis_v2.ipynb)

---

## Technical Skills

**Languages & Analysis:**
- Python (Pandas, NumPy, Matplotlib, Seaborn, SciPy)
- SQL (CTEs, window functions, aggregations, joins)
- Statistical analysis (regression, correlation, time series)

**Visualization & BI:**
- Tableau
- Matplotlib / Seaborn
- Power BI (in progress)

**Specialized:**
- Time series forecasting (Prophet, ARIMA)
- Web scraping (BeautifulSoup, Requests)
- Machine learning (scikit-learn basics)

---

## What I Bring to Analytics Teams

**Business-first thinking** — start with the problem, not the data  
**End-to-end execution** — data collection → cleaning → analysis → recommendations  
**Clear communication** — technical findings translated for non-technical stakeholders  
**Validated work** — every model is tested before results are reported  
**Impact-oriented** — every analysis answers "so what?" and "now what?"
