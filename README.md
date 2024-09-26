# Mini Data Visualization Project
This project explores and visualizes data using various Python libraries, such as pandas, seaborn, and matplotlib. Additionally, it includes regression and correlation analysis to uncover patterns and relationships in the Olympics dataset.

## Project Goals 
This mini project/assignment aims to provide insights through data visualization and statistical analysis. Key visualizations help uncover trends, correlations, and outliers, while regression models are used to predict and analyze potential outcomes regarding how various factors can affect a country’s total medal tally and an individual athlete’s performance at the Olympics.

## Data Cleaning & Transformation
Using plots, to determine the range of years to be used for analysis & visualizations:

![plot of missing data](https://raw.githubusercontent.com/splatpugs/ntu-dsai-past/refs/heads/main/Pictures/plot1.png)
 
For example, based on the plot, I conducted the analysis from 1960 onwards, due to data for height, weight and age missing from the dataset < 1960. I consider this as “bad data points”.

During the data cleaning process, I also identified that the **NOC (National Olympic Committee)** tags for some athletes were still inaccurate. Specifically, **Singapore** was not correctly associated with its respective region.

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

## Summary of Findings

##### Last Updated: Thursday, 26th September 2024
