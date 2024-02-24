# Obesity Level Analysis
Topic:How obesity levels are influenced by eating habits, physical conditions, and genetics. The data sets includes data from Mexico, Peru, and Colombia. 

Data was obtained from UCI learning repository. It has 17 attributes and 2,111 rows. People participating in the study were also asked if they are a smoker or not.

Tools: Excel, R, Tableau
# Data Description
![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/7252fc1d-40c6-4161-b74c-0c98cda1293c)

**Data Pre-Processing**
- Created a new column to calculate the Body Mass Index (BMI) to analyze the relationships of the dataset's attributes and obesity.
- BMI formula in R: obesity$BMI <- obesity$Weight / (obesity$Height)^2 
- Removed 24 duplicates from the dataset (Original number of rows: 2,111. After duplicates removal: 2,087)
- There were no missing values in the dataset

**Quantitative Variables Summary**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/90b24101-69f2-4d66-9511-237a737e93c6)

**Qualitative Variables Summary**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/6611621a-b523-4277-b70c-b1dc306f124e)

**Analysis**

**Number of respondents in each weight classification**
![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/6a27dfd1-4c6e-410f-8d3e-fde49cbb24c4)

There is a disparity between the sample distribution across weight categories and the actual population distribution in Mexico, Peru, and Colombia. While these countries typically have a higher prevalence of overweight individuals compared to obese individuals, the dataset indicates a higher percentage of obesity at 40% and 25% overweight. Additionally, there's a concerning overrepresentation of individuals classified as underweight in the sample, which deviates significantly from the population statistics, particularly in Mexico where only 1.4% are underweight but the dataset shows over 10%.

This discrepancy raises concerns about the representativeness of the sample and its implications for drawing conclusions. Despite this, the relatively balanced distribution of individuals across weight categories in the sample, as opposed to the actual population, might still offer valuable insights.

**Respondents' Height and Weight Distribution**
<img width="1021" alt="Screenshot 2024-02-24 at 12 59 51 AM" src="https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/a02a76af-2da6-431f-80e2-6ad40c3070ac">

Weight and height play crucial roles in determining a person's weight classification, as they are the key components used in calculating BMI. Therefore, examining the distribution of both factors among the respondents provides further insight into our sample.

The weight data exhibits an almost bimodal distribution, with an average around 80 kilograms. On the other hand, the height data follows a more symmetric, normal curve, with an average around 1.7 meters. Neither variable shows significant skewness towards one side.

**Yes/No Questions - General Statistics**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/08b55c94-2ed8-417e-a13d-9684a8ddbd29)

Only a small proportion of respondents, merely 1%, are smokers. It's essential to keep this small sample size in mind when assessing the impact of smoking on obesity and drawing conclusions from a possibly unrepresentative sample. Similarly, when evaluating the influence of calorie intake, it's noteworthy that fewer than 5% of respondents engage in this behavior.

A significant majority of respondents report a family history of weight-related issues and frequently consume high-calorie foods. Conclusions derived from this dataset might be more dependable. However, it's vital to acknowledge that this data may also be biased toward a population with above-average obesity rates.

**Average Age for Weight Classification**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/86b24e0f-62e9-4e11-bde4-2c405ea5b992)

I included a breakdown by gender because gender might influence body fat levels. I arranged the categories from the lowest to the highest weight, revealing that the average age tends to increase with each higher weight category. This suggests that as individuals age, they may become more prone to overweight conditions. Additionally, the graph indicates that females generally have a slightly higher average age than males across most categories, except for type II obesity. Notably, the short error bars across all categories and genders indicate minimal variation in the data and a low level of uncertainty.

**Correlation Matrix**
![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/8ed5823d-2fb7-406d-b239-ea1fa71ea612)

**Relationship between Male and Female**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/ae943c44-64ba-4b5a-b661-8c3186eb41b6)

This analysis aimed to visualize the linear relationship between weight and height, considering gender as a potential influencing factor. The graph illustrates an upward trend in weight with increasing height for both genders, with the regression line for females appearing slightly steeper than that for males. This suggests that, on average, the same increase in weight corresponds to a slightly larger increase in height for females compared to males.

Furthermore, the data points for males appear more tightly clustered than those for females, particularly across the weight range. This indicates that females exhibit a wider variation in weight compared to males. However, it's important to note that despite the observed trends, the data points deviate from the regression line, indicating that the line does not perfectly capture the relationship between weight and height across genders.

**BMI Distribution by Category**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/436bf054-6dd2-4da0-9b3b-16525d3e934e)

The graph illustrates a distinct correlation between BMI levels and various weight categories, validating the use of BMI for characterizing these categories. Each category's median BMI is consistently separated by approximately 5 kg/m², although some intervals are slightly smaller than others. Additionally, the presence of few outliers suggests a strong correlation between BMI and weight categories. This indicates that BMI can effectively serve as a quantitative variable when assessing the impact of different factors on weight category.

**Examining the relationship of BMI with multiple factors**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/64bbc318-4c74-4af5-a859-169438689e0e)

Analyzing BMI as a measure of obesity, I examined how various categorical variables correlate with it to identify influential factors.

In the first subplot, individuals who frequently consume high-calorie food exhibit a median BMI approximately 6 kg/m² higher than those who don't. This suggests that calorie intake likely contributes to increased body fat.

The second subplot indicates a minimal relationship between alcohol consumption and BMI, as individuals who frequently drink alcohol have similar median BMI values to non-drinkers. Notably, only one respondent reported "always" drinking, indicating a need for more data on this aspect.

In the third subplot, individuals with a family history of obesity have a median BMI roughly 11 kg/m² higher than those without such a history, suggesting a genetic predisposition to obesity.

Finally, the fourth subplot reveals no significant relationship between gender and BMI, as both genders exhibit similar median BMI values. However, the quartile analysis suggests that female BMI values are more dispersed, aligning with the observation of a wider weight range among females compared to males.

**Physical Activity & BMI**

![image](https://github.com/eparaschou/Obesity-Level-Analysis/assets/148002149/42a31fd0-7c6e-4872-83e6-7d2989e80180)

The figure displays the relationship between two movement-related variables and their influence on BMI. In the first subplot, the regression line indicates a negative trend between a person's frequency of physical activity and their BMI. However, numerous data points appear significantly distant from the regression line, implying that the frequency of physical activity may not be strongly correlated with BMI.


**Conclusion**
The analysis indicates that variables like a family history of obesity and frequent consumption of high-calorie foods have a significant impact on weight classification. Conversely, factors such as age appeared to exert less influence, while gender showed no discernible effect on weight classification.





  
