# Customer Segmentation using K-Means and Random Forest

## 📌 Project Overview

This project focuses on customer segmentation using RFM analysis (Recency, Frequency, Monetary) and machine learning techniques.

The goal is to identify distinct customer groups based on purchasing behavior and build a model that can automatically assign new customers to these segments.

---

## 🎯 Business Problem

In many businesses, marketing efforts are applied uniformly across all customers. However, customers behave differently:
- some are highly loyal and valuable,
- some are at risk of churn,
- others are new and need engagement.

Without segmentation, companies risk:
- wasting marketing budget,
- losing valuable customers,
- missing growth opportunities.

This project solves this problem by identifying customer segments and enabling targeted strategies.

---

## 📊 Dataset

The dataset contains customer-level aggregated data with the following key features:

- `Days Since Last Purchase` → Recency  
- `Items Purchased` → Frequency  
- `Total Spend` → Monetary  

Additional features:
- Gender, Age, City
- Membership Type
- Satisfaction Level

---

## 🧠 Methodology

### 1. RFM Feature Engineering
RFM metrics were used to represent customer behavior:
- **Recency** – how recently a customer made a purchase  
- **Frequency** – how often they purchase  
- **Monetary** – how much they spend  

---

### 2. Data Preprocessing
- Outlier treatment using winsorization  
- Log transformation for skewed features  
- Feature scaling using StandardScaler  

---

### 3. K-Means Clustering
- Tested different values of K using:
  - Elbow method
  - Silhouette score
- Optimal number of clusters selected: **K = 6**

---

### 4. Cluster Interpretation

Six distinct customer segments were identified:

| Cluster | Segment Name | Description |
|--------|--------------|-------------|
| 1 | Champions | High frequency, high spending, recent activity |
| 2 | Loyal Customers | Frequent buyers with strong value |
| 4 | Potential Loyalists | Active customers with growth potential |
| 0 | Average Customers | Moderate behavior |
| 3 | At Risk | Previously active but inactive recently |
| 5 | Hibernating | Long inactive customers |

---

### 5. Random Forest Classification

A Random Forest classifier was trained to predict customer segments based on RFM features.

This allows:
- real-time segmentation,
- avoiding re-running K-Means for new customers.

---

## 📈 Results

- Accuracy: **1.00**
- F1-score: **1.00 across all clusters**
- Perfect confusion matrix (no misclassifications)

This indicates that:
- RFM features clearly separate customer segments,
- Random Forest successfully learned the clustering structure.

---

## 📊 Visualization

- Elbow Method Plot  
- Silhouette Score Plot  
- Cluster Profile Comparison  
- Confusion Matrix  

---

## 💡 Business Recommendations

- **Champions** → VIP programs, retention campaigns  
- **Loyal Customers** → upselling and cross-selling  
- **Potential Loyalists** → engagement and conversion strategies  
- **At Risk** → reactivation campaigns  
- **Hibernating** → win-back offers or reduced marketing spend  

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

---

## 🚀 How to Run

```bash
git clone https://github.com/YOUR_USERNAME/customer-segmentation.git
cd customer-segmentation
pip install -r requirements.txt
jupyter notebook
