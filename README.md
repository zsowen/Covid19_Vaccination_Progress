<!DOCTYPE html>
## Covid 19 World Vaccination Analysis 

## Goals

Identify what factors from the World Bank API database relate to the vaccination percentage for coutries around the world.

## Extraction
Kaggle CSV of world vaccination progress cribbed from the Our World in Data Github Repository:
https://www.kaggle.com/gpreda/covid-world-vaccination-progress

API which pulls from World Bank for Global Development Indicators:   
https://data.worldbank.org/

ISO conversion for country names:  
https://gist.github.com/tadast/8827699

All data was extracted with pandas and merged into one working frame for analysis.
## Analysis
### Best and Worst Performing Countries by vaccinated population
<img src='./Resources/Output/bestandworst/bot5%.png'></img>

<img src='./Resources/Output/bestandworst/top5%.png'></img>

### Choropleth
<img src='./Resources/Output/Choropleth_Map/Pop_density_chloropleth_map.'></img>

### World Bank Global Development Indicators by Quartile
#### GDP
<img src='./Resources/Output/Box/GDP.vaccMean.png'></img>
<img src='./Resources/Output/Line/GDP.Vaccine%.Q1Line.png'></img>
<img src='./Resources/Output/Line/GDP.Vaccine%.Q2Line.png'></img>
<img src='./Resources/Output/Line/GDP.Vaccine%.Q3Line.png'></img>
<img src='./Resources/Output/Line/GDP.Vaccine%.Q4Line.png'></img>

#### Private Health Expenditure
<img src='./Resources/Output/Box/health_exp.vaccMean.png'></img>
<img src='./Resources/Output/Line/health_exp.Vaccine%.Q1Line.png'></img>
<img src='./Resources/Output/Line/health_exp.Vaccine%.Q2Line.png'></img>
<img src='./Resources/Output/Line/health_exp.Vaccine%.Q3Line.png'></img>
<img src='./Resources/Output/Line/health_exp.Vaccine%.Q4Line.png'></img>

#### Population Density
<img src='./Resources/Output/Box/Pop_Den.vaccMean.png'></img>
<img src='./Resources/Output/Line/Pop_Den.Vaccine%.Q1Line.png'></img>
<img src='./Resources/Output/Line/Pop_Den.Vaccine%.Q2Line.png'></img>
<img src='./Resources/Output/Line/Pop_Den.Vaccine%.Q3Line.png'></img>
<img src='./Resources/Output/Line/Pop_Den.Vaccine%.Q4Line.png'></img>

#### Total Population
<img src='./Resources/Output/Box/Total_Pop.vaccMean.png'></img>
<img src='./Resources/Output/Line/Total_Pop.Vaccine%.Q1Line.png'></img>
<img src='./Resources/Output/Line/Total_Pop.Vaccine%.Q2Line.png'></img>
<img src='./Resources/Output/Line/Total_Pop.Vaccine%.Q3Line.png'></img>
<img src='./Resources/Output/Line/Total_Pop.Vaccine%.Q4Line.png'></img>

## Results
After performing ANOVA testing on each Indicator's quartile:

Level of confidence: 95%  
H<sub>0</sub>: All mean vaccination percents over quartiles are equal  
H<sub>a</sub>: There is at least one mean vaccination percent that is not equal to another

Population Density was the only indicator which rejected the null hypothesis, which would indicate that there is a statistically significant difference in quartiles with a 95% level of confidence. 

Other indicators would require more data to reach any further conclusions. 

## Potential Errors and Further Study

* More indicators can be compared, using a more robust API structure to check for multiyear data and filter for missing values.


