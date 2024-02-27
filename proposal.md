# Syracuse Weather and Road Predictions
 - Catie Shelton (cshelto1) - GitHub repository owner
 - Ed Cogan (CopoM5)
 - Marina
 - Abhi Chakraborty
 - Jackson Bayuk

The goal of this machine learning project is to predict the future road conditions of Syracuse, NY based on the weather and road conditions datasets. This project is novel because it takes three previously unrelated sets of data to predict future infrastructure impacts of Syracuse. If this project is successful, it can help the local government of Syracuse, NY to plan its resources better based on the weather in previous years resulting in better infrastructure. These data sets are owned by the local Syracuse government and are updated either daily or monthly.
The key player stakeholder of this project is the mayor of Syracuse and his supporting city officials who are responsible for the infrastructure maintenance in Syracuse. Syracuse University and local citizens are low interest / high power stakeholders because they aren’t closely involved in daily government decisions, but their tax dollars pay for that work. The Centro Bus Company is a low power / high interest stakeholder as the health of their assets (buses) are dependent on the quality of the roads they operate on [^1].

Today, it is common for meteorologists to use systems such as Road Weather Information Systems (RWIS) in order to get specific, real time data on how roads are being affected by real time weather trends. A RWIS consists of environmental sensor stations that measure atmospheric, pavement, and/or water level conditions. The current road safety information when it comes to weather is strongly based on these three factors. General road weather observations are obtained from national surveillance systems to produce weather watches and warnings for public safety. The National Weather Service (NWS) deploys sensor stations, balloon-borne sensors, Doppler radars, and other technologies to generate national, regional, and county forecasts. As technological advancements are becoming more prevalent the idea of using sensors on snow plows has also become a useful tool of gaging road conditions. Some limits of the current practice is that most of the data on road conditions are collected in real time, however it is important for predictive instances to accumulate data as well as during the precipitation in order to accurately predict how the road will be affected by the incoming weather. 

The weather dataset was curated from NASA’s website, which focuses on predicting worldwide energy resources through the POWER Data Access Viewer. This tool, available on the website, provides “meteorological and solar data with geospatial capabilities and is designed to aid in the assessment and planning of renewable energy systems”. It outputs neat and organized CSV files [^2].

The data was specifically extracted for Syracuse University's location, identified by latitude 43.0345 and longitude -76.1372. The dataset covers the period from November 1, 1983, to November 1, 2023, spanning 40 years and includes 189,943 datapoints (14611r x 13c) of weather data, including Temperature, Dewpoint, Wet Bulb, Humidity, and Precipitation.

In addition to the weather dataset, two other datasets will be used: "Road Ratings" and "Potholes," obtained from the City of Syracuse's Open Data Portal [^3].

Road Ratings: (3675r x 13c)

This dataset includes information from The City of Syracuse's assessment of its roads on a biennial basis, using a rating scale from 1 to 10, where 10 indicates the best condition and 1 the worst. This data will be used in conjunction with the weather data to investigate how weather affects the area's roadways.

Potholes: (58314r x 21c)

This dataset contains information about the city’s potholes. Residents can notify the City of Syracuse's Department of Public Works about specific pothole locations within the city. Potholes are areas of road surface that have deteriorated, often caused by water beneath the asphalt and traffic passing over them. In Syracuse, potholes are common, particularly after winter, when snow plows and fluctuating temperatures contribute to their formation. Like the Road Ratings dataset, this dataset will also be used in conjunction with the weather dataset to understand how weather impacts road conditions in different areas.

To analyze how weather conditions impact roadways and contribute to deterioration and pothole formation, we plan to develop a comprehensive weather model that incorporates various meteorological factors. This model would integrate historical weather data, including temperature, precipitation, humidity, and freeze-thaw cycles, collected from a reliable source (NASA's POWER Data Access Viewer). Utilizing advanced statistical and machine learning techniques, we can then correlate these weather variables with observed road conditions, road ratings, and pothole occurrences over time. By identifying patterns and relationships between weather patterns and roadway deterioration, the model can provide valuable insights into the specific weather conditions that contribute to road damage and pothole formation. This information can help local authorities prioritize road maintenance efforts, implement preventive measures, and improve overall roadway resilience in the face of changing weather patterns.

| Week | Details | Milestone |
| --- | --- | --- |
| Feb 20 - Feb 26 | Identify Data Sets, Identify Problem | Present Proposal, Datasets Identified|
| Feb 27 - March 4 |Stakeholder Analysis, EDA, Initial Visualization| Completed Stakeholder Analysis and data exploration|
| March 5 - March 11 |Preprocessing of Data |Data is preprocessed and cleaned |
| March 12 - March 18 | Initial description | Data Description |
| March 19 - March 25 | Decide on classifiers | Preliminary Descriptive Analysis|
| March 26 - April 1 |Preliminary model runs | Project Checkpoint 2 |
| April 2 - April 8 | Hyperparameter Tuning | Model Progress|
| April 9 - April 15 | Start on Project Report |1st Draft of Checkpoint 3 |
| April 16 - April 22 | Final model tuning and report work | Project Checkpoint 3, 1st draft of report|
| April 23 - May 7 | Final report work | Final Report Submitted|


This proposal outlines a machine learning project aimed at analyzing the relationship between meteorological factors and road conditions, with a focus on predicting road deterioration and pothole formation in Syracuse, NY. 
One potential risk for this project is the quality and reliability of the data sources. While the weather dataset from NASA's POWER Data Access Viewer and the road-related datasets from the City of Syracuse's Open Data Portal provide valuable information, there may be inconsistencies, inaccuracies, or missing data that could impact the effectiveness of the machine learning algorithm. 

Additionally, since the weather data spans a period of 40 years, there may be changes in data collection methods or environmental factors over time that could introduce biases or uncertainties into the analysis. Furthermore, the complexity of correlating weather variables with road conditions and pothole occurrences using machine learning techniques may pose challenges in model interpretation and generalizability. 

It's essential to carefully evaluate and preprocess the data, consider potential extraneous variables, and validate the model to mitigate these risks and ensure the reliability of the results.

[^1]: http://www.ongov.net/dot/highway-paving.html
[^2]: https://power.larc.nasa.gov/data-access-viewer/
[^3]: https://data.syr.gov/
