# Customer Churn Analysis

## 📌 Project Overview

This project focuses on analyzing customer data to understand **customer churn** using Python and data analysis techniques.

The project uses the **Churn Modelling dataset**, which contains information about customers such as credit score, geography, gender, age, balance, number of products, and activity status.

The main focus of this project is **data loading, data exploration, missing value detection, and missing value handling**.

## 🎯 Objectives

* Load the customer churn dataset.
* Understand the structure and characteristics of the dataset.
* Identify missing values.
* Analyze missing values in different columns.
* Handle missing values using appropriate techniques.
* Prepare the dataset for further Machine Learning analysis.

## 📂 Dataset

The dataset contains **10,000 customer records** and **14 columns**.

### Features

| Column            | Description                                         |
| ----------------- | --------------------------------------------------- |
| `RowNumber`       | Row number of the customer                          |
| `CustomerId`      | Unique customer identification number               |
| `Surname`         | Customer surname                                    |
| `CreditScore`     | Customer credit score                               |
| `Geography`       | Customer's country/region                           |
| `Gender`          | Customer gender                                     |
| `Age`             | Customer age                                        |
| `Tenure`          | Number of years the customer has been with the bank |
| `Balance`         | Customer account balance                            |
| `NumOfProducts`   | Number of bank products used                        |
| `HasCrCard`       | Indicates whether the customer has a credit card    |
| `IsActiveMember`  | Indicates whether the customer is an active member  |
| `EstimatedSalary` | Estimated customer salary                           |
| `Exited`          | Indicates whether the customer left the bank        |

### Target Variable

`Exited`

* `0` → Customer stayed
* `1` → Customer exited

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Google Colab
* GitHub

## 🔄 Project Workflow

The project follows these steps:

1. Import required Python libraries.
2. Load the CSV dataset.
3. Explore the dataset using `df.info()`.
4. Check for missing values using `isnull().sum()`.
5. Identify columns containing missing values.
6. Analyze the mean and median of the `Age` column.
7. Handle missing `Age` values using mean imputation.
8. Prepare the dataset for further analysis and Machine Learning.

## 🔍 Data Exploration

The dataset contains:

* **10,000 rows**
* **14 columns**
* Numerical and categorical features
* Missing values in `Gender` and `Age`

Missing values found:

| Column   | Missing Values |
| -------- | -------------: |
| `Gender` |             47 |
| `Age`    |             66 |

All other columns contain no missing values.

## 🧹 Missing Value Handling

The missing values in the `Age` column are handled using **mean imputation**.

The calculated mean age is approximately:

```text
38.92
```

The missing values are replaced using:

```python
df['Age'] = df['Age'].fillna(df['Age'].mean())
```

After imputation, the `Age` column contains **10,000 non-null values**.

## 📊 Mean and Median Analysis

The project also calculates the mean and median of the `Age` column.

```python
df['Age'].mean()
```

Output:

```text
38.92208576605597
```

```python
df['Age'].median()
```

Output:

```text
37.0
```

## 📁 Project Structure

```text
customer-churn-analysis/
│
├── Churn_Modelling.csv
├── customer_churn_analysis.ipynb
├── README.md
└── requirements.txt
```

## 📦 Installation

Install the required libraries:

```bash
pip install pandas numpy matplotlib
```

## ▶️ How to Run

1. Clone or download this repository.
2. Open the Jupyter Notebook or Google Colab.
3. Upload the `Churn_Modelling.csv` dataset.
4. Run the Python cells step by step.
5. Check the dataset information and missing value results.
6. Continue with further data analysis or Machine Learning.

## 🚀 Future Improvements

The project can be extended by:

* Handling missing `Gender` values.
* Removing unnecessary columns.
* Encoding categorical variables.
* Performing exploratory data analysis (EDA).
* Creating visualizations.
* Splitting the dataset into training and testing sets.
* Training Machine Learning models.
* Predicting customer churn.
* Evaluating model performance using accuracy, precision, recall, and confusion matrix.

## 👩‍💻 Author

**Arockiya Jeniliya J**

BCA Student | Machine Learning & Web Development Enthusiast

## 📜 License

This project is created for **educational and academic purposes**.
