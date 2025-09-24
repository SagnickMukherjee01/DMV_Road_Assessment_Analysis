# DMV_Road_Assessment_Analysis

### Table of Contents
 
 - [Project Overview](#project-overview)
 - [Key Objectives](#key-objectives)
 - [Key Performance Indicators](#key-performance-indicators)
 - [Overview of Dataset Structure](#overview-of-dataset-structure)
 - [Tools Used](#tools-used)
 - [Data Cleaning](#data-cleaning)
 - [Feature Engineering](#feature-engineering)
 - [Exploratory Data Analysis](#exploratory-data-analysis)
 - [Statistical Analysis](#statistical-analysis)
 - [Logistic Regression Predicting Road Test Success](#logistic-regression-predicting-road-test-success)
 - [Failure Reasons](#failure-reasons)
 - [Data Analysis and Visualization](#data-analysis-and-visualization)
 - [Key Findings](#key-findings)
 - [Recommendations](#recommendations)
 - [Limitations](#limitations)

### Project Overview
---

This project analyzes a simulated DMV road test dataset to uncover the key factors that influence whether applicants pass or fail their driving test. With high failure rates leading to delays and added costs, the study aims to generate actionable insights that can improve training programs, optimize resource allocation, and support applicants in being better prepared.

### Key Objectives
---

1. Demographic Insights: Explore pass/fail trends across age, gender, and race.

2. Training Effectiveness: Evaluate the impact of different training levels (Advanced, Basic, None) on outcomes.

3. Performance Drivers: Identify the most significant road assessment indicators that predict success.

4. Predictive Modeling: Build and test a logistic regression model to estimate pass likelihood and measure performance using accuracy, precision, recall, and F1-score.

5. Threshold Analysis: Demonstrate how varying cutoff points affect predictions using confusion matrices.

6. Interactive Dashboards: Design Power BI dashboards with dynamic filters (demographics, training, results) to provide intuitive, real-time insights.

### key Performance Indicators
---

<img width="1731" height="801" alt="image" src="https://github.com/user-attachments/assets/12f3696e-dfcb-4040-bf8a-dd6a9e271fa2" />

### Overview of Dataset Structure
---

- ### DADV-2-Capstone Project-Group D-Dataset Drivers License Data:-
  Contains data on applicant’s demographics (age , gender and    race), training participation and road assessment indicators.

### Tools Used
---

 - Excel- Feature Engineering, Exploratory Data Analysis, Statistical Analysis and Data Visualization
   - [Download_Here](https://www.microsoft.com/en-in/microsoft-365/excel)
 - Power Bi- Data Visualization using DAX formulas
   - [Download_Here](https://www.microsoft.com/en-us/download/details.aspx?id=58494)

### Data Cleaning
---

#### Key Data Cleaning Process Included:-

  1. Accurate data types of the fields were assigned.

  2. The dataset was thoroughly checked for all the missing values and for duplication of data and no such things were found.

  3. All the numeric fields are converted into numeric datatypes from general datatypes to ensure proper analysis.

### Feature Engineering
---

  1. The Age column was derived from the Age Group column using Generative AI tools. Applicants in the Teenager group were assigned ages 16–19, Young Adults were assigned ages 20–29,         and Middle Age applicants were assigned ages 30–50.
  2. For logistic regression, categorical variables were encoded into numeric format. The Gender column was converted to binary, with Male = 1 and Female = 0. From the Training_Type           column, two dummy variables were created: Training_Advanced (Advanced = 1, Basic/None = 0) and Training_Basic (Basic = 1, Advanced/None = 0).

### Exploratory Data Analysis
---

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
---
  ##### 1. Relationship between age & Pass-Fail group

   A T test was conducted between ages of passed people and failed people and we got that the age significantly influences the outcome (p = 0.005). On average, candidates who passed the     road test were older (28.7 years) compared to those who failed (26.3 years). This suggests maturity/experience may improve success rates. 

   ![Capture](https://github.com/user-attachments/assets/aa32d7bd-39ad-47ad-907f-7e45cdce739d)

  #### 2. Chi-Square Outcome between gender and pass/fail

   Chi Square test was conducted between Gender vs Pass-Fail and we got that there is no significant relationship between gender and pass/fail outcome.

   ![Capture](https://github.com/user-attachments/assets/8b2face1-4584-48fd-bea6-ed075f450e3f)

 #### 3. Chi-Square Outcome between training type and pass/fail

   Chi Square test was conducted between Training Type and Pass/Fail and we got that there is strong and statistically significant relationship between Training_Type and pass/fail          outcome.

   ![Capture](https://github.com/user-attachments/assets/619761d9-5e9d-45fe-9d30-524f8c2eb714)

### Logistic Regression Predicting Road Test Success
---

1. Logistic regression model built to predict Pass/ Fail outcome.
2. Predictor variables used: Gender ,Age , Training_Advanced , Training_Basic , Theory Test, Reaction time, Signals, Speed Control, Road_signs, Mirror usage ,Confidence, Parking,           Night_Drive, Steer_Control.
3. Categorical variables converted to dummy variables (Males=1, Females=0,In Reaction_Fast Fast=1,Slow & Average=0 and In Reaction_Slow Slow=1, Fast & Average=0).
4. Model assigns a probability of passing (0-1) for each candidate.
5. Cut-off is set in a dynamic way in excel to classify “Pass” Vs “Fail”.
6. By using the Maximum Likelihood Estimation Method(MLE) we got that Training Type Advanced and Basic are the main deciding factors for whether a person will pass or fail in the           driving test.
7. A confusion matrix is set to count True Positive , True Negative , False Positive , False Negative and from that accuracy , precision and F1 score is also calculated where we            minimized False Positives as we can’t afford to mark inefficient drivers as an efficient drivers.
8. Here cutoffs are set in excel in a dynamic way so that whenever we will change the cutoff TP, TN, FP, FN, Accuracy, Precision and F1 score will change automatically when we will         refresh the pivot table.

 #### Key Factors responsible for success

 After Filtering By P Value We got Training Advanced and Training Basic are most important decision making Predictors and negative coefficient for intercept shows without training or     skills the base chance of passing is low.

 The strongest drivers of passing are Advanced Training (coef 0.45) and Basic Training (coef 0.31), followed by skill-based factors like Signals, Road Signs, and Mirror Usage.            Demographics such as age and gender show no significant effect

 ![Capture](https://github.com/user-attachments/assets/f073715e-00f2-4a93-b147-2c8523d7c890)

 ![Capture](https://github.com/user-attachments/assets/cdb0cfa2-b527-4b6c-8857-f8f120b4ade1)

 #### Prediction model Outcome

 ![Capture](https://github.com/user-attachments/assets/950725d5-a655-477f-81f4-fecfa0d8ec50)

 ### Failure Reasons
 ---

 <img width="1731" height="607" alt="image" src="https://github.com/user-attachments/assets/aa85ec9a-153e-40e7-801d-172c24881c93" />

 ### Data Analysis and Visualization
 ---

 After data cleaning ,pre processing, data analysis using statistical techniques all the excel files are loaded into Power Bi. Then with the help of Power Bi DAX formulas ,               Visualization  Charts and other important features of Power Bi Three Dashboards were created to address all the questions in problem statement.
 
 #### 📊 Dashboard 1: DMV Road Test Analysis – Qualification Patterns by Demographics and Training

  - Purpose- Highlights trends in qualification rates across age groups, gender, race, and training types to uncover demographic and behavioral patterns.

  - Viualization-

    ![Capture](https://github.com/user-attachments/assets/cce9dd90-0b5f-4643-8de0-2677f5f23375)

 #### 📊 Dashboard 2: Training & Demographic Influence on Qualification Outcomes
  
  - Purpose- Evaluates the impact of different training programs and demographic attributes on pass/fail outcomes, helping identify factors that enhance success rates.

  - Visualization-

    ![Capture](https://github.com/user-attachments/assets/7e569c15-6c37-4728-8ee6-86c7b7819807)

#### 📊 Dashboard 3: Predicting Pass/Fail in DMV Road Test – Logistic Regression Insights
  
  - Purpose- Applies predictive modeling through logistic regression to estimate the likelihood of qualification, enabling data-driven decision support.

  - Visualization-

    ![Capture](https://github.com/user-attachments/assets/e840ab37-91b0-4253-bfc4-4ebb96bec705)

### Key Findings
---

 #### 1. Training Impact: Applicants with Advanced training achieved the highest pass rate (88.16%). Those with Basic training had more candidates under slower reaction types.

 #### 2. Gender Insights: Males had the highest qualification rate (50.82%), while females had the highest fail rate (51.17%).

 #### 3. Age Trends: The Middle Age group (30–50) had the highest pass rate (39.36%), whereas Teenagers (16–19) experienced the highest fail rate.

 #### 4. Reaction & Performance: Candidates with fast reaction times had the highest pass rate (35.99%).

 #### 5. Race Analysis: The Others race group had the highest qualification rate (34.06%), and White candidates had the highest fail rate.

 #### 6. Test Scores: Average written and theory test scores were highest among Young Adults (20–30) and those with Advanced training.

 #### 7. Correlation Insights: Age positively correlates with qualification, indicating maturity improves success likelihood.

 #### 8. Predictive Modeling: Logistic regression showed applicants with Advanced or Basic training are more likely to pass.

 #### 9.Cutoff Optimization: At a 60–88% cutoff, the model achieved 73% accuracy with minimal false positives, aligning with the goal of reducing candidates incorrectly predicted as                                  passing.

### Recommendations
---

#### 1. Promote Advanced Training Programs
-  Applicants who took advanced training had the highest chance of passing. Increasing access to such programs will improve pass rates.
#### 2. Encourage Basic Training for Beginners
- Even basic training gives applicants a better chance of success compared to no training. Making this more widely available can reduce failures.
#### 3. Focus on Key Driving Skills
- Indicators like signals, road signs, and mirror usage showed significant impact on outcomes. Extra practice and testing in these areas can raise success rates.
#### 4. Regularly Monitor Results with Dashboards
- An interactive dashboard helps DMV officials track pass rates by gender, age, and training type. This makes it easier to spot trends and adjust training programs quickly.
#### 5. Track Demographic Trends
- While gender showed no significant impact , age and training choices did. Monitoring subgroups performance ensures fairness and highlights were extra support is needed.

### Limitations 
---

#### 1. Observational data — causality not proven. 
- We only looked at existing data. We have seen  patterns (like training and pass rates), but we can’t be 100% sure that training causes higher pass rates. There may be other reasons.
#### 2. Training selection may be endogenous (people who opt for training may differ)
- The people who choose “advanced training” might already be more motivated or better prepared than those who don’t. So, their higher pass rate may not be only because of the training.
#### 3. Possible measurement error in skill indicators
- Some information might not be fully accurate (for example, if skills or training were recorded incorrectly, or if people reported it themselves instead of being observed).
#### 4. Model may omit other relevant variables
- We didn’t have all possible factors (like prior driving experience, confidence level, or family income). These could also influence pass/fail results but were not included in the        model.






 












    

