# D2C Customer Churn Intelligence — Part 2: RFM Segmentation & Retention Strategy

## Business Problem

A Direct-to-Consumer (D2C) personal-care brand wants to improve customer retention by identifying:

- high-value customers,
- early churn-risk users,
- declining engagement patterns,
- and customers requiring targeted retention intervention.

Traditional blanket discount campaigns often reduce profitability without improving long-term customer retention.

This project applies RFM (Recency, Frequency, Monetary) analysis combined with behavioral interpretation to build business-oriented customer segments for retention planning and customer intelligence.

---

# Project Objectives

The primary objectives of this project are to:

- calculate customer-level RFM metrics,
- identify valuable and churn-risk customer groups,
- build business-oriented customer segments,
- prioritize retention opportunities,
- analyze customer-value distribution,
- investigate segmentation limitations,
- and generate actionable retention strategies.

---

# Datasets Used

Primary datasets used:

| Dataset | Purpose |
|---|---|
| `orders_clean.csv` | Transaction history used to compute customer RFM metrics |
| `segments.csv` | Output of the RFM segmentation step (customer-level RFM + segment labels) |

Additional reference datasets:

| Dataset | Purpose |
|---|---|
| `manual_review_cases.csv` | Example/registry of customers requiring human inspection |
| `retention_action_list_top200.csv` | Export of the top retention-priority customers for action planning |
| `customer_intelligence_segments.csv` | Customer intelligence/segment export combining segment + business interpretation (as produced by the notebook) |

---

# RFM Framework

## Recency (R)

Measures how recently a customer made a purchase.

Customers with recent activity are generally more engaged and easier to retain.

---

## Frequency (F)

Measures how often a customer purchases.

Higher purchase frequency often indicates stronger customer loyalty and product engagement.

---

## Monetary (M)

Measures total customer spending.

High monetary customers contribute disproportionately to revenue and often require specialized retention strategies.

---

# Customer Segments Created

The project segments customers into business-focused categories:

| Segment | Description |
|---|---|
| Champions | Highly active, high-frequency, high-value customers |
| Loyal Customers | Consistent repeat buyers with stable engagement |
| Big Spenders | High monetary contribution customers |
| Recent Customers | Newly active customers with growth potential |
| Regular Customers | Moderate-value and average-engagement customers |
| At Risk Customers | Customers showing declining activity and churn indicators |

---

# How segments map to retention priorities

Retention actions are selected from the priority framework in `retention_strategy.md`.

In this package, the intended mapping is:

| Segment (from `segments.csv`) | Primary retention priority group |
|---|---|
| Champions | Critical Retention (if churn risk signals are present) |
| Big Spenders | Critical Retention (if disengagement signals are present) |
| Loyal Customers | Engagement Recovery |
| Recent Customers | Onboarding & Nurture |
| Regular Customers | Regular Engagement |
| At Risk Customers | Win-Back Campaign |

---

# Business-Focused Segmentation Approach

This project goes beyond textbook RFM scoring by considering:

- customer engagement behavior,
- churn-risk interpretation,
- support dissatisfaction patterns,
- inactivity signals,
- and retention prioritization logic.

The analysis also highlights situations where traditional RFM segmentation alone may fail to capture true customer risk.

Example:

- a high-spending customer with declining engagement may still require churn intervention,
- while a recent low-frequency customer may not necessarily represent retention risk.

---

# Key Analytical Areas Covered

The notebook includes:

- RFM metric generation,
- customer scoring,
- segment distribution analysis,
- customer-value analysis,
- churn-risk interpretation,
- behavioral segmentation insights,
- retention prioritization logic,
- and manual-review case identification.

---

# Key Business Insights

Some major findings from the segmentation analysis include:

- High-value customers represent a disproportionately important revenue segment.
- Certain customers show strong monetary contribution despite declining activity.
- At Risk customers require proactive retention before becoming fully inactive.
- Regular Customers form the largest operational segment and require scalable engagement strategies.
- Pure RFM segmentation may miss customers affected by dissatisfaction or engagement decline.

---

# Manual Review Philosophy

Not all customers can be accurately evaluated using automated scoring alone.

The project includes manual-review scenarios for ambiguous or high-risk customer cases such as:

- high-spending but declining users,
- recently acquired high-value customers,
- inconsistent purchasing behavior,
- and customers with conflicting engagement signals.

These cases may require additional business review before retention decisions are made.

---

# Repository Structure

```bash
d2c-rfm-segmentation/
│
├── rfm_segmentation.ipynb
├── segments.csv
├── retention_strategy.md
├── manual_review_cases.md
├── README.md
├── requirements.txt
```

---

# Output File

## segments.csv

The exported segmentation file contains:

- customer_id
- Recency
- Frequency
- Monetary
- RFM scores
- customer segments

This dataset can support:

- retention campaigns,
- CRM targeting,
- churn modeling,
- recommendation systems,
- and customer analytics dashboards.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

# Installation & Setup

## Clone Repository

```bash
git clone https://github.com/GuDLish/d2c-rfm-segmentation.git
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

## Run Notebook

Open:

```bash
rfm_segmentation.ipynb
```

using:
- VS Code
- Jupyter Notebook
- or JupyterLab

---

# Future Improvements

Potential future enhancements include:

- ML-based customer scoring,
- churn probability integration,
- automated retention prioritization,
- dashboard deployment,
- and real-time customer monitoring pipelines.

---

# Author

**Prateek Parmar**
