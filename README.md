# Overview
A detailed project going over four socioeconomic factors, ranking their correlations to suicide in Louisiana over the years 2018 to 2023. Project goes over factors such as graduation rates, poverty rates, traced firearms, and child abuse as a proxy for firearm accessibility.

# Questions
With our data, the questions we aim to answer are:
1. Out of all our factors, which ones have the strongest correlation to suicide in Louisiana?
2. Which race has the highest suicide rate?
3. Which demographics have the highest suicide rate?
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
<br/>
**Observations**
<br/>
Here are the age-specific suicide rates by age demographics, sourced through the CDC WONDER. This data was found by dividing the cumulative deaths per demograpgic by their cumulative population, then multiplied by 100,000 for standardization. The reason age-specific rates are used is to standardize the rates by demographic in disregard for bigger or smaller populations. Due to the age range of 5-14 years having suppressed data that is too low & unreliable for observation, it has been omitted from the visualization, but is not to be deemed as inappropriate for the overall observation and still holds significance. By comparing our highest and lowest demographics, there is a **staggering 53.42%** increase in mortality rates from 15-24 year olds to 45-54 years old, an immense percentage that leaves more room for research or gathered data to investigate. <br/>

**Race Demographics**
<img width="2218" height="912" alt="2019-2023 Age-Adjusted Rate By Race" src="https://github.com/user-attachments/assets/20812f78-6cf7-46a5-ae02-9bd4370bc79c"/>
<br/>
The white demographic leads with 19.6%, with the asian demographic being marginally higher at 7.8% and the black demographic being the lowest at 7.6%. Between the highest and lowest demographics here, there is a **157.89%** increase in the white demographic over the black demographic. Due to data constrictions, data for more than one race and the native american population have been omitted, but are not to be deemed insignificant.
<br/>
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
By running a correlation between poverty rates (independent variable) and suicide rates (dependent variable) using the `=CORREL` function in Excel & charting options, we can see that we have an r-squared of **~35%** and an r of **59%**, suggesting a **moderately strong** positive correlation between the two variables. As for interpretation, this means that in areas where poverty is higher, suicide rates tend to be higher aswell. With our r-squared of ~35%, it means that ~35% of the changes in the poverty rates fits with the changes in the suicide rates with the other 65% not being explained by our model.
<br/>
# Factor 2: Graduation Rates
Graduation Rates have been sourced from the National Center for Education Statistics
<img width="534" height="480" alt="Graduatation Rates" src="https://github.com/user-attachments/assets/a108de84-2321-4315-b058-36e9242a4442" />
<br/>
<br/>
**Observation**
<br>
Here, most of the results between the graduation rates and the suicide rates are the opposite; where the suicides increase, the graduation rates decrease, and vice versa. Again, 2020 is a notable year, with suicide being at its lowest rate and graduation rates being at their highest. Overall, graduation rates are high throughout these years, which over 80% of students graduating. 
<br/>
<br/>
**Correlations between variables**
<br/>
<img width="593" height="239" alt="Screenshot 2026-01-17 004136" src="https://github.com/user-attachments/assets/8cfa8d33-2608-479e-8bdf-49ad2c3a1094" />
<br/>
As seen from the scatterplot, there is a negative correlation between graduation rates and suicide, implying that areas with higher graduation rates tend to have lower suicide rates. With an r of **-35%**, this is a **weak** correlation, with only about **12%** of the changes in graduation rates fitting with the changes in our suicide rates. 
# Factor 3: Child Abuse Rates
Child Abuse Rates have been sourced from the Administration of Children and Families. It is to be noted that "child abuse" in this context is more generalized and the collective data include ages up to 18 years old, where in the United States 18 is legally considered an adult. 
<br/>
<img width="531" height="480" alt="Screenshot 2026-01-17 010440" src="https://github.com/user-attachments/assets/8063d7e0-74e1-4157-ad48-56a80f287f2e" />
<br/><br>
**Observation**
<br/>
The child abuse rates start high with 181 victims, a steady drop down to 138 in 2021, and a rise again 193. From 2018 to 2023, there was a **6.63%** increase in child abuse victims. From the lowest (2021) to the highest (2023) points, there is a **55%** difference, or a **39.86%** increase.
<br/>
<br/>
**Correlations between variables**
<br/>
<img width="532" height="239" alt="Screenshot 2026-01-17 011815" src="https://github.com/user-attachments/assets/243568a6-cacd-4cea-b9bd-71c0b450398c" />
<br/>
Here, child abuse frequency carries an r squared of ~36% with an r of 60%, indicating a fairly strong positive correlation between these two factors, and meaning that in areas where child abuse is more frequent, suicide rates are higher. With an r squared of 36%, 36% of the changes in child abuse fit the changes in suicide rate.
# Final Factor: Traced Firearms (Gun Accessibility)
Gun accessibility data sourced from the Bureau of Alcohol, Tobacco, Firearms, and Explosives. An additional note here is that while not all traced firearms are involved in suicide, traced firearms serve as a proxy for general gun accessibility, where most suicides by gun are fatal.
<img width="531" height="478" alt="Screenshot 2026-01-17 014840" src="https://github.com/user-attachments/assets/50237392-9944-47ec-a7c6-3b88455fd3ac" />
<br/>
**Observation**
<br/>
Throughout the years 2019 to 2023, traced firearms have been steadily increasing, with a low in 2019 (about 229 firearms traced) to a highest in 2022 (about 348), witnessing a **51.97%** increase from 2019. In comparison to the age adjusted rates, they share a similar pattern of rising from 2019 to 2022 (besides 2020). Another thing to note is 2023, where traced firearms dropped while suicide rates stayed fixed.
<br/>
<br/>
**Correlations between variables**
<br/>
<img width="532" height="241" alt="Screenshot 2026-01-17 014959" src="https://github.com/user-attachments/assets/2fb80b30-f6c2-454b-ab38-86dc7beb316f" />
<br>
By correlating traced firearm rates and suicide rates, we see our strongest correlation yet, a positive correlation with an r squared of about **46%** and an r of **68%**. What this is means is that in areas where firearms are more commonly traced, there are also more commonly suicides. As for our r squared of 45%, meaning almost half of the changes in the traced firearm variable fit with the changes in the suicide rate. This leaves a big room for further research, maybe to the parish or city level.
<br/>
**Ranking**
Given the shown data and correlations, the top factors with the strongest correlations to suicide are:
1. Firearm accessibility (Traced firearms)
2. Child Abuse
3. Poverty

# Conclusive Storytelling
Suicide is a deep topic that influences many families and communities around the globe. For Louisiana specifically, correlating factors such as firearm accessibility, child abuse, and poverty warrant further research in order to understand their relationship with mental health vulnerability and suicide. Through this data, it is suggested that poverty, childhood abuse, and other socioeconomic factors are associated with mental health vulnerability. Increased investigation into these factors could see a turn in the rate in the foreseeable future, as the data indicates that areas with higher economic hardship or childhood trauma are linked to mental health vulnerabilities.

# Potential Solutions
**For Poverty:**
1. Promoting higher education
2. Improved childhood nutrition

**For Firearm Accessibility**
1. Enforcing stricter gun laws
2. Background checks
3. Secure firearm storage
4. Raising minimum age & purchase

# Sources
- CDC WONDER
- United Stated Census Bureau
- County Health Rankings & Roadmaps
- National Center For Education Statistics
- United States Bureau of Alcohol, Tobacco, Firearms, and Explosives


