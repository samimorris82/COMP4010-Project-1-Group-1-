# Dataset Description
## Olympics Dataset Description
One dataset being used is the `olympics.csv`, downloaded from TidyTuesdays (Harmon, 2024). The description is as follows:

### Provenance
- The data is sourced from **120 years of Olympic history: athletes and results** on Kaggle (Griffin, 2018). Since the Olympics resurfaced in 2024, the dataset is an intentional repeat of the `olympics.csv` uploaded in 2021 (Harmon, 2021).
- This dataset was scraped and wrangled from [www.sports-reference.com](https://www.sports-reference.com) in May 2018 and includes basic athlete data and medal results from Athens 1896 to Rio 2016.

### Dimensions
- **Columns:** 15
- **Rows:** 271,116  

### Description
For each Olympic participant from 1896 until 2016, the dataset records the ID number, sex, age, height, weight, team, National Olympic Committee (NOC), games, year, season, city, sport, event, and medals (if won). It accounts for the Winter and Summer Games being held in the same year until they started being staggered from 1994.  

### **Column Descriptions:**
- `id` – Unique identifier number for each athlete.
- `name` – Full name of the athlete.
- `sex` – "M" for male, "F" for female.
- `age` – Athlete's age at the time of competition.
- `height` – Height in centimetres.
- `weight` – Weight in kilograms.
- `team` – Name of the country the athlete is representing.
- `noc` – Three-letter National Olympic Committee (NOC) code for the athlete's country.
- `games` – Specific Olympic Games the athlete participated in.
- `year` – Year of the Olympic Games the athlete participated in.
- `season` – "Summer" or "Winter" Olympics.
- `city` – The host city of the Olympics.
- `sport` – The sport the athlete competed in.
- `event` – Specific event within that sport (e.g., "Volleyball Men's Volleyball").
- `medal` – Type of medal won by the athlete (Gold, Silver, Bronze, or NaN if no medal was won).

## Countries GDP 1960-2020
The second dataset is Countries GDP 1960-2020.csv downloaded from Kaggle (Christy, 2022). The description is as follows:

### Provenance
- The dataset is obtained from World Bank national accounts and OECD National Accounts data files.

### Dimensions
- 63 columns
- 120 rows

### Description 
- The dataset contains country/region names, country codes (3 letter code) and Gross Domestic Product (GDP) data for every year from 1960 until 2016 (60-year period) - equalling 63 columns.
- Gross Domestic Product (GDP) represents the total value added by all resident producers in an economy, measured at purchaser’s prices. It is calculated as the sum of gross value added by all producers, including product taxes, while subtracting any subsidies on products. 
- Depreciation (consumption of fixed capital) and transport charges are not considered in GDP calculations.
- It uses annual gross domestic income for that year in USD that were converted from domestic currencies using single year official exchange rates, or an alternative conversion factor if required.

# Reason for Choosing the Datasets
The Olympics is very fun to watch and brings the whole world together through our shared love for sport and competition. We thought it would be interesting to analyse the history of people and countries who have achieve highly in worldwide sports, and compare this with GDP. This will help us uncover trends between datasets and the different column variables in the olympics.csv.

# Questions to be answered
## I. "What are the medal-winning trends of selected countries across different Olympic Games?" ##

## 1. Stacked Bar Chart (Graph 1): Number of Medals Won (Gold, Silver, Bronze) per Country
- **Goal**: Display the number of medals (Gold, Silver, and Bronze) won by each country.
- **x-axis**: Countries (based on the "team" column, which identifies the athlete's country).
- **y-axis**: Number of medals won by each country, with each medal type (Gold, Silver, Bronze) stacked.
- **Features**:
  - **Drop-downs**:
    - Select countries desired for display.
    - Choose ascending or descending order based on the total number of medals or any other metric.
  - **Additional Information on Hover**:
    - Displays the medal type, country, and the sum of each medal type for that country.

## 2. Line Chart (Graph 2): Medal Winning Trend per Game for a Selected Country
- **Goal**: Show the trend of medal wins for a specific country over the different Olympic Games.
- **x-axis**: Represents Olympic Games and years (could be Summer or Winter).
- **y-axis**: Displays the total number of medals won by a country selected from the bar chart in Graph 1.
- **Features**:
  - **Additional Information on Hover**:
    - Displays specific Olympic game (e.g., Summer or Winter), the year and host city, and the number of medals won by the selected country during that game.

## 3. Stacked Bar Plot (Graph 3): Top 10 Athletes for Selected Country and Game
- **Goal**: Show the top 10 athletes from a selected country, sorted by the number of medals they won in a particular Olympic game.
- **x-axis**: Athlete's name.
- **y-axis**: Number of medals each athlete won (stacked by medal type).
- **Features**:
  - **Additional Information on Hover**:
    - Displays athlete name, medal type, and the number of medals won.

	    
**II.** How has hosting the Olympics affected the host country's GDP?
-  **Datasets Involved:**

	-   **Olympics dataset:** contains details about Olympic host cities and years (`year`, `city`, `country`).
    
	-   **GDP dataset:** provides GDP data for various countries from 1960 to 2020.
    

-  **Variables to Use:**

	- **Olympics dataset:**

		-   `year`: Year when the Olympics were held.
    
		-   `city`: Host city of the Olympics, which needs to be used to create a new column for the host country  `country`
    

	- **GDP dataset:**

		-   `Country Name` and `Country Code` (if necessary): Identifies the country.
    
		-   Annual GDP data (columns 1960–2020): GDP figures corresponding to Olympic event years and surrounding years.

- **Planned Analysis Steps:**

	1.  **Data Preparation:**
	    - Map Olympic host cities from the Olympics dataset to corresponding countries (`noc` or `team`) clearly.
	    -   Restructure the GDP dataset from wide to long format, with columns for `Country Name`, `Year`, and `GDP`.
        
	2.  **Data Merging:**
    
	    -   Merge Olympic hosting data with GDP data based on year and country to identify host countries' GDP around hosting years.
        
	3.  **Impact Assessment:**
    
	    -   Extract GDP data for host countries several years before and after hosting
	    -   Analyze changes in GDP (growth rates or absolute changes) relative to the Olympic hosting year.
        
	4.  **Comparative Analysis:**
    
	    -   Compare GDP growth of Olympic host countries to similar countries that did not host in those years.
 
	5.  **Visualization & Interpretation:**
    
	    -   We intend to use an interactive world map to visualize our data
            -   For the countries available in the dataset, we will allow on-click interaction and generate the corresponding GDP line chart of that country during the 1960-2020 period.
            -   The graph will also highlight the year(s) that the country hosted an Olympics event

## References  

Christy, R. (2022, April 8). *Countries GDP 1960-2020*. Kaggle. [https://www.kaggle.com/datasets/rinichristy/countries-gdp-19602020](https://www.kaggle.com/datasets/rinichristy/countries-gdp-19602020)  

Griffin, R. (2018, June 15). *120 years of Olympic history: athletes and results*. Kaggle. [https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results/](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results/)  

Harmon, J. (2021, July 27). *TidyTuesday Olympic Dataset (2021)*. GitHub. [https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-07-27/readme.md](https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-07-27/readme.md)  

Harmon, J. (2024, August 6). *Olympics Athletes and Medals (2024)*. GitHub. [https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-08-06/readme.md#olympicscsv](https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-08-06/readme.md#olympicscsv)  

