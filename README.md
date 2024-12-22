# Forecasting Movie Revenue with Machine Learning: A Data-Driven Approach
Explore the full code implementation on [Google Colab](https://colab.research.google.com/drive/1I7Sws_34FHaYJLogppJ_HwRKRuDm-KTl?usp=sharing) *(view-only)*.

## Project Collaborators:
* [Iosif Vard](https://github.com/IosifVard)
* [Jean Vicencio](https://github.com/jpvicencio)
* [Sabrina Linden](https://github.com/LegallyNotBlonde)
___

## Purpose: 
1. **Accurately Predict Movie Revenue:**
Develop a machine learning model to forecast movie revenue based on historical data.
2. **Provide Data-Driven Insights**:
Identify the key factors contributing to high gross revenue and offer actionable insights to movie producers for improving box office performance.
___

## Key Skills Demonstrated:
* **Data Cleaning and Preparation:** Successfully handled real-world data issues, such as missing values and duplicates, ensuring a reliable dataset for analysis (Python, Pandas, NumPy, Google Colab).
* **Exploratory Data Analysis (EDA):** Identified key patterns and correlations in the dataset to inform feature selection and transformations.
* **Machine Learning Expertise:** Applied multiple models, including *Linear Regression* and *Random Forest*, to predict continuous values, showcasing strong understanding of regression techniques and evaluation metrics such as R², MSE, and RMSE.
* **Feature Engineering and Optimization:** Enhanced model performance using advanced techniques like label encoding, feature selection, and hyperparameter tuning.
* **Data Visualization:** Created meaningful visualizations using Matplotlib and Seaborn, including heatmaps, scatter plots, and feature importance charts, to communicate insights effectively.
* **Project Management and Collaboration:** Organized the repository with clear documentation and logical workflows, demonstrating teamwork and version control skills using Git and Google Colab.
___

## Project Overview:

* Movie studios commonly track various metrics to optimize revenue and minimize costs. Key areas include box office performance (e.g., gross revenue and opening weekend sales) and production costs to calculate profit margins. 
* Evaluating marketing effectiveness through advertising ROI, social media engagement, and audience feedback is another key strategy. Timing and competition analysis helps identify optimal release windows, while audience demographics guide content tailoring. 
* Monitoring talent metrics, such as actor popularity, helps predict box office success. Additionally, streaming data, ancillary market performance, and long-term digital distribution trends are analyzed to maximize revenue beyond initial releases. 
* To streamline these critical but time-consuming analyses, we aimed to build a machine learning model to predict movie revenue based on historical records. However, due to limitations in the publicly available data, which are detailed below, the accuracy and scope of our predictions may be affected.

___

## Workflow Overview:

### ETL:
* Data was uploaded as a CSV file from the source.
* Cleaned the data by removing errors, duplicates, or missing values to ensure accuracy and usability. This thorough data cleaning ensures that the models are trained on high-quality data, improving reliability.
* We used Google Colab for its convenience. The code saves 'cleaned_data' and other variables to the Colab environment.
* Given the relatively small size of our data (around 3,000 rows and 30 columns), we did not use PySpark, as it would only increase processing time.

### Data Exploration:
Analyzed the data’s distribution, size, and types to understand its structure and key patterns. This helped identify important features and necessary transformations.

### Machine Learning (predicting continuous values):
* **Model Selection:** Evaluated different machine learning models based on the data type and size.
* Established baseline metrics with a **Linear Regression Model**.
* Given the data size and type, we used a **Random Forest** model with **StandardScaler** and **get_dummies** functions. StandardScaler was used to normalize numerical features, and get_dummies transformed categorical data into machine-readable formats.
* **Data Splitting, Training, and Evaluation**: Split the data into training and testing sets. Trained the model to learn patterns from the training data and evaluated its performance on the testing set to ensure accurate predictions.
* **Feature importance** helps identify key drivers of movie success (e.g., actors, marketing, or release timing), providing insights even when the model shows overfitting or underfitting.
* Assessed model performance to determine which features to develop further using feature engineering.
* **Model Optimization**: Applied **label encoding** and **feature engineering** to enhance the model's accuracy and reliability. Assessed performance on both training and testing data, optimizing to reduce MSE while maintaining a high R².
___

### Visualizations:
1. Data Distribution 
[Link](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/distribution.png)

2. Correlation Heatmap 
[Link](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/original%20heatmap.png)

3. Scatter Plot: Predicted vs. Actual Gross Revenue 
[Linear Regression Plot](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/Linear%20Regression.png)

4. Feature Importance: Numeric and Categorical Features
![Basic Random Forest](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/feature%20importance%20basic%20random%20forest.png)

5. Feature Importance and Heatmap (Optimized Random Forest) 
[Link](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/feature%20importance%20optimized%20random%20forest.png)

6. Train-Test Performance Comparison

![Training vs. Testing Performance Metrics](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/Train-Test%20Performance%20Comparison.png)

7. Accuracy Comparison Across Models: Metrics such as R², MSE, MAE, and RMSE highlight the optimized model's superior performance.

![R-Squared](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/R-squared%20all%20model%20comparison.png)
![MSE](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/MSE%20all%20model%20comparison.png)
[MAE link](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/MAE_comparison.png)
![RMSE](https://github.com/LegallyNotBlonde/Movie_Analysis/blob/main/Visualizations/RMSE_comparison.png)
___

## Results Summary:

This project successfully developed a machine learning model to forecast movie revenue with outstanding accuracy:
* The optimized Random Forest model achieved an R² of 0.999952, far surpassing the performance of Linear Regression (R²: 0.679788) and Basic Random Forest (R²: 0.581184).
* Key factors influencing gross revenue include production budgets, lead actor popularity, and IMDb ratings. 
* The model’s insights provide a strong foundation for guiding movie producers in decision-making related to resource allocation, casting, and marketing strategies.
* Identified data limitations, such as missing release dates and marketing spend, highlight potential areas for model refinement in future iterations.
___

## Conclusion and Recommendations:

The optimized Random Forest model demonstrates that targeted investments can significantly boost movie revenue. Based on our findings, we recommend the following strategies for maximizing gross revenue:
1. **Invest in High Budgets:** Larger budgets typically lead to higher revenue due to improved production quality and extensive marketing efforts.
2. **Cast Popular Lead Actors:** Star power strongly correlates with audience attraction and box office success.
3. **Boost IMDb Ratings:** Enhancing audience engagement and maintaining quality can drive higher ratings, often linked to better revenue.
4. **Optimize Release Timing:** Although not analyzed directly, industry trends suggest strategic timing (e.g., holidays) can enhance box office performance.
By implementing these strategies, producers can make data-driven decisions that enhance profitability while addressing limitations such as data availability for seasonality and marketing insights.
___

## Ethical Considerations:
* We used only publicly available, anonymized data to ensure privacy.
* Dataset limitations and biases, such as missing release dates and Oscar nominations/awards, may impact predictions.
* We aimed to mitigate bias by focusing on diverse variables and transparently communicating our analysis limitations.
___

## Data Limitations and Recommendations:

* Future datasets with inflation-adjusted figures and marketing metrics could enhance prediction accuracy and provide deeper industry insights.
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
