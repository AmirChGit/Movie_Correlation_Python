# Movie Industry Data Analysis Project

## Overview
This project focuses on exploring correlations within a movie industry dataset to understand how different attributes impact gross revenue. The main objective is to identify and analyze these correlations using Python libraries like pandas, seaborn, and matplotlib.

## Project Setup
1. **Download the Dataset**: The movie industry dataset is available on [Kaggle](https://www.kaggle.com).
2. **Environment Setup**: Use Anaconda to set up a Jupyter Notebook environment for easy data analysis and visualization.

## Project Workflow
### 1. Importing Libraries
- Utilize popular Python libraries:
  - `pandas` for data manipulation.
  - `seaborn` and `matplotlib` for data visualization and statistical analysis.

### 2. Reading in the Data
- Load the dataset into a pandas DataFrame using the `read_csv` function.

### 3. Data Cleaning
- **Handling Missing Data**: Iterate through columns to identify and address missing values.
- **Adjusting Data Types**: Convert numeric columns to integers for consistency.
- **Addressing Inconsistencies**: For example, correct the "Year" column using data from the "Release Date".

### 4. Data Analysis
- **Sorting and Removing Duplicates**: Sort data by "Gross Revenue" to identify top films and remove duplicate entries to maintain data quality.
- **Exploring Correlations**:
  - Hypothesize that "Budget" and "Company" could strongly influence "Gross Revenue".
  - Create scatter plots to visualize trends between "Budget" and "Gross Revenue".

### 5. Correlation Analysis
- **Visual Analysis**: Use `scatterplot` and `regplot` from Seaborn to explore visual correlations and fit regression lines.
- **Calculating Correlation Coefficients**:
  - Use the `corr` method to quantify the strength of correlations.
  - Discuss limitations and appropriate usage of correlation methods.

### 6. Correlation Methods
- Explore different methods:
  - **Pearson**: Measures linear relationships.
  - **Kendall** and **Spearman**: Handle non-linear correlations.
- Understand how each method affects the results and interpretation.

### 7. Visualizing Correlations
- **Heatmap**: Use Seaborn's heatmap to display the correlation matrix.
  - The color intensity visually represents the strength of relationships between attributes.

### 8. Handling Non-Numeric Data
- **Numerizing Data**: Convert non-numeric data, like company names, into numerical representations.
- **Re-evaluate Correlations**: Analyze the updated correlation matrix to understand the impact of numerized attributes on gross revenue.

## Key Findings
- **Budget** and **Votes** are highly correlated with gross revenue.
- **Company** has a weaker correlation than expected.
- Understanding and selecting the right correlation methods are crucial for accurate analysis.

## Takeaways
- Visualizing correlations using heatmaps provides an intuitive understanding of relationships.
- Transforming non-numeric data is essential for comprehensive correlation analysis.
- The choice of correlation method can significantly influence analytical outcomes.
