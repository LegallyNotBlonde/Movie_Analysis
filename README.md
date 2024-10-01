# Movie_Analysis

## Project Collaborators:
* [Iosif Vard](https://github.com/IosifVard)
* [Jean Vicencio](https://github.com/jpvicencio)
* [Sabrina Linden](https://github.com/LegallyNotBlonde)

## Purpose: 
1. **Forecasting Movie Sales Based on Historical Performance**
2. **Make suggestions to movie producers on how to maximize their gross revenue**


* **PLEASE GIT PULL THE UPDATED FILES EVERY TIME BEFORE WRITING YOUR CODE**.
* We will need to ensure we have only 1 file with the code (use only 1 file or combine several into one)
* Let's use self-exlanatory names for all files including images and graphs
* **KIND REMINDER FOR EVERYONE TO SUBMIT THEIR CODES IN ADDITIONAL BRANCHES AND NOT THE MAIN BRANCH**
___


## Draft Plan for the project

### ETL
* remove lines with null values
* remove unnecessary columns (like links, etc), but keep majority
* filter out or remove movies outside of US (US scope only)
* check for mispelling, wrong/future dates(years), other anomalies thatare more likely data errors
* correcr the datatypes where needed
* change columns' names for self-explnatory options

### Data Testing
* P value and other statistical test
* data distribution based on gross revenue, budget and other factors

### Machine Learning
* Establish and assess Baseline metrics like linear regression (gross reveue)
<p> PCA, scaling?

* Create Neuron Network model (possibly  Sequential model with ReLU-activate), play with it such as: 
<p> - different number of **hidden layers**, different **activation button**,  adding/creating more **bins** for rare occurrences in columns. Increasing or decreasing the **number of values for each bin**. Adding **more neurons to a hidden layer**. 
<p> - changing the 2nd and 3rd activation function to 'sigmoid' is a good choice, this also helps boost the accuracy. Adding or reducing the number of epochs to the training regimen. 

* optionally use Random forest to identify most influential features and put them on the graph

* **LINKS** for sources https://developers.google.com/machine-learning/intro-to-ml/supervised,
* Here are some links to help you further your understanding on Neural Nets. https://www.scaler.com/topics/binning-in-data-mining/ https://www.geeksforgeeks.org/binning-in-data-mining/ https://www.scaler.com/topics/deep-learning/neural-network-hyperparameters-tuning/ https://towardsdatascience.com/activation-functions-neural-networks-1cbd9f8d91d6 https://www.geeksforgeeks.org/activation-functions-neural-networks/ https://machinelearningmastery.com/choose-an-activation-function-for-deep-learning/ https://scikit-learn.org/stable/modules/neural_networks_supervised.html https://www.tensorflow.org/api_docs/python/tf



### Create at least THREE visualization of the most imprortant trends (some of the posible options)
* Bar Chart: Display box office revenue per genre to highlight which genres perform best.
* Bar Chart: Showcase Top actors box office revenue
* Line Graph: Illustrate of trend of box office sales over the years to identify patterns and seasonality.
* Feature Importance: Visualize the top features that significantly affect movie sales, helping to understand the most influential factors.
* Linear Regression: Demonstrate the relationship between selected features and box office performance.

### Results

### Conclusion

### Create presentation
* verify the time limits for the presentation
* discuss how we want to present, who present each part
* if we have time, discuss how we can keep our audience engaged, like maybe asking them an engaging question like post in the zoom chat their favorote movie or genre

### Ethical considerations
___

### Data Source:
[Primary data will be sourced from Kaggle](https://www.kaggle.com/code/aditimulye/imdb-5000-movie-dataset-analysis)