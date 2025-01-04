---
layout: post
categories: [ programming]
title:  "Data analyst"
date:   2025-1-1 08:00:00
---


# Data analyst

## Data Extraction, Cleaning, and Quality Assessment in PostgreSQL

### 1. Data Extraction, Joining, and Aggregation Tasks

**Aggregate Numeric, Categorical Variables, and Dates by Groups:**
- Use the `GROUP BY` clause to aggregate data in PostgreSQL. This allows you to summarize data into distinct categories based on one or more columns.
- Common aggregate functions include:
  - `SUM()`: Calculates the total sum of a numeric column.
  - `AVG()`: Computes the average of a numeric column.
  - `COUNT()`: Counts the number of rows in a group.
  - Example Query:
    ```sql
    SELECT department_id, AVG(salary) FROM employees GROUP BY department_id;
    ```

**Interpret Database Schema and Combine Tables:**
- Understand the relationships between tables using primary and foreign keys.
- Use different types of joins (INNER JOIN, LEFT JOIN, RIGHT JOIN) to combine data from multiple tables based on common fields.
- Example of a LEFT JOIN:
    ```sql
    SELECT a.*, b.* FROM table_a a LEFT JOIN table_b b ON a.id = b.a_id;
    ```

**Extract Data Based on Conditions:**
- Use the `WHERE` clause to filter records based on specific conditions.
- Example Query:
    ```sql
    SELECT * FROM orders WHERE order_date > '2023-01-01';
    ```

**Subqueries for Referencing Other Tables:**
- Utilize subqueries to reference another table within your main query. This is useful for complex queries requiring data from multiple sources.
- Example of a subquery:
    ```sql
    SELECT * FROM employees WHERE department_id IN (SELECT id FROM departments WHERE location = 'New York');
    ```

### 2. Cleaning Tasks to Prepare Data for Analysis

**Match Strings with Specific Patterns:**
- Use regular expressions with the `SIMILAR TO` or `~` operators for pattern matching.
- Example Query:
    ```sql
    SELECT * FROM users WHERE email ~ '^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\\.[a-zA-Z]{2,}$';
    ```

**Convert Values Between Data Types:**
- Use the `CAST()` function or the `::` operator to convert data types.
- Example Query:
    ```sql
    SELECT CAST(price AS numeric) FROM products;
    ```

**Clean Categorical and Text Data:**
- Functions like `TRIM()`, `LOWER()`, and `UPPER()` can help standardize text data by removing spaces and changing case.
- Example Query:
    ```sql
    UPDATE customers SET name = TRIM(LOWER(name));
    ```

**Clean Date and Time Data:**
- Use date functions to format and validate date entries.
- Example Query:
    ```sql
    UPDATE events SET event_date = TO_DATE(event_date, 'YYYY-MM-DD') WHERE event_date IS NOT NULL;
    ```

### 3. Assess Data Quality and Perform Validation Tasks

**Identify and Replace Missing Values:**
- Use the `COALESCE()` function to replace NULL values with default values.
- Example Query:
    ```sql
    SELECT COALESCE(phone_number, 'N/A') FROM contacts;
    ```

**Perform Data Validation Tasks:**
- Implement checks for consistency and constraints using SQL constraints (e.g., NOT NULL, UNIQUE).
- Example Query for checking uniqueness:
    ```sql
    SELECT email, COUNT(*) FROM users GROUP BY email HAVING COUNT(*) > 1;
    ```

**Identify and Validate Data Types:**
- Use the `pg_typeof()` function to check data types of columns in your dataset.
- Example Query:
    ```sql
    SELECT column_name, pg_typeof(column_name) FROM information_schema.columns WHERE table_name = 'your_table';
    ```

## Detailed Notes on Calculating Metrics in PostgreSQL

### 1. Calculate Measures of Center

**Mean:**
- The mean is calculated by summing all values of a variable and dividing by the total number of values.
- In PostgreSQL, use the `AVG()` function to compute the mean.
- Example Query:
    ```sql
    SELECT AVG(age) AS average_age FROM athletes;
    ```

**Median:**
- The median represents the middle value when data is sorted. If there is an even number of observations, it is the average of the two middle values.
- Use the `PERCENTILE_CONT(0.5) WITHIN GROUP (ORDER BY column_name)` to calculate the median in PostgreSQL.
- Example Query:
    ```sql
    SELECT PERCENTILE_CONT(0.5) WITHIN GROUP (ORDER BY age) AS median_age FROM athletes;
    ```

**Mode:**
- The mode is the most frequently occurring value in a dataset.
- In PostgreSQL, use `MODE() WITHIN GROUP (ORDER BY column_name)` to find the mode.
- Example Query:
    ```sql
    SELECT MODE() WITHIN GROUP (ORDER BY age) AS mode_age FROM athletes;
    ```

### 2. Calculate Measures of Spread

**Range:**
- The range is the difference between the maximum and minimum values in a dataset.
- Use `MAX()` and `MIN()` functions to calculate the range.
- Example Query:
    ```sql
    SELECT MAX(age) - MIN(age) AS age_range FROM athletes;
    ```

**Standard Deviation:**
- Standard deviation measures how spread out numbers are from the mean.
- In PostgreSQL, use `STDDEV()` for sample standard deviation and `STDDEV_POP()` for population standard deviation.
- Example Query:
    ```sql
    SELECT STDDEV(age) AS stddev_age FROM athletes;
    ```

**Variance:**
- Variance quantifies how much values differ from the mean.
- Use `VARIANCE()` for sample variance and `VAR_POP()` for population variance.
- Example Query:
    ```sql
    SELECT VARIANCE(age) AS variance_age FROM athletes;
    ```

### 3. Calculate Skewness

- Skewness measures the asymmetry of the distribution of values in a dataset.
- PostgreSQL does not have a built-in function for skewness, but it can be calculated using custom formulas or extensions like `tablefunc`.
- Example Calculation:
    ```sql
    SELECT (3 * (AVG(age) - MEDIAN(age))) / STDDEV(age) AS skewness_age FROM athletes;
    ```

### 4. Calculate Missingness

**Missing Values:**
- Missingness refers to the presence of NULL values in a dataset. It's crucial to assess how missing data can impact analysis and reporting.
- To calculate missingness, use:
    ```sql
    SELECT COUNT(*) - COUNT(age) AS missing_age_count FROM athletes;
    ```
  
**Influence on Reporting:**
- Missing data can skew results, reduce statistical power, and lead to biased conclusions. It's essential to handle missing values appropriately through imputation or exclusion based on analysis needs.

### 5. Calculate Correlation Between Variables

**Correlation:**
- Correlation assesses how closely related two variables are. It ranges from -1 (perfect negative correlation) to +1 (perfect positive correlation).
- Use `CORR(column1, column2)` to compute correlation in PostgreSQL.
- Example Query:
    ```sql
    SELECT CORR(height, weight) AS correlation_height_weight FROM athletes;
    ```

## Detailed Notes on Data Visualizations and Hypothesis Testing

### 2.2 Read and Analyze Data Visualizations to Demonstrate Characteristics of Data

**Types of Data Visualizations:**
- **Bar Chart:**
  - Used to compare different categories or groups.
  - Displays rectangular bars with lengths proportional to the values they represent.
  - Effective for categorical data.
  
- **Box Plot:**
  - Summarizes data through five-number summaries: minimum, first quartile (Q1), median, third quartile (Q3), and maximum.
  - Shows the distribution of data and identifies outliers.
  
- **Line Graph:**
  - Illustrates trends over time by connecting data points with lines.
  - Best for continuous data and showing changes over intervals.
  
- **Histogram:**
  - Represents the frequency distribution of numerical data by dividing the data into bins.
  - Useful for understanding the distribution shape (e.g., normal, skewed).

**Interpreting Data Visualizations:**
- **Bar Chart Interpretation:**
  - Identify which categories have higher or lower values.
  - Assess trends or patterns across categories.
  
- **Box Plot Interpretation:**
  - Analyze the spread and central tendency of the data.
  - Identify any outliers that may affect analysis.

- **Line Graph Interpretation:**
  - Observe trends over time, such as increases or decreases in values.
  - Determine periods of stability or volatility.

- **Histogram Interpretation:**
  - Assess the shape of the distribution (e.g., normal, bimodal).
  - Identify ranges where most data points fall.

### 2.3 Read and Analyze Data Visualizations to Represent Relationships Between Features

**Types of Data Visualizations for Relationships:**
- **Scatterplot:**
  - Displays values for two variables across a Cartesian plane.
  - Useful for identifying correlations or relationships between features.

- **Heatmap:**
  - Represents data values in a matrix format using color gradients.
  - Effective for visualizing complex relationships and patterns in large datasets.

- **Pivot Table:**
  - A table that summarizes data from a larger dataset, allowing for easy comparison across different dimensions.
  - Enables quick analysis of relationships between multiple variables.

**Interpreting Data Visualizations for Relationships:**
- **Scatterplot Interpretation:**
  - Look for patterns indicating correlation (positive, negative, or none).
  - Assess the strength of the relationship based on how closely points cluster along a line.

- **Heatmap Interpretation:**
  - Identify areas with high or low values based on color intensity.
  - Useful for spotting trends and anomalies in multi-dimensional datasets.

- **Pivot Table Interpretation:**
  - Analyze summarized data to identify relationships and trends across different dimensions.
  - Facilitate comparisons between categories and features effectively.

### 3.1 Describe Statistical Concepts Underpinning Hypothesis Testing and Experimentation

**Statistical Distributions:**
- **Binomial Distribution:**
  - Models the number of successes in a fixed number of independent Bernoulli trials (e.g., coin flips).
  
- **Normal Distribution:**
  - A continuous probability distribution characterized by its bell-shaped curve; defined by its mean and standard deviation.

- **Poisson Distribution:**
  - Models the number of events occurring within a fixed interval of time or space, given a known average rate.

- **t-distribution:**
  - Used in hypothesis testing when sample sizes are small and population standard deviation is unknown; it is similar to the normal distribution but has heavier tails.

- **Chi-square Distribution:**
  - Used primarily in tests of independence and goodness-of-fit; it assesses how observed frequencies differ from expected frequencies.

- **F-distribution:**
  - Used in analysis of variance (ANOVA) tests; it compares variances between two populations.

**Hypothesis Testing Concepts:**
- **Null Hypothesis ($$H_0$$):** 
  - The statement being tested, typically positing no effect or no difference.

- **Alternative Hypothesis ($$H_1$$ or $$H_a$$):** 
  - The statement that indicates the presence of an effect or difference.

- **One-tailed vs. Two-tailed Tests:** 
  - One-tailed tests assess if a parameter is either greater than or less than a certain value, while two-tailed tests assess if it is simply different from that value.

**Steps in Hypothesis Testing:**
1. State $$H_0$$ and $$H_1$$.
2. Collect relevant data.
3. Perform an appropriate statistical test to calculate a test statistic (e.g., t-value).
4. Determine the p-value associated with the test statistic.
5. Compare p-value to significance level ($$\alpha$$); reject $$H_0$$ if $$p < \alpha$$.


## Detailed Notes on Data Management, Exploratory Analysis, and Statistical Experimentation in Python

### 1.1 Perform Standard Data Import, Joining, and Aggregation Tasks

**Import Data from Flat Files:**
- Use the `pandas` library to import data from CSV files or Excel files.
- Example:
    ```python
    import pandas as pd

    # Importing a CSV file
    df_csv = pd.read_csv('data.csv')

    # Importing an Excel file
    df_excel = pd.read_excel('data.xlsx')
    ```

**Import Data from Databases:**
- Use libraries like `SQLAlchemy` or `sqlite3` to connect to databases and fetch data into pandas DataFrames.
- Example using SQLAlchemy:
    ```python
    from sqlalchemy import create_engine

    engine = create_engine('sqlite:///database.db')
    df_db = pd.read_sql('SELECT * FROM table_name', con=engine)
    ```

**Aggregate Numeric, Categorical Variables, and Dates:**
- Use the `groupby()` function to aggregate data by groups.
- Example:
    ```python
    aggregated_data = df.groupby('category_column').agg({'numeric_column': 'mean', 'date_column': 'max'})
    ```

**Combine Multiple Tables by Rows or Columns:**
- Use `pd.concat()` to combine DataFrames either vertically (rows) or horizontally (columns).
- Example:
    ```python
    combined_rows = pd.concat([df1, df2], axis=0)  # Concatenate rows
    combined_columns = pd.concat([df1, df2], axis=1)  # Concatenate columns
    ```

**Filter Data Based on Different Criteria:**
- Utilize boolean indexing to filter DataFrames based on conditions.
- Example:
    ```python
    filtered_data = df[df['column_name'] > value]
    ```

### 1.2 Perform Standard Cleaning Tasks to Prepare Data for Analysis

**Match Strings with Specific Patterns:**
- Use the `str.contains()` method for pattern matching with regular expressions.
- Example:
    ```python
    filtered_data = df[df['text_column'].str.contains('pattern')]
    ```

**Convert Values Between Data Types:**
- Use the `astype()` method to convert data types.
- Example:
    ```python
    df['column_name'] = df['column_name'].astype(float)
    ```

**Clean Categorical and Text Data:**
- Use string manipulation methods such as `str.strip()`, `str.lower()`, and `str.replace()`.
- Example:
    ```python
    df['text_column'] = df['text_column'].str.strip().str.lower().str.replace('old_value', 'new_value')
    ```

**Clean Date and Time Data:**
- Convert strings to datetime objects using `pd.to_datetime()`.
- Example:
    ```python
    df['date_column'] = pd.to_datetime(df['date_column'], format='%Y-%m-%d')
    ```

### 1.3 Assess Data Quality and Perform Validation Tasks

**Identify and Replace Missing Values:**
- Use methods like `fillna()` for imputation or `dropna()` for removal of missing values.
- Example:
    ```python
    df['column_name'].fillna(value='default_value', inplace=True)
    ```

**Perform Different Types of Data Validation Tasks:**
- Check for duplicates using `duplicated()` and remove them with `drop_duplicates()`.
- Example:
    ```python
    df.drop_duplicates(inplace=True)
    ```

**Identify and Validate Data Types:**
- Use the `dtypes` attribute to check data types of columns.
- Example:
    ```python
    print(df.dtypes)
    ```

### 1.4 Collect Data from Non-standard Formats by Modifying Existing Code

**Adapt Provided Code to Import Data from an API:**
- Use libraries like `requests` to fetch data from APIs and convert it into a pandas DataFrame.
- Example:
    ```python
    import requests

    response = requests.get('https://api.example.com/data')
    data = response.json()
    df_api = pd.DataFrame(data)
    ```

**Identify the Structure of HTML and JSON Data:**
- For HTML, use libraries like `BeautifulSoup` to parse web pages.
  - Example:
      ```python
      from bs4 import BeautifulSoup

      html_content = requests.get('https://example.com').text
      soup = BeautifulSoup(html_content, 'html.parser')
      table_data = soup.find_all('table')
      ```
  
- For JSON, use the built-in `json` library to parse JSON strings.
  - Example:
      ```python
      import json
      
      json_data = '{"key": "value"}'
      parsed_data = json.loads(json_data)
      ```

## Detailed Notes on Calculating Metrics and Creating Visualizations in Python

### 2.1 Calculate Metrics to Effectively Report Characteristics of Data and Relationships Between Features

**Calculate Measures of Center:**

- **Mean:**
  - Use the `statistics` module or `pandas` for calculating the mean.
  - Example using `statistics`:
    ```python
    import statistics

    data = [1, 2, 3, 4, 5]
    mean_value = statistics.mean(data)
    print("Mean:", mean_value)
    ```
  - Example using `pandas`:
    ```python
    import pandas as pd

    df = pd.DataFrame({'values': [1, 2, 3, 4, 5]})
    mean_value = df['values'].mean()
    print("Mean:", mean_value)
    ```

- **Median:**
  - Example using `statistics`:
    ```python
    median_value = statistics.median(data)
    print("Median:", median_value)
    ```
  - Example using `pandas`:
    ```python
    median_value = df['values'].median()
    print("Median:", median_value)
    ```

- **Mode:**
  - Example using `statistics`:
    ```python
    mode_value = statistics.mode(data)
    print("Mode:", mode_value)
    ```
  - Example using `pandas`:
    ```python
    mode_value = df['values'].mode()[0]  # mode() returns a Series
    print("Mode:", mode_value)
    ```

**Calculate Measures of Spread:**

- **Range:**
  - Example:
    ```python
    data_range = max(data) - min(data)
    print("Range:", data_range)
    ```

- **Standard Deviation and Variance:**
  - Example using `statistics`:
    ```python
    std_dev = statistics.stdev(data)  # Sample standard deviation
    variance = statistics.variance(data)  # Sample variance
    print("Standard Deviation:", std_dev)
    print("Variance:", variance)
    ```
  - Example using `pandas`:
    ```python
    std_dev = df['values'].std()
    variance = df['values'].var()
    print("Standard Deviation (pandas):", std_dev)
    print("Variance (pandas):", variance)
    ```

**Calculate Skewness:**
- Use the `scipy.stats` library for skewness calculation.
- Example:
  ```python
  from scipy.stats import skew

  skewness = skew(data)
  print("Skewness:", skewness)
  ```

**Calculate Missingness:**
- Identify missing values in a dataset.
- Example:
  ```python
  missing_count = df.isnull().sum()
  print("Missing Values:\n", missing_count)
  ```
- **Influence on Reporting:**
  - Missing data can lead to biased results and affect statistical power. It's crucial to handle missing values appropriately through imputation or exclusion.

**Calculate Correlation Between Variables:**
- Use the `corr()` method in pandas to calculate correlation.
- Example:
  ```python
  df['another_column'] = [2, 3, 4, 5, 6]
  correlation = df.corr().iloc[0,1]  # Correlation between first two columns
  print("Correlation:", correlation)
  ```

### 2.2 Create Data Visualizations to Demonstrate the Characteristics of Data

**Create and Customize Bar Charts:**
- Use `matplotlib` or `seaborn`.
- Example with `matplotlib`:
  ```python
  import matplotlib.pyplot as plt

  plt.bar(df['category'], df['values'])
  plt.title('Bar Chart')
  plt.xlabel('Category')
  plt.ylabel('Values')
  plt.show()
  ```
  
- Example with `seaborn`:
   ```python
   import seaborn as sns

   sns.barplot(x='category', y='values', data=df)
   plt.title('Bar Chart with Seaborn')
   plt.show()
   ```

**Create and Customize Box Plots:**
- Example with `seaborn`:
   ```python
   sns.boxplot(x='category', y='values', data=df)
   plt.title('Box Plot')
   plt.show()
   ```

**Create and Customize Line Graphs:**
- Example with `matplotlib`:
   ```python
   plt.plot(df['date'], df['values'])
   plt.title('Line Graph')
   plt.xlabel('Date')
   plt.ylabel('Values')
   plt.show()
   ```

**Create and Customize Histograms:**
- Example with `matplotlib`:
   ```python
   plt.hist(df['values'], bins=10)
   plt.title('Histogram')
   plt.xlabel('Values')
   plt.ylabel('Frequency')
   plt.show()
   ```

### 2.3 Create Data Visualizations to Represent the Relationships Between Features

**Create and Customize Scatterplots:**
- Example with `seaborn`:
   ```python
   sns.scatterplot(x='feature1', y='feature2', data=df)
   plt.title('Scatterplot')
   plt.show()
   ```

**Create and Customize Heatmaps:**
- Use correlation matrices to create heatmaps.
- Example with `seaborn`:
   ```python
   correlation_matrix = df.corr()
   sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm')
   plt.title('Heatmap of Correlation Matrix')
   plt.show()
   ```

**Create and Customize Pivot Tables:**
- Use pandas to create pivot tables and visualize them.
- Example:
   ```python
   pivot_table = df.pivot_table(values='values', index='category', columns='another_column', aggfunc='mean')
   
   # Visualizing pivot table as a heatmap
   sns.heatmap(pivot_table, annot=True, cmap='viridis')
   plt.title('Pivot Table Heatmap')
   plt.show()
   ```

## Detailed Notes on Sampling Methods and Statistical Tests in Python

### 3.1 Apply Sampling Methods to Data

**Distinguish Between Different Types of Random Sampling Techniques:**
- **Simple Random Sampling:** Each member of the population has an equal chance of being selected. Use `random.sample()` for this.
  ```python
  import random

  population = ['apple', 'banana', 'cherry', 'date', 'elderberry']
  sample_size = 3
  sample = random.sample(population, sample_size)
  print("Simple Random Sample:", sample)
  ```

- **Stratified Sampling:** The population is divided into strata, and random samples are taken from each stratum.
  ```python
  import pandas as pd

  df = pd.DataFrame({
      'category': ['A', 'A', 'B', 'B', 'C', 'C'],
      'value': [1, 2, 3, 4, 5, 6]
  })
  
  stratified_sample = df.groupby('category').apply(lambda x: x.sample(1)).reset_index(drop=True)
  print("Stratified Sample:\n", stratified_sample)
  ```

- **Systematic Sampling:** A starting point is chosen randomly, and every nth member is selected.
  ```python
  systematic_sample = population[::2]  # Taking every second element
  print("Systematic Sample:", systematic_sample)
  ```

**Sample Data from a Statistical Distribution:**
- **Normal Distribution:**
  ```python
  import numpy as np

  normal_samples = np.random.normal(loc=0, scale=1, size=1000)  # mean=0, std=1
  ```

- **Binomial Distribution:**
  ```python
  binomial_samples = np.random.binomial(n=10, p=0.5, size=1000)  # n trials, p probability
  ```

- **Poisson Distribution:**
  ```python
  poisson_samples = np.random.poisson(lam=5.0, size=1000)  # lambda parameter
  ```

- **Exponential Distribution:**
  ```python
  exponential_samples = np.random.exponential(scale=1.0, size=1000)  # scale parameter
  ```

**Calculate a Probability from a Statistical Distribution:**
- **Normal Distribution Probability:**
   ```python
   from scipy.stats import norm

   probability_less_than_40 = norm.cdf(40, loc=50, scale=10)  
   print("P(X <= 40):", probability_less_than_40)
   ```

- **Binomial Distribution Probability:**
   ```python
   from scipy.stats import binom

   probability_k_successes = binom.pmf(k=5, n=10, p=0.5)  
   print("P(X = 5 successes):", probability_k_successes)
   ```

- **Poisson Distribution Probability:**
   ```python
   from scipy.stats import poisson

   probability_k_occurrences = poisson.pmf(k=3, mu=2)  
   print("P(X = 3 occurrences):", probability_k_occurrences)
   ```

### 3.2 Implement Methods for Performing Statistical Tests

**Run Statistical Tests:**

- **T-Test:**
   - Independent T-test to compare means of two groups.
   ```python
   from scipy import stats

   group_a = np.random.normal(5.0, 1.5, size=30)
   group_b = np.random.normal(6.0, 1.5, size=30)

   t_statistic, p_value = stats.ttest_ind(group_a, group_b)
   print(f"T-Statistic: {t_statistic}, P-Value: {p_value}")
   ```

- **ANOVA Test:**
   - One-way ANOVA to compare means of three or more groups.
   ```python
   group1 = np.random.normal(5.0, 1.5, size=30)
   group2 = np.random.normal(6.0, 1.5, size=30)
   group3 = np.random.normal(7.0, 1.5, size=30)

   f_statistic, p_value_anova = stats.f_oneway(group1, group2, group3)
   print(f"F-Statistic: {f_statistic}, P-Value: {p_value_anova}")
   ```

- **Chi-Square Test:**
   - Test for independence between categorical variables.
   ```python
   observed_frequencies = np.array([[10, 20], [20, 25]])
   
   chi2_statistic, p_value_chi2, _, _ = stats.chi2_contingency(observed_frequencies)
   print(f"Chi-Square Statistic: {chi2_statistic}, P-Value: {p_value_chi2}")
   ```

**Analyze the Results of Statistical Tests:**
- Interpret the results based on the p-value:
    - If $$ p < \alpha $$ (commonly set at $$ \alpha = 0.05 $$), reject the null hypothesis.
    - Example interpretation:
      ```python
      alpha = 0.05
      
      if p_value < alpha:
          print("Reject the null hypothesis.")
      else:
          print("Fail to reject the null hypothesis.")
      ```

These notes provide a comprehensive overview of sampling methods and statistical tests in Python. Each section includes practical examples that can be directly applied in real-world scenarios to facilitate understanding and application of statistical concepts and techniques.




Here are examples of SQL commands that utilize the `UNION` and `INTERSECT` operators:

### Using UNION

The `UNION` operator combines the results of two or more `SELECT` statements, returning all unique rows from both queries.

#### Example of UNION

```sql
SELECT Name FROM Employees
UNION
SELECT Name FROM Customers;
```

In this example, the query retrieves all unique names from both the `Employees` and `Customers` tables.

### Using INTERSECT

The `INTERSECT` operator returns only the rows that are common between two `SELECT` statements. Both queries must return the same number of columns with compatible data types.

#### Example of INTERSECT

```sql
SELECT Name, BirthDate FROM Employees
INTERSECT
SELECT Name, BirthDate FROM Customers;
```

This query returns only the names and birth dates that exist in both the `Employees` and `Customers` tables.

### Summary of Usage

- **UNION**: Use when you want to combine results from multiple queries and ensure that duplicate rows are removed.
- **INTERSECT**: Use when you want to find common rows between two queries.

These examples demonstrate how to effectively use the `UNION` and `INTERSECT` operators in SQL to manipulate and analyze data across multiple tables.

