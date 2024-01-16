  # Project_Enoteca

In this fictional scenario, a French wine shop owner, planning to expand his well-established retail store, seeks insights to determine whether it's beneficial to diversify the wine selection beyond France. Specifically, he is interested in identifying potential countries to source wines from. In light of the expansion, he is open to exploring wines up to 1000 euros per bottle. This expanded price range aims to cater to the average consumer while also providing options for wine enthusiasts willing to invest more. 

We are embarking on an analysis of data obtained from wine testers who have assessed wines from various regions worldwide. Our goal is to investigate whether the geographic location has an impact on wine popularity and score and what are the locations that worth pursuing based on their production quality.

We are also interested in exploring opportunities within the budget-friendly market segment while maintaining a focus on quality. Assessing the feasibility of offering affordable yet high-quality options is crucial, as we aim to cater to the average consumer and ensure a diverse range of choices.


I start by creating the table which I will use about my analysis. [View Query](Queries/Query_1_Create_table.txt)


![table_creation](https://github.com/st9ho3/Project_Enoteca/assets/148724871/5635fb47-fff7-455e-8617-847acb06718f)

## Data Cleaning and View Creation

To establish a preliminary understanding of the wine data, I will begin by cleaning out any null values in key columns. Specifically, I will exclude null values in the key columns such as `country`, `description`, `points`, `price`, `province`, `title`, `variety`, and `winery`. The `region_1` and `region_2` columns will not undergo this cleaning process, as I can rely on the `province` and `country` columns to provide a general idea about the location.

Additionally, I will temporarily exclude certain columns, such as reviewer-related columns, as I aim to obtain an initial overview of the wines only. These changes will be saved in a view, which I will subsequently use to focus and analyze the wine data further. [View query](Queries/Query_2_View_creation.txt)

![View_creation](https://github.com/st9ho3/Project_Enoteca/assets/148724871/df55a5c9-eefe-4c60-8b7a-3ff48045112f)

As we proceed, my exploration of the data will focus on the geographic aspect. I aim to identify the top-performing countries in terms of both wine production volume and quality. This entails examining the largest wine producers and assessing the proportion of high-quality and well-acclaimed wines they contribute to the total production percentage.

## Defining "high" quality
Before delving further, let's establish the criteria for defining `good` quality. This clarification will guide our analysis and ensure a consistent and meaningful assessment of wine quality in the subsequent exploration of the data. [View query](Queries/Query_3.txt)

![max_min_median_score_values](https://github.com/st9ho3/Project_Enoteca/assets/148724871/05f8e339-2238-47ee-813b-664e76bb2285)

For the purpose of our analysis, we will define a "good" wine as having a rating greater than **88**, while an "excellent" wine will be considered to have a rating exceeding **95**. These thresholds will serve as our benchmarks for evaluating and categorizing wine quality.

## Exploring Wine Production and Quality Across Countries and Provinces: Insights into Volume, Excellence, and Regional Dynamics

Next, I aim to determine the overall wine production for each country and assess the respective proportions of good and excellent wines based on that total. [View query](Queries/Query_4.txt)
![good_wines_table_countries](https://github.com/st9ho3/Project_Enoteca/assets/148724871/34b2757a-402e-427c-8808-f91ec30c1f41)

The results indeed present an intriguing picture. In terms of production volume, USA, France, and Italy emerge as the frontrunners, leading the pack. Following closely are Spain, Portugal, Chile, and Argentina, while Austria, Australia, and Germany round out the list as significant producers, albeit towards the lower end.

![wine_market_share](https://github.com/st9ho3/Project_Enoteca/assets/148724871/82e3a12f-018e-4782-9b7e-7474a032f697)

![good_percentage_new](https://github.com/st9ho3/Project_Enoteca/assets/148724871/0c2e69d4-fa86-4f9f-9fc8-437e042e150a)

The notable trend here is the consistent quality performance of the top three countries, even with their substantial production volumes. The USA stands out by surpassing France in terms of producing excellent wines within this price range.

![excellent_percentage_new](https://github.com/st9ho3/Project_Enoteca/assets/148724871/a3f59b92-996b-481b-bd6f-404e0b7f2601)

Additionally, Austria, despite its lower production volume, impressively generates four times more excellent wines than the other two countries in this category. Furthermore, Portugal exhibits a remarkable achievement, producing twice as many excellent wines as Spain. These observations highlight the potential for quality excellence in regions with varying and lower production volumes.

### Running the same query for provinces provides additional interesting insights. [View here](Queries/Query_4b.txt)

![good_wines_table_province](https://github.com/st9ho3/Project_Enoteca/assets/148724871/48068c54-0b5b-4356-a5de-465dba4db5c8)

![province_wine_market_share](https://github.com/st9ho3/Project_Enoteca/assets/148724871/6d81a3e4-fb5c-479c-b30e-64c0c8d382e0)

California emerges as a significant wine producer with both high volume and consistently decent quality. Washington and Oregon, forming part of the US trio, showcase the potential to contend with Italian and French regions for the title of producing good-quality wines.


![good_wines_province](https://github.com/st9ho3/Project_Enoteca/assets/148724871/f04220a2-8ffe-49db-9d3f-e85a853493e8)

However, when it comes to excellence, Piedmont and Alsace stand out as outliers. Despite other regions' notable production volumes, these two provinces distinguish themselves by consistently producing wines of exceptional quality. This further emphasizes the nuanced dynamics within different wine-producing regions.



![excellent_percentage_province](https://github.com/st9ho3/Project_Enoteca/assets/148724871/4e38e439-7dc7-48dc-b2ea-87771428fa6e)

## "Discovering Hidden Gems: Analyzing Wineries Worldwide for Affordable Excellence"

 In the next step,I will try to find cheap excellent wines all over the world. I guess it's worth check. [View Query](Queries/Query_5.txt)



![no_excellent_wines](https://github.com/st9ho3/Project_Enoteca/assets/148724871/b43fe502-157e-4735-98d8-14e758662d3f)

It's very interresting but on this price range you can't find an excelent wine all over the world. So I will narrow my anticipation and filtering more in order to analyze wineries in the previously selected countries based on their wine cost and winery score (points). The focus is on identifying wineries that offer competitive pricing while maintaining the highest possible quality within that price range. [View query](Queries/Query_6.txt)


![winery_price_distribution](https://github.com/st9ho3/Project_Enoteca/assets/148724871/7d3ddd6b-db03-4e42-92fd-4966badec9f4)

In terms of wineries, we aim to select a representative sample from each country, acknowledging the vast multitude available. This selection allows us to gain insights into their performance and assess whether they align with their respective country's trends. An intriguing observation emerges—price and score do not consistently follow each other. This discrepancy motivates us to delve deeper, as it suggests the presence of hidden gems that offer exceptional quality at affordable prices. Our exploration goes beyond the obvious, seeking out these treasures and unveiling the nuances that make each winery unique.


![wineries_score_pricing](https://github.com/st9ho3/Project_Enoteca/assets/148724871/436d426c-97f0-472e-9be3-ddc2c18d6277)
