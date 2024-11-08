# eda_for_data_clustering
exploratory data and explanatory data analysis

# Introduction to EDA
## What are the techniques commonly used for EDA?
Some of the commonly used techniques and tools in EDA include:
1. Descriptive Statistics : mean, median, mode, standard deviation, quartiles.
2. Data Visualization : histograms, scatter plots, box plots, and heatmaps.
3. Pattern and Anomaly Search : clustering, outlier detection, and trend analysis.

## What does EDA take place?
1. Explanatory Data Analysis (EDA) is a data analysis process that aims to explore and understand the characteristics and patterns of data before conducting further analyses or statistical models. 
2. EDA typically involves the use of data visualisation, summary statistics, and other techniques to identify relationships, trends, and anomalies in the data.

# Some of the main objectives of EDA include:
1. Identifying patterns: Looking for patterns and relationships that may exist in the data.
2. Detecting anomalies: Finding unusual values or outliers that might affect the analysis.
3. Recognising distributions: Understanding the distribution of variables and their properties (normal, skewed, etc.).
4. Assist in model selection: The information obtained from EDA can guide the selection of the most appropriate statistical technique or model for the data.

# Introduction to The Dataset
## This dataset is a collection of information about nutrition in fast food that is sold in several well-known restaurants. while this data contains 515 rows and 17 columns
1. restaurant: restaurant's name
2. item: menu's name
3. calories: calories
4. cal_fat: calorie fat score
5. total_fat: total fat score
6. sat_fat: sat fat score
7. trans_fat: trans fat score
8. cholesterol: cholesterol score
9. sodium: sodium score
10. total_carb: total carbohydrate score
11. fiber: fiber score
12. sugar: sugar score
13. protein: protein score
14. vit_a: vitamin a
15. vit_c: vitamin c
16. calcium: calcium score
17. salad: salad category

# Objectives
1. Understanding Data Structure
2. Identifying Patterns and Trends
3. Exploring the distribution of important variables
4. Detecting and dealing with outliers or extreme values
5. Create data visualizations as tools that facilitate data understanding
6. Exploring more detailed information within the dataset
7. Identifying and handling data preprocessing tasks
8. Perform hypothesis testing to see relationships or patterns in the data
9. Support Decision Making
10. Effectively communicate results and insights from the EDA process

# Work Flow
1. Reading Dataset
2. View Information
3. Data Preprocessing
4. Descriptive Statistics
5. Pivot Table
6. Hypothesis testing & Correlation Test
7. Data Exploratory and Data Visualizations using pygwalker

# Understanding Data Distribution for Categorical Data
1. .nunique() is used to indicate the number of distinct categorical data in a column. In the restaurant column, there are 8 distinct data (8 restaurant exist)
2. .value_counts() is used to count the number of data in each different categorical data (the number of data in each restaurant, item and salad)

# Understanding Data Distribution
From the results of the skewness calculation that has been carried out, it is found that the average skewness is in the range -0.5 < skewness < 0.5, which means that the data is quite positive slope but still distribute normally. However, only the carbohydrate score variable gets a skewness result < 1, which means the data is not too skewed. Meanwhile, the results of the kurtosis calculation show that the data has a sharp peak with a value above 0. 

# Descriptive Statistics for Numerical Data
1. there are 5 columns that have null values,
2. the dataset has different scales, this can be caused by the units used to write the information are different,
3. the min value in all columns except calories is 0,
4. the distance between the minimum and maximum values is quite far and significant, this can cause outliers.

# Descriptive Statistics for Categorical Data
1. there are 8 different data in the restaurant column (8 different restaurant names)
2. there are 505 different data in the item column which contains the name of the food menu available at each restaurant.
3. Taco bell is the data with the highest frequency of occurrence, which is 115 data.
4. There are 3 Crispy Chicken Sandwich menus in the dataset.

# Summary Data from Pivot Table
1. Here the pivot table to summarize the data is presented in 2 separate tables, this is because each variable represents different nutrients.
2. protein, fat, carbohydrate, fat and sugar represent macronutrients
3. salt, calcium, vitamin a, and vitamin c represent micronutrients
4. caloric value has a very high value because the caloric value is obtained from the sum of (9 x fat) + (4 x carbohydrates) + (4 x protein)
5. The value between salt and other micronutrients is quite different, this could be because the micronutrients in the table are presented in units of micrograms while sodium has units of gr/mg.

# Frequencies of Categorical Data
Based on this graph, it can be seen that Taco Bell restaurant provides the most varied menu among other restaurants, while Check Fil-A is the restaurant with the least variety of menus. 

# Understanding Data Distribution and Detecting Anomalies/Outliers
Outliers are data values that are significantly different from most of the data in a dataset. The presence of outliers can have various effects on data analysis and machine learning models. 
Here are some of the main effects of outliers:
1. Disrupting descriptive statistics
2. Affects graph analysis
3. Disrupt machine learning models
4. Prediction errors
5. Decision-making errors

From visualizing the data using boxplots, we can see that almost all of the variables have outliers, with the most outliers in the variables calories, cal_fat, cholesterol and sodium.

# Understanding outliers
1. Outliers in fast food datasets, such as extreme nutritional values, are often viewed as anomalies to be removed. However, these outliers can actually provide valuable insights. 
2. It can represent unique menu items with distinct characteristics, such as low-calorie or high-protein foods, due to the ingredients used or preparation methods. 
3. By retaining these outliers, the integrity of the data is maintained, allowing for a more comprehensive analysis of nutritional variation across menus. This deeper analysis helps consumers make informed food choices and be aware of the nutritional value of the food they consume.
4. Based on the table, it can be seen that foods that contain high sodium are also classified as high protein foods.

# Hypothesis testing & Correlation Test
1. Chi-Square: It shows the difference between the observed and expected frequencies. The larger this value, the larger the difference.
2. p-value: The p-value indicates the extent to which the observed data supports or does not support H0. If the p-value is smaller than the pre-determined significance level (alpha), then the null hypothesis (H0) is rejected and the alternative hypothesis is accepted.
3. Degrees of Freedom (df) is an important concept in statistics that reflects the number of independent values that can vary in a particular statistical calculation. 
4. Based on the item column, there is information that can explain why the menu has a high protein content, some of which are because the food contains chicken, milk and butter.
5. In the hypothesis test using Chi-Square, the H0 result was rejected because there is a significant relationship among the calories variable and the other variables (sugar, sodium, fiber, cholesterol).

# Visualization for Correlation Test
1. Based on the pairplot on the side, it can be seen that calories have a correlated relationship with almost all variables except vitamin a and vitamin c.
2. From the graph, it can also be seen that the distribution of data on all variables tends to be positively skewed.
3. Vitamin c and vitamin a have no correlation with other variables

# Data Exploration 1
1. From the two bar charts, it is known that before the classification of the menu based on the similarity of the menu names, Taco Bell Restaurant has a total menu of > 110 menus, while after the classification of Taco Bell restaurant only has about 45 menus.
2. Before the classification, Subway ranks second as a restaurant with quite a lot of menu variations, but after the classification, Subway's position is occupied by Burger King.
3. The last order before and after the classification is still occupied by Chick Fil-A.

# Data Exploration 2
Information from the results of data mining based on the bar graph that has been done before, obtained the following details: 
1. The number of restaurants before and after menu classification is 8 restaurants.
2. Taco Bell is the restaurant that experienced the most drastic changes among other restaurants.
3. The number of menus from all restaurants before classification is 505 menus, The number of menus from all restaurants after classification is 243 menus

# Data Exploration 3
Based on extracting information related to the menu at a restaurant, the following results were obtained:
- The most available menu at Taco Bell before classification is the high-calorie food category, and the most is the very high-calorie food after classification.

# Data Exploration 4
Based on data mining about restaurants that have the most diverse menu, namely Taco Bell, the following information is obtained:
1. the most available menu category is Burrito with a total of 16 menus.
2. the least available menu categories are Cirpsy and other with 2 menu varieties each.
3. of the 16 menu items available, 9 of them contain very high calories.  

# Data Exploration 5
The following are the results of data mining about Chick Fil-A as a restaurant with the least number of menus available:
1. the most available menu category is grilled with 6 menu varieties
2. there are 3 menu categories that only have 1 variety of menus, namely salad, smoke and wrap.

# Data Exploration 6
On the face of it, both graphs have the same proportion.
The only difference is that the number of datasets after the menu column is classified, the frequency decreases. 

# Data Exploration 7
Based on extracting information related to food classification based on calories in the fastfood dataset is as follows:
1. after classification, the number of menus in each category has decreased drastically, which is about 50% of the menus missing from the dataframe.
2. before being classified by menu, foods with very high calories amounted to 246 menus, after classification the number of foods with very high calorie content was 122 menus.
3. Before classification, the menu with low calorie level was 5 menus, after classification it was reduced to only 2 menus.

# Data Exploration 8
Based on extracting information related to calorie classification, the following results were obtained:
1. 2 menus with the lowest calories are available at two different restaurants, namely Chick Fil-A and Subway.
2. the lowest calorie food menu comes from the grilled and salad menu category, namely 4 Piece Grilled Chicken Nuggets and Veggie Delite
3. 5 very high calorie meals are available at McDonalds, Sonic and Dairy Queen.
4. Very high calorie food categories are Crispy, Nuggets and Strips
5. The calorie content of the low calorie food menu is 50 Kcal, while the calorie content of the very high calorie class food menu is 2430 Kcal.

# Data Exploration 9
Based on food classification based on menu similarity, the following results are obtained:
1. 16 food categories consisting of crispy, grilled, salad, roast, steak, burrito, nuggets, burger, strip, taco, fries, smoke, wrap, pizza, pretzel, others menu.
2. The most frequent menu category is crispy.
3. The least menu category is pretzel which is only 1 menu.
4. The pretzel menu is only available at Sonic with the menu name Cheesy Bacon Pretzel Dog - 6 in.
5. Crispy menu is most widely sold at McDonalds, which is 17 menu varieties

# Summary
Based on the results of our data exploration, we can draw some important conclusions about the patterns and menu variations in fast food restaurants:
1. Popularity of High-Calorie Foods: Very high-calorie meals were found to be the most widely offered, with a total of 122 items. This shows consumers' preference for the menu.
2. McDonald's dominance: McDonald's stood out as the restaurant that offered the most very high calorie menu items, reaching 2000 Kcal. 
3. Limited Low-Calorie Food Options: There are very few low-calorie foods available at fast food restaurants, with only two items - nuggets and salads - on offer. This suggests that options for consumers looking for low-calorie meals are very limited in the fast food environment.
4. Wide Menu Variety at Taco Bell: Taco Bell has the most menu variety, with 46 menu items.
5. Limited Menu at Chick-fil-A: In contrast, Chick-fil-A has the least variety of menus, offering only 16 menu items.
6. Wide Variety of Menu at Taco Bell: Taco Bell has the most menu variety, with 46 menu items, indicating greater flexibility and diversity in food choices compared to other fast food restaurants.
7. Popularity of Specific Menu Items in Restaurants: At Taco Bell, the Burrito is the most sold menu item, while at Chick-fil-A, the Grill is the most available menu item. In contrast, 8. Pretzels are the least commonly available item, sold only at Sonic, and crisps are the most widely available food category overall, with 42 items.
9. Calorie Patterns in Popular Menu Items: At Taco Bell, the Burrito menu is not only popular but also high in calories, with 10 of the Burrito menu items being in the very high calorie category (>500 Kcal). Meanwhile, McDonald's stands out with three menus that have the highest caloric value, all of which are above 1500 Kcal.
10. Low Calorie Menu at Subway and Chick-fil-A: Subway and Chick-fil-A are two restaurants that offer low-calorie options with one menu item each, namely Grilled Chicken Nuggets and Veggie Delite Salad, suggesting there are options for more calorie-conscious consumers, although these options are very limited.
11. Overall, this analysis shows a tendency for fast food restaurants to offer high-calorie menu items, which tend to be more popular and more diverse, while healthy or low-calorie options are still very limited. Menu diversification also varies significantly between restaurants, with some restaurants offering more variety and options than others.

# Decision Making
Based on the results of the initial data exploration (EDA), there are several next steps that can be taken for more in-depth analysis:

Consumer Segmentation Based on Calorie Preference:
Objective: 
1. Identify consumer segments that are more likely to prefer high calorie foods versus low calorie foods.
   identify foods that are classified as healthy and unhealthy
   Steps: Use clustering or segmentation techniques to group menus by calorie content and sales frequency. This can provide insight into the target market for each food category.
2. Deeper Nutrition Analysis:
   Objective: Further explore the content of other nutrients (such as fat, protein, fiber) and how they relate to calorie preferences and sales.
   Steps: Conduct multivariate analysis to see how different nutritional components interact with each other and influence consumer decisions.
3. New Menu Evaluation or Product Development:
   Objective: Identify opportunities to develop new menus or modify existing menus to meet the needs of calorie-conscious consumers.
   Steps: Based on findings about the popularity of high-calorie versus low-calorie menus, consider designing experiments or piloting new menus with a more balanced calorie composition.
4. Inter-Restaurant Benchmarking:
   Objective: Comparing the performance of different restaurants in offering certain menus, especially high-calorie versus low-calorie menus.
   Steps: Use comparative analysis to see how restaurants like McDonald's, Taco Bell, and others differ in terms of menu variety, caloric value, and sales patterns.
   This can inform competitive strategies. Menu Sales Prediction:
     Objective: Create a predictive model to predict menu sales based on calorie content and other nutrients.
     Steps: Use machine learning techniques such as linear regression, decision trees, or random forest to predict sales based on nutrition variables and menu categories.
     These steps can help deepen understanding of fast food consumption patterns and inform strategic decisions for businesses, both in product development and marketing strategies.
