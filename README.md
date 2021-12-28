# Machine Learning Trading Bot

In this application, I assume the role of a financial advisor at a top financial advisory firm. My firm would like me to improve the existing algorithmic trading systems and mantain the firm's competitve advantage in the market. To do so, I'll enhance the existing trading signals with machine learning algorithms that can adapt to new data.

---  

## Overview

My first step is to establish a baseline performance. To begin, I import the OHLCV dataset into a Pandas Dataframe. Then, I generate trading signals using short- and long-window SMA values. I split the data into training and testing datasets and use the SVC classifier method to fit the training data and make predictions on the testing data. With the prediction finished, I generate a classification report and create a Dataframe for my predictions.
I then create a cumulative return plot that shows the actual returns vs. the strategy returns. This will serve as my baseline against which to compare the effects of tuning the trading algorithm. The objective is to tune the algorithm to give my firm optimal returns.

![screenshot of the baseline model](https://raw.githubusercontent.com/chaimkriger/Challenge_14/main/4-100-3%20orignal%20svm%20(2).png)

This is my baseline algorithm. As you can see above, the strategy returns are clearly greater than the actual returns. Meaning, it would be more profitable for my firm to use the baseline trading algorithm than to simply hold the equity. Attached below is the classification report for this model.

![screenshot of classification report of baseline model](https://raw.githubusercontent.com/chaimkriger/Challenge_14/main/SVM%20Testing%20Report%20(2).png)

Although the trading algorithm is clearly giving positive returns, my firm wants me to better the parameters for the algorithm with some tuning.

My next step is to change the amount of months for the trading period. The baseline model used a training period of 3 months, and so I attempt the run the algorithm with a training period of 6 months. Below is my results: