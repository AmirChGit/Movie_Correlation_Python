# Movie Industry Data Analysis Project

## Overview
This project uses Python to analyze a movie industry dataset, focusing on exploring the correlations between various features and movie revenue. The project leverages popular libraries such as Pandas, Seaborn, and Matplotlib to clean, manipulate, and visualize the data.

## Project Setup
1. **Download the Dataset**: Obtain the dataset from [Kaggle](https://www.kaggle.com). The dataset includes features like budget, company, genre, gross revenue, movie name, release date, and more.
2. **Install Anaconda**: Anaconda is used to set up a Jupyter Notebook environment, which is ideal for interactive data analysis in Python.

## Steps and Workflow
### 1. Setting Up the Environment
- **Launch Jupyter Notebook**: Use Anaconda to open Jupyter Notebook for coding and analysis.
- **Import Libraries**:
  - `pandas` for data manipulation.
  - `seaborn` and `matplotlib` for data visualization.

### 2. Loading the Data
- Use `pandas`' `read_csv()` function to load the dataset into a DataFrame.
- **Handle File Path Issues**: If you encounter a Unicode error, add an 'r' before the file path to fix it.

### 3. Checking for Missing Data
- Use a loop to iterate through each column and check for missing values with `numpy`'s `isnull()` function.
- The initial check reveals no missing values in this dataset.

### 4. Data Cleaning
- **Adjust Data Types**: Convert the `budget` and `gross revenue` columns to integers to remove unnecessary decimal points.
- **Resolve Year Inconsistencies**:
  - There is a discrepancy between the `year` column and the `released date` column.
  - Create a new `yearreleased` column by extracting the year from `released date` using string slicing. This ensures consistency in the year representation.

### 5. Data Analysis
- **Sorting Data**: Sort the dataset by `gross revenue` to identify the highest-grossing films. This analysis shows that higher-budget movies tend to generate more revenue.
- **Adjust Pandas Settings**: Modify the settings to display all rows in the DataFrame for better data visibility.

### 6. Checking for Data Inconsistencies
- While there are no duplicate company names, it's crucial to watch for inconsistencies, such as variations in the company name due to mergers or rebranding.

### 7. Exploring Correlations
- **Budget vs. Gross Revenue**:
  - Create a scatter plot using `seaborn` to visually explore the relationship between `budget` and `gross revenue`.
  - A positive trend is observed, suggesting a correlation, but a scatter plot alone isn't enough to determine the correlation's strength.
- **Regression Analysis**:
  - Use `seaborn`'s `regplot()` to add a regression line to the scatter plot, providing a clearer view of the relationship.
  - The regression line confirms a positive correlation between `budget` and `gross revenue`.

### 8. Calculating Correlation Coefficients
- Use `df.corr()` to calculate correlation coefficients between numerical fields. This function helps compare the correlation strengths between various attributes.

### 9. Understanding Correlation Methods
- **Types of Correlation**:
  - **Pearson**: Measures linear relationships.
  - **Kendall** and **Spearman**: Handle non-linear correlations.
- Understand the nuances of each method and how they impact data interpretation.

### 10. Visualizing Correlations
- **Correlation Matrix**: Create a heatmap using `seaborn` to visualize the correlation matrix.
  - Colors represent the strength of correlations: darker colors for low correlations and brighter colors for higher correlations.
  - Strong correlation is observed between `budget` and `gross revenue`.

### 11. Numerizing Non-Numeric Data
- **Numerization**: Convert non-numeric features (e.g., company names, directors) into numerical data. This allows for a more comprehensive correlation analysis.
- **Re-evaluate Correlations**: Analyze the updated matrix to uncover new insights.

### 12. Key Insights
- **Positive Correlations**: Strong correlations between `votes` and `gross revenue`, as well as between `budget` and `gross revenue`.
- **Negative Correlations**: A negative correlation between `runtime` and `gross revenue` suggests longer movies may not always be more successful.

## Conclusion
- Data analysis and visualization techniques are crucial for understanding the relationships between different features in the movie industry.
- By using methods like regression plots and correlation matrices, we gain valuable insights into the factors influencing movie revenue.
