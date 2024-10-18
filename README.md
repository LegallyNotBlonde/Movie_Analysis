# Movie Revenue Forecasting with Machine Learning

## Project Collaborators:
* [Iosif Vard](https://github.com/IosifVard)
* [Jean Vicencio](https://github.com/jpvicencio)
* [Sabrina Linden](https://github.com/LegallyNotBlonde)


## Purpose: 
1. **Forecasting Movie Revenue Based on Historical Performance**
2. **Provide recommendations to movie producers on maximizing gross revenue**:
identify key factors for successful movies, such as which features contribute most to high gross revenue.

___

## Project Overview:

<p>Movie studios commonly track various metrics to optimize revenue and minimize costs. Key areas include box office performance (e.g., gross revenue and opening weekend sales) and production costs to calculate profit margins. 
<p>Evaluating marketing effectiveness through advertising ROI, social media engagement, and audience feedback is another key strategy. Timing and competition analysis helps identify optimal release windows, while audience demographics guide content tailoring. <p>Monitoring talent metrics, such as actor popularity, helps predict box office success. Additionally, streaming data, ancillary market performance, and long-term digital distribution trends are analyzed to maximize revenue beyond initial releases. 
<p>To streamline these critical but time-consuming analyses, we aimed to build a machine learning model to predict movie revenue based on historical records. However, due to limitations in the publicly available data, which are detailed below, the accuracy and scope of our predictions may be affected.

<p> To streamline these critical but potentially time-consuming analyses, we aimed to build a machine learning model to predict movie revenue based on historical records. However, due to limitations in our publicly available data, which are detailed below, the accuracy and scope of our predictions may be affected.

___

## Workflow Overview:

### ETL:
* Data was uploaded as a CSV file from the source.
* Cleaned the data by removing errors, duplicates, or missing values to ensure accuracy and usability. Clean data is essential for reliable results.
* We used Google Colab for its convenience. The code saves 'cleaned_data' and other variables to the Colab environment.
* Given the relatively small size of our data (around 3,000 rows and 30 columns), we did not use PySpark, as it would only increase processing time.

### Data Exploration:
Analyzed the data’s distribution, size, and types to understand its structure and key patterns. This helped identify important features and necessary transformations.

### Machine Learning (predicting continuous values):
* **Model Selection:** Evaluated different machine learning models based on the data type and size.
* Established baseline metrics with a **Linear Regression Model**.
* Given the data size and type, we used a **Random Forest** model with **StandardScaler** and **get_dummies** functions.
* **Data Splitting, Training, and Evaluation**: Split the data into training and testing sets. Trained the model to learn patterns from the training data and evaluated its performance on the testing set to ensure accurate predictions.
* **Feature importance** helps identify key drivers of movie success (e.g., actors, marketing, or release timing), providing insights even when the model shows overfitting or underfitting.
* Assessed model performance to determine which features to develop further using feature engineering.
* **Model Optimization**: Applied **label encoding** and **feature engineering** to enhance the model's accuracy and reliability. Assessed performance on both training and testing data, optimizing to reduce MSE while maintaining a high R².

### Visualizations:
<p> 1. Data Distribution
<p> 2. Correlation Heatmap
<p> 3. Scatter Plot: Predicted vs. Actual Gross Revenue (Linear Regression)
<p> 4. Feature Importance: Numeric and Categorical Features (Basic Random Forest)
<p> 5. Feature Importance and Heatmap (Optimized Random Forest)
<p> 6. Train-Test Performance Comparison
<p> 7. Accuracy Comparison: Linear Regression vs. Basic vs. Optimized Random Forest (R², MSE, MAE, RMSE)

## Conclusion:

The optimized Random Forest model outperforms both the Multiple Linear Regression and Basic Random Forest models. With an R² of 0.999952, it explains nearly all variance, while the other models score 0.679788 and 0.581184, respectively. The optimized model also achieves lower MSE, MAE, and RMSE, showing that optimization significantly improves performance.
___

## Ethical Considerations:
* We used only publicly available, anonymized data to ensure privacy.
* Dataset limitations and biases, such as missing release dates and Oscar nominations/awards, may impact predictions.
* We aimed to mitigate bias by focusing on diverse variables and transparently communicating our analysis limitations.
* An important ethical question: Could such predictions encourage studios to favor blockbuster films, sidelining smaller, more diverse projects?

___

## Data Limitations and Recommendations:
* Gross revenue and budget figures are not adjusted for inflation, making it difficult to compare movies released in different years.
* Absence of release dates prevents analysis of seasonality trends and competition from other films during the same period.
* Lacking data on awards for movies, actors, and directors, which could influence a film’s revenue and long-term success.
* The dataset only captures first-week revenue, omitting crucial insights into long-term earnings.
* Key factors like marketing spend, plot popularity, theater count, and audience demographics are not included, which limits prediction accuracy.
* Incorporating these variables would significantly enhance the model’s predictive power. With individual films generating up to $500M in profit, further investment in data analytics could unlock valuable insights for the movie industry.

___

## Other Details:
This project is intended for data analysts and machine learning professionals. Due to the 10-minute presentation limit, we focused on concise analysis to develop the most reliable machine learning model for forecasting gross revenue. Our visualizations center on the model’s development.

___

## Data Source:
[Kaggle](https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset)

___

## Repository Organization:
* **Main_Code_Colab**: Contains all code for data cleaning, exploration, modeling, and visualization.
* **Notebooks**: Includes files for cleaning, exploration, and evaluating machine learning models.
* **Outcome_Files_DFs**: Stores intermediate files like 'cleaned_data.csv' and 'model_comparison.csv'.
* **Proposal**: Contains the final proposal PDF. After further analysis, we chose Random Forest over a Neural Network.
* **Visualizations**: Contains plots and graphs used in the project.
* **Resources**: Includes the dataset 'movie_metadata.csv'.
