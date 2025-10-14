# Project 03: Olympic Medals Analysis & Visualization

This project dives into the Summer Olympics dataset to uncover insights about country performances, medal distributions, and trends over time. Using Python libraries like Pandas for data wrangling and Matplotlib for visualization, we create a series of plots to tell a story with the data.

---

## Project Goal

The main objective is to perform an exploratory data analysis (EDA) on the Olympics dataset. We aim to answer specific questions through data visualization, such as:
- Which countries have dominated the Summer Olympics in terms of total medals?
- What is the distribution of Gold, Silver, and Bronze medals for the top-performing countries?
- How has Iran's performance in the Summer Olympics evolved over the years?

---

## Technical Details & Methodology

The analysis follows several key steps:

1.  **Data Loading & Preprocessing:** The initial dataset is loaded. A crucial step involves creating a `Total` column by summing the `Gold`, `Silver`, and `Bronze` medals for each country to facilitate ranking.

2.  **Filtering & Sorting:**
    - The dataset is filtered to include only countries that have won at least one medal (`Total > 0`).
    - The filtered data is then sorted in descending order based on the `Total` medals to identify the top-performing nations.

3.  **Visualization with Matplotlib:**
    - A **horizontal bar chart** is created to display the top 10 countries with the most total medals.
    - Specific styling is applied to enhance readability and visual appeal:
        - `figure(figsize=(10, 8))`: Sets a custom size for the plot.
        - `plt.style.use('seaborn-v0_8-whitegrid')`: Applies a professional and clean grid style.
        - `barh()`: Used for creating horizontal bars, which is ideal for long labels like country names.
        - `xlabel`, `ylabel`, `title`: Set to provide clear context for the plot.
        - `plt.gca().invert_yaxis()`: Inverts the y-axis to display the top country at the top of the chart.

4.  **Stacked Bar Chart for Medal Breakdown:**
    - A **stacked bar chart** is generated for the top 10 countries to visualize the composition of their total medals (Gold, Silver, and Bronze).
    - This provides a deeper insight than just the total count, showing which countries excel in winning gold.

5.  **Time-Series Analysis (Iran's Performance):**
    - A new DataFrame is created specifically for Iran's performance across different years.
    - A **line plot** is used to visualize the trend of total medals won by Iran in the Summer Olympics over time, showing peaks and troughs in its historical performance.

---

## Technologies & Libraries

- **Python 3.x**
- **Pandas:** For loading, cleaning, and manipulating the dataset (e.g., creating the `Total` column and filtering).
- **Matplotlib:** The core library used for creating all static visualizations, including bar charts, stacked bar charts, and line plots.
- **Jupyter Notebook:** For interactive development, step-by-step execution, and documentation of the analysis.

---

## How to Run

1.  Clone this repository and navigate to the `03-Olympics-Matplotlib-Visualization/` directory.
2.  Ensure you have the required libraries: `pip install pandas matplotlib jupyterlab`
3.  Launch Jupyter Notebook (`jupyter notebook`) and open the `.ipynb` file to view the step-by-step analysis and code.
