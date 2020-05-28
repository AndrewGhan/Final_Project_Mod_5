# Final_Project_Mod_5
Link to my Presentation: https://docs.google.com/presentation/d/1xIKQeRhfjv2uzAHZgmz35gf8qtI8Dl9YfbgERCIbzEw/edit?usp=sharing
## Introduction
In this project, my goal was to predict future S&P 500 index values to help investors guide their investments. The S&P 500 is an index that is comprised of the stock prices of the top 500 companies (weighted by company size) and divided by a proprietary divisor. Throughout American history, most investors have looked at the Dow Jones Industrial Average and the Dow Jones Transportation Average to make investment decisions, now the S&P 500 has taken their spot due to the amount of companies that are included. The S&P 500 is a more wholesome index that is a better representation of our economy as a whole. My project follows the OSEMI Data Science Process and is be formatted in the following manor:
 1. Obtained S&P 500 Data
 2. Cleaned my data 
 3. Explored my data to find trends 
 4. Formated my Data to run through my model 
 5. Ran a base model and progressively created better models
 6. Interpreted my results 
 8. Provided Future steps to improve my model
---------------------------------------------------------
## Proceedure
### Download-Clean-Explore
I obatained my Data from https://finance.yahoo.com/quote/%5EGSPC/history?p=%5EGSPC as a CSV file. I downloded index historical information from 1980-2019. After I got my information into my notebook explored my data, in my data I have 10,087 rows and 7 columns before doing any data preperation. Then I relized my data had random days missing in the data. To remedy this problem, first I formated the Date colunm to DateTime and I set it as my index, then, I resampled my data to months. Then, I calculated my opening index price's rolling mean, rolling standard mean, and percent change, then ran basic visualizations to find trends in my data. 
What I found was that the S&P 500 has grown by 2771% in the past 40 years. In other words, if you had invested $100,000 dollars in an S&P ETF 40 years ago you would have made $2,771,000. After I created these visulaizations, I used the original dataset and created a dataframe resampled to days and I filled the missing values with the value that came before it. 
### Data Preprocessing 
After properly setting up and exploring my data, I created my train test split and formated my variables as scaled 3D vectors in sets of 60 days so that they could be pased through my model. How I formatted my data allows the model to predict 1 day ahead using 60 previous days of data. 
### Modeling
Once I formatted my train test split properly then I created 4 different models to test what the best hyperparameter set up are. After my running all of my models I calculated their RMSE,
Baseline Model RMSE = 69.20
Model2 RMSE = 15.75
Model3 RMSE = 38.50
Final Model RMSE = 45.67
Model 2 hase the best RMSE score though I suspect that this could be due to overfitting of my data.
### Interpretation 
After testing all of my models with a few different iterations of hyper parameters, Model 4 is the best. This is because it can track the pattern of the S&P 500 fairly well and includes dropout parameters to reduce the problem of over fitting. This model is not ready for production, though once fully developed this model could revoluionize the way we trade and make investment decisions.
### Future Steps
My next steps for this model is to 
1) Include NLP Sentiment Analysis to see if average daily news sentiment in the finance and business sections of the New York Times attribute to the S&P moving in an up or down.
2) Run this model on data from the Dow Jones Industrial Average and Dow Jones Transit Average. 
3) Create an app encompassing predictions for all major indices.

![alt text](https://github.com/AndrewGhan/Final_Project_Mod_5/blob/master/Final_Project_Pictures/Screen%20Shot%202020-05-27%20at%203.23.05%20PM.png)

![alt text](https://github.com/AndrewGhan/Final_Project_Mod_5/blob/master/Final_Project_Pictures/Screen%20Shot%202020-05-27%20at%203.07.13%20PM.png)

![alt text](https://github.com/AndrewGhan/Final_Project_Mod_5/blob/master/Final_Project_Pictures/Screen%20Shot%202020-05-27%20at%203.06.59%20PM.png)

![alt text](https://github.com/AndrewGhan/Final_Project_Mod_5/blob/master/Final_Project_Pictures/Screen%20Shot%202020-05-27%20at%203.06.44%20PM.png)

![alt text](https://github.com/AndrewGhan/Final_Project_Mod_5/blob/master/Final_Project_Pictures/Screen%20Shot%202020-05-27%20at%203.06.35%20PM.png)



















