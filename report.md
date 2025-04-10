## Introduction

We chose Olympic and global GDP datasets to analyse the history of people and countries who have achieved highly in worldwide sports and compare this with GDP. We aimed to uncover trends between the economies of different countries and their impact on success in sports. The first dataset our project uses is `olympics.csv`, downloaded from TidyTuesdays but was scraped and wrangled from [www.sports-reference.com](http://www.sports-reference.com) in May 2018 (Harmon, 2024). The dataset contains 15 columns and 271,116 rows detailing athlete data and medal results from summer and winter Olympic events from Athens 1896 to Rio 2016. The column names include athlete ID number, sex (M/F), age, height (cm), weight (kg), team, National Olympic Committee (three-letter code for the country), games (Olympic game athlete competed in), year (of Olympic game), season (summer/winter), city (Olympic host city), sport, event (specific sports event), and medals (gold, silver or bronze if achieved). Overall, the dataset was detailed and comprehensive, but it required cleaning to remove duplicate rows and non-medallists, conversion of team names (e.g. United States, United States-1, and United States-3 all converted to United States), and host cities mapped to host countries.

The second dataset used is `Countries GDP 1960-2020.csv`, which is obtained from the World Bank national accounts and OECD National Accounts data files. It contains 120 rows and 63 columns, detailing country/region names, country codes (3 letter code), and Gross Domestic Product (GDP) data for every year from 1960 until 2016 (60-year period). Gross Domestic Product (GDP) represents the total value added by all resident producers in an economy, measured at purchaser’s prices. It is calculated as the sum of gross value added by all producers, including product taxes while subtracting any products subsidies. 

## Question 1: What are the medal-winning trends of selected countries across different Olympic Games?
## Introduction:
The Olympic Games globally allows athletes and countries to demonstrate and celebrate their athletic success and engage an excited global audience. Understanding the trends in medal-winning achievements offers valuable insights into a country's focus on sports, investment in athlete training, and potential physiological or demographic advantages. With Question 1, we aim to explore how selected countries have performed across different Olympic Games by analysing their medal counts over the years. This analysis will not distinguish between Summer and Winter Olympics but will instead focus on overall performance trends.
To answer this question, focused on the following columns from the olympics.csv dataset: ['name', 'sex', 'height', 'weight', 'team', 'medal', 'year', 'city', 'games', 'country']. These attributes help track the number and type of medals won by athletes from selected countries over time, identify the top-performing athletes from each nation, and determine how consistent a country's performance has been. This exploration identifies high and low-performing nations and investigates the fluctuations in performance across different Olympic events. These insights could be valuable for sports analysts aiming to assess national athletic development, historians studying geopolitical influences on sports, and policymakers seeking to improve or benchmark national performance in international competitions.

## Approach:

This question was answered by being broken down into four graphs. The first is a stacked bar chart where you can select the countries where you want to see the total number of Olympic medals they have won and order the chart in either ascending or descending order. Hovering over parts of the stacked barplot breaks the data down further e.g. hovering over the yellow section will show the country’s sum of gold medals. Additionally, the stacked bar plot can be ordered in either ascending or descending order depending on the user’s viewing preference.

The user will then click on the medals from one country they want to investigate further. A stacked barplot was chosen for this Olympics data visualisation because it effectively displays the total number of medals won by each country and the breakdown by medal type (gold, silver, and bronze) in a single intuitive view. A line plot would not be effective here because it is more useful for showing trends over time rather than categorical comparisons. Similarly, a boxplot highlights data spread like medians and outliers, which is not the focus of this visualisation. The goal here is to compare quantities and compositions of medals across countries, which the stacked barplot does clearly and efficiently.

## upload image 

The second graph is a line plot that uses this input to show the total medals won by that one country over the Summer and Winter Olympics from 1960-2016. By hovering over one of the dots, the user can see further details including the Olympic game edition, the number of medals won during that game, the host country, and city. The country Romania was selected for the following example of graph 2. The user will then click on one Olympic game for that country (Romania in this example) where they would like to investigate the medal winners further. A line plot was the type of graph chosen because it effectively visualises trends and patterns in continuous data. It helps us see the rises and falls of Romania’s performance in the Olympics, helping identify long-term performance trends including peaks and declines.

## upload image 

By using the same country from graphs 1 and 2, and selecting a specific Olympic Games edition in graph 2, a third graph is generated in the application. This third graph highlights the top individual medal winners (up to 10 athletes) from that country during the selected Olympics. The example below shows the top 10 medal winners from Romania in the 1980 Summer Olympics. A stacked barplot is used to represent the number and types of medals (gold, silver, and bronze) each athlete won. The bars are organised by medal type and quantity, making it easy to compare the performance results of different athletes. This plot provides a more detailed and athlete-focused perspective on a country’s success, extending upon the medal trends shown in the earlier graphs. A stacked barplot was chosen because one chart visualises medals by type (gold, silver, bronze) for each athlete, making it easy to compare how many medals each athlete won and what kinds of medals they earned. Other charts, like a scatterplot or boxplot, would not suitably show this information because they will not effectively show totals and comparisons, they are better for quantitative analysis.

## upload image 

Additionally, a table was made listing all the athletes that won medals from the specific country and Olympic games to show the user more information. This table displays each athlete’s name, the number of each medal type won, and the total medal count for that Olympic game. It allows users to explore the data further which is not displayed in the barplot and the tabular format offers a precise, text-based summary, instead of a visual summary.

## upload image

## Analysis (plots are shown in Approach section): 
Here is a copy of the code used for the graphs within the app. Data cleaning code is included within project 1-q1-final.ipynb. 

## upload code images




