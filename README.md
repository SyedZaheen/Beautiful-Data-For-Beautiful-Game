# Beautiful-Data-For-Beautiful-Game
NTU SC1015 (Intro Data Science and AI) Project by Syed Zaheen and Jayden Yeo. Lab DSF1 Group 3 

## About

This is a Mini-Project for SC1015 (Introduction to Data Science and Artificial Intelligence) which focuses on the English Premier League Dataset. For detailed walkthrough, please view the source code in order from:

1. [Data Preparation](https://github.com/SyedZaheen/Beautiful-Data-For-Beautiful-Game/blob/main/Data%20Preparation.ipynb)
2. [Problem Formulation 1, 2 and Data Visualisation](https://github.com/SyedZaheen/Beautiful-Data-For-Beautiful-Game/blob/main/Problem%20formulation%201%20and%20Exploratory%20Data%20Analysis.ipynb)
3. [Multivariate Linear Regression and Random Forest Classifer](https://github.com/SyedZaheen/Beautiful-Data-For-Beautiful-Game/blob/main/Multivariate%20Linear%20regression%20and%20random%20forest%20classifier.ipynb)
4. [Problem Formulation 3, Clustering and Feature Engineering](https://github.com/SyedZaheen/Beautiful-Data-For-Beautiful-Game/blob/main/Clustering%20and%20feature%20engineering.ipynb)


## Storyboard

Given the sheer popularity of the English Premier League, we decided to center our project around matches from 8 seasons from this competition. Our overall project aim is to **generate recommendations** for Premier League teams so that they can **score more goals** and ultimately win more matches  

Our initial angle to the project was to find out which variable predicts number of goals scored the best. The idea was that we can ask teams to maximise or minimise this particular variable so that they score more goals. Thus, we used **multivariate linear regression** to compare the coefficients of each of our variables used.

As multivariate linear regression was quite inaccurate in predicting goals, we adopted a **random forest classifier** instead to determine if goals is best predicted as a numerical or categorical data type. Our findings showed that it was best predicted as a categorical data type. The prediction was far more accurate.

However, our findings showed that, unsurprisingly, number of shots on target predicts number of goals scored the best, and by a large margin too. Thus, our recommendation is to take more shots in order to score more goals - which is pretty obvious. Since our problem had such an easy answer, we decided to refine our problem. 

We wanted to now see if there is **any patterns in the data outside of number of shots that relate to average number of goals scored per team**. The rationale was that, if we saw that **maximising or minimising certain variables** (a little bit like the 'style of play' of the team) ultimately resulted in the team scoring more goals, we can then recommend that more Premier League teams adopt these style of play.

We used **K-means clustering** to determine certain clusters in our data. We saw that the algorithm had decided to classify the data according to maximising 3 variables - possession, passing, and touches - and these variables also resulted in the most number of goals scored. 

However, it is well-known that certain football teams purposely choose to give possession to the oppostion and minimise the above three, and still be successful. So, in order to re-test our hypothesis, we **feature engineered a new variable called "Shot Quality"**, because the idea was that perhaps maximising the above variables also lead to lower shot quality, and thus certain teams may still choose to give up possession, passes and touches in order to gain greater shot quality. 

However, in the contrary, our findings showed that teams that had high possession, touches and clearances also had higher shot quality. Thus, our final recommendation to Premier League teams is to maximise possession, passsing and touches, because they ultimately will lead to more goals, and result in more wins. 

## Problem Formulation

1. Are we able to predict the **number of goals scored** (response) using the **other variables in the data** (predictors)?
2. Which variables are most relevant in predicting goals? (feautre importance)
3. Which playstyle (or patterns in the data) results in the team scoring more goals? (unsupervised clustering problem)

## Models Used

- K-Means clustering
- Linear regression
- Random forest classifier

## Conclusion

- Shots and Shots on Target have a high correlation with number of goals scored (unsurprisingly).
- Treating number of goals scored as a categorical variable and using the random forest classifier model lead to a higher accuracy in the prediction of goals.
- Teams that adopt high possession, passing and touches are generally more successful.
- Teams who play higher possession take better quality shots. 

## What did we learn from this project?

- Web scraping techniques
- Silhouette score and how to generate an optimal mnumber of clusters for centroid-based clustering
- Feature engineering: generating a new feature based on the results of linear regression


