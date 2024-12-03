# Airline Customer Satisfaction Analysis and Prediction

## Project Overview  
This project explores customer satisfaction in the airline industry using a dataset of over 129,000 records sourced from Kaggle. The analysis was performed using **R** with the inclusion of a **Shiny Dashboard** for interactive visualization. By leveraging data manipulation, exploratory data analysis (EDA), and machine learning techniques, the project identifies critical factors affecting customer satisfaction and builds a predictive model for classification.

---

## Problem Statement  
Customer satisfaction is essential for the airline industry to maintain a competitive edge and foster loyalty. However, the vast data generated by customer interactions poses challenges for traditional analysis. This project addresses these challenges by employing R and creating a **Shiny Dashboard** to provide actionable insights and predictions.

---

## Features  
- **Data Cleaning and Transformation**: Data preview, cleaning, and transformation into lists, arrays, and matrices for analysis.  
- **Categorization**: Customers categorized into age groups (Young, Adult, Senior) for focused analysis.  
- **Visualizations**:  
  - Travel Type Distribution (Pie Chart).  
  - Customer Satisfaction by Customer Type (Bar Chart).  
  - Satisfaction by Age Group (Counts).  
  - Flight Distance by Class (Box Plot).  
  - Average Departure Delay by Customer Satisfaction (Line Graph).  
- **Interactive Dashboard**: Created with Shiny to allow users to explore visualizations and manipulate filters dynamically.  
- **Machine Learning**: Decision tree classification using the `caret` package to predict customer satisfaction.

---

## Dataset  
The dataset includes 22 features and 129,880 rows, collected from airline passengers.  

### Key Features  
1. **Personal Information**: Gender, Age.  
2. **Travel Information**: Type of Travel, Class, Flight Distance.  
3. **Service Ratings**: 12 features including Inflight Wifi Service, Food and Drink, Cleanliness.  
4. **Operational Data**: Departure Delay, Arrival Delay.  
5. **Target Variable**: Customer Satisfaction (Satisfied, Neutral, Dissatisfied).

---

## Repository Contents  
1. **R Markdown File (`analysis.Rmd`)**:  
   - Data cleaning, transformation, and analysis workflow.  
   - Exploratory visualizations and manipulation code.  
   - Machine learning implementation for classification.  
2. **Shiny Dashboard File (`dashboard.R`)**:  
   - Interactive dashboard visualizations for data insights.  
   - Code to dynamically filter and explore the dataset.  
3. **Dataset**:  
   - `Airline_customer_satisfaction.csv` (provided).  
4. **Report**: Detailed analysis and key insights in the attached PDF.

---

## How to Run the Project  
1. Clone the repository.  
2. Open `analysis.Rmd` in RStudio and knit the file to view the analysis.  
3. Run the Shiny dashboard by executing `dashboard.R` in RStudio to interact with visualizations.
---

## Shiny Dashboard Visualization  
The **Shiny Dashboard** provides interactive visualizations for insights derived from the analysis:  
1. **Pie Chart**: Explore travel type distribution.  
2. **Bar Chart**: Compare satisfaction levels between loyal and disloyal customers.  
3. **Line Graphs**: View satisfaction trends by age group and analyze delay impacts.  
4. **Box Plot**: Compare flight distance across travel classes.  

The dashboard enhances user experience by allowing dynamic data exploration and visualization in real-time.

---

## Analysis Highlights  

### 1. Travel Type Distribution  
*Interpretation*
1.	Dominance of Business Travel: The majority of the travel (69%) is for business purposes. This indicates that business travel is more prevalent within the observed population.
2.	Significant Personal Travel Segment: Although personal travel comprises a smaller portion (31%) of the total, it still represents a significant segment of the travel population.

*Insights*
1.	Service Prioritization for Business Travelers: Given that a larger percentage of travellers are traveling for business, it would be beneficial for airlines and travel-related services to prioritize features and amenities that cater to business travellers. This could include options for more flexible travel schedules, enhanced connectivity, and comfortable workspaces.
2.	Opportunities in Personal Travel: The 31% of travellers who are traveling for personal reasons still represent a substantial market. Services tailored to personal travellers, such as family-friendly amenities, leisure packages, and vacation deals, can enhance customer satisfaction and loyalty in this segment.
3.	Marketing Strategies: Marketing efforts can be tailored based on these proportions. For instance, campaigns targeting business travellers could focus on efficiency and productivity, while those aimed at personal travellers could emphasize relaxation, family activities, and leisure.


### 2. Satisfaction by Customer Type  
*Interpretation*
1.	Loyal Customers: A significantly higher proportion of loyal customers are satisfied (50%) compared to disloyal customers (4%). However, there is still a notable portion of loyal customers who are dissatisfied (31%).
2.	Disloyal Customers: The majority of disloyal customers are dissatisfied (14%), with only a small fraction being satisfied (4%).

*Insights*
1.	Customer Loyalty and Satisfaction: There is a strong correlation between customer loyalty and satisfaction. Loyal customers have a much higher satisfaction rate compared to disloyal customers.
2.	Dissatisfaction Rate: The dissatisfaction rate among loyal customers (31%) is lower compared to the dissatisfaction rate among disloyal customers (14%).
3.	Target Areas for Improvement: Efforts to improve customer satisfaction should focus on reducing the dissatisfaction rate, especially among loyal customers, as they form a significant portion of the customer base.

In conclusion, the bar chart suggests that building customer loyalty is crucial for achieving higher satisfaction levels. Companies should focus on strategies to convert disloyal customers into loyal ones and address the factors contributing to dissatisfaction among loyal customers to further enhance overall customer satisfaction.


### 3. Age distribution and satisfaction 

| Age Group      | Satisfied | Dissatisfied |
|----------------|-----------|--------------|
| Ages 0 - 10    | 1,318     | 1,845        |
| Ages 10 - 20   | 4,742     | 6,153        |
| Ages 20 - 30   | 12,091    | 12,697       |
| Ages 30 - 40   | 13,695    | 14,731       |
| Ages 40 - 50   | 19,084    | 9,922        |
| Ages 50 - 60   | 15,755    | 7,793        |
| Ages 60 - 70   | 4,116     | 4,974        |
| Ages 70 - 80   | 259       | 659          |
| Ages 80 - 90   | 0         | 12           |


Insights
1.	Middle-Aged Satisfaction: The middle-aged groups (40 to 60 years) exhibit the highest levels of satisfaction, suggesting that services are well-tailored to their needs.
2.	Room for Improvement: Younger travellers (under 40) and older travellers (over 60) show higher dissatisfaction rates, indicating potential areas for service improvement.
3.	Age-Specific Strategies: To improve overall customer satisfaction, targeted strategies should be developed for the under 40 and over 60 age groups.

The chart reveals significant variability in satisfaction levels across different age groups. Middle-aged travellers are generally more satisfied, while younger and older travellers have higher dissatisfaction rates. This suggests a need for age-specific approaches to enhance customer satisfaction, particularly focusing on the needs and preferences of younger and older travellers.


### 4. Average Departure Delay Analysis  
*Distribution*
1.	Dissatisfied Customers (Red): The average departure delay for dissatisfied customers is approximately 10 minutes.
2.	Satisfied Customers (Green): The average departure delay for satisfied customers is approximately 7.5 minutes.

*Interpretation*
1.	Impact of Departure Delay on Satisfaction: There is a clear correlation between shorter departure delays and higher customer satisfaction. On average, satisfied customers experience shorter delays compared to dissatisfied customers.
2.	Magnitude of Difference: The difference in average departure delay between satisfied and dissatisfied customers is about 2.5 minutes. While this may seem minor in absolute terms, it is significant enough to impact customer satisfaction levels.

*Insights*
1.	Delay Management: Managing and minimizing departure delays can play a crucial role in improving customer satisfaction. Efforts to reduce delays by even a few minutes can have a noticeable impact on customer perceptions and satisfaction levels.
2.	Customer Experience: The data suggests that customers are sensitive to delays, and even small reductions in wait times can enhance their overall experience.
3.	Operational Efficiency: Improving operational efficiency to reduce departure delays should be a priority for improving customer satisfaction. This could involve better scheduling, improved turnaround times, and more efficient boarding processes.

In conclusion, the chart highlights the importance of departure delays in determining customer satisfaction. Satisfied customers tend to experience shorter delays, indicating that reducing departure delays is a key strategy for enhancing customer satisfaction. Therefore, airlines and service providers should focus on operational improvements to minimize delays and improve the overall customer experience.



### 5. Online Boarding Ratings and Satisfaction  
*Interpretation and Analysis*
1.	Rating 0/5: No customers are satisfied, and only a few are dissatisfied. This indicates a very poor online boarding experience, likely due to a lack of functionality or significant issues.
2.	Rating 1/5: A significant number of customers are dissatisfied (11,291), and relatively few are satisfied (4,068). This suggests that at this rating level, customers find the online boarding experience to be inadequate.
3.	Rating 2/5: The number of dissatisfied customers (13,352) still exceeds the number of satisfied customers (5,221). However, there is a slight improvement in satisfaction compared to Rating 1.
4.	Rating 3/5: This rating shows a notable shift, with more customers satisfied (16,919) than dissatisfied (13,861). This indicates that customers find the online boarding experience to be acceptable at this level.
5.	Rating 4/5: A high level of satisfaction is observed, with 22,946 satisfied customers compared to 12,235 dissatisfied customers. This suggests that the online boarding experience is considered very good by most customers at this rating.
6.	Rating 5/5: The highest satisfaction level is observed here, with 21,933 satisfied customers and only 8,040 dissatisfied customers. This indicates an excellent online boarding experience.

*Key Insights*
1.	Positive Correlation: There is a clear positive correlation between higher ratings of the online boarding experience and customer satisfaction. As the rating increases from 0 to 5, the proportion of satisfied customers increases significantly, while the proportion of dissatisfied customers decreases.
2.	Significant Improvement Threshold: The most critical improvement appears between Ratings 2 and 3, where the number of satisfied customers surpasses the number of dissatisfied customers.
3.	Focus on High Ratings: Ensuring that the online boarding experience meets the criteria for higher ratings (4 and 5) can significantly enhance overall customer satisfaction.

The chart indicates that enhancing the online boarding experience to achieve higher ratings is crucial for increasing customer satisfaction. Ratings of 3 and above show a majority of satisfied customers, with the highest satisfaction levels at Ratings 4 and 5. Therefore, airlines and service providers should focus on improving their online boarding systems to achieve higher customer ratings, thereby boosting overall satisfaction and customer loyalty.


---

## Machine Learning Model  
A decision tree classification model using the `caret` package was developed to predict customer satisfaction:  
- **Accuracy**: 82.72%  
- **Kappa**: 0.647 (substantial agreement).  
- **Metrics**: High performance as per the confusion matrix and statistical tests.
- **Balanced Accuracy**: 81.97% is the average of sensitivity and specificity, providing a balanced view of the model performance across both classes.

---
