# Machine-Learning-Projects
These are my machine learning projects that I have completed for Data Science that showcase my skills in Python, data cleaning, and machine learning.

## Car Resell (Linear Regression)
This is one of my Linear Regression practice projects. I got this dataset from Kaggle to practice my Linear Regression models. This is a web scraped dataset that is of used cars posted for resell. This means the prices aren't always going to be a fair or reasonable price but it makes it interesting to look at.
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. I see right away that there is 7 columns that need to be changed because they are object data types. So next I go through each of these columns and see if one hot encoding is the right way to go about it and to see if there is other data cleaning to do. This dataset did have a lot of values put in the wrong columns or values that didn't belong there. A few examples of what I had to do was create masks to drop rows with certain values in the string, renaming a column, one hot encoding, changing object to datetime, using a simple imputer, dropping useless columns, and creating an age column.
</details>
<details>
<summary>Model Training & Testing</summary>
Now I did a heatmap to get a sense of correlation between price and the other variables, then split the dataset into the training and testing splits. I then used the Standard Scaler and fit the datasets, then import the Linear Regression model from sklearn.
</details>
<details>
<summary>Results</summary>
The score I got was 0.01999 which is awful and shows that the model was not good at predicting the price at all. This is most likely due to the fact that the prices aren't regulated or calculated by the people posting them so the prices can be very off from what would be considered fair. There could be other factors like the brand name that will increase a car's price because of the name, and general wear and tear that could bring these other prices down. This was a great dataset for learning and practicing data cleaning but not so great for predictions.
</details>

## Cancer Diagnosis (K Nearest Neighbors)
This is one of my K Nearest Neighbors practice projects. I got this dataset from Kaggle to practice my KNN models. We are classifying a patients diagnosis as Benign (B) or Malignant (M)
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. This dataset didn't need much cleaning other than an error column.
</details>
<details>
<summary>Model Training & Testing</summary>
I got right to splitting the dataset and Scaling it using Sklearn StandardScaler and train_test_split. I use the square root of the size of the test dataset so the amount of nearest neighbors makes sense. I then set the metric to euclidean which is standard, fit the data, and printed out the results.
</details>
<details>
<summary>Results</summary>
For this project I used a confusion matrix to analyze how it predicted the diagnoses. Then I printed out the f1 score and accuracy and saw the model was very good at predicting the state of the tumor given this data.
</details>

## Lakers Predictor (Random Forest Classifier)
This is one of my own machine learning practice projects. I got this dataset from the NBA api. In this project I was still learning the api and what info I could get from where and how to access the data so it was very messy and inefficient, eventually I want to build a newer and better model as well as a more efficient notebook to run as I should pull less data in.
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. I then dropped a lot of columns that wouldn't help the model. Then I took the matchup column and took the opposing team's abbreviation so I could join other data into this dataset. My plan was to get each team's ranks by record and join that into the data using the opponent's abbreviation. This is where the discovery of the API shows as I have to pull a new dataset. Then I clean this dataset so the Lakers are out of it and all I have is the team id and their rank. Then I pull all team's team id and abbreviation and join them, then I join this new datset with the original dataset so it now has the opponents rank. This is going to be my training dataset. 
My next idea to predict the games is using an average game performance from the Lakers would be the prediction dataset. Unfortunately I don't think there is a way to pull only this season's averages so I pulled a lot of data doing this. Then I built a pipeline to drop the unnecessary columns and to convert the stats to per game stats. This will save code and time later.
</details>
<details>
<summary>Model Training & Testing</summary>
Now here I run these only once then I add the echo skipping code to not run this when I run the full notebook later to predict the games. I ran the predictions and the accuracy isn't great as it is a very bare bones model, but I believe it was around 60+% accuracy. Now whenever I want to run this again I change the value of the opponent variable to the team's abbreviation and it adds the new row to the dataset and I have a simple custom message showing the result clearly.
</details>
<details>
<summary>Results</summary>
So far this model is 1-1 in predicting, I don't expect this model to be very accurate as sports are very complicated and I have a super simple model.
</details>

## Bank Churn (Logistic Regression)
This is one of my Logistic Regression practice projects. I got this dataset from Kaggle to practice my Logistic Regression models. We are classifying a user as churned or stayed and will use it to predict other customers on if they will churn or stay.
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. I dropped the State column as I didn't think it was very important, and reformatted the voice mail plan and international plan columns to boolean columns.
</details>
<details>
<summary>Model Training & Testing</summary>
Then I did my standard scaler and train test split.
</details>
<details>
<summary>Results</summary>
Here I used a confusion matrix and the classification report to get more in-depth with the results and how the model predicts. You can see that when it is true that the user churned, it wasn't good at predicting that. This could be due to the lower amount of churned users in the dataset, so it couldn't train well enough. I think that the model is good at predicting when a user will stay, but not when a user is going to leave. This could be fixed with more data potentially.
</details>

## Diagnosis Model Comparison (SVM & KNN)
This was project to compare the effectiveness of the SVM and KNN models. I got another cancer diagnosis dataset that was similar to the last one I used. We are classifying a patients diagnosis as Benign (B) or Malignant (M).
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. Nothing to clean on this dataset luckily.
</details>
<details>
<summary>Model Training & Testing</summary>
I just used my standard procedure of StandardScaler, train_test_split. I then trained the SVM model and used it to predict and get the scores of it. Then repeated the process for the KNN model.
</details>
<details>
<summary>Results</summary>
You can see that the SVM had a 0.03 higher score in accuracy. This usually wouldn't be significant but because of how high their accuracy already is, that last 3% is very important. So the SVM model is definitely the way to go for this dataset.
</details>

## Sales Predictor (Linear Regression)
This is one of my Linear Regression practice projects. I got this dataset from Kaggle to practice my LR models. This is supposed to predict sales based on how much is invested in other forms of advertising.
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. The only things I need to do now is to one hot encode the influencer column and to impute the missing values. 
</details>
<details>
<summary>Model Training & Testing</summary>
I just used my standard procedure of StandardScaler, train_test_split.
</details>
<details>
<summary>Results</summary>
I got the results with an accuracy of 99%. This is almost certainly due to the dataset being for practicing and not really a random dataset. I then used just the TV column because it had almost a 1:1 correlation with the sales and the results were almost identical. This concludes that if this was real, TV advertisements have a linear affect on sales.
</details>

## Titanic (Random Forest)
This was my first ever project with machine learning. This was a guided project as I followed someone else's directions> I learned a lot about the process of training these models and getting them ready to train and predict.
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. I created a pipeline to transform, impute and drop columns. This saved a ton of time and taught me a lot about the process.
</details>
<details>
<summary>Model Training & Testing</summary>
Then I use the scaler and the random forest model with a parameter grid to determine the best parameters for the model. Then I do this for the actual test dataset and submitted the results. I got a score of 77.
</details>
<details>
<summary>Results</summary>

</details>

## Model Comparison (Decision Tree and Random Forest)
This project was for me to see how much of a difference there is between a single tree and a forest. This was done with a bank churn dataset.
<details>
<summary>Data Cleaning</summary>
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. I dropped the Surname column, gender column, and one hot encoded the card type and geography columns.
</details>
<details>
<summary>Model Training & Testing</summary>
I just used my standard procedure of StandardScaler, train_test_split.
</details>
<details>
<summary>Results</summary>
The accuracy score was identical between the two models. This could be due to a biased dataset or that it wasn't a real dataset and is simply for practicing machine learning.
</details>
