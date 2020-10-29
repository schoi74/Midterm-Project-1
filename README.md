# Midterm-Project-1

## Background

Public health, now more than ever, is an issue that requires further action. In the midst of the current coronavirus pandemic, how do existing (and perhaps underlying) health factors and socioeconomic conditions affect (if at all) COVID-19 infection and death rates? Can we identify any common relationships (or at least correlations) between these three groups of data? 	If any relationships can be identified, this has implications for ways to not only tackle the COVID-19 pandemic but also to potentially reduce the negative implications for pandemics that may arise in the future. While it is extremely important to tackle the current COVID-19 crisis and flatten the curve, we must also address issues that may exacerbate the consequences of a pandemic or any general financial or public health crisis: issues like income inequality, poverty rates, and morbidity/mortality rates. Analysis of public health data can inform future public health research, politics and laws and government initiatives to improve existing disparities, efforts to improve communities, and more. 

## Business Question

How are counties in the state of Maryland grouped based on different health and socioeconomic metrics? Furthermore, how does COVID-19 data relate to existing health/socioeconomic data? 

## Data Analysis

We used data from the [Maryland Open Data Portal](https://opendata.maryland.gov/), the Johns Hopkins Center for a Livable Future’s [Maryland Food System Map](https://mdfoodsystemmap.org/), and the Johns Hopkins University’s Center for Systems Science and Engineering (CSSE) [daily reports of COVID-19 data](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data) as of October  24th, 2020. For the Maryland Open Data Portal, we used data about [socioeconomic characteristics](https://opendata.maryland.gov/Demographic/Maryland-Counties-Socioeconomic-Characteristics/is7h-kp6x) and [demographics](https://opendata.maryland.gov/Demographic/Choose-Maryland-Compare-Counties-Demographics/pa7d-u6hs) across counties in Maryland. For the Maryland Food System Map, we used 2018 data regarding the [obesity prevalence rate](https://data-clf.hub.arcgis.com/datasets/35ba641edca9421da541242e66ec288e_476), the [diabetes prevalence rate](https://data-clf.hub.arcgis.com/datasets/a1faf09747be4911b20838c639341480_475), the [diabetes mortality rate](https://data-clf.hub.arcgis.com/datasets/dd16ad94a1b344b090868e0181c99674_479), and the [overall mortality rate](https://data-clf.hub.arcgis.com/datasets/75684f521c374e408d2dc082a41cafc0_477).
	
We first grouped the data into three categories: health data, socioeconomic/demographic data, and COVID-19 data. We then conducted a cluster analysis for each group to see what clusters (by county in MD) existed; that was then used to create one cluster map (color-coded by anchor) per data group. We then looked at correlation rates between all variables across the three data groups. Finally, we looked at which counties were clustered into which anchors and interpreted what that meant for each county across the three data groups. 
	
We decided to focus mainly on the percents and rates where possible, as absolute values of numbers are difficult to compare across groups (ex: the effect that a mortality rate of 1000 people affects a county with a total population of 10,000 vs a county with a total population of 100,000 differently). 

It is important to note that the health data are from 2018 and the socioeconomic data are from 2019, but our COVID-19 data are obviously from 2020. Even though the timeline does not add up, we will conduct this analysis thinking about how the COVID-19 data relates to the health and socioeconomic datasets if they were all from the year 2020.

## Data Answer

### How are counties grouped in Maryland based on different health metrics?

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/health_cluster.png)

__Anchor 1__ is a cluster of _slightly greater_ overall mortaltity rate, _slightly less than one standard deviation greater_ diabetes mortality rate, _slightly less than average_ diabetes prevalence rate, and _less than average_ obesity prevalence rate.

__Anchor 2__ is a cluster of _one standard deviation greater_ overall mortality rate, _slight more than one standard deviation less than average_ diabetes mortality rate, _slightly less than one standard deviation greater_ diabetes prevalence rate, and _slightly less than one standard deviation greater_ obesity prevalence rate.

__Anchor 3__ is a cluster of _one and a half standard deviations less than average_ overall mortality rate, _slightly more than one standard deviation less than average_ diabetes mortalityr rate,  _slightly less than  one standard deviation less than average_ diabetes prevalence rate, and _less than average_ obesity prevalence rate.

In general, the overall health ranking is:

    1. Anchor 3
    2. Anchor 1
    3. Anchor 2
    
![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/health_min_dist2.png)

Here, we see that the sum of the mininum distance squared is 48.138. For 24 counties, the average comes out to be about 2 units of mininum distance squared per county. This is not the strongest correlation of each county in their corresponding anchor groups, but it is a fair number to assume that these counties are grouped fairly.

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/health_cluster_count.png)

Here, the counties are distributed more heavily in anchor 1 and even spread out between anchors 2 and 3.

- Anchor 1: 12 counties (Baltimore County)

- Anchor 2: 6 counties (Caroline)

- Anchor 3: 6 counties (Talbot)

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/health_list_counties.png)

### How are counties grouped based on different COVID-19 variables?

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/covid_cluster.png)

__Anchor 1__ is a cluster of _less than average_ confirmed cases, _less than average_ deaths, _less than average_ active cases, _less than average_ incidence rate, and _less than average_ case-fatality ratio.

__Anchor 2__ is a cluster of _about one and a half standard deviations greater_ confirmed cases, _slightly less than two standard deviations greater_ deaths, _about one and a half standard deviations greater_  active cases, _slightly less than one standard deviation greater_ incidence rate, and _slightly greater_ case-fatality ratio.

__Anchor 3__ is a cluster of _less than average_ confirmed cases, _slightly less than average_ deaths, _less than average_ active cases, _slightly less than one standard deviation greater_ incidence rate, and _two standard deviations greater_ case-fatality ratio.

In general, the overall COVID-19 ranking is:

    1. Anchor 1
    2. Anchor 3
    3. Anchor 2
    
![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/covid_min_dist2.png)

Here, we see that the sum of the minimum distance squared is about 34.44. For 24 counties, the average comes out to be about 1.435 units of mininum distance squared per county. This is a stronger correlation than that of the health cluster analysis.

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/covid_cluster_count.png)

Here, the counties are distributed heavily in anchor 1 and evenly distributed in anchors 2 and 3.

- Anchor 1: 16 counties (Washington)

- Anchor 2: 4 counties (Baltimore County)

- Anchor 3: 4 counties (Carroll)

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/covid_list_counties.png)

### How are these three different clusters related to each other?

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/master_cluster.png)

Here, the numbers are color coded comparing all the possible cluster groups. The code 111 means anchor 1 for health, socioeconomic, and covid clusters.

- Cluster 111: average mortality rate, high diabetes, affluent area, low COVID presence
        i. Cecil County
        ii. Charles County
        iii. Frederick County
        iv. Harford County
        
- Cluster 113: average mortality rate, high diabetes mortality, affluent area, low COVID presence but high case-fatality ratio
        i. Carroll County
        ii. St. Mary's County
        
- Cluster 121: average mortality rate, high diabetes rate, low poverty/unemployment rates, low COVID prevalence
        i. Anne Arundel County
        
- Cluster 122: average mortality rate, high diabetes mortality, large population, high COVID presence
        i. Baltimore County
        ii. Prince George's County
        
- Cluster 131: average mortality rate, high diabetes mortality rate, high poverty/unemployment, low COVID presence
        i.  Washington County
        ii. Wicomico  County
        
- Cluster 132: average mortality, high diabetes mortality, high poverty/unemployment, high COVID presence
        i. Baltimore City
        
- Cluster 231: high overall mortality and morbidity prevalence, high poverty/unemployment, low COVID prevalence
        i. Caroline County
        ii. Dorchester County
        iii. Somerset County
        iv. Worcester County
        
- Cluster 233: high mortality and morbidity, high poverty/unemployment, low COVID presence but high COVID fatality ratio
        i. Allegany County
        ii. Kent County

- Cluster 311: healthy area, affluent area, low COVID presence
        i. Calvert  County
        ii. Howard County
        iii. Queen Anne's County
        iv. Talbot County
        
- Cluster 322: healthy area, large population and average socioeconomics, high COVID prevalence
        i. Montgomery County
        
- Cluster 331: healthy area, high poverty/unemployment, low COVID presence
        i. Garrett County
    
## Summary
- The three most common or prevalent clusters are Clusters 111, 231, and 311.
	
	1. Cluster 111: average mortality rate, high diabetes, affluent area, low COVID presence
		Cecil County, Charles County, Frederick County, Harford County
	2. Cluster 231: high overall mortality and morbidity prevalence, high poverty/unemployment, low COVID prevalence
		Caroline County, Dorchester County, Somerset County, Worcester County
	3. Cluster 311: healthy area, affluent area, low COVID presence
		Calvert  County, Howard County, Queen Anne's County, Talbot County

- For health, even though there are 12 counties for the middle ranked cluster and 6 for each cluster with the highest and lowest overall mortality rate, there should be a distribution more heavily in the anchor 3 with _less than average_ confirmed cases, _slightly less than average_ deaths, _less than average_ active cases, _slightly less than one standard deviation greater_ incidence rate, and _two standard deviations greater_ case-fatality ratio.

- Overall, Maryland has done a decent job so far dealing with the coronavirus as only 4 out of the 24 counties have higher than average COVID prevalence and that 16 counties are in the lowest COVID numbered anchor (anchor 1).

- If bigger data sample sizes were available for all these counties with Maryland state, 
	
	we think it would be helpful to even incorporate how these counties are grouped based on other health metrics, such as mortality rates for obesity and 		heart diseases or heart disease mortality rate.
	
	we think it would be helpful to even incorporate how these counties are grouped based on other socioeconomic metrics, such as availability to vehicles or 	  accessibility to food or healthcare.
	
- If we were to manage the state plans to improve certain parts of the state to improve people's lives, we would either incorporate more variables to further reason why and how the counties are grouped into these clusters or delve more into the causes of overall mortality rate or the confirmed cases of COVID, for example, are higher in some regions or clusters than others and some possible resolutions to alleviate the discrepancy. Moreover, we could even look closer into each county that need improvement in health, socioeconomy, or even COVID-19 to analyze the root causes and resolve.
