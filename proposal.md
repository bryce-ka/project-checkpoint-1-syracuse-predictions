## Predictive Analysis on US Fertility Trends Using Socio-Economic Factors

### Team

Point of contact: Tian Tian (Github id: MayliaCypher)

Ayush Saseendran (Github id: ayushsaseendran)

Yoon Lee (Github id: oliveingithub)

Francesca Fan (Github id: ffan04)

### Introduction

Amidst the backdrop of significant demographic shifts, our project proposes a predictive analysis using the Real-Time Population Survey (RPS) dataset to understand the declining fertility trends in the U.S. population in detail. The U.S. Census Bureau's latest projections underscore the urgency of addressing these shifts, noting a peak population in 2080 with a gradual decline thereafter (U.S. Census Bureau, 2023). Our analysis aims to provide actionable insights for stakeholders to address the long-term demographic challenges highlighted by these projections.

### Goals

Our goal is to build a machine-learning model to predict the fertility of U.S. adults aged 18-64 using data from the Real Time Population Survey (RPS). Specifically, we want to be able to predict whether an individual is predisposed to have children based on characteristics such as gender, age, race and ethnicity, education, marital status, number of children in the household, and household income.

### Literature Review

Countries around the world, notably Japan and Italy, are currently experiencing challenges posed by low fertility rates. Low fertility rates are worrisome as a super-aged society—defined by the U.N. as a society with at least 20 percent of its population above 65—lacks available workers while the government is put under pressure to find the money to support retirees (Feng, 2023; Moses, 2023).

With a constant decrease in the fertility rate, the United States is approaching similar demographic challenges. The limitation of current demographic prediction practices is that they rely on standard statistical methods. While the decision to have children often depends on personal choice, we aim to capture the complex socio-economic factors influencing the decision to have children.

### Novelty and success factors

We are planning to use the several waves of the RPS dataset. One wave of data has more than 50,000 rows, and by combining more waves of data, we expect to obtain more. This dataset contains information such as gender, age, race and ethnicity, education level, marital status, number of children in the household, and household income. By combining these features, we can gain a more comprehensive understanding of individual fertility and improve the predictive power of the model. In addition, we will use weights and other adjustments to deal with data biases and imbalances to improve the robustness and generalization ability of the model.

### Stakeholders and impacts

It is vitally important to carry out the predictive analysis study on U.S. fertility trends utilizing socioeconomic parameters, as its successful completion could have significant effects on many facets of society. This initiative has broad implications for the general public, which includes you and me as well as future generations, in addition to legislators and economic planners. The following summarizes the effect and the reasons it matters:

#### For Government Officials and Policymakers
Informed Policy Development: The information obtained from the predictive analysis can help direct the creation of laws intended to lessen the effects of population changes. To maintain the sustainability of the workforce, this entails developing family-friendly legislation, immigration reforms, and retirement age adjustments.

Planning for Healthcare and Social Services: Managing resources for education, senior care, and maternal and child health, in particular, requires an understanding of fertility trends.

#### For Businesses and Economic Planners
Forecasting the Labor Market: The size of the labor force is impacted by a diminishing population, which has an impact on competitiveness and economic growth. These findings can be used by companies and economic planners to plan their workforce development, automation, and recruitment of skilled immigration strategies.

Forecasting Market Demand: Consumer demographics are impacted by fertility rates, which in turn affects demand for different goods and services. Businesses can adjust their marketing and product development plans to meet the needs of shifting demographic patterns.

#### For the Awareness and Preparedness of the General Public
The project's findings can encourage personal planning with regard to retirement, finances, and family size by educating the public on the implications of dropping fertility rates.

Socio-Economic Stability: Economic stability and the viability of social security systems are upheld by steady population growth that strikes a balance between the working-age population and dependents.

### Risks

There are a large number of features in this data that we may not need, so if we choose features that do not have an obvious relationship with the target, or if there are covariances, it is likely to affect the performance of the model. Also, the model has many missing values that we need to process before modeling.

In order to solve these problems, we need to clean and filter the data properly first, try to select appropriate and useful features for modeling and compare the results of using different features to choose the best solution. In addition, if the data were collected earlier, we may need to obtain more recent datasets for further analysis.

### Data and Methods

https://www.openicpsr.org/openicpsr/project/158081/version/V4/view

The dataset includes more than 70,000 rows and more than 20 columns of data, with features such as gender, age, race and ethnicity, educational attainment, marital status, number of children in the household, census tract, and household income.

This dataset is from OPENICPSR and includes metadata. These data come from the Real Time Population Survey (RPS), a national labor market survey of U.S. adults ages 18-64. Thus there is some assurance of the reliability of this dataset.

Depending on the nature of the problem and the characteristics of the data, we may use methods such as logistic regression, random forests, support vector machines, neural networks, etc. for modeling and comparing results.

### Weekly work schedule / Coordination of the work
					
| Week              | Details                  |Milestone|
|---|---|---|
| W 6/ CP 1 DUE   | Select topic, dataset, and work on the proposal   |  Identify the required data set. Then prepare the project proposal |
| W 7  | Merge data | Begin merging the selected datasets to create a unified dataset for subsequent analysis |
| W 8 | Clean data	Talk about outliers and missing data together   | Handle outliers and missing data to ensure data quality. Identify needed features and perform data culling |
| SPRING BREAK | Descriptive analysis    | Perform basic statistical descriptions, visualizations and preliminary exploratory analyses of data |
| W 9/ CP 2 DUE | Prelim model runs	| Begin building and training predictive models, and perform initial evaluations of the models |
| W 10-11 | finetune  | The model is tuned, including adjusting model parameters and feature selection |
| W 12 |  Try models  | Try more types of models further and compare their performance |
| W 13 | More models  | Meticulous tuning and optimization of the final model to achieve the best prediction |
| W 14/ CP 3 DUE | Work on deliverable | Complete preparation of project deliverables, including writing final reports, preparing presentations or demonstrations, and ensuring that all tasks are completed as planned |


### Reference

U.S. Census Bureau. (2023, November, 09). U.S. Population projected to begin declining in Second Half of Century [Press release]. https://www.census.gov/newsroom/press-releases/2023/population-projections.html

Moses, C. (2023, February 19). Aging Societies: Asia’s population is shrinking faster than any other continent’s. The New York Times. https://www.nytimes.com/2023/02/19/briefing/asia-aging-popupulation.html#:~:text=Asia%20faces%20a%20problem%3A%20Its,the%20money%20to%20support%20retirees.

Feng, J. (2023, April 30). Japan’s shrinking populations faces point of no return. Newsweek Magazine. https://www.newsweek.com/japan-population-decline-births-deaths-demographics-society-1796496

Bick, Alexander, Blandin, Adam, and Mertens, Karel. Real-Time Population Survey. Ann Arbor, MI: Inter-university Consortium for Political and Social Research [distributor], 2022-11-08. https://doi.org/10.3886/E158081V4

BICK, A. AND A. BLANDIN (2022). Employer Reallocation During the COVID-19 Pandemic: Validation and Application of a Do-It-Yourself CPS. Working Paper 2022-012A, Federal Reserve Bank of St. Louis.

BICK, A., A. BLANDIN, AND K. MERTENS (2022). Work from Home Before and After the
COVID-19 Outbreak. Working Paper 2022-008A, Federal Reserve Bank of St. Louis.

What is it that youre actually predicting and how will it be used. 
Could you use census data or NHANES to see what people binarily have kids and use your model to predict a %chance
Could be interesting to try determine the % chance an individual will have children given their circumstances. 
Or use the model to identify specific factors that would make an individual more liekly to have children. 

