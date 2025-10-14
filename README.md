# Project 01: COVID-19 Exploratory Data Analysis with Pandas

This project performs an in-depth exploratory data analysis (EDA) on a global COVID-19 dataset from November 2020. Using the Pandas library, the dataset is cleaned, transformed, and analyzed to answer specific questions about the state of the pandemic.

---

## Key Questions & Analysis Steps

The core of this project was to answer several key questions through data manipulation. The main steps performed in the analysis were:

1.  **Calculating Recovery Rate:**
    *   A new column, `Recovery_Rate`, was created by dividing the number of `Recovered` cases by the number of `Confirmed` cases. This provides a crucial metric for understanding outcomes. The result was saved to `recovery_rate.csv`.

2.  **Calculating Incident Rate:**
    *   To normalize the data across countries with different populations, the `Incident_Rate` per 100,000 people was calculated. This was achieved using the `.apply()` method on the `Total_Cases` column.

3.  **Identifying Top Affected Countries:**
    *   The dataset was filtered to identify the top 10 countries with the highest number of total confirmed cases. This subset of data was exported to `top10cases.csv`.

4.  **Comparative Analysis with Iran:**
    *   A specific analysis was conducted to compare Iran's COVID-19 statistics against other countries in the dataset. The results were saved in `vsiran.csv`.

5.  **Advanced Filtering:**
    *   The data was filtered to create a new dataframe containing only countries with more than 20,000 deaths, providing insights into the most severely impacted nations. This was saved as `20percent.csv`.

---

## Dataset & Generated Files

The primary dataset is a snapshot of the COVID-19 pandemic from **November 11, 2020**. During the analysis, the following derivative datasets were generated and saved as `.csv` files inside the `data/` directory:

-   `recovery_rate.csv`
-   `top10cases.csv`
-   `vsiran.csv`
-   `20percent.csv`

---

## 🛠️ Technologies & Libraries Used

-   **Python 3.x**
-   **Pandas:** For all data manipulation, cleaning, and analysis tasks.
-   **NumPy:** For numerical operations.
-   **Jupyter Notebook:** As the interactive development environment.

---

## How to Run the Project

1.  **Clone the repository:**
```bash
git clone https://github.com/YourUsername/ML-Bootcamp-Projects.git
cd ML-Bootcamp-Projects/COVID-19-analysis-project

