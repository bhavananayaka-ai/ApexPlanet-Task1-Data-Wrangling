# ApexPlanet Data Analytics Internship – Task 1

## Data Immersion & Wrangling

### 📌 Project Overview

This project is completed as part of the **ApexPlanet Software Pvt. Ltd. 60-Day Data Analytics Internship Program**.

**Task 1: Data Immersion & Wrangling** focuses on understanding, assessing, cleaning, transforming, and preparing a sales dataset for further data analysis.

The objective is to convert the raw dataset into a reliable and analysis-ready dataset by identifying and addressing data quality issues.

---

## 🎯 Objectives

The main objectives of this task are:

* Understand and familiarize myself with the dataset.
* Identify the meaning and relevance of each variable.
* Create a data dictionary.
* Assess the quality of the dataset.
* Identify missing values and duplicate records.
* Check data types and formatting consistency.
* Detect potential outliers.
* Validate important numerical calculations.
* Clean and transform the dataset.
* Perform feature engineering.
* Produce a final analysis-ready dataset.

---

## 📊 Dataset Description

The dataset contains **sales transaction records** with information related to orders, customers, products, pricing, quantities, and sales values.

### Main Variables

| Column        | Description                         |
| ------------- | ----------------------------------- |
| `Order_ID`    | Unique identifier for a sales order |
| `Order_Date`  | Date on which the order was placed  |
| `Customer_ID` | Unique customer identifier          |
| `Gender`      | Gender of the customer              |
| `Age`         | Age of the customer                 |
| `City`        | Customer's city                     |
| `Product`     | Product purchased                   |
| `Category`    | Product category                    |
| `Quantity`    | Number of units purchased           |
| `Unit_Price`  | Price per unit                      |
| `Total_Sales` | Total value of the transaction      |

A detailed data dictionary is included in the repository.

---

## 🛠️ Technologies Used

* **Python**
* **Google Colab**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Microsoft Excel**
* **GitHub**

---

# 🔍 Data Immersion

The dataset was first loaded into Python using Pandas.

The initial exploration included:

* Number of rows and columns
* Column names
* Data types
* First few records
* Statistical summary
* Unique values
* Missing-value analysis

The dataset contains **1,000 records and 12 original columns**.

---

# 🔎 Data Quality Assessment

Several data-quality checks were performed.

### 1. Missing Values

Missing values were checked for every column.

The dataset contained missing values in fields such as:

* `Age`
* `City`

These missing values were handled during the cleaning stage.

### 2. Duplicate Records

Exact duplicate rows were checked using Pandas.

No exact duplicate transaction rows were identified.

Duplicate `Order_ID` values were also investigated separately because an identifier should ideally be unique.

### 3. Date Validation

The `Order_Date` column was converted into a standard datetime format using Pandas.

Invalid date values were also checked.

### 4. Categorical Consistency

Categorical fields such as:

* Gender
* City
* Product
* Category

were examined for inconsistent values and unnecessary whitespace.

### 5. Outlier Detection

The **Interquartile Range (IQR)** method was used to identify potential outliers in numerical variables such as:

* Age
* Quantity
* Unit Price
* Total Sales

Potential high-value sales transactions were investigated rather than automatically removed.

---

# 🧹 Data Cleaning

The following cleaning operations were performed.

### Missing Age

Missing values in `Age` were replaced using the **median age**.

Median imputation was selected because it is less sensitive to extreme values than the mean.

### Missing City

Missing values in `City` were replaced using the **mode**, which represents the most frequently occurring city.

### Duplicate Rows

Exact duplicate rows were removed using:

```python
df.drop_duplicates()
```

### Duplicate Order IDs

Repeated `Order_ID` values were investigated.

The repeated records represented different transactions rather than identical rows, so they were not simply deleted. Unique identifiers were created for the affected records.

### Text Standardization

Text fields were cleaned by removing unnecessary leading and trailing whitespace.

### Date Standardization

`Order_Date` was converted into a proper datetime format.

### Total Sales Validation

The `Total_Sales` column was validated using:

```text
Total Sales = Quantity × Unit Price
```

The calculation was checked to ensure the recorded sales values were consistent with the quantity and unit price.

---

# ⚙️ Feature Engineering

Additional features were created to make the dataset more useful for future analysis.

### Order Year

Extracted from `Order_Date`.

```text
Order_Year
```

### Order Month

Extracted as the numerical month.

```text
Order_Month
```

### Order Month Name

The month name was extracted for easier reporting.

```text
Order_Month_Name
```

### Age Group

Customers were grouped into age categories:

* Under 18
* 18–30
* 31–45
* 46–60
* 60+

---

# 📈 Outlier Treatment

Outliers were detected using the **IQR method**.

Potential outliers in `Total_Sales` were not automatically removed.

The reason is that a high-value transaction can be a legitimate business transaction rather than a data-entry error.

Therefore, valid high-value sales were retained in the cleaned dataset.

---

# ✅ Final Data Validation

After cleaning, the dataset was checked again for:

* Missing values
* Duplicate rows
* Duplicate identifiers
* Correct data types
* Valid dates
* Correct sales calculations
* Consistent categorical values

The resulting dataset is prepared as an **analysis-ready dataset** for future exploratory data analysis and business intelligence tasks.

---

# 📁 Repository Structure

```text
ApexPlanet-Task1-Data-Wrangling/
│
├── ApexPlanet_Task1_Data_Wrangling.ipynb
│
├── ApexPlanet_Task1_Cleaned_Sales_Dataset.csv
│
├── ApexPlanet_Task1_Data_Dictionary.xlsx
│
├── ApexPlanet_Task1_Cleaning_Summary.xlsx
│
└── README.md
```

---

# 📄 Deliverables

The following deliverables were prepared for Task 1:

### GitHub

* Data cleaning and wrangling notebook
* Cleaned dataset
* Data dictionary
* Cleaning summary
* Project documentation

### LinkedIn

A **3–5 minute walkthrough video** will demonstrate:

1. Dataset introduction
2. Data quality issues
3. Missing-value analysis
4. Duplicate analysis
5. Outlier detection
6. Cleaning process
7. Feature engineering
8. Final cleaned dataset

---

# 🎓 Key Skills Demonstrated

Through this task, the following skills were practiced:

* Data Loading
* Data Exploration
* Data Profiling
* Data Quality Assessment
* Missing Data Handling
* Duplicate Detection
* Data Cleaning
* Data Transformation
* Date Handling
* Outlier Detection
* Feature Engineering
* Data Validation
* Python
* Pandas
* NumPy
* Data Visualization
* GitHub Project Documentation

---

# 🚀 Conclusion

Task 1 successfully demonstrates the complete initial stage of a data analytics workflow, from understanding the raw sales dataset to cleaning, validating, transforming, and preparing the final dataset for analysis.

The cleaned dataset can now be used for further **Exploratory Data Analysis (EDA), SQL analysis, business intelligence, and dashboard development** in the subsequent internship tasks.

---

## 👩‍💻 Internship

**ApexPlanet Software Pvt. Ltd.**

**Program:** 60-Day Data Analytics Internship

**Task:** Task 1 – Data Immersion & Wrangling

**Tools:** Python | Pandas | NumPy | Matplotlib | Seaborn | Google Colab | GitHub

