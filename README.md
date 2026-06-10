# 🧠 Customer Segmentation using PCA and K-Means Clustering

## 📘 Project Overview
This project focuses on **customer segmentation** using **Principal Component Analysis (PCA)** and **K-Means clustering**.  
The main objective is to identify distinct customer groups based on their purchasing behavior and campaign responses.  
These insights can help businesses **optimize marketing campaigns**, **personalize offers**, and **increase overall profitability**.

---

## 🗂️ Dataset Description
The dataset contains customer demographic, behavioral, and marketing response data.  
Each row represents a unique customer, and the columns include:

| Feature | Description |
|----------|--------------|
| `Year_Birth` | Year of birth of the customer |
| `Income` | Annual household income |
| `Kidhome`, `Teenhome` | Number of children and teenagers in the household |
| `Recency` | Days since the last purchase |
| `MntWines`, `MntMeatProducts`, `MntFruits`, `MntFishProducts`, `MntSweetProducts`, `MntGoldProds` | Amount spent on various product categories in the last 2 years |
| `NumDealsPurchases` | Number of purchases made with a discount |
| `NumWebPurchases`, `NumCatalogPurchases`, `NumStorePurchases` | Number of purchases via web, catalog, or store |
| `NumWebVisitsMonth` | Number of website visits in the last month |
| `AcceptedCmp1`–`AcceptedCmp5`, `Response` | Whether the customer accepted each marketing campaign |
| `Complain` | Whether the customer has complained in the last 2 years |
| `DtCustomer` | Date of enrolment with the company |

---

## ⚙️ Project Workflow

### **1️⃣ Data Preprocessing**
- Selected **numeric features** only.  
- Handled missing values using **median imputation**.  
- Standardized all features using **`StandardScaler()`** to ensure equal weighting in PCA.

### **2️⃣ Dimensionality Reduction (PCA)**
- PCA was applied to reduce the dataset to its principal components.  
- **9 components** were retained, explaining **~70% of total variance**.  
- This helped remove noise and multicollinearity among correlated variables.

### **3️⃣ Clustering (K-Means)**
- K-Means was applied to the PCA-transformed data to group similar customers.  
- The **Elbow Method** and **Silhouette Score** were used to determine the optimal number of clusters.  
- Optimal number of clusters: **k = 3**

### **4️⃣ Evaluation**
- Visualized explained variance and silhouette scores.  
- Analyzed each cluster’s demographic and behavioral profile.

---

## 🎯 Cluster Insights

### **Cluster 0 – The Deal-Seeking Family**
- Families with teenagers, highly motivated by **discounts**  
- Prefer online purchases and responded positively to the **4th campaign**  
- Spend significantly on **wines**

### **Cluster 1 – The High-Spending, Campaign-Responsive Customer**
- **Affluent customers** with high expenditure on **meat, fish, and fruits**  
- Responsive to **1st and 5th campaigns**  
- Represent a key target group for **premium and loyalty marketing**

### **Cluster 2 – The Browsing, Inactive Family**
- Families with children who visit the website frequently  
- **High Recency** → no recent purchases  
- Higher complaint rate but responsive to the **3rd campaign**  
- Hard to engage — may need targeted reactivation strategies

---

## 💡 Key Insights
- PCA effectively reduced dimensionality while retaining major patterns.  
- K-Means revealed **clear, behaviorally distinct customer groups**.  
- Segmentation helps marketers design **personalized, cost-efficient campaigns**.

---

## 🚀 Future Improvements
- Integrate **RFM analysis (Recency, Frequency, Monetary)**  
- Build **predictive response models** for future campaigns  
- Use advanced clustering algorithms like **DBSCAN** or **Gaussian Mixture Models**

---

## 🧰 Tech Stack
- **Programming Language:** Python  
- **Libraries Used:**  
  - `pandas`, `numpy` — data handling  
  - `sklearn` — PCA, KMeans, scaling, and evaluation  
  - `matplotlib`, `seaborn` — visualizations  

---

## 📊 Results Summary
| Step | Method | Outcome |
|------|---------|----------|
| PCA | 9 Components | 70% variance retained |
| Clustering | K-Means | 3 Optimal clusters |
| Evaluation | Elbow + Silhouette | Confirmed stable segmentation |
