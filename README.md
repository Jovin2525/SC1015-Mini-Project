![alt text](https://storage.googleapis.com/pr-newsroom-wp/1/2020/03/Header.png)

# SC1015-Mini-Project-Group 8
Repository for NTU Module SC1015 Mini-Project

## About
Our team's objective for this Mini-Project is on the Spotify Top 200 Charts from 2020-2021. With the increasing interconnectedness due to globalisation and the emergence of Covid-19, music preferences have seen a major shift. This is evident with the coming of the term "corona-music". 

As such, it is ever more so difficult for budding artistes to be able to identify what songs will be streamed more. It would be good for artists to be able to gauge their song streams before releasing their music, i.e. 'test the waters'.

## Problem Statement
Which regression model can best accurately predict the number of streams a song will receive based on a song's characteristics?

## Files in Repository
For a detailed walkthrough, please view the source code in order from:
1. Data Cleaning and Exploratory Analysis

   - Due to GitHub's static render of notebooks, to view the Plotly graphs, do download and rerun the Python Notebook on a local system. 
   - Otherwise, they can be found in our presentation slides or can be viewed through this link: https://nbviewer.org/github/Jovin2525/SC1015-Mini-Project/tree/main/Group%208/Codes/
   
2. Model 1: Linear Regression

   - Linear Regression was first used to predict song streams using "Streams" as the response variable. However, due to low correlation between "Streams" and the other numerical predictor variables, with most not exceeding an absolute correlation value of 0.1, it seemed that our regression problem is not linearly related. Additionally, when the model was fit, very low R^2 values of 0.18 and 0.12 were achieved for our train and test datasets respectively. As such, we decided to model our regression problem using other non-linear regression methodologies to see where that would take us.

3. Model 2: Random Forest Regression
  
   - Random Forest Regression was used to predict song streams through the use of decision trees. Initially, using an evaluation function, we were able to achieve a high accuracy of 91.74% for our base model. Not satisfied, we tried to tune our hyperparameters further using Grid Search Cross Validation. However, the tuned model only achieved an insignificant improvement of 0.37%. Though the improvement between the tuned model and the base model was insignificant, the MSE, RMSE and MAPE all improved quite a bit from the linear model. The data points were also much better fitted under the random forest model. Hence, we concluded the random forest model to be undoubtedly better than the linear model. 
   - Moving on, we decided to analyse our problem using Gradient Boosted Regression.
   
4. Model 3: Gradient Boosted Regression
   
   - Gradient Boosted Regression (GBR) was the third model we used to predict song streams. GBR also utilizes an ensemble of decision tress, but differs from Random Forest in terms of the order and way the results of each tree are combined. Instead of having random samples to train individual trees such like Random Forest, GBR builds one tree at a time where each new tree helps to correct errors made by the previously trained tree. By using our evaluation function, we achieved an initial accuracy of 82.71%. We then tuned our hyperparameters using Grid Search Cross Validation as well. The tuned model returned an accuracy of 91.42%, showcasing an improvement of 10.54%. The differences in MSE, RMSE and MAPE were also significant as compared to the linear model. The data points were also much better fitted under the Gradient Boosted Regression.
   - Next, we compare between the 3 regression models we have used.

## Conclusion
With the help of R^2 values (for Linear Regression) and Mean Absolute Percentage Error (for Random Forest and Gradient Boosted Regression), we were able to conclude the high accuracy obtained for predicting total number of streams a song will garner based on its attributes using either Random Forest Regression or the Gradient Boosted Regression. The accuracy both models showed on the train and test datasets achieve a very high accuracy of above 90%. 

Though the differences in accuracy from both models are mostly insignificant, the deciding factor of which model is best lies it its time efficiency. Random Forest Regression edges out on its efficiency in building the model, with an average runtime of 20 seconds when tuning the hyper-parameters, compared to that of Gradient Boosted Regression which took an average of 10 minutes.

With similar prediction accuracies, but faster model building, Random Forest Regression is thus chosen as the preferred model to predict the number of streams a song will receive based on its characteristics.

## What have we learnt from this project
- Identifying and cleaning of invalid data from a dataset through exploration of data
- Interactive Data Visualisation through Plotly (recommended)
- Conversion of a categorical type value to numerical type, through the use of One-Hot Encoding and Label Encoding
- Random Forest Regression
- Gradient Boosted Regression
- Cross-validation of data for the tuning of hyper-parameters
- Different metrics to analyse model accuracy such as MAPE
- How to determine, with reasons, which model is most appropriate

## Contributors
- @Jovin2525 (Ng Zu Wei, Jovin) 
- @haofah14 (Lam Hao Fah) 
- @yauuuuuu (Ng Shang Yau) 

The three of us worked tirelessly together to complete every aspect of this project, from ideation, to coding, and lastly to the presentation. Each of us contributed a fair share and we are happy with the final outcome. We have also built a solid friendship through this project.

## Dataset 
- https://www.kaggle.com/datasets/sashankpillai/spotify-top-200-charts-20202021

## References
- https://www.forbes.com/sites/evaamsen/2021/02/27/coronamusic-gives-people-a-sense-of-belonging-according-to-research/?sh=64b584df131d
- https://towardsdatascience.com/random-forest-in-python-24d0893d51c0
- https://towardsdatascience.com/hyperparameter-tuning-the-random-forest-in-python-using-scikit-learn-28d2aa77dd74
- https://machinelearningmastery.com/gradient-boosting-machine-ensemble-in-python/
- https://vitalflux.com/gradient-boosting-regression-python-examples/
