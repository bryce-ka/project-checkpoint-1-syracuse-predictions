**TITLE: MADE EASY**
## Predicting the helpfulness of a review. 


# AML Project Analysis

## Team
List of team members, including full names and GitHub IDs

- Likhith Kolli (likki152) - Point of Contact
- Goutham sri Vishwesh Bikkumalla (GouthamBikkumalla)
- Mani Kiran Chatrathi (ManiKran)
- Sahil gauba (sahilgauba9)
- Harsh Bhanushali (Harshatul3199)
- Xiaoying Feng (Awing91333)

## Introduction
Business Question 1: 
•	Objective: Predicting the helpfulness of a review
•	What’s new: Including a measurement between the review text and the image similarity with image processing and NLP.
•	Who cares: food critics, the Yelp elite program which offers benefits to elusive events, however, the member is selected based on the contribution they have for the Yelp community. 

Business Question 2:
•	Objective: Predicting the rating of a restaurant
•	What’s new: Evaluating the impact of menu design on customer ordering patterns by incorporating a measure of the availability of combo options and specials. This analysis goes beyond the menu layout to assess how the menu composition, particularly the presence of well-designed combos and specials, influences customer satisfaction and, consequently, restaurant ratings.
•	Who cares: Restaurant owners and managers interested in optimizing menu offerings to enhance customer experience, drive sales, and improve ratings.

Potential Business Question 3:
•	Objective: Building a restaurant recommendation system (Welcome comments)

## Literature Review

Traditionally, scholars and professionals have heavily concentrated on natural language processing for insights derived from written text (Fedewa and Holder, 2022). Nevertheless, photos serve as crucial tools for consumers to express their experiences. Presently, a majority of consumers assert their reliance on visual content when making decisions and express a preference for user-generated visual content over professionally crafted material (Power Reviews, 2021). Ceylan et al. (2024) employed the Google Cloud Platform Vision API and utilized the "Detect Labels" function to scrutinize review images and employed Doc2Vec for extracting labels from the review text, subsequently measuring the similarity between these labels. The findings suggested that the inclusion of photos enhances the helpfulness of a review, and a higher alignment between photos and text further amplifies review helpfulness. However, it is important to note that this study only examined the similarity of object labels, neglecting other concealed aspects such as restaurant ambiance and overall vibe. There exists an opportunity to capture a more comprehensive narrative by extracting additional features beyond object labels.

## Data

Link: https://www.yelp.com/dataset

The Yelp dataset is a subset of their businesses, reviews, and user data for use in connection with academic research. The dataset includes 11 metropolitan areas centered on Montreal, Calgary, Toronto, Pittsburgh, Charlotte, Urbana-Champaign, Phoenix, Las Vegas, Madison, and Cleveland. There are in total 6,990,280 reviews, 150,346 businesses, 200,100 pictures, 908,915 tips by 1,987,897 users. Over 1.2 million business attributes are included in the dataset like hours, parking availability, and ambiance. Aggregated check-ins over time for each of the 131,930 businesses are also available.

This dataset is reliable because it comes from the Yelp Open Dataset Challenge, which has been serving as an academic purpose for teaching NLP, Image Processing, or as sample production data for developing mobile apps. There are multiple sub-datasets, and we can merge them with the unique business ID:

- Business data including location data, attributes, and categories.
- Review text data including the user_id that wrote the review and the business_id the review is written for.
- User data including user's friend mapping and all the metadata associated with the user.
- Check-in data indicating whether the business is still running or not.
- Tips data, which is written by a user on a business, and tips are shorter than reviews and tend to convey quick suggestions.
- Photo data including the caption and classification (one of "food," "drink," "menu," "inside," or "outside").

## Modeling Methods

The modeling methods will depend on the specific objectives. Potential approaches include:

- **Machine Learning Models:** Utilizing machine learning algorithms for sentiment analysis, recommendation systems, or predicting business success based on certain attributes.
- **NLP Techniques:** Applying natural language processing techniques for text analysis, topic modeling, or extracting valuable information from reviews.
- **Image Processing:** Extracting the texture features including identification of patterns, textures, and surface characteristics within the image.
- **Data Visualization:** Using visualization tools to present insights in a comprehensible manner for stakeholders.
- **Statistical Analysis:** Employing statistical methods to identify patterns or trends within the dataset.



Project Plan
| *Period* | *Activity* | *Milestone* |
| --- | --- | --- |
| Week1 | Detailed Stakeholder Analysis & Objective Specification | Complete analysis of stakeholders and define project objectives |
| Week2 | Data Identification | Secure access to Yelp Dataset and verify its suitability |
| Week3 | Data Preparation | Clean and preprocess the data for analysis |
| Week4 | Exploratory Data Analysis (EDA) | Gain insights into the dataset and identify potential features for modeling |
| Week5 | Model Development - NLP Techniques | Develop NLP models for sentiment analysis and topic modeling |
| Week6 | Model Development - Machine Learning | Build and train ML models for recommendation systems and predicting business success |
| Week7 | Model Evaluation and Refinement | Evaluate model performance and refine models based on feedback |
| Week8 | Final Review & Stakeholder Presentation | Finalize project and present findings to stakeholders |






## **Risks**:


1. **Data Quality and Completeness**: The Yelp Dataset, while extensive, might have inconsistencies, missing values, or outdated information that could affect the analysis. The risk here is drawing inaccurate conclusions due to poor data quality.

2. **Computational Resources**: The scale of the data and the complexity of the models (especially if deep learning techniques are used) may require significant computational resources, posing a risk if there are limitations in access to such resources.

3. **Stakeholder Alignment**: Ensuring that the project's outcomes align with the needs and expectations of the diverse set of stakeholders identified (academic researchers, data scientists, business owners, app developers) may be challenging.

4. **Changing Business Environments**: The dynamic nature of businesses and consumer behavior, especially in response to external factors like economic shifts or pandemics, could affect the relevancy and applicability of the findings.



*Stakeholder Analysis - Who Cares?*

Potential stakeholders for the Yelp Dataset include:

- *Academic Researchers:* They may be interested in using the dataset for various research purposes, such as studying user behavior, sentiment analysis in reviews, or analyzing the impact of reviews on businesses.
- *Data Scientists and Analysts:* Professionals in these fields may leverage the dataset for developing recommendation systems, sentiment analysis models, or other data-driven insights.
- *Business Owners and Managers:* Individuals who run or manage businesses listed on Yelp could be interested in understanding customer reviews and feedback to improve their services.
- *App Developers:* Those learning to develop mobile apps could use the Yelp Dataset as sample production data to create applications related to restaurant recommendations, review analysis, or other Yelp-related services.

## References 
- Ceylan, G., Diehl, K., & Proserpio, D. (2024). Words Meet Photos: When and Why Photos Increase Review Helpfulness. Journal of Marketing Research, 61(1), 5–26. https://doi.org/10.1177/00222437231169711
- Fedewa, Dave and Chauncey Holder (2022), “Why Business Must Heed Customer Reviews,” McKinsey (February 22), https://www. mckinsey.com/capabilities/operations/our-insights/why-businessmust-heed-customer-reviews.
- Power Reviews (2021), “How User-Generated Visual Content Became Fundamental to Ecommerce,” (accessed September 30, 2022), https://www.powerreviews.com/insights/how-visual-ugc-becamefundamental/.
- 

  What is your overall outcome and how are you going to evaluate your model. I really like the idea but im struggling to understand how you will evaluate your approach.

How is your project affecting the stakeholders of the yelp dataset?

maybe you can use the difference between the specific review and average review as a measurement of helpfulness. This could also be done over time periods to show whether restaraunts are getting better or worse?


