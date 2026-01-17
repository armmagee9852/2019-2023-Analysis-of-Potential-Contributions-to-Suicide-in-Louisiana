# Overview
A detailed project going over four socioeconomic factors, ranking their correlations to suicide in Louisiana over the years 2018 to 2023. Project goes over factors such as graduation rates, poverty rates, traced firearms, and child abuse as a proxy for firearm accessibility.
# Limitations
Before going into the documentation. It is crucial to first look into the limitations of the analysis to account restraints to depth.
Limitations included:
- **Suppression**
  - In the original data gathering process, data was omitting beyond a value of < 10 in order to protect the identities of individual listed. Because of this, smaller minority groups in certain parishes could not be gathered, reducing integrity of data, especially for the aforementioned minority groups. As an alternative, the original question was changed to include the entire populations of Louisiana regardless of parish. While this leads to less suppression and more available data, individual research deeper into parish-level data is still worthwhile.

- **Size of Data**
    - With a sample size < 30, there is not enough data to conduct predictive analysis. Because of this, data is strictly and only meant to be understood from the perspective of an exploratory analysis of these factors over the specified year range.

- **Analyzed Factors**
  - While there are plentiful other factors to be taken into regard, this analysis is only for these three factors and to see how strongly they correlate with suicide rates. For example, additional factors worth considering are:
    1. **Mental Health Provider Availability**
    2. **Substance Abuse Rates**
    3. **Rural/Urban Areas (Data probably less likely to show due to suppression)**

# Suicide Analysis
For a descriptive analysis of these rates, we will look at the standardized rates among age demographics and the age-specific rate by race.
<br/>
<img width="2216" height="1041" alt="Age-Specific Suicide Rates From 2019-2023, 10 Years Age" src="https://github.com/user-attachments/assets/30702eef-2984-4c87-9a3b-e736ce42bc1a"/>
<br/>
**Observations**
<br/>
Here are the age-specific suicide rates by age demographics, sourced through the CDC WONDER. This data was found by dividing the cumulative deaths per demograpgic by their cumulative population, then multiplied by 100,000 for standardization. The reason age-specific rates are used is to standardize the rates by demographic in disregard for bigger or smaller populations. Due to the age range of 5-14 years having suppressed data that is too low & unreliable for observation, it has been omitted from the visualization, but is not to be deemed as inappropriate for the overall observation and still holds significance. Ages 45 - 54 lead the demographic as the highest, with an annual average rate of **22.4%**. 35-44 leads next with an annual rate of **20.9%**. The 25-34 year age demographic leads next with a rate of **19.4%** and the 85+ demographic being just .1 lower at **19.3%**. 55-64 Year olds follow after with a rate of **18.6%**, 75-84 Year olds come in at **17.3%** and finally, both 65-74 year old and 15-24 year olds sharing the same rate of 14.6%

# Factor 1: Poverty
Collection of poverty data was done through the United States Census Bureau, using Microsoft Excel for aggregation via Pivot Tables & Visualization.  

<img width="449" height="391" alt="Age Adjust Suicide   Poverty Rate Graphs" src="https://github.com/user-attachments/assets/0f98e957-1638-48ff-879b-9dcdb79c2bc7"/><br/><br/>
**Observations**
<br/>
Here, you can see both the poverty rates and age adjusted suicide rates per 100k. Here, the age adjusted rates are used to avoid any issues that may be due to age makeup, and standardizes the rates if all ages consisted of the same makeup instead. One notable pattern that will come up often is the "drop" present during 2020, which was during the peak of the COVID outbreak. Afterwards, the trends steadily rise back up. During these rises, there is an increase from up to **8%**, with the suicide rates being highest towards the end of the year. Overall, from the lowest to highest rate, there was an increase to **13.14%** from 2020 to 2023. As for the poverty rate, the trends follow a similar pattern to the suicide rates, with decrease in 2020 back towards a steady rise, fall, and rise again towards the later years. In 2021, poverty was at its highest, with a **9.55%** increase from its lowest in 2020.
<br/>
<br/>
**Correlation Between these Factors**
<br/>
<img width="384" height="223" alt="Suicide   Poverty Correlation" src="https://github.com/user-attachments/assets/f4a3a548-0449-4e1a-b723-b086bd11fd15" />
<br/>
By running a correlation between poverty rates (independent variable) and suicide rates (dependent variable) using the `=CORR` function in Excel & charting options, we can see that we have an r-squared of ~35% and an r of 59%, suggesting a moderately strong positive correlation between the two variables. As for interpretation, this means that in areas where poverty is higher, suicide rates tend to be higher aswell. With our r-squared of ~35%, it means that ~35% of the changes in the poverty rates fits with the changes in the suicide rates with the other 65% not being explained by our model.
<br/>
<br/>

