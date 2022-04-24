![alt text](https://storage.googleapis.com/pr-newsroom-wp/1/2020/03/Header.png)

# SC1015-Mini-Project-Group 8
Repository for NTU Module SC1015 Mini-Project

## About
Our team's objective for this Mini-Project is on the Spotify Top 200 Charts from 2020-2021. With the increasing interconnectedness due to globalisation and the emergence of Covid-19, music preferences have seen a major shift. This is evident with the coming of the term "corona-music". 

As such, it is ever more so difficult for budding artistes to be able to identify what songs will be streamed more. It would be good for artists to be able to gauge their song streams before releasing their music, i.e. 'test the waters'.

## Problem Statement
Which regression model can best accurately predict the number of streams a song will receive based on a song's characteristics.

## Files in Repository
For a  detailed walkthrough, please view the source code in order from:
1. Data Cleaning and Exploratory Analysis

   (Due to GitHub's static render of notebooks, to view the Plotly graphs, do download and rerun the Python Notebook on a local system. Otherwise, they can be found in our presentation slides or can be viewed through this link: https://nbviewer.org/github/Jovin2525/SC1015-Mini-Project/tree/main/Group%208/Codes/)
   
2. Model 1: Linear Regression
3. Model 2: Random Forest Regression
4. Model 3: Gradient Boosted Regression

## Conclusion
With the help of R^2 values (for Linear Regression) and Mean Absolute Percentage Error (for Random Forest and Gradient Boosted Regression), we were able to conclude the high accuracy obtained for predicting total number of streams a song will garner based on its attributes using either Random Forest Regression or the Gradient Boosted Regression. The accuracy both models showed on the train and test datasets achieve a very high accuracy of above 90%. 

Though the differences in accuracy from both models are mostly insignificant, the deciding factor of which model is best lies it its time efficiency. Random Forest Regression edges out on its efficiency in bulding the model, with an average runtime of 20 seconds when tuning the hyper-parameters, compared to that of Gradient Boosted Regression which took an average of 10 minutes.

With similar prediction accuracies, but faster model building, Random Forest Regression is thus chosen as the preferred model to predict the number of streams a song will receive based on its characteristics.

## What have we learnt from this project
- Identifying and cleaning of invalid data from a dataset through exploration of data
- Data Visualisation through recommended Plotly
- Conversion of a categorical type value to numerical type, through the use of One-Hot Encoding and Label Encoding
- Random Forest Regression
- Gradient Boosted Regression
- Cross-validation of data for the tuning of hyper-parameters
- Different metrics to analyse model accuracy such as MAPE
- How to determine, with reasons, which model is most appropriate

## Contributors
- @Jovin2525 (Jovin Ng Zu Wei) 
- @haofah14 (Lam Hao Fah) 
- @yauuuuuu (Ng Shang Yau) 

The three of us worked tirelessly together to complete every aspect of this project. Each of us contributed a fair share and we are happy with the final outcome.

## References
- https://www.kaggle.com/datasets/sashankpillai/spotify-top-200-charts-20202021
- https://www.forbes.com/sites/evaamsen/2021/02/27/coronamusic-gives-people-a-sense-of-belonging-according-to-research/?sh=64b584df131d
- https://towardsdatascience.com/random-forest-in-python-24d0893d51c0
- https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
- https://machinelearningmastery.com/gradient-boosting-machine-ensemble-in-python/

