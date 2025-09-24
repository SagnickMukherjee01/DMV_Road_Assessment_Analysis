# DMV_Road_Assessment_Analysis

### Project Overview

This project analyzes a simulated DMV road test dataset to uncover the key factors that influence whether applicants pass or fail their driving test. With high failure rates leading to delays and added costs, the study aims to generate actionable insights that can improve training programs, optimize resource allocation, and support applicants in being better prepared.

### Key Objectives

1. Demographic Insights: Explore pass/fail trends across age, gender, and race.

2. Training Effectiveness: Evaluate the impact of different training levels (Advanced, Basic, None) on outcomes.

3. Performance Drivers: Identify the most significant road assessment indicators that predict success.

4. Predictive Modeling: Build and test a logistic regression model to estimate pass likelihood and measure performance using accuracy, precision, recall, and F1-score.

5. Threshold Analysis: Demonstrate how varying cutoff points affect predictions using confusion matrices.

6. Interactive Dashboards: Design Power BI dashboards with dynamic filters (demographics, training, results) to provide intuitive, real-time insights.

### key Performance Indicators

<img width="1731" height="801" alt="image" src="https://github.com/user-attachments/assets/12f3696e-dfcb-4040-bf8a-dd6a9e271fa2" />

### Overview of Dataset Structure

- ### DADV-2-Capstone Project-Group D-Dataset Drivers License Data:-
  Contains data on applicant’s demographics (age , gender and    race), training participation and road assessment indicators.

### Tools Used

 - Excel- Feature Engineering, Exploratory Data Analysis, Statistical Analysis and Data Visualization
   - [Download_Here](https://www.microsoft.com/en-in/microsoft-365/excel)
 - Power Bi- Data Visualization using DAX formulas
   - [Download_Here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)

### Data Cleaning

#### Key Data Cleaning Process Included:-

  1. Accurate data types of the fields were assigned.

  2. The dataset was thoroughly checked for all the missing values and for duplication of data and no such things were found.

  3. All the numeric fields are converted into numeric datatypes from general datatypes to ensure proper analysis.

### Feature Engineering

  1. The Age column was derived from the Age Group column using Generative AI tools. Applicants in the Teenager group were assigned ages 16–19, Young Adults were assigned ages 20–29, and       Middle Age applicants were assigned ages 30–50.
  2. For logistic regression, categorical variables were encoded into numeric format. The Gender column was converted to binary, with Male = 1 and Female = 0. From the Training_Type           column, two dummy variables were created: Training_Advanced (Advanced = 1, Basic/None = 0) and Training_Basic (Basic = 1, Advanced/None = 0).

### Exploratory Data Analysis

EDA involved exploring the DMV road assessment data to answer key questions, such as:
  
  1. What is the total number of applicants, and among them, how many successfully qualified versus how many did not qualify?

  2. What is the Qualification rate in DMV Road Assessment?

  3. What is the distribution of applicants by gender (male vs. female), and within each group, how many passed and how many failed?

  4. What is the distribution of applicants across different age groups?

  5.  What is the distribution of applicants across different race?

  6.  What is the distribution of applicants across different training types, and within each type, how many passed, how many failed, and what is the qualification rate?

  7.  What is the overall average age of applicants, and how does it compare between those who qualified and those who did not?

  8.  What is the distribution of pass rates across gender, age groups, training types, and race?

  9.  What are the pass rates of male and female applicants across different training types (Advanced, Basic, None)?

  ![Capture](https://github.com/user-attachments/assets/3d142cc7-de43-4e81-9e7a-8b95f483f271)

  ![Capture](https://github.com/user-attachments/assets/957ea8c7-66b8-4900-b6b3-da86ffdafd0d)

  ![Capture](https://github.com/user-attachments/assets/d2fb038c-f68f-4082-b713-5f81079bc6b3)

### Statistical Analysis
  #### Relationship between age & Pass-Fail group





    

