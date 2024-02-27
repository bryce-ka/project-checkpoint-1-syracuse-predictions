
### Title : Syracuse Weather and Road Predictions

### Team Members:

Catie Shelton (cshelto1)
Ed Cogan (CopoM5)
Marina Mitiaeva (marinamitiaeva)
Abhi Chakraborty (abchakrasyr)
Jackson Bayuk (JackBCuse)

### Goal: The goal of this machine learning project is to predict the future road conditions of Syracuse, NY, based on weather and road conditions datasets.

### Introduction

In this project, we aim to predict road conditions using data collected from various sources such as weather reports, traffic sensors, and historical accident records. Our objective is to develop a model that can accurately forecast the state of the roads, such as whether they are wet, icy, or clear, to enhance road safety and inform travelers and authorities about potential hazards.

What sets our approach apart is the integration of diverse data sources and the application of advanced machine learning techniques to capture the complex relationships between weather conditions, traffic patterns, and road states. By leveraging the latest algorithms and computational methods, we anticipate improved accuracy and reliability in our predictions.

The significance of this work cannot be overstated. If successful, it will revolutionize road safety by providing timely and accurate information about road conditions, thereby reducing the likelihood of accidents and traffic jams. It will also assist transportation authorities in better managing road maintenance and emergency responses, ultimately saving lives and resources.

### Literature Review

The current approach to predicting road conditions primarily relies on historical weather data, traffic patterns, and sensor data from roadways. Traditional methods include using statistical models and rule-based systems to forecast road conditions based on temperature, precipitation, and traffic flow. However, these methods often fall short in accurately predicting complex scenarios, such as rapidly changing weather conditions or unforeseen traffic incidents.

Recent advancements in machine learning and data analytics have opened up new avenues for road condition prediction. Studies have explored the use of deep learning algorithms, such as Convolutional Neural Networks (CNNs) and Recurrent Neural Networks (RNNs), to analyze large datasets and capture the intricate relationships between various factors influencing road conditions. For example, Zhang et al. (2019) utilized a CNN-based model to predict road surface conditions by analyzing weather data and road surface images[^1]. Similarly, Li et al. (2020) proposed an RNN-based approach for real-time road condition forecasting using data from weather stations and traffic sensors[^2].

Despite these advancements, challenges remain in the integration of diverse data sources, handling of high-dimensional data, and the real-time processing of information. Moreover, the generalization of models across different geographic regions and varying weather conditions is an ongoing area of research.

[^1]: Zhang, Y., et al. (2019). "Road Surface Condition Prediction Using Convolutional Neural Networks." *IEEE Access*, 7, 174929-174938.
[^2]: Li, X., et al. (2020). "Real-time Road Condition Forecasting Using Recurrent Neural Networks." *Transportation Research Part C: Emerging Technologies*, 111, 83-98.

### Stakeholders:

Key Stakeholder: The mayor of Syracuse and his supporting city officials responsible for infrastructure maintenance.

Low Interest / High Power Stakeholders: Syracuse University and local citizens, as their tax dollars fund the government's work but they aren't closely involved in daily decisions.

Low Power / High Interest Stakeholder: The Centro Bus Company, as the quality of the roads they operate on affects the health of their assets (buses).


#### Data

The weather dataset was curated from NASA’s website, which focuses on predicting worldwide energy resources through the POWER Data Access Viewer. This tool, available on the website, provides “meteorological and solar data with geospatial capabilities and is designed to aid in the assessment and planning of renewable energy systems”. It outputs neat and organized CSV files (https://power.larc.nasa.gov/data-access-viewer/).

The data was specifically extracted for Syracuse University's location, identified by latitude 43.0345 and longitude -76.1372. The dataset covers the period from November 1, 1983, to November 1, 2023, spanning 40 years and includes 189,943 datapoints (14611r x 13c) of weather data, including Temperature, Dewpoint, Wet Bulb, Humidity, and Precipitation.

In addition to the weather dataset, two other datasets will be used: "Road Ratings" and "Potholes," obtained from the City of Syracuse's Open Data Portal (https://data.syr.gov/).

Road Ratings: (3675r x 13c)

This dataset includes information from The City of Syracuse's assessment of its roads on a biennial basis, using a rating scale from 1 to 10, where 10 indicates the best condition and 1 the worst. This data will be used in conjunction with the weather data to investigate how weather affects the area's roadways.

Potholes: (58314r x 21c)

This dataset contains information about the city’s potholes. Residents can notify the City of Syracuse's Department of Public Works about specific pothole locations within the city. Potholes are areas of road surface that have deteriorated, often caused by water beneath the asphalt and traffic passing over them. In Syracuse, potholes are common, particularly after winter, when snow plows and fluctuating temperatures contribute to their formation. Like the Road Ratings dataset, this dataset will also be used in conjunction with the weather dataset to understand how weather impacts road conditions in different areas.

### Methods

To predict road conditions, we will approach the dataset with a combination of preprocessing, feature engineering, and modeling techniques. Our primary goal is to develop a model that can accurately classify road conditions, which can be critical for traffic management, safety, and maintenance planning. The following steps outline our approach:

## Data Preprocessing:

Handling Missing Values: We will assess the dataset for any missing values and employ appropriate imputation techniques, such as mean or median imputation for numerical features and mode imputation or the use of a placeholder value for categorical features.
Outlier Detection and Treatment: We will identify and treat outliers in the dataset, as they can skew the model's performance. Techniques such as the Interquartile Range (IQR) method or Z-score can be used for outlier detection.
Data Normalization/Standardization: We will scale the numerical features to ensure that no particular feature dominates the model due to its scale. Standardization (z-score normalization) or Min-Max normalization can be used depending on the distribution of the data.


## Feature Engineering:

Feature Selection: We will employ techniques such as correlation analysis, recursive feature elimination (RFE), or feature importance from tree-based models to select relevant features that contribute most to the prediction of road conditions.

Feature Construction: We may create new features from existing ones, such as interaction terms or polynomial features, to capture complex relationships in the data.


## Modeling Techniques:

Baseline Model: We will start with a simple model, such as Logistic Regression or Decision Trees, to establish a baseline performance.
Advanced Models: We will then explore more sophisticated models like Random Forests, Gradient Boosting Machines (GBM), Support Vector Machines (SVM), and Neural Networks. These models can capture non-linear relationships and interactions between features more effectively.
Model Tuning: We will use techniques like Grid Search or Random Search to fine-tune the hyperparameters of the models for optimal performance.
Model Evaluation:

Cross-Validation: We will use k-fold cross-validation to evaluate the models' performance and ensure that they generalize well to unseen data.
Evaluation Metrics: Consistent with stakeholder needs, we will use metrics such as Accuracy, Precision, Recall, F1-score, and the Area Under the Receiver Operating Characteristic Curve (AUC-ROC) to assess the models. For imbalanced datasets, metrics like F1-score and AUC-ROC are particularly useful.
Model Comparison: We will compare the performance of different models based on the evaluation metrics and select the best-performing model for deployment.


## Model Interpretability:

We will use techniques like SHAP (SHapley Additive exPlanations) or feature importance scores to interpret the model's predictions and understand the impact of different features on road condition predictions.
By following this approach, we aim to develop a robust and interpretable model that can accurately predict road conditions, thereby aiding in effective road management and safety measures.


### Project Plan

| Week              | Details                                   | Milestone                                  |
|-------------------|-------------------------------------------|--------------------------------------------|
| Feb 20 - Feb 26   | Identify Data Sets, Identify Problem      | Present Proposal, Datasets Identified      |
| Feb 27 - March 4  | Stakeholder Analysis, EDA, Initial Visualization | Completed Stakeholder Analysis and data exploration |
| March 5 - March 11 | Preprocessing of Data                     | Data is preprocessed and cleaned           |
| March 12 - March 18 | Initial description                       | Data Description                           |
| March 19 - March 25 | Decide on classifiers                     | Preliminary Descriptive Analysis           |
| March 26 - April 1 | Preliminary model runs                    | Project Checkpoint 2                       |
| April 2 - April 8  | Hyperparameter Tuning                     | Model Progress                             |
| April 9 - April 15 | Start on Project Report                   | 1st Draft of Checkpoint 3                  |
| April 16 - April 22 | Final model tuning and report work        | Project Checkpoint 3, 1st draft of report  |
| April 23 - May 7   | Final report work                         | Final Report Submitted                     |



### Risks

The primary risk in this project is the quality and reliability of the data sources. Inaccuracies or missing data in the weather dataset from NASA or the road-related datasets from the City of Syracuse could significantly impact the effectiveness of the machine learning algorithm. Additionally, changes in data collection methods or environmental factors over the 40-year span of the weather data could introduce biases that may affect the results.

The complexity of correlating weather variables with road conditions using machine learning techniques also poses a challenge. Machine learning models can be sensitive to the quality and structure of the input data, and any discrepancies or anomalies in the data could lead to inaccurate predictions.

To mitigate these risks, careful evaluation and preprocessing of the data are essential. This includes identifying and addressing any missing or inaccurate data points, as well as considering potential extraneous variables that could influence the results. Additionally, validating the model through various techniques such as cross-validation or holdout validation can help ensure the reliability and accuracy of the predictions.

what exactly is it that youre predicting, is it like tv weather where you get daily updates or is this long term we think x will happen. 
Also what is the outcome youre predicting there seems to be several different outcomes - weather related road conditions, road quality, where these are occuring 
could focusing on the rate of decay be a useful outcome
can topographical information potentially come into play as a feature 



