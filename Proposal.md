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

### Provenance: 
- The dataset is obtained from World Bank national accounts and OECD National Accounts data files.

### Dimensions:
- 63 columns
- 120 rows

### Description: 
- The dataset contains country/region names, country codes (3 letter code) and Gross Domestic Product (GDP) data for every year from 1960 until 2020 (60-year period) - equalling 63 columns.
- Gross Domestic Product (GDP) represents the total value added by all resident producers in an economy, measured at purchaser’s prices. It is calculated as the sum of gross value added by all producers, including product taxes, while subtracting any subsidies on products. 
- Depreciation (consumption of fixed capital) and transport charges are not considered in GDP calculations.
- It uses annual gross domestic income for that year in USD that were converted from domestic currencies using single year official exchange rates, or an alternative conversion factor if required.

# Reason for Choosing the Datasets
The Olympics is very fun to watch and brings the whole world together through our shared love for sport and competition. We thought it would be interesting to analyse the history of people and countries who have achieve highly in worldwide sports, and compare this with GDP. This will help us uncover trends between datasets and the different column variables in the olympics.csv.

# Questions to be answered
**I.** How have the average age, height, and weight of Olympic athletes changed over the years across different sports or by gender?
- **Primary Variables (dependent variables):**
	- `age`: Numeric (age of athletes)
	- `height`: Numeric (height of athletes)
	- `weight`: Numeric (weight of athletes)
        
-   **Grouping Variables (independent variables):**
    -   `year`: Numeric (Olympic year, useful for analyzing trends over time
    -   `sport`: Categorical (different sports categories to examine specific trends)
    -   `sex`: Categorical (gender-based comparisons: Male vs. Female athletes)
        
-   **Additional (contextual) Variables:**
    -   `season`: Categorical (Summer/Winter), useful for distinguishing trends between seasonal Olympics if needed.
 
-  **Planned Analysis Steps:**
	1. Data Cleaning:
    
	    -   Handle missing values in `age`, `height`, and `weight`.
        
	    -   Ensure consistency and accuracy of data.
        
	2.  **Aggregation:**
    
	    -   Calculate average age, height, and weight by `year`.
        
	    -   Further segmentation by `sport` and/or `sex`.
        
	3.  **Trend Analysis:**
	    -   Visualize and interpret changes across years.
	    
**II.** How has hosting the Olympics affected the host country's GDP?
-  **Datasets Involved:**

	-   **Olympics dataset:** contains details about Olympic host cities and years (`year`, `city`, `team`, `noc`).
    
	-   **GDP dataset:** provides GDP data for various countries from 1960 to 2020.
    

-  **Variables to Use:**

	- **Olympics dataset:**

		-   `year`: Year when the Olympics were held.
    
		-   `city`: Host city of the Olympics.
    
		-   `team` and `noc`: Information to identify the host country.
    

	- **GDP dataset:**

		-   `Country Name` and `Country Code`: Identifies the country.
    
		-   Annual GDP data (columns 1960–2020): GDP figures corresponding to Olympic event years and surrounding years.

- **Planned Analysis Steps:**

	1.  **Data Preparation:**
	    - Map Olympic host cities from the Olympics dataset to corresponding countries (`noc` or `team`) clearly.
	    -   Restructure the GDP dataset from wide to long format, with columns for `Country Name`, `Year`, and `GDP`.
        
	2.  **Data Merging:**
    
	    -   Merge Olympic hosting data with GDP data based on year and country to identify host countries' GDP around hosting years.
        
	3.  **Impact Assessment:**
    
	    -   Extract GDP data for host countries several years before and after hosting.
        
	    -   Analyze changes in GDP (growth rates or absolute changes) relative to the Olympic hosting year.
        
	4.  **Comparative Analysis:**
    
	    -   Compare GDP growth of Olympic host countries to similar countries that did not host in those years.
 
	5.  **Visualization & Interpretation:**
    
	    -   Create visualizations (e.g., line plots, bar charts) to illustrate GDP trends around Olympic events clearly.

## References  

Christy, R. (2022, April 8). *Countries GDP 1960-2020*. Kaggle. [https://www.kaggle.com/datasets/rinichristy/countries-gdp-19602020](https://www.kaggle.com/datasets/rinichristy/countries-gdp-19602020)  

Griffin, R. (2018, June 15). *120 years of Olympic history: athletes and results*. Kaggle. [https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results/](https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results/)  

Harmon, J. (2021, July 27). *TidyTuesday Olympic Dataset (2021)*. GitHub. [https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-07-27/readme.md](https://github.com/rfordatascience/tidytuesday/blob/main/data/2021/2021-07-27/readme.md)  

Harmon, J. (2024, August 6). *Olympics Athletes and Medals (2024)*. GitHub. [https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-08-06/readme.md#olympicscsv](https://github.com/rfordatascience/tidytuesday/blob/main/data/2024/2024-08-06/readme.md#olympicscsv)  

