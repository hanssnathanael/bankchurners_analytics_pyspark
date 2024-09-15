<h1 align="center">Big Data Analytics with PySpark: Bank Churner Dataset</h1>
<p align="center" style="font-size: 25px">💼💳💼💳💼</p>

## 🧰 Tools
- PySpark
- Python
- Pandas
- Numpy
- Matplotlib
- Seaborn
- SQL

## 📊 Project Overview
This project involves the exploration, transformation, and visualization of the **Bank Churner** dataset using PySpark. It aims to analyze customer behavior, specifically focusing on transaction patterns, customer demographics, and key metrics that may influence customer attrition.

## 🗂️ Documentation


### 1. Data Transformation (Results)
   - **Average Transaction Amount by Age Group**
     This analysis highlights how different age groups engage in transactions, providing insights into customer segments.

   - **Correlation Heatmap**
     A correlation matrix is generated to understand the relationships between key numeric variables, such as `Customer_Age`, `Total_Trans_Amt`, `Total_Trans_Ct`, and `Total_Revolving_Bal`.

   - **Customer Attrition Analysis**
     A breakdown of customers by attrition status, visualizing important features like transaction count and revolving balance.

     <b>Attrited vs. Active Customers - Total Transactions</b>        
    

### 3. Visualization Examples
   - **Distribution of Customer Age**
     A histogram that visualizes the age distribution of customers in the dataset.


   - **Average Transaction Amount by Gender**
     A bar chart showing the differences in transaction amounts between male and female customers.


   - **Transaction Patterns by Card Category**
     This visualization shows the total transaction amounts across different credit card categories.


### 4. Advanced Statistical Analysis
   - **Correlation between Variables**
     Using Pearson’s correlation, we analyze the relationships between key customer attributes.

     ```python
     from pyspark.mllib.stat import Statistics
     
     rdd_table = df_features.rdd.map(lambda row: Vectors.dense([row["Customer_Age"], row["Total_Trans_Amt"], row["Total_Trans_Ct"], row["Total_Revolving_Bal"]]))
     corr_mat = Statistics.corr(rdd_table, method="pearson")
     ```

   - **Statistical Insights**
     This section focuses on detailed statistical analysis, including standard deviations, correlations, and summary statistics.


### 5. Conclusion
Through this project, we explored the Bank Churner dataset using PySpark, and derived key insights into customer behavior, attrition risk, and transactional patterns. The visualizations and transformations highlighted key metrics that businesses can leverage to improve customer retention strategies.

---

## 🚀 How to Run This Project
1. Clone the repository:
   ```bash
   git clone https://github.com/hanssnathanael/big-data-analytics-pyspark.git
