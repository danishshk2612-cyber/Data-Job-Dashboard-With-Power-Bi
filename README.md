# Telecom Customer Churn Prediction & Segmentation

A data science project that predicts customer churn and identifies customer segments for a telecom company, using behavioral data from 99,999 prepaid subscribers.

---

## Business Problem

Telecom companies lose significant revenue when customers switch providers (churn). This project aims to:
1. **Predict** which customers are likely to churn next month
2. **Segment** customers into groups for targeted retention campaigns

**Dataset:** 4 months of usage data (June–September) for ~100K prepaid mobile subscribers from an Indian telecom company. Churn is defined as zero calls and zero data usage in September.

---

## Results

| Model | Accuracy | Precision | Recall | AUC-ROC |
|---|---|---|---|---|
| Random Forest | 91.2% | 73.8% | 74.1% | 0.912 |
| **XGBoost** | **92.4%** | **76.2%** | **77.8%** | **0.928** |

**4 Customer Segments identified:**
- Segment 0 — High-Value Loyal (~27K customers, ~3% churn)
- Segment 1 — At-Risk High-Value (~18K customers, ~23% churn)
- Segment 2 — Low-Engagement (~31K customers, ~10% churn)
- Segment 3 — Dormant/Low-Value (~24K customers, ~14% churn)

---

## Tech Stack

- Python 3.10+
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- xgboost

---

## Project Structure

```
telecom-churn/
├── data/
│   └── telecom_churn_data.csv
├── Telecom_Churn_Prediction.ipynb
├── requirements.txt
└── README.md
```

---

## How to Run

```bash
# 1. Clone the repo
git clone https://github.com/<your-username>/telecom-churn.git
cd telecom-churn

# 2. Install dependencies
pip install -r requirements.txt

# 3. Place the dataset in the data/ folder

# 4. Open the notebook
jupyter notebook Telecom_Churn_Prediction.ipynb
```

Run all cells from top to bottom. The notebook is fully self-contained.

---

## Notebook Sections

1. **Business Problem** — Context and project objectives
2. **Data Understanding & EDA** — Visualizations and churn patterns
3. **Data Preprocessing** — Cleaning, feature engineering
4. **Customer Segmentation** — RFM features + K-Means (K=4)
5. **Churn Prediction** — Random Forest and XGBoost
6. **Model Evaluation** — Metrics, ROC curve, feature importance
7. **Business Insights** — Recommendations per segment

---

## Key Findings

- **ARPU decline** (June → August) is the strongest churn predictor
- Customers who stopped recharging in August are ~3x more likely to churn
- **3G users** churn at roughly half the rate of voice-only users
- The top 20% of high-risk customers account for ~65% of revenue at risk

---

## Business Recommendations

| Segment | Recommended Action | Est. Impact |
|---|---|---|
| At-Risk High-Value | Retention call + personalised discount | Recover ~₹1.8 Cr/month |
| Loyal High-Value | Upsell to premium plan + referral rewards | +₹0.6 Cr/month |
| Low-Engagement | Sachet data pack promotions | Increase stickiness |
| Dormant | Automated ₹50 bonus recharge SMS | Reactivate 10–15% |

---

**[Shaikh Danish]** | 
