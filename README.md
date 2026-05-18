# d2c-rfm-segmentation

# D2C Customer Churn Capstone — Part 2: RFM Segmentation & Customer Analysis

## Project Overview

This project focuses on customer segmentation using the RFM (Recency, Frequency, Monetary) framework for a Direct-to-Consumer (D2C) business.

The objective of this analysis is to identify valuable customers, detect churn-risk users, and generate actionable business insights using customer purchasing behavior.

The project helps businesses understand:
- which customers are most valuable,
- which customers are at risk,
- which users spend the most,
- how retention strategies can be improved.

---

## Objectives

The main objectives of this project are:

- perform RFM analysis,
- calculate Recency, Frequency, and Monetary metrics,
- assign RFM scores to customers,
- segment customers into business-focused categories,
- generate retention strategies,
- export segmented customer data for future use.

---

## Repository Structure

```bash
Part2_RFM_Segmentation/

│── rfm_segmentation.ipynb
│── segments.csv
│── retention_strategy.md
│── manual_review_cases.md
│── README.md
│── requirements.txt
```

---

## Datasets Used

The analysis uses the following datasets:

- customers.csv
- orders.csv

Additional reference datasets:

- support_tickets.csv
- web_events_snapshot.csv
- churn_labels.csv
- intervention_history.csv

---

## RFM Analysis

### Recency (R)
Measures how recently a customer made a purchase.

### Frequency (F)
Measures how often a customer purchases.

### Monetary (M)
Measures total customer spending.

---

## Customer Segments Created

The following customer segments were identified:

- Champions
- Loyal Customers
- Big Spenders
- Recent Customers
- At Risk Customers
- Regular Customers

---

## Key Insights

- Regular Customers form the largest customer segment.
- Loyal Customers contribute significantly to repeat purchases.
- Big Spenders generate high revenue despite smaller population size.
- At Risk customers require immediate retention campaigns.
- Champions should receive loyalty rewards and exclusive benefits.

---

## Visualizations Performed

The notebook includes:

- customer segment distribution,
- RFM score analysis,
- spending analysis,
- customer behavior comparison charts.

---

## Output File

### segments.csv

Contains:
- customer_id
- Recency
- Frequency
- Monetary
- RFM Scores
- Customer Segment

This file can be used for:
- retention campaigns,
- recommendation systems,
- churn prediction models,
- customer analytics dashboards.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Installation & Setup

### Clone Repository

```bash
git clone https://github.com/GuDLish/d2c-rfm-segmentation.git
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Notebook

Open:

```bash
rfm_segmentation.ipynb
```

using VS Code or Jupyter Notebook.

---

## Future Improvements

Possible future enhancements:
- automated customer scoring,
- predictive churn analysis,
- dashboard integration,
- machine learning segmentation,
- real-time customer analytics.

---

## Author

Prateek Parmar
