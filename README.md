# *Module 14 Challenge*
## Deep Neural Network for Predicting Successful Funding Applicants

**Welcome to my Module 14 Challenge repository. Here, you can check out the algorithmic trading bot I created that learns and adapts to new data and evolving markets. Find out more in the follwing sections!**

---

## Background
In this project, I assumed the role of a financial advisor at one of the top five financial advisory firms in the world. 

My firm constantly competes with the other major firms to manage and automatically trade assets in a highly dynamic environment. In recent years, my firm has heavily profited by using computer algorithms that can buy and sell faster than human traders. The speed of these transactions gave my firm a competitive advantage early on. But, people still need to specifically program these systems, which limits their ability to adapt to new data. 

I thus planned to improve the existing algorithmic trading systems and maintain the firm’s competitive advantage in the market. To do so, I enhanced the existing trading signals with machine learning algorithms that can adapt to new data.

This project consists of three technical deliverables:
- Implementing an algorithmic trading strategy that uses machine learning to automate the trade decisions.
- Adjusting the input parameters to optimize the trading algorithm.
- Training a new machine learning model and compare its performance to that of a baseline model.

---

## Technologies & Usage
This project leverages Python 3.7, TensorFlow and the Keras Library, SciKit-Learn, and the Pandas library with the following requirements and dependencies:
- import pandas as pd
- from pathlib import Path
- import tensorflow as tf
- from tensorflow.keras.layers import Dense
- from tensorflow.keras.models import Sequential
- from sklearn.model_selection import train_test_split
- from sklearn.preprocessing import StandardScaler,OneHotEncoder

---

## Evaluation Report
The first model tested in this project uses the SVC classifier model from SKLearn's cupport vector machine (SVM) learning method to fit the training data and make predicitions based om the testing data. The baseline paramters include a DateOffset value of 3 months with SMA input features of short_window = 4 and long_window = 100. The classification report showed the model to a have an accuracy of 0.55, with recall and f1 vlaues that indicated the model to be much better at predicting '1' than -1.
INSERT IMAGE

The second model tested in this project was a variation on the first, which still used the SVC classifier and kept the same SMA input features, but changed the DateOffset value to 6 months. The classification report was nearly identical to the baseline, with a slight increase in the accuracy score from 0.55 to 0.56.
INSERT IMAGE

The third model tested was, again, a tuning of the baseline's parameters. This time, I continued to use the SVC classifier and kept the DateOffset at 3 months, but changed the SMA input features to short_window = 10 and long_window = 200. The classification report showed that this tuning helped the model perform a little better in predicting '-1', but had an accuracy score that was the same as the baseline.
INSERT IMAGE

The fourth model tested kept the same SMA input features and the DateOffset value as the baseline, but used the DecisionTreeClassifier instead of the SVC classifier. The classification report showed that this change in classifier helped the model achieve a much more balanced performance in predicting the -1 and 1, but at a slight cost to the higher recall and f1 values we had seen for '1' in the earlier instances. But, this classifier didn't help with the accuracy of the model, and, in fact, showed a decrease in accuracy from the baseline's 0.55 to 0.49.
INSERT IMAGE.









