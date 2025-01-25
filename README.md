# Zeotap-Assignment

Here’s a **README-style explanation** of the **Jupyter Notebook** for the **Customer Segmentation** task. This explanation provides an overview of the task, the steps performed, and the insights derived.

---

## **Customer Segmentation using Clustering**

### **Overview**
This notebook performs **customer segmentation** using clustering techniques. The goal is to group customers based on their profile and transaction behavior to derive actionable business insights. The dataset includes:
- **Customers.csv**: Customer profile information.
- **Transactions.csv**: Transaction details.
- **Products.csv**: Product information.

The notebook follows these steps:
1. **Data Preparation**: Load and merge datasets.
2. **Feature Engineering**: Create customer profiles using transaction and product data.
3. **Clustering**: Use K-Means clustering to segment customers.
4. **Evaluation**: Evaluate clustering using metrics like the Davies-Bouldin Index and Silhouette Score.
5. **Visualization**: Visualize clusters using PCA and interactive plots.
6. **Business Insights**: Derive insights from the clusters.

---

### **Steps Performed**

#### **1. Data Preparation**
- Loaded `Customers.csv`, `Transactions.csv`, and `Products.csv`.
- Merged the datasets on `CustomerID` and `ProductID` to create a unified dataset.

#### **2. Feature Engineering**
- Created customer profiles by aggregating transaction data:
  - **Total Spending**: Sum of `TotalValue` for each customer.
  - **Total Quantity Purchased**: Sum of `Quantity` for each customer.
  - **Average Product Price**: Mean of `Price` for each customer.
  - **Most Purchased Category**: Mode of `Category` for each customer.
  - **Customer Tenure**: Calculated as the number of days since the customer signed up.
- One-hot encoded categorical features (`Region` and `Category`).
- Normalized numerical features using `StandardScaler`.

#### **3. Clustering**
- Used **K-Means clustering** to segment customers into groups.
- Determined the optimal number of clusters using the **Elbow Method** or **Silhouette Score**.

#### **4. Evaluation**
- Evaluated clustering using:
  - **Davies-Bouldin Index**: Measures the quality of clustering (lower is better).
  - **Silhouette Score**: Measures how similar a customer is to their own cluster compared to other clusters (higher is better).

#### **5. Visualization**
- Reduced dimensionality using **PCA** to visualize clusters in 2D space.
- Created static plots using **Matplotlib** and interactive plots using **Plotly**.

#### **6. Business Insights**
- Analyzed the characteristics of each cluster to derive actionable insights:
  - **High-Spending Customers**: Identify customers with high total spending.
  - **Frequent Buyers**: Identify customers who purchase frequently.
  - **Loyal Customers**: Identify customers with long tenure.
  - **Category Preferences**: Identify customers with a preference for specific product categories.

---

### **Key Insights**

#### **1. Total Spending by Region**
- **Insight**: Identify which region contributes the most to total sales.
- **Visualization**: Bar chart showing total spending by region.

#### **2. Average Transaction Value by Region**
- **Insight**: Compare the average transaction value across regions.
- **Visualization**: Bar chart showing average transaction value by region.

#### **3. Most Purchased Product Categories**
- **Insight**: Identify the most popular product categories.
- **Visualization**: Bar chart showing the number of purchases per category.

#### **4. Customer Tenure Distribution**
- **Insight**: Analyze how long customers have been with the company.
- **Visualization**: Histogram showing the distribution of customer tenure.

#### **5. Total Spending vs. Quantity Purchased**
- **Insight**: Explore the relationship between total spending and quantity purchased.
- **Visualization**: Scatter plot showing total spending vs. quantity purchased.

#### **6. Cluster Characteristics**
- **Insight**: Analyze the characteristics of each cluster (e.g., high spenders, frequent buyers, loyal customers).
- **Visualization**: PCA plot showing customer clusters.

---

### **Deliverables**
1. **Jupyter Notebook**:
   - Contains the complete code for data preparation, feature engineering, clustering, evaluation, and visualization.

2. **Clustering Metrics**:
   - Davies-Bouldin Index and Silhouette Score for evaluating clustering quality.

3. **Visualizations**:
   - Static plots (Matplotlib) and interactive plots (Plotly) for cluster visualization.

4. **Business Insights**:
   - Summary of key insights derived from the clusters.

---

### **How to Use the Notebook**
1. **Install Dependencies**:
   - Ensure the required libraries are installed:
     ```bash
     pip install pandas scikit-learn matplotlib seaborn plotly
     ```

2. **Run the Notebook**:
   - Open the notebook in Jupyter or any compatible environment.
   - Execute each cell sequentially to perform the analysis.

3. **Customize**:
   - Adjust the number of clusters or feature engineering options as needed.

---

### **Evaluation Criteria**
1. **Clustering Logic**:
   - The choice of clustering algorithm and number of clusters is justified.

2. **Clustering Metrics**:
   - The Davies-Bouldin Index and Silhouette Score are calculated and interpreted.

3. **Visualization**:
   - Clusters are visualized using PCA and interactive plots.

4. **Business Insights**:

   - Insights are derived from the clusters and presented clearly.

