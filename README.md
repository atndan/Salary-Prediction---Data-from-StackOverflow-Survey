# Salary-Prediction---Data-from-StackOverflow-Survey

Stack Overflow is popular website that allows users to post questions and answers on a wide range of topics in computer programming.
For this project the data is get from the Stack Overflow Developer Survey1, which is a large annual survey that examines many aspects of the developer experience such as career satisfaction, work habits, and opinions on different technologies

## Exploratory Data Analysis

Starting by exploring the data a little. explore the association between salary and some of the predictors. Since many of the predictors are qualitative, or on a discrete scale, box plots are useful for visualization.


Here we can see a positive relationship between company_size_number and Salary, which mean the bigger
the company is, the higher the salary is in average.

<img width="700" alt="image" src="https://user-images.githubusercontent.com/91353356/176011419-0dc3128a-2a10-40d6-92a0-41ad99c4d960.png">


From the plot, the salary is significantly different between countries, US is the highest salary group, while
Canada, Germany and UK are pretty equal.

<img width="682" alt="image" src="https://user-images.githubusercontent.com/91353356/176011862-1b36c9ef-dcfd-477a-a064-0204b6653458.png">

It is interesting that there is not much different in salary between group that they code as hobby with group
that they do not code as hobby.

<img width="715" alt="image" src="https://user-images.githubusercontent.com/91353356/176011932-09358b70-7af5-4bf6-8ddb-9af4b9fbfade.png">


## Cross-Validation

The stack_overflow dataset is randomly splited into a 70% training and 30% test set. 

**Multiple Linear Regression & Stepwise selection**

<img width="638" alt="image" src="https://user-images.githubusercontent.com/91353356/176012590-110e6fb7-f8aa-4947-a57b-62a4918d26f9.png">
<img width="498" alt="image" src="https://user-images.githubusercontent.com/91353356/176012555-8640d7d9-b49d-4a21-8d51-1f5ffad65352.png">

<img width="685" alt="image" src="https://user-images.githubusercontent.com/91353356/176012323-4f051d3c-f821-4b72-bddb-d0d90a130bd6.png">
The importance plot gives a ranking of the predictors in the model, the most important variable is
years_coded_job, and the least important variable is remote.



**Regression Tree**

<img width="659" alt="image" src="https://user-images.githubusercontent.com/91353356/176012701-9d7209b1-aeb4-4fc3-9b44-c6f3486fe316.png">


**RSME & R_square** 



<img width="943" alt="image" src="https://user-images.githubusercontent.com/91353356/176013804-cbe3f76a-5e2e-4727-8fe5-22b9470cfba2.png">

From the summary table, Random Forest model has the smallest RMSE, and the highest R_square 67.8%.
In terms of predictive performance, Random Forest is the best performance model.
In terms of interpretability, Regression Tree is the best modelfor interpret since it has only 4 nodes and 6 leafs in the model and RSME is just slightly higher than Random Forest.


<img width="749" alt="image" src="https://user-images.githubusercontent.com/91353356/176013984-5f7ea967-fa83-46cd-9521-b196be05ceab.png">


