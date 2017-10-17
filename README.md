# Freddie-Mac-Data-Analysis

Part 1: Data wrangling
Data Download and pre-processing:
Your first challenge is to programmatically download the data from https://freddiemac.embs.com/FLoan/Data/download.php by getting past the login page using Python.

Exploratory Data analysis:
• Write a Jupyter notebook using Python to graphically represent different summaries of data. Summarize your findings in this notebook.

• Analyse the quarterly data from 2007,2008, 2009 data including summary measures for different attributes, trends over time for different variables. Counts, variability of numerical measures etc. Leverage postal codes and states to indicate location specific information.

• Look at things like interest rate trends, delinquency trends over quarters, location specific insights etc.

Sharing the work:
Run the docker image:
docker pull joshisn/assignment3:part2
Docker run -it joshisn/assignment3:part2 /bin/bash

Change csv file quarter_input_1.csv with your credentials

Python Script_part2.py

Part II: Building and evaluating models.

Prediction 
• Write a prediction script in a Jupyter notebook that given input (For example Q12005)

o Programmatically downloads Q12005 and Q22005 origination data and pre-processes it.

o Builds a Regression model for the interest rate using Q12005 data as training data (col 13)

o Does variable selection to choose the best Regression model using Forward, Backward, Stepwise and Exhaustive search methods.

o Validates against the Q22005 datasets

o Computes MAE, RMS, MAPE for training and testing datasets

o Repeat this using Random Forest & Neural Network algorithms.

o Choose the best model amongst the 3 types of algorithms.

• Perform what-if analysis and have your algorithm used in various scenarios:

o Financial crisis (https://www.stlouisfed.org/financial-crisis/full-timeline )

▪ Run the algorithm for 4 rolling quarters and report your findings and discuss it in your report. (i.e Use Q12007, Q22007, Q32007, Q42007 for training and predict for Q22007,Q32007,Q42007,Q12008)

▪ Run the algorithm 2 years later (i.e, 2009 for all 4 quarters)
o Economic boom (1999, 2013) (https://www.thebalance.com/stock-market-returns-by-year-2388543 )

▪ Discuss your design and results in a report. Would you recommend using this model for the next quarter? Justify

o Regime change (2016) from election

Classification 

• Write a new jupyter notebook that given input (For example Q12005)

o Programmatically downloads Q12005 and Q22005 origination data and pre-processes it.

o Builds a Logistic regression model for the CURRENT LOAN DELINQUENCY STATUS using Q12005 data as training data (col 4). Note anytime col 4 is > 0, add a new variable as Delinquent. Use this variable as your “Y” variable. IGNORE COL 4 AND DON’T USE IT IN YOUR MODEL.

o Validates against Q22005 data and selects the best Classification model

o Computes ROC curve and Confusion matrices for training and testing datasets

o Repeat this using Random Forest & Neural Network algorithms.

o Choose the best model amongst the 3 types of algorithms.

• Parameterize the input (example it should take Q12005) and modify the code so that it outputs the 5 parameters listed in the matrix.

• Write another script that calls the above classification script from Q11999-Q42016 and computes the matrix.

