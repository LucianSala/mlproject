# Student score prediction - End to End ML Project

### Introduction About the Data :

**The dataset** The goal is to predict the `math_score` based on a number of explanatory variables.

There are 7 independat varuiables, as follows:
* `gender` : male or female
* `race_ethnicity` : race/ethnicity encoded    
* `parental_level_of_education`: level of eduction for parents (i.e. college)
* `lunch`: beneficiary of lunch programs and type of programs students qualify for
* `test_preparation_course` : presents the level of preparation of students for the test
* `reading_score` : reading score
* `writing_score`: writing score

Target variable:
* `math_score` : math score

Dataset Source Link :
[https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?select=StudentsPerformance.csv](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams?select=StudentsPerformance.csv)

# Approach for the project 

1. Data Ingestion : 
    * In Data Ingestion phase the data is first read as csv. 
    * Then the data is split into training and testing and saved as csv file.

2. Data Transformation : 
    * In this phase a ColumnTransformer Pipeline is created.
    * for Numeric Variables first SimpleImputer is applied with strategy median, then Standard Scaling is performed on numeric data.
    * for Categorical Variables SimpleImputer is applied with most frequent strategy, then ordinal encoding performed , after this data is scaled with Standard Scaler.
    * This preprocessor is saved as pickle file.

3. Model Training : 
    * In this phase base model is tested. The best model found was Linear Regression.
    * After this hyperparameter tuning is performed.
    * After tunning the model is saved as pickle file.

4. Prediction Pipeline : 
    * This pipeline converts given data into dataframe and has various functions to load pickle files and predict the final results in python.

5. Flask App creation : 
    * Flask app is created with User Interface to predict the gemstone prices inside a Web Application.

# Exploratory Data Analysis Notebook

Link : [EDA Notebook](./notebook/1. EDA Student Data.ipynb)

# Model Training Approach Notebook

Link : [Model Training Notebook](./notebook/2. Model Training.ipynb)