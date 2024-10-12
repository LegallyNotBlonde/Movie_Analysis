# Movie Revenue Forecasting with Machine Learning

## Project Collaborators:
* [Iosif Vard](https://github.com/IosifVard)
* [Jean Vicencio](https://github.com/jpvicencio)
* [Sabrina Linden](https://github.com/LegallyNotBlonde)


## Purpose: 
1. **Forecasting Movie Revenue Based on Historical Performance**
2. **Provide recommendations to movie producers on maximizing gross revenue**
Identify key factors for successful movies, such as which types or features contribute most to high gross revenue.

___

## Project Overview:

<p> Movie studios commonly track various metrics to optimize revenue and minimize costs. Key areas include box office performance (e.g., gross revenue and opening weekend sales) and production costs to calculate profit margins. 
<p> Evaluating marketing effectiveness through advertising ROI, social media engagement, and audience feedback is another effective strategy. Timing and competition analysis help identify optimal release windows, while audience demographics guide content tailoring. 
<p> Monitoring talent metrics, such as actor popularity, helps predict box office success. Additionally, streaming data, ancillary market performance, and long-term digital distribution trends are analyzed to maximize revenue beyond initial releases.

<p> To streamline these critical but potentially time-consuming analyses, we aimed to build a machine learning model to predict movie revenue based on historical records. However, due to limitations in our publicly available data, which are detailed below, the accuracy and scope of our predictions may be affected


**BEFORE RUNNING A CODE IN GOOGLE COLAB:**
Please **upload 'movie_metadata.csv' from the 'Resources' folder to the same directory level as the code in Google Colab**.
___

## Workflow Overview:

### ETL:
Cleaining data by removing errors, duplicates, or missing values to ensure the data is accurate and usable. Clean data is essential for reliable results.

#### Data Exploration:
Analyze the data's distribution, size, and types to understand its structure and key patterns. This helps identify which features are important and what transformations may be needed.

### Machine Learning 
* **Model Selection:** Evaluate different machine learning models based on the type and size of the data.
* Establish and assess Baseline metrics like **Linear Regression Model**
* Based on size our data, we used **Random Forest** model using **StandardScale**
* **Data Splitting, Training, and Evaluation:** Divide the data into training and testing sets. Train the model using the training data to learn patterns and relationships, then evaluate its performance with the testing set to ensure it accurately predicts new information.
* **Feature importance** and its implementation depend on whether the model is overfitting or underfitting. However, identifying the most influential features can still provide crucial insights into effective movie strategies, such as prioritizing actors, marketing, or release timing, regardless of model performance.
* **Model Tuning:** Adjust parameters and fine-tune the model to optimize its performance. This step maximizes accuracy and reliability.

### Create at least THREE visualization related to the scope of the project 
* Data Distribution and/or Averages
* Heatmap
* Model Accuracy Rates
* Numeric Feature Importance
* Scatter plot of predicted vs. actual sales?


## Results:


### Presentation preparation:
* Our audience - other data analysts and the focus is a technical aspect of the project
* The presentation is up to 10 minutes. Ensure we don't spend too much time on less important details and allocate enough time for the most important information
* Combine our code into 1 file, keeping only the most important thinngs that we're going to present
* Keeping audience engaging, but keeping the serious tone of our presentation

___

### Ethical considerations:
In this project, we used only publicly available, anonymized data to ensure privacy. We acknowledged dataset limitations and biases, such as missing release dates and revenue data, which may impact prediction accuracy. We mitigated bias by focusing on diverse variables and clearly communicated our analysis limitations. Our aim was to provide actionable insights to producers responsibly, supporting data-driven decisions while respecting creative integrity.

___

### Data Limitations and Recommendations:
* Gross revenue, budget, and profit figures are not adjusted for inflation.
* The dataset lacks release dates, hindering analysis of seasonality effects or competition when other major films are released close by.
* It only captures earnings from the first week in cinemas, missing subsequent revenue.
* Movie genres and plot keywords are arranged alphabetically instead of by significance, impacting the model's precision.
* The data does not capture critical variables like marketing spend, plot popularity, theater count, and audience demographics.
* Including these influential elements could greatly enhance the accuracy of the prediction mode.
* Given that modern movies can generate up to 500 million dollar profit, continued investment and advancements in data analytics can provide even greater benefits.
___

### Data Source:
[Kaggle](https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset)

___

### Repository Organization
* **Main_code** contains all the code for data cleaning, exploration, machine learning models, and related plots
* **Notebooks** folder includes separate files with codes to clean and explore the data, and to create machine learning  models.
* **Outcome_Files_DFs** folder has intermediate files like 'cleaned_data.csv'
* **Presentation_and_Proposal** folder contains our final proposal in PDF format. However, after closely analyzing our data, we chose a Random Forest model instead of a Neural Network.
* **Resources** folder includes our data source called "movie_metadata.csv"
