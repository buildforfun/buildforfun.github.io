---
layout: post
title:  "Data Science Handbook"
categories: [ programming]
date:   2024-10-13 07:00:00
---

# What is Data science and Data engineering?

- [What is Data Science?](#what-is-data-science)
- [What is Data Engineering?](#what-is-data-engineering)


# What is Data Engineering
Data engineering is the control the flow of data, it is creating custom data storage systems that transport data through it's various forms into formats needed by the organisations.

1. Data collection and storage (data engineer)
2. Data preparation (data scientist)*
3. Exploration and visualisation (data scientist)*
4. Experimentation and prediction (data scientist)*
5. Data storytelling and communication (data scientist)*

## A typical data engineering  work flow

1. Understand problem: to solve this problem, the data engineer must first get clarity on the problem and data:
    - Determine frequency in time
    - Determine whether any filters should be applied to the data
    - Determine the timeframe of the data
    - Determine the data sources of the data
2. Data extraction and exploration
    - Determine what joins should be used between the tables and what the relationships are between these tables.
    - Assess the quality of the data: decide if missing or anomalous data may need to be corrected.
3. Design and create database architecture
    - Design and create a database that can be used to hold the required data.
4. Ingest correct data from different sources
    - Import the data from various sources into the database.
    - Sources of data:
        - Web data
        - Survey data
        - Customer data
        - Financial transactions
		- IoT devices
    - How to access public data?
        - API - where you request data from a company over the internet.
        - Public data records are another great way of gathering data.

5. Build automated data pipelines
    - If we are collecting from different sources, it is helpful to have a way of bringing all that data together in one go. That's where a data pipeline comes in! It does exactly that, it moves data from the source into the format needed for analysis in one flow and automates the whole process. This pipeline can then be scheduled to run either manually or automatically.

## How to a design databases
When I was looking to the best books on database design, the book that I kept coming back to was the "Database design for Mere Mortals" by Michael J. Hernandez. I’ve simplified the steps, but all the main steps are nearly all the same.

1. Develop a mission statement and mission objective.
    1. Mission statement: purpose of database
    2. Mission objectives: what tasks the user should be able to perform with the data.
2. Analyse the current database
    1. Look at how data is currently collected
    2. Review of other similar databases
    3. Look at how data is presented
    4. Create initial field list
3. Create the database structure
    1. Use initial list of fields to identify tables within data
    2. Compose table descriptions for table
    3. Create field specification
4. Determine and establish table relationship
    1. Understand how the different tables are related
    2. Create relationship diagrams
5. Define and establish database rules
    1. Review and determine if constraints are needed
    2. Update field specification
    3. Think about how to test database rule
6. Determine and Define views
    1. Views Subset of database
7. Review data integrity
    1. Go through and check if implemented correctly
    2. Collate all the documentation
8. Database design complete!

# What is Data Science
Data science is the extracting insights from data using scientific techniques. At what stage of the data flow does the data scientist come in?

1. Data collection and storage (data engineer)
2. Data preparation (data scientist)*
3. Exploration and visualisation (data scientist)*
4. Experimentation and prediction (data scientist)*
5. Data storytelling and communication (data scientist)*

## Step 1:  Data collection

Data engineer collects data and creates SQL databases for data to be stored in.

## Step 2:  Data preparation

This stage is cleaning and transforming the data into a format that’s ready for analysis. Cleaning techniques such as removing duplicates, inconsistent data and normalisation are used. Cleaning techniques such as removing duplicates, inconsistent data and normalisation are used. Tidy data is a way of presenting a matrix of data, with observations on rows and variables as columns.

1. Remove duplicates or Unique ID
2. Homogeneity - same units etc.
3. Same data types
4. Missing values
    1. Impute - use a mean value
    2. Drop
    3. Keep

Common pipeline names are Extract Transform Load (ETL) have been created to help manage data from multiple sources.

## Step 3: Exploration and visualisation

During this phase, data scientists explore the data to understand patterns, understand characteristics or spot anomalies. Statistics and visualisation plots are used to gain meaningful insights from the data.

### Step 3a: Exploration

Streaming through the data gives you little information. Descriptive statistics do better, but can be misleading; visualisation teaches us the most.

Anscombe's quartet is a group of datasets (x, y) that have the same mean, standard deviation, and regression line, but which are qualitatively different.

### Step 3b: Visualisations

Rules for plots:
    - Use colours intentially
    - Axes - make sure the axes are sensible. Not always 0, as you might want to see change.

Dashboard
    - A picture of several pictures. Individually, these pieces of information are useful. But together, they paint a much bigger picture

## Step 4: Experimentation and prediction

We run experiments and predictions on the data to get insights.

At this stage, the data scientist runs experiments and predictions on the data to get insights. The aim is to meet the project objective to predict future outcomes, classify data, or uncover hidden patterns. They can use A/B testing and/or machine learning -  where a model is trained on data to make predictions.

### Step 4a: Experimentation

Experiments help drive decisions and draw conclusions. Generally, they begin with a question and a hypothesis, then data collection, followed by a statistical test and its interpretation. This is where we might use A/B testing:

1. Picking a metric
    1. Our metric is click-through rate, the percent of people who click on a link after viewing the title.
2. Picking a sample size
    1. Next, we'll run the experiment until we reach a sample size large enough to be certain that results aren't due to random chance.
    2. The size depends on a "baseline metric" that helps gauge any changes. In our case, it's how often people click on a link to one of our blogs usually. If the rate is much larger or smaller than 50%, then we need a larger sample size. Click-rate is typically under 3%.
    3. The sample size depends on the sensitivity we want. A test's sensitivity tells us how small of a change in our metric we can detect. Larger sample sizes allow us to detect smaller changes. You might think that we want a high sensitivity, but we actually want to optimise for an amount that is meaningful for our question
3. We run our experiment until we reach the calculated size. Stopping the experiment before or after could lead to biassed results
    1. Once we reach the target size, we check our metric. We see some difference between the titles, but how do we know if it's meaningful? We check by performing a test of statistical significance. If they are significant, we can be reasonably sure that the difference is not due to random chance, but to an actual difference in preference.
4. Checking for significance.
    1. Once we reach the target size, we check our metric. We see some difference between the titles, but how do we know if it's meaningful? We check by performing a test of statistical significance. If they are significant, we can be reasonably sure that the difference is not due to random chance, but to an actual difference in preference.
    2. A statistically significant result means that your result is probably not due to chance given the statistical assumptions made.
    3. If it’s not significant, we can't conclude which option is better because the observed difference is likely due to random chance.
5. Finally, we interpret the results. In our case, we want to choose the better performing title

### Step 4b: Make models for prediction

Models attempt to represent a real-world process with statistics. At a high level, models define relationships between variables with equations. These definitions are based on statistical assumptions and historical data.

Predictive modelling is a subcategory of modelling used for prediction. By modelling a process, we can enter new inputs and see what outcome it outputs. Predictive models can be as simple as a linear equation with an x and y variable to a deep learning algorithm that is uninterpretable by humans.

Often when plotting time series, you can find patterns. Seasonality is when there are repeating patterns related to time such as months and weeks.Time series data is used in predictive modelling to predict metrics at future dates. We call this forecasting. We can build predictive models using time series data from the past years or decades to generate predictions. This uses a combination of statistical and machine learning methods.

Machine learning simply is teaching a machine to learn from data.

While Supervised Learning uses data with features and labels, Unsupervised Learning uses data with only features. Labels are what we want to predict, like the customer churning. Features are data that might help predict the label, such as profession or date of last purchase.

### Step 4c: Model evaluation

After training a model, how do we know if it's any good? It's always good practice not to allocate all of your historical data for training. Withheld data is called a test set and can be used to evaluate the goodness of the model. In our example, we could ask the model to predict whether a set of customers would churn, and then measure the accuracy of our prediction.

### Step 5. Data storytelling and communication

The final stage is communicating your insights effectively. The language must be clear, concise with compelling visuals for a non-technical audience.

<br>
