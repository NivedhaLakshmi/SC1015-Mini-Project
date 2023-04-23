# SC1015-Mini-Project-Airline-Passenger-Satisfaction

Welcome to our customer satisfaction analysis project for an airline company! We are a team of three from Nanyang Technological University - Yaxin, Nivedha, and Chaw Kay. Our project aims to identify the critical factors that influence passenger satisfaction and provide actionable insights for the aviation industry in the post-pandemic era. The dataset for this project is obtained from Kaggle and contains the data sourced from a survey conducted by airlines on the satisfaction level of passengers/customers based on various factors. Our analysis will focus on the provided dataset which includes ratings for each service, to identify the factors that impact passenger satisfaction and provide insights to improve customer service and maintain customer loyalty.


## Background

Passenger satisfaction is a critical factor for the success of any airline. Satisfied passengers are more likely to become loyal customers, provide positive reviews, and recommend the airline to others. On the other hand, dissatisfied passengers may switch to other airlines or share negative feedback, which can impact an airline's reputation and bottom line. Therefore, understanding the factors that influence passenger satisfaction is essential for airlines to improve their services and maintain customer loyalty.

## The Research Question

Our primary objective is to offer recommendations to the airline company regarding the key service categories that have the greatest impact on customer satisfaction, as well as areas that require improvement in order to attract new customers and retain loyal ones. Our analysis aims to identify significant variables, patterns, and trends that could affect customer service in the aviation sector. To achieve this, we will construct a classification model utilizing data from the flight satisfaction survey, with the intention of answering the following research inquiry:

"What patterns, trends, and significant variables can be identified from analyzing the airline passenger satisfaction dataset that impact passenger satisfaction levels? Specifically, what are the critical factors that have a significant impact on passenger satisfaction with airline services to improve customer service and maintain customer loyalty in the aviation industry?"

| Procedure | Related Information|
| ---------------- | ---------------- |
| Data Preparation  | Remove unnecessary column, Handle outliers, Check balance of the dataset, Replace rating '0' with mean, Split the dataset into different generations |
| EDA  | Gender, Customer Type, Pre-boarding and onboarding, Age, Class Type |
| Machine Learning  | LazyPredict, Decision tree, LGBM Classifier, Random forest, Grid-search |


## Data Preparation
Data preparation is a crucial step before conducting exploratory data analysis (EDA) to ensure that the data is clean and relevant. The process involves removing unnecessary columns such as the "ID" column, handling missing values, addressing outliers and checking the balance of the dataset to avoid bias. Upon examining the outliers in the arrival and departure delays, we found it surprising that this variable was not a top predictor for passenger satisfaction levels. So, we decided to look into deeper and analyze whether passengers were still satisfied despite experiencing a delay or if delays had a negative impact on their satisfaction levels.

In addition, we replaced the 0 rating values with the mean rating value to handle the situation where '0' means the rating is not applicable. Lastly, to gain insights into different generations, the dataset is splitted according to different generational groups.

## Visualisation- EDA

In our exploratory data analysis (EDA), we focus on understanding passenger satisfaction levels in different categories such as gender, customer type, pre-boarding and onboarding, age, and travel class type. The purpose of this data visualization is to identify any differences in satisfaction levels across these categories and to better understand what factors impact passenger satisfaction.

By examining these categories, we can gain valuable insights into the factors that influence passenger satisfaction levels and help airlines to improve the overall customer experience for all passengers. Our analysis will include visualizations such as bar charts, scatter plots, and heat maps to provide a clear understanding of the relationships between these categories and passenger satisfaction. Overall, our goal is to provide a comprehensive analysis of passenger satisfaction levels across different categories and provide actionable insights for airlines to improve the overall customer experience.

After analyzing satisfaction ratings across various categories, our findings suggest that gender is not a significant factor in determining satisfaction levels. The airline has a high percentage of returning passengers. However, there is a considerable level of dissatisfaction among them. Baggage handling, check-in, and gate location services were the most dissatisfying, while passengers were highly satisfied with online booking and onboard services during pre-boarding. Among in-flight services, passengers in Business Class were highly satisfied with spacious legroom, and age played a significant role, with the age group of 39-60 having higher expectations and satisfaction levels. Passengers on longer flights or business travel were more inclined towards Business Class, resulting in higher satisfaction levels due to its amenities. Our recommendations to the airline include considering these factors in their strategies to ensure continued satisfaction and loyalty among customers.


## Machine Learning
### DecisionTree
Despite the fact that LazyPredict has shown that DecisionTreeClassifier has lower accuracy compared to other models across all age groups, we have opted to utilize it as our initial prediction model. This decision was made because DecisionTreeClassifier is a relatively straightforward and easy-to-grasp concept that we learned in our labs, and it is also highly interpretable. In fact, decision trees can be graphically represented, making it easier to visualize and understand the decision-making process of the model.

![decisionTree](https://user-images.githubusercontent.com/51477400/233843063-9aec1632-0c50-4e04-8882-26a1b1616bce.png)

### Accuracy Comparison
![accuracyComparison](https://user-images.githubusercontent.com/51477400/233843122-ec76c689-0fc3-463d-a8d9-e2627a863d87.png)

### Feature Importance
The analysis of different machine learning models revealed that online boarding and WiFi services significantly influence flight satisfaction. For the decision tree model, online boarding and WiFi were identified as the most important variables, while for the LGBMclassifier model, flight distance and WiFi were the significant factors. Similarly, the Random Forest model also identified online boarding and WiFi as the most important features.

The analysis also revealed that passengers aged between 26 to 41 years consider online boarding and WiFi services as crucial factors for their flight satisfaction. However, the importance of other features varied across different age groups. For example, passengers aged between 42-57 years consider class, leg room, WiFi, online boarding, and flight distance important. In contrast, passengers aged between 68-76 years consider WiFi, leg room, and flight distance as crucial factors.

Based on the analysis, the following features were identified as important for each age group:

| Generation | Key Services |
| -------- | -------- |
| Gen Z | Online Boarding, In-flight Wifi Service (Flight Distance) |
| Millennials | Online Boarding, In-flight Wifi Service, Arrival Delay (Flight Distance) |
| Gen X| Online Boarding, In-flight Wifi Service,(Flight Distance) |
| Boomer I | Class, Leg Room Service, In-flight Wifi Service, Online Boarding (Flight Distance) |
| Boomer II | Type of Travel, In-flight Wifi Service, Online Boarding (Flight Distance) |
| Post War | In-flight Wifi Service, Leg Room Service (Flight Distance) |
| WWII | Leg Room Service, In-flight Wifi Service (Flight Distance) |

While flight distance appears to have a significant impact on passenger satisfaction levels, it is important to note that this is not a feature that the airline can improve upon, as it is not a service that is directly provided by the airline company.



## Conclusion
In conclusion, airlines can improve flight satisfaction by focusing on providing efficient online boarding and WiFi services as this is a crucial factor for all generations.. Additionally, airlines should also consider other factors such as flight distance, class, leg room, and arrival delay to enhance the flight experience for different age groups.


Through this project, our group has gained valuable knowledge and skills. In the EDA phase, we learned how to use the FacetGrid function for efficient visualization and comparison of multiple subsets of data within a single plot. In the ML phase, we applied the Chi square and wrapper methods for feature importance and utilized the Lgbmclassifier to produce more accurate machine learning outcomes. Furthermore, we conducted research and implemented the Lazypredict tool to calculate accuracy before selecting the best model for each group, resulting in improved predictive performance.

## Recommendations
To enhance passenger satisfaction levels, it is recommended that the airline improve their Wi-Fi service and online boarding, as this is a crucial factor for all generations.

Additionally, airlines should also consider other factors such as class, leg room, and arrival delay to enhance the flight experience for different age groups.  Regarding the class of service, our analysis indicates that airlines should prioritize improving their services for economy class passengers. This is supported by our findings in the EDA part, which revealed that aspects such as leg room service and type of travel are closely related to the class of service. Specifically, we found that a majority of business class passengers rated the leg room service highly, and that individuals traveling for business purposes tend to opt for the business class.

## Acknowledgements
We want to thank our professor, Smitha K G and our lab teaching assistant Prof Manoj Shakya for continuous support and help throughout the project.

## References
Beresford Research. (n.d.). Age Range by Generation. Available at: https://www.beresfordresearch.com/age-range-by-generation/ (Accessed: 23-Apr-2023).

Izen AI. (2021). Feature Selection – Filter Method, Wrapper Method, and Embedded Method. Available at: https://www.izen.ai/blog-posts/feature-selection-filter-method-wrapper-method-and-embedded-method/ (Accessed: 23-Apr-2023).

Kharwal, A. (2019, March 12). Chi-Square Test for Feature Selection in Machine Learning. Towards Data Science. https://towardsdatascience.com/chi-square-test-for-feature-selection-in-machine-learning-206b1f0b8223

Mysarahmad Bhat (2021). Airline Passenger Satisfaction Dataset. Kaggle. Available at: https://www.kaggle.com/datasets/mysarahmadbhat/airline-passenger-satisfaction (Accessed: 23-Apr-2023).

Nugroho, A. (n.d.). Airline Passenger Satisfaction. GitHub. Available at: https://github.com/arienugroho050396/Airline-Passenger-Satisfaction/blob/main/Airline%20Passenger%20Satisfaction.ipynb (Accessed: 23-Apr-2023).

Shanmuganathan, Y. (n.d.). Airline Passenger Satisfaction. GitHub. Available at: https://github.com/yogeshwaran-shanmuganathan/Airline-Passenger-Satisfaction/blob/master/Code/airline_passenger_satisfaction.ipynb (Accessed: 23-Apr-2023).

Shukla, A. (2020, July 20). 10 Techniques to Deal with Class Imbalance in Machine Learning. Analytics Vidhya. Available at: https://www.analyticsvidhya.com/blog/2020/07/10-techniques-to-deal-with-class-imbalance-in-machine-learning/ (Accessed: 23-Apr-2023).




