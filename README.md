# **Project:** Analyzing Customer Sales Data for a Retail Store

**Author:** Azeem (Data Scientist) | **Date:** 27 / 11 / 2025 | **Email:** azeem.datascientist@gmail.com  
**GitHub:** [My Github Profile Link](https://github.com/azeemdatascientist-hub) | **LinkedIn:** [Your LinkedIn Profile Link]

---

## 🎯 **Business / Project Overview**

*   **Context:** A local retailer, "Islamabad Mart," has given you a messy sales dataset. They want to understand their business performance to make better decisions.
*   **Objective:**\
They have 3 Key Questions;
    1. Who are our top 5 customers by total sales value?
    2. What is our total revenue, and which product category is the most profitable?
    3. On which day of the week do we make the most sales?

*   **Value:** "This analysis transforms raw transactional data into actionable business intelligence. By identifying top customers, high-performing product categories, and peak sales days, Islamabad Mart can optimize marketing spend, inventory planning, and staffing schedules to directly increase profitability."

## 📊 **The Data**

*   **Sources:** The Dataset that is used: `islamabad_mart_sales.csv`.
*   **Description:**
     - This dataset contains transectional sales information, encompassing details about customer purchases, the products involved, and the associated sales matrix.
*   **Initial State:** The Dataset have Quality issues such as (text-formatted dates, missing values, & duplicate records).

## 🔧 **Data Wrangling & Cleaning**


*   **Steps Taken:**
    1.  **Standardized Text Data:** Converted the `Customer Name` column from uppercase to consistent Title Case.
    2.  **Handling Missing Values:** Filled missing values in `Product Category` column with 'Unknown'.
    3.  **Corrected Data Type:** Convert `Date` column from string to datetime format.
    4.  **Removed Duplicates:** Removed 48 duplicate transection records.
    5.  **Feature Engineering**: Created a `DayOfWeek` column to analyze weekly sales pattern.

*   **Final Dataset Shape:** `(1002, 5)`

## 📈 **Analysis & Methodology**


*   **Tools & Libraries:** Python, Pandas, Jupyter Notebook.
*   **Key Analyses Performed:**
    1. **Customer Revenue Ranking:** Used `groupby()` on the `Customer Name` column with `.sum()` and `.sort_values()` to identify the top 5 customers by total sales.
    2. **Product Category performance:** Used `groupby()` on the `Product Category` column to sum sales and find the highest-grossing category.
    3. `Weekly Sales Trends:` Used `.dt.day_name()` to extract the day of the week then, `groupby()` to find the day with the highest total sales.

## 💡 **Key Findings & Business Insights**


*   **Insight 1: Customer Value**
    *   **Finding:** The top 5 customers (`Customer Name: [Ayesha Malik, Sana Farooqi, Ali Raza, Bilal Yousuf, Fatima Khan]`), & the sum of revenue of these 5 customers is **17059829.50 PKR**.
    *   **Recommendation:** Implement a targeted loyalty program for these customers to increase retention.

*   **Insight 2: Product Category**
    *   **Finding:** Product Category with the Highest Total Sales -> `Electronics` with Revenue **6778531.57 PKR**.
    *   **Recommendation:** Focus marketing and inventory investment on the `Electronics` category. Consider discontinuing or promoting underperforming other categories.

*   **Insight 3: Sales by the Day of Week**
    *   **Finding:** Sales peaked on `Saturday`, accounting for approximately **15.06%** of weekly revenue.
    *   **Recommendation:** Schedule additional staff and run targeted promotions or weekend discounts on Fridays and Saturdays to capitalize on this high-demand period.


## **📁 Project Structure**


```
islamabad-mart-sales-analysis/
│
├── data/                    # Contains the dataset
│   └── islamabad_mart_sales.csv
│
├── notebooks/               # Jupyter Notebook with the full analysis
│   └── 01_pandas_project.ipynb
│
├── README.md                # This file
└── .gitignore              # Standard git ignore file
```


## **🚀 How to Run This Project**

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/azeemdatascientist-hub/islamabad-mart-sales-analysis.git
    cd islamabad-mart-sales-analysis
    ```

2.  **Install dependencies:**
    ```bash
    pip install pandas numpy
    ```

3.  **Run the analysis:** Open and execute the cells in `notebooks/01_pandas_project.ipynb` using Jupyter Notebook or VS Code.


## **👁️ Preview of Results**

**Top 5 Customers by Revenue:**
| Customer Name   | Total Sales (PKR) |
|-----------------|-------------------|
| Ayesha Malik    | 3,792,625.49      |
| Sana Farooqi    | 3,419,662.05      |
| Ali Raza        | 3,408,271.56      |
| Bilal Yousuf    | 3,262,560.91      |
| Fatima Khan     | 3,176,709.50      |


 - *These five customers contribute over 66% of the total revenue, highlighting a high-value segment.*


## **🧠 Lessons Learned & Reflections**

*   **Technical:** This project solidified my understanding of core Pandas operations for data cleaning (`str.title()`, `fillna()`, `to_datetime()`, `drop_duplicates()`) and analysis (`groupby`, `sum`, `sort_values`).
*   **Business:** I learned how to translate raw sales data into clear business recommendations, such as focusing loyalty efforts on top customers and aligning staffing with peak sales days.
*   **Challenge:** Initially, I incorrectly tried to filter unique names instead of transforming the entire column. Debugging this error taught me the crucial difference between element-wise operations and filtering in Pandas.

**--->**
*This project is part of my Data Science portfolio. Feedback is welcome!*
