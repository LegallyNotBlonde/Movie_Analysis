# Movie_Analysis

## Project Collaborators:
* [Iosif Vard](https://github.com/IosifVard)
* [Jean Vicencio](https://github.com/jpvicencio)
* [Sabrina Linden](https://github.com/LegallyNotBlonde)

## Purpose: 
1. **Forecasting Movie Sales Based on Historical Performance**
2. **Make suggestions to movie producers on how to maximize their gross revenue**: 
<p> - *identifying key secret sauce to successful movies such as which types of movies made the highest gross revenue, which features affected the revenue the most*


* **PLEASE GIT PULL THE UPDATED FILES EVERY TIME BEFORE WRITING YOUR CODE**.
* We will need to ensure we have only 1 file with the code (use only 1 file or combine several into one)
* Let's use self-explanatory names for all files including images and graphs
* **KIND REMINDER FOR EVERYONE TO SUBMIT THEIR CODES IN ADDITIONAL BRANCHES AND NOT THE MAIN BRANCH**
___


## Draft Plan for the project

### ETL: clean the data and save a data frame - Iosif - due date:
* remove lines with missing values - several columns have missing values
* remove unnecessary columns: column R, AA
* filter out or remove movies outside of US (US scope only) 
* options to validate the data: check for mispelling, wrong/future dates(years), other anomalies thatare more likely data errors
* correct the datatypes where needed
* change columns' names for self-explnatory options
* **After the data is cleaned the DataFrame will be saved in 'Outcome_Files' folder.**

<p> GROUP: *After clean up, check the data what is left (size of the data, number of languages).* to verify if we have sufficient data


#### Averages and data distribution - Jean - due date: 
* Create a copy of the cleaned dataframe for safety (in case of any errors our cleaned data stays intact)
* Averages of the whole data set gross revenue, budjet, movie duration, actors (do we need to do averages group by, for example, genre or budget?)
* Data distribution for the following values: gross revenue, budget, and movie durations
* T-test and ANOVA tests - are they beneficial for our type of data with multiple generes combined?

### Machine Learning - Sabrina: question to TAs: if Jean and I work in paralel on the same file and submit it to GitHub via different branches, will it combine them both well (no code will be lost)?

1. Establish and assess Baseline metrics like linear regression ( gross revenue on y, using scaling)

2.1. Create Neuron Network model (possibly  Sequential model with ReLU-activate), play with it such as: 
<p> - different number of **hidden layers**, different **activation button**,  adding/creating more **bins** for rare occurrences in columns. Increasing or decreasing the **number of values for each bin**. Adding **more neurons to a hidden layer**. 
<p> - changing the 2nd and 3rd activation function to 'sigmoid' is a good choice, this also helps boost the accuracy. Adding or reducing the number of epochs to the training regimen. 

2.2. Use one of the options to identify the most influential features in neuron network (to avoid creating an additional Random Forest Model):
<p> - Feature Importance Using Permutation Importance (evaluates feature importance by measuring the increase in the model's error);
<p> - SHAP (SHapley Additive exPlanations) (provides insight into the importance of features and how they impact the model’s predictions);
<p> - Partial Dependence Plots (PDP) (show the relationship between a feature and the predicted outcome).

* **LINKS** for sources https://developers.google.com/machine-learning/intro-to-ml/supervised,
* Additional Neural Nets Links: https://www.scaler.com/topics/binning-in-data-mining/ https://www.geeksforgeeks.org/binning-in-data-mining/ https://www.scaler.com/topics/deep-learning/neural-network-hyperparameters-tuning/ https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6 https://www.geeksforgeeks.org/activation-functions-neural-networks/ https://machinelearningmastery.com/choose-an-activation-function-for-deep-learning/ https://scikit-learn.org/stable/modules/neural_networks_supervised.html https://www.tensorflow.org/api_docs/python/tf


### Create at least THREE visualization of the most important trends (some of the possible options):
* Feature Importance: Visualize the top features that significantly affect movie sales, helping to understand the most influential factors.
* Bar Chart: Display box office revenue per genre to highlight which genres perform best.
* Bar Chart: Showcase Top 10 actors box office revenue.
* Line Graph:  Illustrate the trend of box office sales over the years to identify patterns.
* Linear Regression: Demonstrate the relationship between selected features and box office performance.

### Results:

### Conclusion:

### Create presentation:
* Up to 10 minutes for presentation - make sure we don't spend too much much on less imprtant things, and give anough time to present the most important information
* Discuss how we want to present, who present each part (each collaboratior must preent at least one slide)
* If we have time, discuss how we can keep our audience engaged, like maybe asking them an engaging question like post in the zoom chat their favorite movies or genres

### Ethical considerations:

### Data Limitations:
* Prices for older movies may not include inflation adjustments.
* Facebook likes (actors and directors popularity) were not available prior to wide spread of Facebook users.
* Our data did not include date or month to establish if seasonality plays a role
___

### Data Source:
[Kaggle](https://www.kaggle.com/code/aditimulye/imdb-5000-movie-dataset-analysis)