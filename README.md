# Uncovering the Unseen Patterns of Global Food Waste: Analysis and Conclusions

## Team Members:
Mark Bishoff

Tatyana Grishanina

Alanis Perez

Tai Reagan
- - -

[Project Overview](#project-overview)

[Project Questions](#project-questions)

[Data Collection and Cleaning](#data-collection-and-cleaning)

[Analysis and Visualizations](#analysis-and-visualizations)

[Summary and Conclusion](#summary-and-conclusion)

[Data Limitations](#data-limitations)

---
![foodloss.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/foodloss.jpg)

## Background
Food loss is a critical global issue affecting food security, economic stability, and environmental sustainability. It refers to the reduction in the quantity or quality of food available for human consumption. According to the Food and Agriculture Organization (FAO), approximately one-third of all food produced for human consumption is lost or wasted every year, amounting to about 1.3 billion tons.

The implications of food loss are vast. Economically, it results in significant financial losses for farmers, businesses, and consumers. Environmentally, it contributes to wasted resources, such as water, land, and energy, used in food production, and generates greenhouse gas emissions from decomposing food in landfills.

 Addressing food loss requires a multifaceted approach involving improvements in agricultural practices, better storage and transportation infrastructure, and changes in consumer behavior. Global efforts are underway to reduce food loss and waste, with initiatives focusing on enhancing supply chain efficiencies, promoting sustainable consumption, and implementing policies and regulations to support food waste reduction

- - -
## Project Overview
Our project aims to conduct a comprehensive analysis of food waste on a global scale, focusing on quantifying and mapping the magnitude and distribution of food loss and waste throughout the entire food value chain. Utilizing extensive datasets from diverse sources, we will investigate the specific types of food that are most frequently lost or wasted, pinpoint the geographical regions with the highest incidence of food waste, and identify the critical stages in the value chain—from production through to consumption—that contribute the most to this issue. By generating detailed visualizations and performing in-depth data analysis, we aim to uncover key insights that will highlight opportunities for improvement, ultimately striving to enhance economic efficiency and sustainability within the food value chain.


## Our process for analyzing the data
- Extract, clean and upload data with Python 
- Perform statistical analysis and create data visualization using Jupyter Notebook
- Gather all our findings and visualizations and put them into a deck to present to the global food loss prevention committee. 

## Resources
- Data: [Food Loss and Waste Database](https://www.fao.org/platform-food-loss-waste/flw-data/en/)
- Data: [World Bank GDP Database](https://data.worldbank.org/indicator/NY.GDP.PCAP.CD)

- - -

## Project Questions
- How does food loss and waste vary across different stages of production?
  
- Which countries waste the most on average, and how does national wealth correlate with food waste?
  
- Which countries waste the most on average, and how does national wealth correlate with food waste?
  
- How has global food waste rates changed over time?



- - -
# Data Collection and Cleaning

## Collection Process
Our dataset contains 2 CSV files, obtained from [FAO]( https://www.fao.org/platform-food-loss-waste/flw-data/en/) and [World Bank](https://data.worldbank.org/indicator/NY.GDP.PCAP.CD). The data was then clean and organized by the following process:

## Cleaning Process 
We read in the CSV files for the FAO dataset and World Bank GDP dataset. Drop empty/ irrelevant columns. Once smaller or merged data frames are created, drop empty rows in empty values as “NaN”.

![Datacleaning.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/Datacleaning1.png)

Once We dropped all missing values we created a new DataFrame filtering out all the empty columns.

![filtering_empty_columns.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/filtering_empty_columns.png)

## Inserting the GDP Values
After importing the GDP dataset from the World Bank, we integrated it with the FAO dataset. We then categorized all countries into five distinct income groups based on their GDP: low income, lower middle income, middle income, upper middle income, and high income.

![gdp_values.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/gdp_values.png)

## Organizing countries into bins
The groups were classified based on their 2021 GDP per capita values as follows: Low Income: $0 - $1,000, Lower Middle Income: $1,001 - $5,000, Middle Income: $5,001 - $15,000, Upper Middle Income: $15,001 - $50,000, and High Income: $50,000 and above. These classifications were derived from the World Bank's categorizations available on their website, where the dataset was sourced.

![Organizing_into_bins.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/Organizing_into_bins.png)

## Simplified Supply Stages
 We then analyzed each group's waste by 'simplified supply stages.' To facilitate visualization, we consolidated several of the original stages, such as harvest and farming, into broader categories, ensuring only similar stages were combined. We subsequently created a stacked bar graph illustrating each income group's waste based on these newly simplified supply stages.

![supply_stages_1.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/supply_stages_1.png)
![supply_stages_2.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/supply_stages_2.png)

- - -

# Analysis and Visualizations

## Question One:
### How does food loss and waste vary across different stages of production?
**Food Supply Process** 

The supply stages refer to the distinct steps in the farm-to-table process. This journey begins with farming, which includes sowing, growing, and harvesting. The middle stages consist of storage, transportation, and export. Food then reaches institutions and consumers through the wholesale, retail, and food service (restaurant) stages, ultimately ending with consumption in households. The objective of this analysis was to identify which of these stages experiences the highest rate of food loss.

**Focus on Africa**

The analysis focuses on food loss in Africa for several compelling reasons. Firstly, Africa is one of the most comprehensively documented continents regarding food loss data, providing a robust foundation for accurate, data-driven analysis. Secondly, examining this region allows for the study of an area with regional similarities such as GDP, food processes, and cultural habits, enabling a more targeted and relevant investigation.

**Methodology**

We isolated data from African countries by creating a specific dataframe. This involved compiling a list of African countries and calculating the average food loss for each supply stage within these countries. Several graphs were then generated to detail these calculations and provide a visual representation of the findings.

![country_list.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/country_list.png)


# Heat Map Analysis

## Key Takeaways:
**High Food Waste Percentages**

- Benin exhibits one of the highest food waste percentages among the analyzed countries, as indicated by the darkest color on the map. This suggests significant challenges in managing food waste.

**Lower Food Waste Percentages**

- Angola shows the lowest food waste percentages, represented by lighter shades of blue. This indicates better efficiency in food handling and waste management compared to other African nations with darker blue shades

**Regional Insights**

- East Africa generally displays higher food waste percentages. While Central and West Africa exhibit a mix of high and moderate food waste percentages.

![high_and_low_food_waste.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/high_and_low_food_waste.png)


# Bar Graph Analysis

## Key Takeaways:
**Export Stage Inefficiencies**

- The data reveal that the Export stage has the highest food loss percentage, suggesting potential inefficiencies in shipping and handling processes.

**High Loss Stages**

- In addition to the Export stage, the Retail, Post-harvest, Wholesale, and Whole Supply Chain stages also show elevated food loss percentages. These stages represent key areas where improvements could significantly reduce overall food waste.

![distribution_graph.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/distribution_graph.png)


**Focused Analysis**

- Further analysis was conducted to understand the reasons for higher food loss at these stages, assessing the statistical significance of the differences to inform targeted interventions.

# Box Plot Analysis

## Key Takeaways:
**Export Stage Losses**

- Box plot analysis revealed that the Export stage has the highest median food loss percentage, indicating significant losses during export compared to other stages. This stage also showed greater variability in losses.

**Farm and Storage Variability**

- The Farm and Storage stages exhibited lower median food loss percentages but showed many outliers, indicating occasional spikes in food loss. Despite these spikes, overall losses in these stages were lower and less variable compared to the Export stage.

![box_plot.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/box_plot.png)

# ANOVA and Tukey Test Results

## Key Takeaways:
**Statistical Analysis**

- ANOVA and Tukey tests confirmed that the Export stage's food loss is significantly higher than other stages, with the difference between Export and Farm being more pronounced than between Export and Storage.

![anova_test.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/anova_test.png)
![tukey_test.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/tukey_test.png)


## Question Two:
### How does national wealth correlate with food waste?
We conducted multiple analyses to investigate the relationship between food waste and national wealth. Our hypothesis posited that wealthier countries might waste more food due to overabundance; however, poorer countries could experience higher waste levels due to a lack of resources or technology. To gain deeper insights, we categorized countries by income levels and performed linear regression analyses to identify significant trends.

# Simple Bar Graph Analysis
## Key Takeaways:
- The first bar graph presents the average loss percentages for each income group over the 2011-2021 period, chosen due to data availability and consistent GDP classifications. 
- The high-income group exhibited the highest average percentage of food loss during this timeframe.

![foodwaste_gdp.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/foodwaste_gdp.png)

# Stacked Bar Graph Analysis
## Key Takeaways:
- Less wealthy countries were the only ones to experience losses due to exports. In contrast, higher-income countries faced more significant losses during the transport stage. Lastly, the wealthiest countries exhibited the highest levels of food waste at the household stage.

![waste_class_by_supply.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/waste_class_by_supply.png)

# Scatterplot Analysis
## Key Takeaways:
- Independently of the previous bar graphs and groupings, we generated scatterplots to illustrate the relationships between wealth and food loss/waste. We conducted a statistical analysis on overall GDP and food waste, followed by an analysis for each supply stage.
  
- A linear regression analysis of food waste based on GDP did not reveal a significant relationship, with a correlation value of 0.25, which is insufficient for statistical significance. However, analysis of individual supply stages yielded stronger results: for the market stage, there was a correlation of 0.88 between GDP and food waste percentages; for the food services stage, a correlation of 0.62; and for the household stage, a correlation of 0.58. Other stages did not show any statistically significant relationship between GDP and waste. Overall, we can conclude that wealthier countries tend to be more wasteful during the consumer stages of the production process.

![scatter_plot.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/scatter_plot.png)

## Question Three:
###  Which countries waste the most on average, and how does national wealth correlate with food waste?
To evaluate if certain types of commodities are more susceptible to losses, we categorized them into six groups: fruits, dairy, legumes, proteins, grains, and vegetables. Our analysis revealed that fruits reported the highest waste percentage. Additionally, when examining which countries were the most wasteful, we found that the United States reported the highest waste percentage, with fruits being the most wasted food group.

# Simple Bar Graph Analysis
## Key Takeaways:
**Food Group Composition**

- The dataset included 147 commodities categorized into six food groups: dairy, legumes, fruits, proteins, grains, and vegetables. Grains were the most represented group.

**Unexpected High Loss in Fruits**

- Contrary to expectations, fruits accounted for the highest percentage of food loss at 27.4%, surpassing other food groups. This high loss rate is likely due to fruits' vulnerability to damage, rot, pests, and the need for specific growing, harvesting, and preservation conditions.
 
**Lower Losses in Grains**
- Despite being the most documented group, grains exhibited lower loss percentages. This can be attributed to their lower maintenance requirements and simpler cultivation and harvesting processes compared to more delicate commodities like fruits and vegetables.
  

![food_waste_by_group.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/food_waste_by_group.png)

# Stacked Bar Graph Analysis
## Key Takeaways:
**United States Leads in Waste Percentage**

- Among the 127 countries analyzed, the United States reported the highest food waste percentage, which aligns with its extensive data representation in the dataset

**Fruits as the Most Wasted Food Group**

- Fruits were identified as the most wasted food group, with 44 out of 127 countries reporting it as the primary source of waste. This trend was also evident among the top 10 most wasteful countries.

**Grains as a Common Food Group**

- Grains were the only food group consistently reported across all of the top 10 most wasteful countries, highlighting their widespread presence and potential impact on food waste patterns.

![top_ten.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/top_ten.png)

## Question Four:
###  How have global food waste rates changed over time?
To uncover trends in food waste rates over time, we found the mean rate for each year, then displayed the calculations via simple line graphs.

# African Countries Time Series Analysis
## Key Takeaways:
**Pre-1990 Variability**

- The analysis of fifteen African countries revealed significant fluctuations in food waste rates in the years leading up to 1990, indicating a period of instability in food waste management.

**Early 1990s Surge**

- A pronounced spike in food waste levels was observed in the early 1990s, highlighting a critical period of increased food loss across the region.

**Sustained Reduction Post-1990**

- Following the early 1990s spike, food waste rates significantly decreased and have remained consistently low over the past 20 years, suggesting improved efficiency and stability in food waste management practices.

![Africa_time_series.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/Africa_time_series.png)

# Income Group Time Series Analysis
## Key Takeaways:
**Consistent Trend in Lower Income Groups**

- The low- to middle-income groups exhibited trends similar to those observed in the African nations: a notable spike in food waste in the 1990s, followed by consistently low waste levels in subsequent years.

**Lack of Trends in Higher Income Groups**

- The upper-middle and high-income groups did not display any discernible trends over time. Food waste levels in these wealthier groups remained relatively stable, with no significant fluctuations reported.

**Data Limitations for High-Income Countries**

- Due to a lack of data for higher-income countries before 2010, tracking trends during that period was not possible. Despite this limitation, it is evident that these countries did not experience significant changes in food loss percentages over the years for which data was available.


![waste_by_income_time_series.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/waste_by_income_time_series.png)


# Global Food Waste Time Series Analysis
## Key Takeaways:
**Notable Spikes in Food Waste**

- The plot reveals a significant spike in food waste rates just before 2000 and a smaller increase around the onset of the COVID-19 pandemic. These trends may be influenced by global events, although the data does not specify exact causes.

**Potential Factors for 1990s Spike**

- The increase in food waste rates in the 1990s could be attributed to factors such as increased globalization, economic fluctuations, and natural disasters, which may have disrupted food supply chains and increased waste.

**Sustained Improvement in Recent Years**

- The lower food waste rates observed over the last 20 years may result from improved agricultural practices, increased awareness of food waste issues, technological advancements, policy interventions, and greater economic stability.

![global_food_loss_time_series.png](https://github.com/alanisrperez/food-waste-patterns/blob/tai/Images/global_food_loss_time_series.png)

# Summary and Conclusion

## Summary
Food waste is influenced by numerous factors, including supply chains, food groups, countries, and their economic status. This project aims to analyze these factors to better understand the different stages where food waste occurs and the impact of economic status on food waste levels.

### Analyzing Food Waste in Supply Chains
We began by investigating the stages in the food supply chain where food is wasted the most, using data provided by the Food and Agriculture Organization. We discovered that the highest levels of waste occur in the Export, Retail, and Post-Harvest stages, all hovering around 18-25%. In contrast, distribution was rated the lowest at just over 1%.
By comparing the groups in various box plots, we observed that many early stages in the food supply chain, such as Farm, Storage, and Harvest, have low averages but large quantities of statistical anomalies. The middle stages of the supply chain, such as Post-Harvest, Exports, Processing, and Retail, have larger means with their quartiles being spread out, implying greater variety in the data.

### Economic Impact on Food Waste
We collected data on various countries' GDPs over 20 years and grouped them into different classes, such as low income, lower middle, and high income. The trends showed that, on average, the lower to upper middle-income groups have a steady increase in waste, with high-income groups experiencing the largest spike.
By comparing the food waste stages through bar graphs and scatter plots, we observed a clear increase in waste by total percentage, with the upper middle and high-income groups wasting the most. However, the scatter plots revealed no clear correlation, with a correlation score of 0.24. Each scatter plot compared a country's GDP with its food waste percentage. By creating scatter plots of all data groups, specifically focusing on each supply chain's food waste percentage, we found positive correlations with Retail, Markets, and Food Services, indicating that the rise in waste percentage occurs at the final stages of production at the consumer level.

## Food Groups and Waste
Next, we categorized food into vegetables, fruits, grains, dairy, proteins, and legumes and found that fruits and vegetables make up more than half of all food waste in the world, with grains being the lowest at only 8%. Fruits specifically made up the largest waste group, especially in countries with the highest waste levels.

## Historical Trends in Food Waste
When examining food waste over time, we found that most food waste occurred prior to 2000, particularly during the 1980s and 1990s, hovering around 20 to 30 percent loss on average. After 2000, food waste levels leveled off significantly, with the graph hovering around 5%.

## Conclusion
In conclusion, most waste occurs at the export and farm levels, but a correlation between food waste and a country’s GDP is only seen in the later stages of the supply chain at the consumer level. Most of the food waste comes from fruits and vegetables, and after 2000, we observe the lowest levels of food waste.


# Data Limitations

### Data Availability
Lack of comprehensive data across all countries and production stages can limit the scope of analysis. Some regions or countries may not have consistent or up-to-date data on food loss and waste.

### Product Specificity 
An insufficiency of detailed data on specific product types can impede the analysis of which products are more susceptible to losses. Aggregated product categories may obscure significant differences in food loss rates among various product types.

### Economic and Environmental Factors
Data may not account for economic and environmental factors that influence food loss and waste, such as market prices, weather conditions, and policy changes. Lack of contextual information can limit the ability to understand the underlying causes of food loss and waste.

### Methodological Differences:
Differences in how food loss and waste are defined and measured can lead to inconsistencies in the data.
