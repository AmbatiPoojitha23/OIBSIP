# Task 2 · Customer Segmentation Analysis (RFM + K-Means Clustering)

## 📌 Objective
Apply clustering algorithms to segment an e-commerce company's customer base into
distinct groups based on purchasing behaviour, enabling targeted marketing strategies.

## 🛠️ Tech Stack
- Python
- pandas, numpy
- scikit-learn (KMeans, StandardScaler, silhouette_score)
- matplotlib, seaborn
- Jupyter Notebook

## 📂 Files in this Repository
| File | Description |
|---|---|
| `Customer_Segmentation_RFM_KMeans.ipynb` | Main analysis notebook — data cleaning, RFM feature engineering, K-Means clustering, visualizations, and insights |
| `ecommerce_transactions.csv` | Raw transaction-level dataset (InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country) |
| `customer_segments.csv` | Final output — each customer with their RFM scores, cluster number, and segment label |

## 🔍 Approach
1. **Data Cleaning** — handled missing CustomerIDs, duplicate rows, cancelled orders, and invalid prices
2. **Descriptive Statistics** — average order value, purchase frequency, customer lifetime value
3. **Feature Engineering** — built RFM (Recency, Frequency, Monetary) features per customer
4. **Standardisation** — log-transformed and scaled features using `StandardScaler`
5. **Clustering** — applied K-Means, used the Elbow Method + Silhouette Score to choose K=4
6. **Visualization** — scatter plots (Recency vs Monetary, Frequency vs Monetary, Recency vs Frequency)
7. **Cluster Profiling** — labeled segments as Champions, Loyal, At-Risk, and Hibernating customers
8. **Business Insights** — recommended a marketing action for each segment

## 📊 Customer Segments Identified
- **Champions / VIP** — most recent, most frequent, highest spend
- **Loyal / Steady Spenders** — regular repeat buyers
- **At-Risk / Needs Attention** — engagement declining, worth a win-back campaign
- **Hibernating / Lost** — long inactive, low value

## 💡 Key Insight
The At-Risk segment offers the highest-leverage opportunity for retention marketing —
they've already proven repeat-purchase behaviour, unlike Hibernating customers.

## 🚀 How to Run
1. Clone this repo
2. Install dependencies: `pip install pandas numpy scikit-learn matplotlib seaborn`
3. Open `Customer_Segmentation_RFM_KMeans.ipynb` in Jupyter Notebook / JupyterLab
4. Run all cells

## 🎓 About
This project was completed as part of the **Oasis Infobyte Data Science Internship
(OIBSIP)** — Task 2.

**Author:** Ambati Poojitha
**LinkedIn:** [linkedin.com/in/poojitha-ambati23](https://linkedin.com/in/poojitha-ambati23)
