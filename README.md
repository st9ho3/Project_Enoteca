# Project_Enoteca

In this fictional scenario, a French wine shop owner, planning to expand his well-established retail store, seeks insights to determine whether it's beneficial to diversify the wine selection beyond France. Specifically, he is interested in identifying potential countries to source wines from. In light of the expansion, he is open to exploring wines up to 1000 euros per bottle. This expanded price range aims to cater to the average consumer while also providing options for wine enthusiasts willing to invest more. 

We are embarking on an analysis of data obtained from wine testers who have assessed wines from various regions worldwide. Our goal is to investigate whether the geographic location has an impact on wine popularity and score and what are the locations that worth pursuing based on their production quality.

We are also interested in exploring opportunities within the budget-friendly market segment while maintaining a focus on quality. Assessing the feasibility of offering affordable yet high-quality options is crucial, as we aim to cater to the average consumer and ensure a diverse range of choices.


I start by creating the table which I will use about my analysis. [View Query](Queries/Query_1_Create_table.txt)


![table_creation](https://github.com/st9ho3/Project_Enoteca/assets/148724871/5635fb47-fff7-455e-8617-847acb06718f)

## Data Cleaning and View Creation

To establish a preliminary understanding of the wine data, I will begin by cleaning out any null values in key columns. Specifically, I will exclude null values in the key columns such as `country`, `description`, `points`, `price`, `province`, `title`, `variety`, and `winery`. The `region_1` and `region_2` columns will not undergo this cleaning process, as I can rely on the `province` and `country` columns to provide a general idea about the location.

Additionally, I will temporarily exclude certain columns, such as reviewer-related columns, as I aim to obtain an initial overview of the wines only. These changes will be saved in a view, which I will subsequently use to focus and analyze the wine data further.



