# Customer Segmentation with K-Means Clustering

This project is part of the **CodeClause Internship** and focuses on applying unsupervised machine learning techniques to segment customers based on their behaviors and attributes.

## 📌 Objective

The main goal of this project is to analyze customer data and group them into distinct segments using **K-Means Clustering**. This segmentation helps businesses understand their customer base and design targeted marketing strategies.

---

## 📁 Dataset Description

The dataset used in this project contains **1,000 customer records** with the following features:

- `customer_id` : Unique customer identifier (removed during clustering)
- `age` : Age of the customer
- `income` : Annual income
- `spending_score` : Customer's spending behavior
- `visits_per_month` : Number of store visits per month

---

## 🔍 Exploratory Data Analysis (EDA)

- Checked for missing values
- Analyzed basic statistics (mean, std, etc.)
- Visualized income vs spending score to understand behavior distribution

---

## ⚙️ Preprocessing

- Dropped non-numeric columns (like `customer_id`)
- Scaled data using **StandardScaler** to normalize features before clustering

---

## 📊 K-Means Clustering

- Used **Elbow Method** to determine the optimal number of clusters (k)
- Final model used **k = 4** clusters
- Added a new column `Cluster` to label each customer with a cluster ID

**Elbow Plot:**
![image](https://github.com/user-attachments/assets/368f5acd-7782-4dfc-821b-f772125e3bc2)


**Cluster Plot:**
![image](https://github.com/user-attachments/assets/0f7dbe5c-4def-4160-91da-685e6bd4e2d3)


---

## 📈 Results & Insights

Each cluster exhibits different characteristics:

| Cluster | Avg Age | Avg Income | Avg Spending Score | Avg Visits/Month |
|---------|---------|------------|--------------------|------------------|
|   0     | 47.5    | 54,373     | 39.4               | 15.0             |
|   1     | 39.0    | 77,888     | 24.8               | 5.4              |
|   2     | 52.0    | 83,310     | 73.4               | 5.7              |
|   3     | 37.7    | 120,390    | 60.0               | 13.4             |

- **Cluster 0**: Older customers with moderate income and spending, but high visit frequency
- **Cluster 1**: Younger customers with average income and low spending
- **Cluster 2**: Older high spenders with average income
- **Cluster 3**: High-income, high-spending customers visiting frequently

---

## 📁 Output

- Final clustered data saved as: `segmented_customers.csv`

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn (KMeans, StandardScaler)

---

## 🤝 Acknowledgements

- **CodeClause Internship**
- Dataset used is fictional and created for academic and project purposes.

---

## 📎 How to Run

```bash
# Install required packages
pip install pandas numpy matplotlib seaborn scikit-learn

# Run the Python script
python customer_segmentation.py
