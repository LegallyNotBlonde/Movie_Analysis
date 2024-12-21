# Movie Revenue Forecasting with Machine Learning
[Google Colab Code Link](https://colab.research.google.com/drive/1I7Sws_34FHaYJLogppJ_HwRKRuDm-KTl?usp=sharing) *This link grants view-only access.*

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
<p> 1. [Data Distribution](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/distribution.png)
<p> 2. Correlation Heatmap
img src="https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/optimized%20random%20forest%20heatmap.png" alt="Correlation Heatmap" width="600" 
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

* Gross revenue and budget figures are not adjusted for inflation, so comparisons between movies across years may vary. Adjusting for inflation could improve historical insights.
* Release dates are not included, limiting the ability to analyze seasonality trends or competition. Adding this data would enhance market timing analysis.
* Information on awards for movies, actors, and directors is missing, though such achievements often impact long-term revenue and audience appeal.
* The dataset focuses on first-week revenue, offering a glimpse into initial performance. Including long-term earnings data would provide a more comprehensive view.
* Key variables like marketing spend, theater count, plot popularity, and audience demographics are not included, creating opportunities for improved prediction accuracy with richer data.
* Expanding the dataset with these factors could unlock deeper insights into what drives gross revenue. With some films generating up to $500M in profit, further investment in data analytics holds great potential for the industry.

___

## Other Details:
This project is intended for data analysts and machine learning professionals. Due to the 10-minute presentation limit, we focused on concise analysis to develop the most reliable machine learning model for forecasting gross revenue. Our visualizations center on the model’s development.

___

## Data Source:
[Kaggle](https://www.kaggle.com/datasets/carolzhangdc/imdb-5000-movie-dataset)

___

## Repository Organization:
* **Main_Code_Colab**: Contains the complete code for data cleaning, exploration, modeling, and visualization. **This is the primary code to run.**
* **Notebooks**: Includes intermediate (development) code files for data cleaning, exploration, and optimization of various machine learning models.
* **Outcome_Files_DFs**: Stores intermediate files like 'cleaned_data.csv' and 'model_comparison.csv'.
* **Proposal**: Contains the final proposal PDF. After further analysis, we chose Random Forest over a Neural Network.
* **Visualizations**: Contains plots and graphs illustrating the process of building the most reliable ML model.
* **Resources**: Includes the dataset 'movie_metadata.csv'.
