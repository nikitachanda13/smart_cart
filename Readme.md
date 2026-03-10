# 🛒 SmartCart Customer Segmentation System

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Machine Learning](https://img.shields.io/badge/Machine-Learning-orange)
![Scikit-Learn](https://img.shields.io/badge/Library-ScikitLearn-green)
![Status](https://img.shields.io/badge/Project-Completed-success)

A **Machine Learning project** that performs **customer segmentation using K-Means clustering** to identify groups of customers based on their purchasing behaviour.

The goal of this project is to help businesses improve **targeted marketing, customer engagement, and customer retention strategies**.

---

# 📌 Project Overview

SmartCart is a growing e-commerce platform that serves customers across multiple countries. The company has collected a dataset containing **2240 customer records and 22 attributes**, including:

* Customer demographics
* Purchase behaviour
* Website activity
* Customer engagement

Currently, SmartCart uses **generic marketing strategies** for all customers. This leads to:

* Inefficient marketing campaigns
* Missed opportunities to retain high-value customers
* Difficulty identifying customers who may stop purchasing

This project builds a **customer segmentation system using unsupervised machine learning** to discover patterns in customer behaviour and group customers into meaningful clusters.

---

# 🎯 Objectives

The objectives of this project are:

* Analyze customer behaviour patterns
* Segment customers into meaningful groups
* Identify high-value customers
* Improve targeted marketing strategies
* Support data-driven business decisions

---

# 📊 Dataset Description

The dataset contains **2240 customers and 22 features**.

Each row represents a **single customer** and includes demographic information, purchasing behaviour, and engagement metrics.

## 1️⃣ Customer Demographics

| Feature        | Description                |
| -------------- | -------------------------- |
| ID             | Unique customer identifier |
| Year_Birth     | Year of birth              |
| Education      | Education level            |
| Marital_Status | Marital status             |
| Income         | Yearly household income    |
| Kidhome        | Number of children         |
| Teenhome       | Number of teenagers        |
| Dt_Customer    | Date customer joined       |

---

## 2️⃣ Purchase Behaviour (Amount Spent)

| Feature          | Description                   |
| ---------------- | ----------------------------- |
| MntWines         | Amount spent on wine          |
| MntFruits        | Amount spent on fruits        |
| MntMeatProducts  | Amount spent on meat          |
| MntFishProducts  | Amount spent on fish          |
| MntSweetProducts | Amount spent on sweets        |
| MntGoldProds     | Amount spent on gold products |

---

## 3️⃣ Purchase Behaviour (Frequency)

| Feature             | Description                    |
| ------------------- | ------------------------------ |
| NumDealsPurchases   | Purchases made using discounts |
| NumWebPurchases     | Purchases through website      |
| NumCatalogPurchases | Purchases through catalog      |
| NumStorePurchases   | Purchases in physical store    |
| NumWebVisitsMonth   | Website visits per month       |

---

## 4️⃣ Customer Feedback

| Feature  | Description                                       |
| -------- | ------------------------------------------------- |
| Recency  | Days since last purchase                          |
| Complain | Whether the customer complained (1 = Yes, 0 = No) |

---

# ⚙️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* K-Means Clustering
* Jupyter Notebook

---

# 🧠 Machine Learning Approach

## 1️⃣ Data Preprocessing

The following preprocessing steps were performed:

* Handling missing values
* Converting categorical variables
* Feature scaling
* Feature selection

---

## 2️⃣ Finding the Optimal Number of Clusters

The **Elbow Method** was used to determine the optimal number of clusters by calculating **WCSS (Within Cluster Sum of Squares)**.

Example code used:

```python
wcss = []

for i in range(1,11):
    kmeans = KMeans(n_clusters=i)
    kmeans.fit(X)
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11), wcss, marker='o')
plt.xlabel("Number of Clusters")
plt.ylabel("WCSS")
plt.title("Elbow Method")
plt.show()
```

---

# 📊 Customer Segmentation Insights

After applying **K-Means clustering**, customers can be grouped into different segments such as:

### 🟢 High Value Customers

* High spending across product categories
* Frequent purchases
* Loyal customers

### 🟡 Discount Sensitive Customers

* Prefer buying during discounts
* Highly price sensitive

### 🔵 Regular Customers

* Moderate spending behaviour
* Consistent purchases

### 🔴 Low Engagement Customers

* Rare purchases
* Low website activity

These insights can help businesses design **personalized marketing strategies**.

---

# 📂 Project Structure

```
SmartCart-Clustering
│
├── smart_cart.ipynb
├── smartcart_customers.csv
└── README.md
```

---

# ▶️ How to Run the Project

### 1️⃣ Clone the Repository

```
git clone https://github.com/your-nikitachanda13/smartcart-clustering.git
```

### 2️⃣ Navigate to the Project Folder

```
cd smartcart-clustering
```

### 3️⃣ Install Required Libraries

```
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 4️⃣ Open the Notebook

Run the following command:

```
jupyter notebook
```

Then open:

```
smart_cart.ipynb
```

Run all cells to reproduce the analysis and clustering results.

---

# 🚀 Future Improvements
n
Possible future improvements include:

* Applying **PCA (Principal Component Analysis)** for dimensionality reduction
* Building a **data visualization dashboard**
* Deploying the model using **Streamlit**
* Trying other clustering algorithms like **DBSCAN** or **Hierarchical Clustering**

---

# 👩‍💻 Author

**Nikita Chanda**


* Machine Learning Enthusiast
* Interested in AI, Data Science

---

⭐ If you found this project useful, consider **starring the repository**!
