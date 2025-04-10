# Data-analysis_Sugarcane-Production
Sugarcane Production Project - Overview

This project analyzes global sugarcane production by exploring key factors like production volume, land usage, and yield per hectare across different countries and continents. Through comprehensive Exploratory Data Analysis (EDA), we'll identify top-producing regions, understand relationships between variables, and visualize the distribution of production. The insights gained will help inform agricultural strategies and enhance resource management in the sugarcane industry.

Remove Unwanted Characters
In the dataset "List of Countries by Sugarcane Production," we clean the numerical columns by removing unwanted characters such as periods (.) and commas (,). This ensures that the data is in a proper format for numerical computations.
oActions:
Remove periods from "Production (Tons)" and "Acreage (Hectare)" columns.
Replace commas with periods in "Production per Person (Kg)" to standardize decimal notation.
Remove Unwanted Columns
The dataset contains extra columns like "Unnamed: 0" that are not necessary for the analysis. We can remove these using the drop() function:
oDrop the "Unnamed: 0" column using axis=1.
Rename Columns for Consistency
We clean up column names to remove any extra spaces or special characters for consistency.
oChange "Production (Tons)" to "Production(Tons)" (remove spaces).
oRename other columns similarly.
2. Checking Missing Values
Checking for missing values is critical, as it can impact the results of our analysis. The isna().sum() function helps identify columns with missing values.
Missing Values Output:
Country                      0
Continent                    0
Production(Tons)             0
Production_per_person(Kg)    0
Acreage(Hectare)             1
Yield(Kg/Hectare)            1
dtype: int64

Handling Missing Values:
oDrop the rows with missing values in "Acreage(Hectare)" and "Yield(Kg/Hectare)" columns.
oReset the index after dropping rows to ensure clean data.
3. Data Conversion
We convert numerical columns related to production, acreage, and yield into the appropriate data types (float) to facilitate analysis.
Univariate Analysis
In univariate analysis, we focus on understanding each variable individually. This includes examining distribution, central tendencies, and any potential outliers.
1. How Many Countries Produce Sugarcane from Each Continent?
By using the "Continent" column, we identify how many countries produce sugarcane in each continent.
Result:
Africa           38
Asia             25
North America    22
South America    11
Oceania           4
Europe            2

We can visualize this using a bar chart to highlight the geographical distribution of sugarcane production.
2. Distribution of Key Variables
We analyze the distribution of the following columns using histograms:
Production (Tons)
Production per Person (Kg)
Acreage (Hectare)
Yield (Kg/Hectare)
Using sns.distplot(), we visualize the distribution of these variables, helping us identify skewness, normality, and outliers.
Production(Tons): Skewed with a few countries (Brazil, India, China) having extremely high production.
Production per Person (Kg): Skewed with a few countries showing much higher production per person.
Acreage (Hectare): Less skewed compared to production.
Yield (Kg/Hectare): Varies by country; efficient farming shows high yield.
3. Outlier Detection with Boxplots
Boxplots help visually identify outliers in the dataset.
Key Insights from Boxplots:
oProduction(Tons): Outliers are visible, indicating countries like Brazil, India, and China contribute disproportionately.
oYield (Kg/Hectare): High-yielding countries stand out as outliers.
4. Violin Plot for Production (Tons)
A violin plot helps better understand the distribution of "Production (Tons)" and identify skewness, spread, and outliers.
Expected Insights:
oWide spread with skewness.
oA few countries with very high production values.
Bivariate Analysis
Bivariate analysis investigates relationships between two variables to identify any correlations or patterns.
1. Which Country Has the Highest Acreage (Land)?
Using a bar plot, we identify the top 15 countries with the largest sugarcane acreage, showing that Brazil, India, and China dominate the land area dedicated to sugarcane cultivation.
2. Which Country Has the Highest Yield per Hectare?
By analyzing yield per hectare, we identify Guatemala as the country with the highest yield, indicating efficient farming techniques.
3. Which Country Has the Highest Production per Person?
We use production per person (Kg) to determine that Paraguay leads in production efficiency relative to population size.
4. Correlation Analysis
We perform a correlation analysis to understand the relationships between key variables:
Production (Tons) and Acreage (Hectare): Strong positive correlation (0.997).
Production (Tons) and Yield (Kg/Hectare): Low correlation (0.132).
We visualize the correlation using a heatmap.
5. Do Countries with the Highest Land Produce More Sugarcane?
We create a scatter plot to show the relationship between Acreage (Hectare) and Production (Tons). The plot confirms that larger land areas correlate with higher production.
6. Do Countries Yield More Sugarcane per Hectare Produce More Sugarcane in Total?
Another scatter plot explores the relationship between Yield (Kg/Hectare) and Production (Tons). The plot indicates that higher yields do not always correlate with higher total production.
Continental Analysis
1. Analyzing Sugarcane Production by Continent
We group the data by continent and sum the key metrics to analyze global production trends.
Total Production by Continent:
oSouth America: Leading producer.
oAsia: Second in production.
oAfrica: Third.
We visualize this using a bar plot.
2. Does the Number of Countries in a Continent Affect Sugarcane Production?
We analyze the impact of the number of countries on sugarcane production per continent.
Key Insight:
oEven continents with fewer countries (e.g., South America) can have high total production due to a few dominant producers (e.g., Brazil).
Conclusion
This project provides a comprehensive analysis of global sugarcane production, offering insights into the distribution of production, the role of land usage, and yield efficiency across different countries and continents. By understanding these factors, agricultural strategies can be improved, and resource management in the sugarcane industry can be optimized.
