# Zeotap Assignment: Customer Segmentation

## Overview
This notebook performs **customer segmentation** using clustering to group customers based on profiles and transaction behavior. Datasets used:
- **Customers.csv**: Customer profiles.
- **Transactions.csv**: Transaction details.
- **Products.csv**: Product information.

---

## Steps
1. **Data Prep**: Load and merge datasets.
2. **Feature Engineering**: Create customer profiles (e.g., total spending, tenure, most purchased category).
3. **Clustering**: Use K-Means to segment customers. Optimal clusters determined via Elbow Method or Silhouette Score.
4. **Evaluation**: Assess clustering with Davies-Bouldin Index and Silhouette Score.
5. **Visualization**: Plot clusters using PCA (Matplotlib/Plotly).
6. **Insights**: Analyze clusters for actionable insights (e.g., high spenders, loyal customers).

---

## Key Insights
1. **Total Spending by Region**: Top-performing regions.
2. **Average Transaction Value**: Compare across regions.
3. **Popular Categories**: Most purchased product categories.
4. **Customer Tenure**: Loyalty analysis.
5. **Cluster Profiles**: High spenders, frequent buyers, etc.

---

## Deliverables
1. **Notebook**: Complete analysis code.
2. **Metrics**: Davies-Bouldin Index, Silhouette Score.
3. **Visuals**: PCA plots (static/interactive).
4. **Insights**: Actionable cluster summaries.

---

## How to Use
1. Install dependencies:
   ```bash
   pip install pandas scikit-learn matplotlib seaborn plotly
   ```
2. Run the notebook and customize as needed.
