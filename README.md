# Udacity Capstone Starbuck_project

[TOC]

## Project introduction

The current project is my Capstone Challenge for Udacity’s Data Scientist Nanodegree. We obtained the simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks. Not all users receive the same offer. In this project, I aim to investigate the following three questions:

Q1:How does the number of new member change along with time?

Q2: For those customers who didn’t receive offer but purchase coffee through transaction, which demographic factor predicts their average transaction?

Q3: : For the offers related data, which factors predict whether the offer was eventually successfully completed?

Please find the detailed introduction and results of this project at my [Blog Post](https://lydiafz-zoe.medium.com/will-you-redeem-a-cup-of-coffee-c7703383d2b5).

## Files Description

The following files were included in the current project:

- Data files: In the Data folder, there are three datasets:

    ***Portfolio dataset\*** 

  Portfolio dataset provides the detailed information of the 10 different offers (i.e., reward, channel, difficulty, duration, offer type, offer id). 

    ***Profile dataset\***

  The profile dataset provides the detailed information of customers (i.e., age, gender, income, the time became the member, and annual income)

    ***Transcript dataset\***

  The Transcript dataset provides the detailed transaction and offer information.

- The jupyter file for the detailed data processing and results

## Project steps

### Packages

- Python 3.5+
- Jupyter notebook
- Sklearn machine learning models (i.e. LinearRegression; RandomForestClassifier; DecisionTreeClassifier; LogisticRegression)

### Data Processing

- Data cleaning: removing missing values; create dummy columns for categorical variables; replace Nan values with zero.
- Data merging: Merge the portfolio, profile,transcript into one dataset by customer_id and offer_id

### Exploratory analysis and Machine Learning Models

- For Q1, I used exploratory analysis to visualize the number of new members changing with year and age group;
- For Q2, I used the LinearRegression model to investigate which demographic factors predict the average purchase transaction;
- For Q3, I' applied three different models (i.e. Logistic regression; RandomForest; DecisionTree) to investigate which factors predict the offer completing situation (i.e. expired, valid, invalid) and compared the results.

## Conclusions

**For transactions:**

- There is a clear trend that the female has the higher transaction than other two gender group;
- Although there is a little bit difference between gender group, overall, the higher income group has the higher transaction;

**For offers:**

- Three models all provide fair to good results, but the DecisionTreeClassifier model generated the best result;
- According  to  the results, we can see that the reward given by completing the offer provides is the most important predictor of the offer complete.
- Among the three offer type (i.e.informational, discount, bogo), the informational type offer is more likely to be completed.

- The  social channel might has the better effect on the offer complete
- The longer duration of the offer might result in more complete.

## Limitations

- It was kind of arbitrary when separating the income and age group, which might influence the regression analysis results;
- In further analysis, more statistics analysis should be included (e.g. if there is significant difference in transaction between different income groups? if there is interaction effect between income and gender etc.)
- Recommendation analysis can be considered in future.

## Licensing, Authors, and Acknowledgements

The project is finished by Zhuo Fang. I would like to thank Udacity for providing the dataset and the project supports.