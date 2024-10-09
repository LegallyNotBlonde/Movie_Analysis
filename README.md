# Movie_Analysis

## Project Collaborators:
* [Iosif Vard](https://github.com/IosifVard)
* [Jean Vicencio](https://github.com/jpvicencio)
* [Sabrina Linden](https://github.com/LegallyNotBlonde)


## Title: Forecasting Movie Sales Based on Historical Performance

## Purpose: 
1. **Forecasting Movie Sales Based on Historical Performance**
2. **Provide recommendations to movie producers on maximizing gross revenue:**: 
Identify key factors for successful movies, such as which types or features contribute most to high gross revenue.


* **PLEASE GIT PULL THE UPDATED FILES EVERY TIME BEFORE WRITING YOUR CODE**.
* We will need to ensure we have only 1 file with the code (use only 1 file or combine several into one)
* Let's use self-explanatory names for all files including images and graphs
* **KIND REMINDER FOR EVERYONE TO SUBMIT THEIR CODES IN ADDITIONAL BRANCHES AND NOT THE MAIN BRANCH**

__

**BEFORE RUNNING A CODE IN GOOGLE COLAB:**
Please **upload to google colab 'movie_metadata.csv' from 'Resources' folder to the same directory level as the code in Google Colab**.
Other details of the repo structure are provided below the data sources.
___

## Project Plan:

### ETL: clean the data and save a data frame - Iosif - due date:
* Load the Dataset: Use pandas to read the dataset.
* Remove Null Values: Check for nulls in important columns and handle them (drop or impute); several columns have missing values
* Drop Irrelevant Columns: movie_imdb_link and aspect_ratio (column R, AA)
* Convert Data Types where needed: Ensure that all features are in the appropriate format (e.g., convert categorical variables to numerical using encoding).
* Filter out or remove movies outside of US (US scope only) 
* Other options to validate the data: check for mispelling, wrong/future dates(years), other anomalies thatare more likely data errors
* Change columns' names for self-explnatory options where needed
* **After the data is cleaned the DataFrame will be saved in 'Outcome_Files' folder.**



#### Averages and data distribution - Jean - due date: 
* Use .describe() to get an overview of the dataset
* Create a copy of the cleaned dataframe for safety (in case of any errors our cleaned data stays intact)
* Averages of the whole data set gross revenue, budjet, profit, movie duration, actors (do we need to do averages group by, for example, genre or budget?) **create a sepate data frame for it to is in Tablea**
* Min and Max - for example 5 movies with the highest revenue and 5 movies with the lowest revenue - **create a sepate data frame for it to is in Tablea**
* Visualize the distribution of key features using box plots.for the following values: gross revenue, budget, and movie durations
* T-test and ANOVA tests - are they beneficial for our type of data with multiple generes combined?

### Machine Learning - Sabrina 

1. Establish and assess Baseline metrics like Linear Regression Model
* Remove 'profit' column as added aggr field from gross-budget 
* Use scaling (gross revenue, budject)
* Split the Data: Use train-test split for model validation.
* Build the Model: Use scikit-learn to create a linear regression model.
* Evaluate Performance: Assess model performance using metrics like R², Mean Absolute Error (MAE), and Mean Squared Error (MSE).
* Visualization: Scatter plot of predicted vs. actual sales.

2.1. Create Neuron Network model (possibly  Sequential model with ReLU-activate), play with it such as: 

* Define the Neural Network: Use Keras to build a neural network model with appropriate layers.
* Train the Model: Train the model on the training set and validate on the test set.
* Evaluate Performance: Use the same metrics as in the linear regression phase.
* Model Optimization
•	Hyperparameter Tuning: Experiment with different architectures, activation functions, learning rates, and batch sizes:

<p> - different number of **hidden layers**, different **activation button**,  adding/creating more **bins** for rare occurrences in columns. Increasing or decreasing the **number of values for each bin**. Adding **more neurons to a hidden layer**. 
<p> - changing the 2nd and 3rd activation function to 'sigmoid' is a good choice, this also helps boost the accuracy. Adding or reducing the number of epochs to the training regimen. 

2.2. Use one of the options to identify the most influential features in neuron network (to avoid creating an additional Random Forest Model):
<p> - Feature Importance Using Permutation Importance (evaluates feature importance by measuring the increase in the model's error);
<p> - SHAP (SHapley Additive exPlanations) (provides insight into the importance of features and how they impact the model’s predictions);
<p> - Partial Dependence Plots (PDP) (show the relationship between a feature and the predicted outcome).

* **LINKS** for sources https://developers.google.com/machine-learning/intro-to-ml/supervised,
* Additional Neural Nets Links: https://www.scaler.com/topics/binning-in-data-mining/ https://www.geeksforgeeks.org/binning-in-data-mining/ https://www.scaler.com/topics/deep-learning/neural-network-hyperparameters-tuning/ https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6 https://www.geeksforgeeks.org/activation-functions-neural-networks/ https://machinelearningmastery.com/choose-an-activation-function-for-deep-learning/ https://scikit-learn.org/stable/modules/neural_networks_supervised.html https://www.tensorflow.org/api_docs/python/tf


### Create at least THREE visualization of the most important trends (some of the possible options): to ne assigned
* Feature Importance: Visualize the top features that significantly affect movie sales, helping to understand the most influential factors.
<p> Create a visualization comparing the most profitable features on the X-axis (e.g., movies with very popular actors vs. less popular actors) and gross revenue on the Y-axis. 
Add a line showing the average gross revenue across all movies to highlight the influence. Use a similar visualization style for other graphs:
<p>  * Bar Chart: Display box office revenue per genre to highlight which genres perform best. 
<p>  * Bar Chart: Showcase Top 10 actors box office revenue.
<p>  * Line Graph:  Illustrate the trend of box office sales over the years to identify patterns.
<p>  * Linear Regression: Demonstrate the relationship between selected features and box office performance.


### Results:

### Conclusion:

### Create presentation:
* Up to 10 minutes for presentation - make sure we don't spend too much much on less imprtant things, and give anough time to present the most important information
* Discuss how we want to present, who present each part (each collaboratior must preent at least one slide)
* If we have time, discuss how we can keep our audience engaged, like maybe asking them an engaging question like post in the zoom chat their favorite movies or genres

### Ethical considerations:

### Data Limitations:
* **Prices for older movies** may not include inflation adjustments.
* **Information for older movies may be biased** since such movies are rarely shown during prime time, and the number of likes on social media platforms may not be accurate.
* **Our data does not include date or month** information, making it difficult to analyze potential seasonality effects.
* **Gross revenue in the dataset is recorded only for the first week** in theaters, excluding revenue from later shows. This may introduce biases, and gross revenue could also be affected by factors not included in the data, such as the number and quality of movie advertisements.

### Data Source:
[Kaggle](https://www.kaggle.com/code/aditimulye/imdb-5000-movie-dataset-analysis)

___

### Repository Organization