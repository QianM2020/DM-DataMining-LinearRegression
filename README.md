
### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [CRISP-DM](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python.  The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

As a statistics graduate student, I'm passionate about DS and ML.The programming
is becoming part of my life. I'm interested what the platform and program tech
these Professional programers are using in their work. Also what factors are related
their JobSatisfaction.


## File Descriptions <a name="files"></a>
#Code
  Project 1.ipynb : You can find all the python code for this project.
    Markdown cells were used to assist in walking through the thought process for individual steps.
# Data
  survey_results_public.csv : The data from Stack Overflow’s 2017 Annual Developer Survey. (154 columns*19,102 row )
  survey_results_schema.csv : Reference of Columns in survey_results_public

## CRISP-DM<a name="results"></a>
  Business Understanding
    1. What's the target market of Stackoverflow?
    2. What are the most popular platforms and databases among the Employed Professional Developers?
    3. What relates to the Employed Professional Developers' job satisfaction?

  Data Understanding
    1. In order to understand Q1 the features of Stack Overflow users, I check the the Professional, EmploymentStatus fields.
    2. To answer Q2, I took a closer look at the HaveWorkedDatabase and WantWorkDatabase column, and HaveWorkedPlatform and WantWorkPlatform column with Professional Employed Developers data.
    3. For Q3, I chose only quantity variables ('CareerSatisfaction', 'JobSatisfaction', 'HoursPerWeek', 'Salary') with Professional Employed Developers data.

  Prepare Data
    * Missing Data: Before fitting model for Q3, I dropped the rows whose ‘JobSatisfaction’ is missing, delete the column ‘Expected Salary’ since the values of whole column is missing. For the other columns, I used the mean of the column to fill the missing values respondingly.
    * Data transform: for Q1, I set all ‘Professional developer’ user as ‘Professional’ and all the others as ‘Not professional’, and the users who are ‘Employed full-time’,‘Independent contractor, freelancer, or self-employed’,‘Employed part-time’ as ‘Employed’ and all the others as ‘Not Employed.’

  Model Data
    Linear regression model is used to predict ‘JobSatisfaction’ in Q3, since the respondent ‘JobSatisfaction’ is evaluated as numeric.
    The whole dataset was randomly split into training data(70%) and testing data (30%) to train the model and do prediction.

  results
    Rsqure score of the model for both training and prediction is about 40%.

   Deploy
    Summary the whole project and results by publishing a blog.
    https://blog.csdn.net/QianMeng2020/article/details/111402868

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Must give credit to Stack Overflow for the data.  You can find the Licensing for the data and other descriptive information at the Kaggle link available [here](https://www.kaggle.com/stackoverflow/so-survey-2017/data).  Otherwise, feel free to use the code here as you would like!
