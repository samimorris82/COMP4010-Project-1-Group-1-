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
## Reason for Choosing
##sami is writing this now

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
    

