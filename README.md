# 🛍️ Retail Customer Sentiment & Behavior Analysis

This project focuses on analyzing customer behavior and sentiments across the retail journey using data-driven techniques and visual storytelling. It integrates multiple data sources and applies advanced sentiment analysis to uncover insights that can drive marketing, product, and customer experience strategies.

## 📌 Key Objectives
- Enrich customer reviews with **sentiment scores** using **VADER NLP**.
- Analyze customer **journey data** to understand engagement across touchpoints.
- Classify products by **price category** and correlate with sentiment trends.
- Clean and standardize **digital engagement** data (views, clicks, likes).
- Create an **interactive Power BI dashboard** to visualize trends.

## 🧰 Tech Stack
- **Python (Pandas, NLTK)** – Text preprocessing, sentiment analysis.
- **SQL (MSSQL)** – Data extraction, cleaning, and enrichment.
- **Power BI** – Dashboard creation and time-series visualizations.
- **DAX** – Custom date calendar for flexible time analysis.

## 📊 Modules & Data Pipelines

### 1. Sentiment Enrichment (Python)
- Used `nltk.sentiment.vader` to calculate **compound sentiment scores**.
- Merged textual sentiment with numerical ratings to create **hybrid sentiment categories**:
  - Positive, Negative, Neutral, Mixed Positive/Negative.
- Created **score buckets** to understand sentiment strength distribution.

### 2. Data Cleaning (SQL Scripts)
- `fact_customer_reviews.sql`: Cleaned review text.
- `fact_customer_journey.sql`: Removed duplicate journeys, standardized stage names, filled missing durations.
- `fact_engagement_data.sql`: Normalized content types, extracted views/clicks from combined fields.

### 3. Customer & Product Enrichment
- Joined `dim_customers` with geography data to analyze sentiment **by region**.
- Categorized products into `Low`, `Medium`, and `High` based on price.

### 4. Power BI Dashboard
- Integrated cleaned and enriched data into **Power BI (.pbix)** file.
- Created interactive visuals:
  - Sentiment distribution and trends.
  - Customer journey funnel.
  - Product sentiment breakdown.
  - Engagement metrics over time.

## 📈 Sample Insights
- High ratings (4–5 stars) correlate with **strong positive sentiment**.
- Mixed reviews indicate mismatches between product experience and expectations.
- Most engagement happens through **social media content**, with spikes around campaign periods.
- **Drop-offs** identified in the "Consideration" stage of the customer journey.

## 📂 Project Structure
```
├── data/
│   ├── fact_customer_reviews_enrich.csv
├── scripts/
│   ├── customer_reviews_enrichment.py
│   ├── *.sql
│   └── Calendar DAX Script.txt
├── visuals/
│   ├── Customer_Sentiment_Analysis_Report.pdf
├── dashboard/
│   └── Dashboard.pbix
```

## 🚀 How to Run
1. Load SQL data into a local SQL Server (`PortfolioProject_MarketingAnalytics`).
2. Run `customer_reviews_enrichment.py` to generate sentiment-enriched reviews.
3. Open `Dashboard.pbix` in Power BI to view interactive dashboards.

## 📌 Future Enhancements
- Add product-category level sentiment mapping.
- Predict churn based on sentiment trends.
- Integrate with real-time review feeds using APIs.
