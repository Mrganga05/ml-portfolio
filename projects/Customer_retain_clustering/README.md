# Customer Segmentation using Clustering (RFM + KMeans)

## Project Overview
This project performs **customer segmentation** using transactional data from an online retail dataset.  
The goal is to identify distinct groups of customers based on **Recency, Frequency, and Monetary (RFM)** features using **KMeans clustering**.  

Customer segmentation helps businesses:
- Understand different types of customers
- Target marketing campaigns effectively
- Increase revenue by personalizing offers

---

## Dataset
- Source: [Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)  
- Columns used for RFM analysis:
  - `CustomerID` → Unique identifier for each customer  
  - `InvoiceDate` → Transaction date  
  - `Quantity` → Number of items purchased  
  - `UnitPrice` → Price per item  

Other columns like `Invoice`, `StockCode`, `Description`, `Country` were not used for clustering.

---

## Features
- **Recency** → Days since last purchase  
- **Frequency** → Number of invoices per customer  
- **Monetary** → Total spending per customer  
- **Log-transformed Frequency & Monetary** → For normalization before clustering  

---

## Tools & Libraries
- Python 3.x  
- Pandas, NumPy → Data manipulation  
- Matplotlib, Seaborn → Data visualization  
- Scikit-learn → StandardScaler, PCA, KMeans  
- Jupyter Notebook → Development environment  

---

## Methodology

1. **Data Cleaning**
   - Removed rows with missing `CustomerID`
   - Filtered out negative `Quantity` and `UnitPrice`
   - Calculated `TotalPrice = Quantity * UnitPrice`

2. **RFM Feature Engineering**
   - `Recency` = Days since last purchase
   - `Frequency` = Number of invoices per customer
   - `Monetary` = Total spending per customer

3. **Data Preprocessing**
   - Log transformation for `Frequency` and `Monetary`
   - Standard scaling

4. **Clustering**
   - Determined optimal clusters using **Elbow method** and **Silhouette score**
   - Applied **KMeans clustering** (`k=4`)

5. **Analysis & Visualization**
   - Visualized clusters using **PCA projection**
   - Cluster profiling to understand average RFM values per cluster

---

## Results
- **Number of clusters:** 4  
- Each cluster represents a distinct type of customer based on spending patterns, recency, and purchase frequency.  
- **Insights example:**  
  - Cluster 0 → High spending, frequent, recent buyers  
  - Cluster 1 → Low spending, infrequent buyers  
  - Cluster 2 → Medium spending, recent buyers  
  - Cluster 3 → Low spending, long inactive customers  

---

## How to Run
1. Clone this repository:
   ```bash
   git clone <your-repo-url>
