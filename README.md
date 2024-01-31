**Abstract**

Every industry is experiencing financial crunch because of the pandemic, including the movie business. Hence, to decrease the financial risk, prediction of the gross earnings of a movie is essential to the movie industry. Therefore, the goal of the project is to create a regression model that will predict US movies’ gross after considering several features. The features include IMDb rating, certification, duration of the movie, number of votes and metascore. Anyone interested in financing or investing in the movie, including individual producers, film studios, private investors, etc. will benefit from this model.

**Design**

The project is designed to webscrape the information of the movies from IMDb website and then utilize the data to build and select the most accurate predictive model for gross earnings of a movie based on its features. Several regression models like linear regression, ridge regression, lasso regression, etc. will be utilized to evaluate the training and validation scores of the dataset to choose the model with the best metric values and run the test data.

**Data**

The data is scraped from IMDb.com website using Python libraries and packages including Request and BeautifulSoup. Initially, the data had 3000 movies with 9 features. After the data cleaning, an interaction feature was added, and the irrelevant columns were eliminated during feature engineering. This resulted in 2951 movies with 20 features.  


**Algorithms**

•	Feature Engineering: 

   -Categorical feature (certificates) was converted to dummy variables.

   -Interactive terms were subtracted to make the feature (year) more relevant.

•	Models:

  -Several regression models were explored to select the best predictive model. 
  
  -Data was split into 60% training, 20% validating and 20% testing.
  
  -Following are the results of various models:

  **Regression Models	      Training Score	      Validation Score**
  
Normal Linear Regression	  0.389285939	      0.461151975
    
K-fold Linear Regression	  0.389285939	      0.379048417

Polynomial Regression Degree 2	0.00471088	  -0.07468319

Polynomial Regression Interaction	0.50838276	  0.3800856

Ridge Regression	                0.46113795	  0.38928325

Ridge Regression Cross-Validation	0.389283247	0.379102316

Lasso Regression Cross-Validation	0.389285939	0.379048764

Ridge Regression on polynomial interaction only	0.61451453	0.54744346



o	The model that was selected was Ridge regression on polynomial interaction only features.


Ridge Regression on poly interaction only validation Score: 0.54744346

Ridge Regression on poly interaction only Training Score: 0.61451453

Ridge Regression on poly interaction only Testing Score: 0.59082610



**Tools**

•	Python libraries including Request, BeautifulSoup, Pandas and Numpy for web scraping, parsing and data manipulation.

•	Scikit-learn for modeling and evaluation metrics.

•	Matplotlib and Seaborn for data visualizations.



**Communication**

As stated above, Ridge Regression on polynomial interaction only features is the best model for prediction of gross earnings. Following charts were utilized to analyze and communicate the results: 

**Heatmap Correlations**


![image](https://github.com/Himani0924/Regression_predicting_movies_earnings/assets/99743248/6fe67fb1-8edc-491c-905a-0abfa2f5a16e)


**Pairplot of features and target variable**

![image](https://github.com/Himani0924/Regression_predicting_movies_earnings/assets/99743248/0c986e1c-ea4c-4ba4-b706-33b4e0fec11a)


**Gross based on metascore, rating and duration**

![image](https://github.com/Himani0924/Regression_predicting_movies_earnings/assets/99743248/bbc2e4cc-6d88-420b-9e4c-ecb98b58148c)


**Top 10 Movies by Votes on IMDB**

![image](https://github.com/Himani0924/Regression_predicting_movies_earnings/assets/99743248/5505d4d9-18b7-42f1-8588-8ee4b113f8a3)



![image](https://github.com/Himani0924/Regression_predicting_movies_earnings/assets/99743248/f190196b-4c51-4bfc-bf39-3e92a33aaa8a)




![image](https://github.com/Himani0924/Regression_predicting_movies_earnings/assets/99743248/7cd61c5b-3f3a-4ceb-9545-84a1c7e95834)






