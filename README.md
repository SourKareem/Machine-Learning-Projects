# Machine-Learning-Projects
These are my machine learning projects that I have completed for Data Science that showcase my skills in Python, data cleaning, and machine learning.
## Car Resell (Linear Regression)
### Summary
I got this dataset from Kaggle to practice my Linear Regression models. This is a web scraped dataset that is of used cars posted for resell. This means the prices aren't always going to be a fair or reasonable price but it makes it interesting to look at.
### Data Cleaning
I start off every project looking at the data using .info(), .describe(), and just looking at the first and last 5 rows of the dataset. This gives a quick insight on how everything looks and what you need to change. I see right away that there is 7 columns that need to be changed because they are object data types. So next I go through each of these columns and see if one hot encoding is the right way to go about it and to see if there is other data cleaning to do. This dataset did have a lot of values put in the wrong columns or values that didn't belong there. A few examples of what I had to do was create masks to drop rows with certain values in the string, renaming a column, one hot encoding, changing object to datetime, using a simple imputer, dropping useless columns, and creating an age column.
### Model Training & Testing
Now I did a heatmap to get a sense of correlation between price and the other variables, then split the dataset into the training and testing splits. I then used the Standard Scaler and fit the datasets, then import the Linear Regression model from sklearn.
### Results
The score I got was 0.01999 which is awful and shows that the model was not good at predicting the price at all. This is most likely due to the fact that the prices aren't regulated or calculated by the people posting them so the prices can be very off from what would be considered fair. There could be other factors like the brand name that will increase a car's price because of the name, and general wear and tear that could bring these other prices down. This was a great dataset for learning and practicing data cleaning but not so great for predictions.

## Laker Predictor
### Laker Predictor
#### Laker Predictor
