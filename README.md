# NorthStar Urban Mobility & Logistics

## Project Overview

NorthStar Urban Mobility has grown rapidly through acquisition, leaving its data fragmented across legacy systems and newer semi‑structured platforms. This project applies an integrated analytics pipeline – SQL, R, Python, and MongoDB – to identify the root causes of declining service quality and rising operational costs.

The analysis combines structured operational data (orders, deliveries, customers, drivers, vehicles, hubs) with **semi‑structured records** (complaints, incidents, app events) to answer four management questions:
- Where do inefficiencies originate?
- Why does service quality vary across locations and service types?
- Which factors drive failure, delay, and customer dissatisfaction?
- How should the data environment be redesigned to support better decision‑making?


## Technologies Used

| Technology | Purpose |
| **SQL (sqldf in R)** | Eight analytical queries joining nine relational datasets |
| **R (ggplot2, stats)** | Correlation matrix, ANOVA, multiple regression, t‑tests |
| **Python (Pandas, NumPy, Matplotlib, Seaborn)** | Data cleaning, zone standardisation, missing value audit, visualisation |
| **MongoDB Atlas (PyMongo)** | Document database design with embedded customer &amp; delivery documents, CRUD operations, aggregation pipeline, indexing |


## Key Findings

- **'On‑Time' is a vanity metric:** Deliveries marked on‑time still generate high‑severity complaints (DriverBehaviour, MissedPickup)
- **Operational metrics explain only 42% of satisfaction:** The regression model isolates **delay** and **failure** as the only significant predictors of customer rating; human factors (driver conduct, communication) dominate the unexplained variance
- **Zone performance is uniformly mediocre:** ANOVA shows no significant rating differences, yet complaint volumes vary widely across zones
- **Vehicle battery health predicts failure:** A clear failure‑rate gradient exists as battery health declines; BatteryAlert incidents are the most common and slowest to resolve
- **22.5% of app events are orphaned:** 144 of 640 events have no order_id, breaking the customer interaction chain
- **A small cohort of high‑value customers is at risk:** Enterprise and SME clients with repeat complaints represent a disproportionate revenue threat


## How to Run

1. **Clone or download** this repository
2. Open any notebook in **Google Colab** (or Jupyter)
3. Upload the `data/` folder to your Colab session
4. For the MongoDB notebook, replace the connection string with your own Atlas cluster credentials

---

## Author

Anup Batha | Student_ID = 33119491
