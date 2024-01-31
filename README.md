**Abstract**

Every industry is experiencing financial crunch because of the pandemic, including the movie business. Hence, to decrease the financial risk, prediction of the gross earnings of a movie is essential to the movie industry. Therefore, the goal of the project is to create a regression model that will predict US movies’ gross after considering several features. The features include IMDb rating, certification, duration of the movie, number of votes and metascore. Anyone interested in financing or investing in the movie, including individual producers, film studios, private investors, etc. will benefit from this model.

**Design**

The project is designed to webscrape the information of the movies from IMDb website and then utilize the data to build and select the most accurate predictive model for gross earnings of a movie based on its features. Several regression models like linear regression, ridge regression, lasso regression, etc. will be utilized to evaluate the training and validation scores of the dataset to choose the model with the best metric values and run the test data.

**Data**

The data is scraped from IMDb.com website using Python libraries and packages including Request and BeautifulSoup. Initially, the data had 3000 movies with 9 features. After the data cleaning, an interaction feature was added, and the irrelevant columns were eliminated during feature engineering. This resulted in 2951 movies with 20 features.  


**Algorithms**

  •	Feature Engineering: 
  
    o	Categorical feature (certificates) was converted to dummy variables.
    
    o	Interactive terms were subtracted to make the feature (year) more relevant.

  •	Models:
  
    o	Several regression models were explored to select the best predictive model. 
    
    o	Data was split into 60% training, 20% validating and 20% testing.
    
    o	Following are the results of various models:

        **Regression Models            Training Score	    Validation Score**
        Normal Linear Regression	0.389285939	0.461151975
        K-fold Linear Regression	0.389285939	0.379048417
        Polynomial Regression Degree 2	0.00471088	-0.07468319
        Polynomial Regression Interaction	0.50838276	0.3800856
        Ridge Regression	0.46113795	0.38928325
        Ridge Regression Cross-Validation	0.389283247	0.379102316
        Lasso Regression Cross-Validation	0.389285939	0.379048764
        Ridge Regression on polynomial interaction only	0.61451453	0.54744346


