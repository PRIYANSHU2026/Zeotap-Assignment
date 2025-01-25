# **Zeotap Assignment: Customer Segmentation**  
**By: Priyanshu Tiwari**  

---

## **Overview**  
This notebook performs **customer segmentation** using clustering techniques to group customers based on their profiles and transaction behavior. The datasets used include:  
- **Customers.csv**: Customer profiles.  
- **Transactions.csv**: Transaction details.  
- **Products.csv**: Product information.  

**Note**: Please also consider the file **`PRIYANSHU_TIWARI_ALL_trainning_and_test__Lookalike.ipynb`** for a comprehensive view of my work, including training, testing, and evaluation steps.  

---

## **Steps Performed**  

### **1. Data Preparation**  
- Loaded and merged `Customers.csv`, `Transactions.csv`, and `Products.csv` on `CustomerID` and `ProductID`.  

### **2. Feature Engineering**  
- Created customer profiles:  
  - **Total Spending**: Sum of `TotalValue`.  
  - **Total Quantity Purchased**: Sum of `Quantity`.  
  - **Average Product Price**: Mean of `Price`.  
  - **Most Purchased Category**: Mode of `Category`.  
  - **Customer Tenure**: Days since sign-up.  
- One-hot encoded categorical features (`Region` and `Category`).  
- Normalized numerical features using `StandardScaler`.  

### **3. Clustering**  
- Applied **K-Means clustering** to segment customers.  
- Determined optimal clusters using the **Elbow Method** or **Silhouette Score**.  

### **4. Evaluation**  
- Evaluated clustering using:  
  - **Davies-Bouldin Index**: Lower values indicate better clustering.  
  - **Silhouette Score**: Higher values indicate well-defined clusters.  

### **5. Visualization**  
- Reduced dimensionality using **PCA** for 2D cluster visualization.  
- Created **static plots** with **Matplotlib** and **interactive plots** with **Plotly**.  

### **6. Business Insights**  
- Analyzed clusters to identify:  
  - **High-Spending Customers**: High total spending.  
  - **Frequent Buyers**: High purchase frequency.  
  - **Loyal Customers**: Long tenure.  
  - **Category Preferences**: Preferred product categories.  

---

## **Key Insights**  

1. **Total Spending by Region**: Identified top-performing regions.  
2. **Average Transaction Value**: Compared transaction values across regions.  
3. **Most Purchased Categories**: Determined popular product categories.  
4. **Customer Tenure Distribution**: Analyzed customer loyalty.  
5. **Cluster Profiles**: Profiled clusters (e.g., high spenders, frequent buyers).  

---

## **Deliverables**  

1. **Jupyter Notebook**: Complete analysis code.  
2. **Clustering Metrics**: Davies-Bouldin Index and Silhouette Score.  
3. **Visualizations**: PCA plots (static and interactive).  
4. **Business Insights**: Actionable summaries of cluster characteristics.  

---

## **How to Use**  

1. **Install Dependencies**:  
   ```bash  
   pip install pandas scikit-learn matplotlib seaborn plotly  
   ```  
2. **Run the Notebook**: Execute cells sequentially.  
3. **Customize**: Adjust clustering parameters or features as needed.  

---

## **Evaluation Criteria**  

1. **Clustering Logic**: Justification for algorithm and cluster count.  
2. **Clustering Metrics**: Interpretation of Davies-Bouldin Index and Silhouette Score.  
3. **Visualization**: Effective use of PCA and interactive plots.  
4. **Business Insights**: Clear and actionable insights derived from clusters.  

---

**Highlight**: Please refer to **`PRIYANSHU_TIWARI_ALL_trainning_and_test__Lookalike.ipynb`** for a detailed view of my work, including training, testing, and evaluation steps.  

--- 

✨ **Thank you for considering my work!** ✨
