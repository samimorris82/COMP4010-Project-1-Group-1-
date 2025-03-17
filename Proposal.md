# Dataset Description
## Brief Context
##sami is writing this now
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
    

