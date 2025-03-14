# Mini Data Visualization Project
This project explores and visualizes data using various Python libraries, such as pandas, seaborn, and matplotlib. Additionally, it includes regression and correlation analysis to uncover patterns and relationships in the Olympics dataset.

## Project Goals 
This mini project/assignment aims to provide insights through data visualization and statistical analysis. Key visualizations help uncover trends, correlations, and outliers, while regression models are used to predict and analyze potential outcomes regarding how various factors can affect a country’s total medal tally and an individual athlete’s performance at the Olympics.

## Data Cleaning & Transformation
Using plots, to determine the range of years to be used for analysis & visualizations:

![plot of missing data](https://raw.githubusercontent.com/splatpugs/ntu-dsai-past/refs/heads/main/Pictures/plot1.png)
 
For example, based on the plot, I conducted the analysis from 1960 onwards, due to data for height, weight and age missing from the dataset < 1960. I consider this as “bad data points”. During the data cleaning process, I also identified that the **NOC (National Olympic Committee)** tags for some athletes were still inaccurate. Specifically, **Singapore** was not correctly associated with its respective region.

## Steps to Resolve (Data Cleaning)
1. **Import the `noc_regions.csv` Dataset**:
   - The **`noc_regions.csv`** dataset contains the correct NOC tags and corresponding country names.
     
2. **Merge Datasets**:
   - Performed a merge between the athlete dataset and **`noc_regions.csv`** to verify and update the NOC tags.
   - After merging, the data was re-examined to confirm the accuracy of the NOC tags for all athletes.
   - This step ensures that the correct **NOC** was associated with its respective **country/region**, resolving issues such as the incorrect association of countries.

3. **Fill Missing Height & Weight Values**:
   - This step is crucial since our analysis involves factors such as height and weight.
   - This can be done using **.mean()**

## Additional Datasets
To further enhance the analysis, additional datasets were incorporated:

1. **Import World GDP Dataset**:
   - Brought in the global GDP dataset for countries from 1961 onwards.

2. **Import World Population Dataset**:
   - Added the world population dataset, also starting from 1961.

3. **Merge Datasets**:
   - Merged the **athlete dataset**, **GDP dataset**, and **population dataset** to create a unified dataset.
   - This allowed for further analysis, including economic and demographic factors alongside Olympic data.

 For more information, it can be found in:
 * [Olympic Athletes 1](https://github.com/splatpugs/ntu-dsai-past/blob/main/Olympic%20Athletes%201.ipynb)
 * [Olympic Athletes 2](https://github.com/splatpugs/ntu-dsai-past/blob/main/Olympic%20Athletes%202.ipynb)

## Data Visualisations
In notebook 3, I did some analyses on various topics regarding Olympic medal counts, such as:

1. **Total Medals Won By Country (1960 - 2018)**  
   ![Total Medals by Country](https://raw.githubusercontent.com/splatpugs/ntu-dsai-past/refs/heads/main/Pictures/medalsforeachcountry.png)
   
3. **Total Medals Won Other Countries VS Singapore**  
   A focused analysis of the Olympic medals won by other countries against Singapore & some additional context.  
   ![Singapore Medals](https://raw.githubusercontent.com/splatpugs/ntu-dsai-past/refs/heads/main/Pictures/bubbleplotformedals.png)
   
4. **Predicting Total Medals**  
   Using regression analysis to predict a country's total medals can win based on historical data and identify other influencing factors.  
   ![Regression Analysis](https://raw.githubusercontent.com/splatpugs/ntu-dsai-past/refs/heads/main/Pictures/regressionanalysis.png)
   
5. **Exploring Other Possible Factors**  
   Investigating other factors that may influence medal counts, such as GDP, population, etc.
   ![GDPvMedal](https://raw.githubusercontent.com/splatpugs/ntu-dsai-past/refs/heads/main/Pictures/gdpvmedalcorrelation.png)

### Quick Findings:

* Top 3 countries are: USA, Russia & Germany
* Interestingly, from 1960, Russia was leading up till 1968, when the USA overtook.
* From 1972 onwards, Germany overlooked both countries until 1976 and 1980, but it was eventually overtaken by the USA in 1984. 
* For the rest of the years, the USA tends to remain on top compared to other countries at the Olympics.
* **Wealthier Nations**: The regression shows wealthier countries = better competency across events/athletic performance.
* **Population Impact**: Population when considering factors such as **home team advantage (host country)** affects athletes performance too.

For more findings, refer to [Olympic Athletes 3 - Medal Counts](https://github.com/splatpugs/ntu-dsai-past/blob/main/Olympic%20Athletes%203%20-%20Medal%20Counts.ipynb)

## Summary Of Key Findings on Olympics Success Factors (1960 to 2016)

Olympic success appears to correlate with national economic performance. However, this correlation is limited, as the first regression model indicates. A larger pool of athletes (or contenders) is crucial for increasing the chances of winning medals. Countries like **China** and the **U.S.A.**, with their larger populations, exemplify this advantage.

## What About Singapore?
In section 2 of Data Visualisations, I also side-tracked a little bit to understand more about Singapore's performance @ Olympics till 2016:

**Country Wise Analysis: Singapore**

| Metric                              | Value                                      |
|-------------------------------------|--------------------------------------------|
| **Olympics Appearances**            | 13                                         |
| **Total Participants**              | 97                                         |
| **Female Participants**             | 41 (42.27%)                               |
| **Male Participants**               | 56 (57.73%)                               |
| **Total Medals**                    | 5 (medals include every individual medal in team sport) |
| **Gold Medals**                     | 1                                          |
| **Silver Medals**                   | 2                                          |
| **Bronze Medals**                   | 2                                          |
| **Popular Sports**                  | Table Tennis, Swimming, Weightlifting     |
| **Most Medals (Athlete)**           | Feng Tian Wei (Sport - Table Tennis)     |
| **Gold Medalists**                  | Joseph Isaac Schooling - Swimming Men's 100 metres Butterfly |

Singapore has actively participated in the Summer Olympic Games since 1948, continuing its presence after gaining complete independence from Malaysia in 1965, despite the sizeable Olympic boycott in 1980. 

In total, Singapore has won 5 Olympic medals:
- The first medal, a silver, was secured by **Tan Howe Liang** in lightweight weightlifting at the **1960 Summer Games**.
- Subsequent medals included the second at the **2008 Summer Games** and two more at the **2012 Summer Games**.
- The nation's first gold medal was achieved by **Joseph Schooling** in the men's 100-metre butterfly at the **2016 Summer Olympics**.

## Implications for Singapore?

**Limited Athlete Pool**:
- Given Singapore's smaller population, the pool of athletes is limited, which may impact the overall medal tally.
  
**Need for Strategic Development**:
- To enhance Olympic performance, Singapore may benefit from strategies that focus on identifying and developing talent across a broader range of sports.

##### This project was done around July 2018 as part of an interest in learning Python & data viz.
##### Last Updated: Thursday, 26th September 2024
