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

<p> To streamline these critical but potentially time-consuming analyses, we aimed to build a machine learning model to predict movie revenue based on historical records. However, due to limitations in our publicly available data, which are detailed below, the accuracy and scope of our predictions may be affected.

___

## Workflow Overview:

### ETL:
* Data was uploaded as csv file from the source.
* Cleaining data by removing errors, duplicates, or missing values to ensure the data is accurate and usable. Clean data is essential for reliable results.
* We used Google Colab because of it convenience. The code saves 'cleaned_data' to Colab Environment.
* Given the relatively small size of our data (around 3,000 lines with around 30 columns), we did not use PySpark, as it would only increase processing time

### Data Exploration:
Analyze the data's distribution, size, and types to understand its structure and key patterns. This helps identify which features are important and what transformations may be needed.

### Machine Learning: 
* **Model Selection:** Evaluate different machine learning models based on the type and size of the data.
* Establish and assess Baseline metrics like **Linear Regression Model**
* Based on size our data, we used **Random Forest** model using **StandardScale** and **get_dummies** function.
* **Data Splitting, Training, and Evaluation:** Divide the data into training and testing sets. Train the model using the training data to learn patterns and relationships, then evaluate its performance with the testing set to ensure it accurately predicts new information.
* **Feature importance** and its implementation depend on whether the model is overfitting or underfitting. However, identifying the most influential features can still provide crucial insights into effective movie strategies, such as prioritizing actors, marketing, or release timing, regardless of model performance.
* Assess model performance to determine which to develop further by implementing feature engineering techniques.
* **Model Optimization:** **Label encoding** and **feature engineering** helped enhance the model and maximize its accuracy and reliability.

### 'Main_Code.ipynb' includes the following visualizations related to the scope of the project: 
* Please find the following visualization in our 'Main_Code_United' file: 
<p> 1. Data Distribution
<p> 2. Correlation Heatmap
<p> 3. Scatter plot of predicted vs. actual gross revenue (Multiple Linear Regression Model)
<p> 4. Feature Importance for Numeric and Categorical Features (Basic Random Forest Model)
<p> 5. Feature Importance and Heatmap for Numeric Values in the Optimized Random Forest Model
<p> 6. Model Accuracy Rates Comparison: Linear Regression vs Basic vs Optimized Random Forest

## Conclusion:

The Optimized Random Forest model outperforms both the Multiple Linear Regression and Basic Random Forest models. With an R-Squared of 0.999952, it explains nearly all the variance, while the other models show lower values (0.679788 and 0.581184). The optimized model also has much lower MSE, MAE, and RMSE, indicating far more accurate predictions. This demonstrates that optimization significantly improves the model's performance.

___

### Ethical considerations:
* In this project, we used only publicly available, anonymized data to ensure privacy. We acknowledged dataset limitations and biases, such as missing release dates and revenue data, which may impact prediction accuracy. We mitigated bias by focusing on diverse variables and clearly communicated our analysis limitations. Our aim was to provide actionable insights to producers responsibly, supporting data-driven decisions while respecting creative integrity.
* Could this analysis encourage studios to greenlight only projects predicted to be blockbusters, potentially sidelining smaller, more diverse films? While we can't know for certain, this is an important ethical consideration worth discussing.

___

### Data Limitations and Recommendations:
* Gross revenue, budget, and profit figures are not adjusted for inflation.
* The dataset lacks release dates, hindering analysis of seasonality effects or competition when other major films are released close by.
* The data lacks information on Oscar nominations and awards.
* It only captures earnings from the first week in cinemas, missing subsequent revenue.
* The data does not capture critical variables like marketing spend, plot popularity, theater count, and audience demographics (more specific than just content rating).
* Including these influential elements could greatly enhance the accuracy of the prediction mode.
* Given that modern movies can generate up to 500 million dollar profit, continued investment and advancements in data analytics can provide even greater benefits.
___

___
### Other Details: 
* This project is intended for Data Analysts and Machine Learning professionals. Given the 10-minute presentation limit, we kept our analysis concise, focusing on forecasting gross revenue using the available data.

___

### Data Source:
[Kaggle](https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset)

___

### Repository Organization
* **Main_Code** contains all the code for data cleaning, exploration, machine learning models, and related visualization.
* **Notebooks** folder includes separate files with codes to clean and explore the data, and to create machine learning  models.
* **Outcome_Files_DFs** folder has intermediate files like 'cleaned_data.csv'
* **Proposal** folder contains our final proposal in PDF format. However, after closely analyzing our data, we chose a Random Forest model instead of a Neural Network.
* **Visualizations** folder contains plots and graphs.
* **Resources** folder includes our data source called "movie_metadata.csv"
