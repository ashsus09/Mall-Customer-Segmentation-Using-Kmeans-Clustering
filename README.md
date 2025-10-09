# 🛍️ Mall Customer Segmentation using KMeans

This project performs **Customer Segmentation** on the **Mall Customers dataset** using **KMeans Clustering**.  
The main objective is to group mall customers into distinct clusters based on their **Age, Gender, Annual Income, and Spending Score**, which helps businesses identify different customer groups and target them with personalized marketing strategies.

---

## 🚀 Features
- Exploratory Data Analysis (EDA) with visualizations  
- Gender distribution and spending analysis  
- **Elbow Method & Silhouette Score** to find the optimal number of clusters  
- KMeans clustering implementation  
- **2D & 3D visualizations** of customer clusters  
- Cluster profiling with **business insights**  

---

## 📂 Dataset

The dataset contains **200 mall customers** with the following features:

| Feature               | Description                                |
|------------------------|--------------------------------------------|
| **CustomerID**        | Unique ID                                  |
| **Gender**            | Male / Female                              |
| **Age**               | Customer’s age                             |
| **Annual Income (k$)**| Annual income in thousand dollars          |
| **Spending Score (1–100)** | Score assigned based on spending behavior |

---

## ⚙️ Installation & Setup

Clone the repository:
```bash
git clone https://github.com/ashsus09/Mall-Customer-Segmentation-Using-Kmeans-Clustering.git
cd Mall-Customer-Segmentation-Using-Kmeans-Clustering
```

Install dependencies:
```bash
pip install -r requirements.txt
```

**requirements.txt**
```
pandas
numpy
matplotlib
seaborn
scikit-learn
```

---

## 📊 Exploratory Data Analysis (EDA)

- Visualized **Age distribution, Annual Income, and Spending Scores**.  
- Compared **Gender distribution** across spending categories.  
- Found that **Gender does not significantly affect cluster results** (clusters are mainly driven by Income and Spending Score).  

**Example Visualization:**  
📈 Histograms, scatter plots, and distribution plots for customer insights.  

---

## 🤖 Clustering Process

### Elbow Method
- Plotted **WCSS (Within-Cluster Sum of Squares)** to determine the best number of clusters.  
- Found **optimal clusters = 5**.  

### Apply KMeans
```python
from sklearn.cluster import KMeans

kmeans = KMeans(n_clusters=5, random_state=42)
df['Cluster'] = kmeans.fit_predict(df[['Annual Income (k$)', 'Spending Score (1–100)']])
```

### Visualize Clusters
- Scatter plots for **Income vs Spending Score**.  
- 3D plots for **Age vs Income vs Spending Score**.  

---

## 📑 Cluster Profiling

| Cluster | Profile                        | Description                               |
|---------|--------------------------------|-------------------------------------------|
| **0**   | High Income, High Spending     | VIP Customers                             |
| **1**   | Low Income, Low Spending       | Budget Customers                          |
| **2**   | High Income, Low Spending      | Careful Spenders                          |
| **3**   | Average Income, Average Spending | Mid-range Customers                     |
| **4**   | Low Income, High Spending      | Young / Impulsive Shoppers                |

---

## 📈 Business Insights

- Target **VIP Customers** with **loyalty programs**.  
- Provide **discounts/offers** to budget-conscious shoppers.  
- Upsell **high-income careful spenders** with premium options.  
- Improve engagement strategies for each cluster group.  

---

## 🔮 Future Improvements
- Use other clustering techniques (**DBSCAN, Hierarchical, Gaussian Mixture**).  
- Apply **PCA / t-SNE** for dimensionality reduction and better visualization.  
- Build an **interactive dashboard** using Streamlit or Dash.  
- Test clustering with additional features (e.g., purchase history).  

---

## 👨‍💻 Author
**Aastha**  
GitHub: [@ashsus09](https://github.com/ashsus09)  
