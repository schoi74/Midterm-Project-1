# How counties are grouped based on health, socioeconomic, and COVID-19 metrics

## Background

Meredith Cohn, Nathan Ruiz, and Pamela Wood published an [article](https://www.baltimoresun.com/coronavirus/bs-md-coronavirus-race-data-20200409-ffim7y4bljcz3hjk4dmt773mp4-story.html) in _The Baltimore Sun_ in April 2020 about how the rate of COVID-19 infections of the Black population in Maryland "is higher...than whites or other groups, according to the new Maryland Department of Health data," where 49.4% of those infected were black, 36.9% were white, and 13.7% were Asian or another race. As public health, now more than ever, is a pressing issue and given our being in the midst of a COVID-19 pandemic, we wondered: How do existing (and perhaps underlying) health factors and socioeconomic conditions affect (if at all) COVID-19 infection and death rates? Can we identify any common relationships (or at least correlations) between them? 

If any relationships can be identified, this has implications for ways to not only tackle the COVID-19 pandemic but also to potentially reduce the negative implications for pandemics that may arise in the future. While it is extremely important to tackle the current COVID-19 crisis and flatten the curve, we must also address issues that may exacerbate the consequences of a pandemic or any general financial or public health crisis: issues like income inequality, poverty rates, and morbidity/mortality rates. Analysis of public health data can inform future public health research, politics and laws and government initiatives to improve existing disparities, efforts to improve communities, and more. 

## Business Question

How are counties in the state of Maryland grouped based on different health and socioeconomic metrics? Furthermore, how does COVID-19 data relate to existing health/socioeconomic data? 

## Data Analysis

We used data from the [Maryland Open Data Portal](https://opendata.maryland.gov/), the Johns Hopkins Center for a Livable Future’s [Maryland Food System Map](https://mdfoodsystemmap.org/), and the Johns Hopkins University’s Center for Systems Science and Engineering (CSSE) [daily reports of COVID-19 data](https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data) as of October  24th, 2020 (2 recent weeks average). For the Maryland Open Data Portal, we used data about [socioeconomic characteristics](https://opendata.maryland.gov/Demographic/Maryland-Counties-Socioeconomic-Characteristics/is7h-kp6x) and [demographics](https://opendata.maryland.gov/Demographic/Choose-Maryland-Compare-Counties-Demographics/pa7d-u6hs) across counties in Maryland. For the Maryland Food System Map, we used 2018 data regarding the [obesity prevalence rate](https://data-clf.hub.arcgis.com/datasets/35ba641edca9421da541242e66ec288e_476), the [diabetes prevalence rate](https://data-clf.hub.arcgis.com/datasets/a1faf09747be4911b20838c639341480_475), the [diabetes mortality rate](https://data-clf.hub.arcgis.com/datasets/dd16ad94a1b344b090868e0181c99674_479), and the [overall mortality rate](https://data-clf.hub.arcgis.com/datasets/75684f521c374e408d2dc082a41cafc0_477). The map of counties in Maryland is from [worldatlas.com](https://www.worldatlas.com/webimage/countrys/namerica/usstates/counties/mdcountymap.htm).
	
We first grouped the data into three categories: health data, socioeconomic/demographic data, and COVID-19 data. We then conducted a cluster analysis for each group to see what clusters (by county in MD) existed; that was then used to create one cluster map (color-coded by anchor) per data group. We also looked at correlation rates between all variables across the three data groups. Finally, we looked at which counties were sorted into which clusters and interpreted what that meant for each county across the three data sets. 
	
We decided to focus mainly on the percents and rates where possible, as absolute values of numbers are difficult to compare across groups (ex: a mortality rate of 1000 people has a different effect on a county with a total population of 10,000 vs a county with a total population of 100,000). 

It is important to note that the health data are from 2018 and the socioeconomic data are from 2019, but our COVID-19 data are from 2020. We conducted this analysis thinking about how the COVID-19 data relates to the health and socioeconomic data sets as if all data were for 2020.

## Data Answer

### How are counties grouped in Maryland based on different health metrics?

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/health_cluster.png)

__Cluster 1__ is an average health cluster of _slightly greater_ overall mortality rate, _slightly less than one standard deviation greater_ diabetes mortality rate, _slightly less than average_ diabetes prevalence rate, and _less than average_ obesity prevalence rate.

__Cluster 2__ is a more unhealthy cluster of _one standard deviation greater_ overall mortality rate, _slight more than one standard deviation less than average_ diabetes mortality rate, _slightly less than one standard deviation greater_ diabetes prevalence rate, and _slightly less than one standard deviation greater_ obesity prevalence rate.

__Cluster 3__ is a very healthy cluster of _one and a half standard deviations less than average_ overall mortality rate, _slightly more than one standard deviation less than average_ diabetes mortalityr rate,  _slightly less than  one standard deviation less than average_ diabetes prevalence rate, and _less than average_ obesity prevalence rate.
    
![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/health_min_dist2.png)

Here, we see that the sum of the mininum distance squared is 48.138. For 24 counties, the average comes out to be about 2 units of mininum distance squared per county. This is not the strongest correlation of each county in their corresponding anchor groups, but it is a fair number to assume that these counties are grouped fairly.

The counties are distributed more heavily in anchor 1 and even spread out between anchors 2 and 3.

- Anchor 1: 12 counties (Baltimore County)

- Anchor 2: 6 counties (Caroline)

- Anchor 3: 6 counties (Talbot)

![alt_text](https://github.com/schoi74/how-counties-are-grouped-based-on-health-socioeconomic-and-COVID-19-metrics/blob/main/counties_health%20clusters.jpg)

This map shows how the counties are clustered (by color). 

### How are counties grouped in Maryland based on different socioeconomic characteristics?

![alt_text](https://github.com/schoi74/how-counties-are-grouped-based-on-health-socioeconomic-and-COVID-19-metrics/blob/main/socioeconomic_clusters.jpg)

__Cluster 1__ is an affluent cluster with an average population size, an above average income level, and a below average rate of poverty and unemploymenat.

__Cluster 2__ is a highly-populated but "average" cluster. It has an above average population size, average income level, and a slightly below average rate of poverty and unemployment.

__Cluster 3__ is a lower-income cluster with a below average population size, below average income level, and an above average rate of poverty and unemployment.

Below, we can see that Cluster 1 and 3 have a higher concentration of counties in their respective clusters, and Cluster 2 does not feature as many counties. 

![alt_text](https://github.com/schoi74/how-counties-are-grouped-based-on-health-socioeconomic-and-COVID-19-metrics/blob/main/counties_socio-demo%20clusters.jpg) 

This map shows how the counties are clustered (by color) for the socioeconomic data.

### How are counties grouped based on different COVID-19 variables?

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/covid_cluster.png)

__Cluster 1__ is a cluster that has a low COVID-19 presence. It has _less than average_ confirmed cases, _less than average_ deaths, _less than average_ active cases, _less than average_ incidence rate, and _less than average_ case-fatality ratio.

__Cluster 2__ is a cluster with a high COVID-19 presence. It has _about one and a half standard deviations greater_ confirmed cases, _slightly less than two standard deviations greater_ deaths, _about one and a half standard deviations greater_  active cases, _slightly less than one standard deviation greater_ incidence rate, and _slightly greater_ case-fatality ratio.

__Cluster 3__ is a cluster with a low COVID-19 presence, but a high case-fatality ratio. It has _less than average_ confirmed cases, _slightly less than average_ deaths, _less than average_ active cases, _slightly less than one standard deviation greater_ incidence rate, and _two standard deviations greater_ case-fatality ratio.
    
![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/covid_min_dist2.png)

Here, we see that the sum of the minimum distance squared is about 34.44. For 24 counties, the average comes out to be about 1.435 units of mininum distance squared per county. This is a stronger correlation than that of the health cluster analysis.

The counties are distributed heavily in anchor 1 and evenly distributed in anchors 2 and 3.

- Anchor 1: 16 counties (Washington)

- Anchor 2: 4 counties (Baltimore County)

- Anchor 3: 4 counties (Carroll)

![alt_text](https://github.com/schoi74/how-counties-are-grouped-based-on-health-socioeconomic-and-COVID-19-metrics/blob/main/counties_covid-19%20clusters.jpg)

This map shows the clusters for the COVID-19 data.

It is interesting to note that the three data sets all have different anchors and clusters, and not all counties were sorted into the same cluster for each cluster analysis.

### How are these three different clusters related to each other?

![alt_text](https://github.com/schoi74/how-counties-are-grouped-based-on-health-socioeconomic-and-COVID-19-metrics/blob/main/visualization_clusters.jpg)

This visually represents the clusters for all three data sets. 

The health data is generally split beween an average health cluster, a cluster with higher morbidity/mortality rates, and a cluster with low morbidity/mortality rates. 

The socioceconomic data is clustered as follows: One cluster is affluent, one cluster is lower-income, and one cluster is average for income but has a high population size. 

The COVID-19 data is generally split as having one cluster with a low presence of COVID-19 (healthy), a cluster, with a high COVID-19 presence, and a cluster with low COVID-19 presence but a high case-to-fatality ratio.

![alt_text](https://github.com/schoi74/Midterm-Project-1/blob/main/master_cluster.png)

Here, the numbers are color coded comparing all the possible cluster groups. The code 111 means that these counties were in cluster 1 for health, socioeconomic, and COVID-19 clusters respectively. 

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
        
- Cluster 322: healthy area, large population, high COVID prevalence
        i. Montgomery County
        
- Cluster 331: healthy area, high poverty/unemployment, low COVID presence
        i. Garrett County
	
It is interesting to note cluster 131 and 231, which are clusters that have more risk factors for COVID-19 and for health issues. However, they have a low COVID-19 presence. Our data at hand does not explain why this cluster came to be, but further analysis of more data is required. We speculate that it may be due to factors in data sets we did not explore. Perhpas the counties in this cluster are following social distancing protocols, and perhaps schools in these counties are fully online, reducing exposure to the virus? 
    
## Summary
- The three most common or prevalent clusters are Clusters 111, 231, and 311.
	
	1. Cluster 111: average mortality rate, high diabetes, affluent area, low COVID presence
		Cecil County, Charles County, Frederick County, Harford County
	2. Cluster 231: high overall mortality and morbidity prevalence, high poverty/unemployment, low COVID prevalence
		Caroline County, Dorchester County, Somerset County, Worcester County
	3. Cluster 311: healthy area, affluent area, low COVID presence
		Calvert  County, Howard County, Queen Anne's County, Talbot County

For health, even though there are 12 counties for the middle ranked cluster and 6 for each cluster with the highest and lowest overall mortality rate, there should be a distribution more heavily in the anchor 3 with _less than average_ confirmed cases, _slightly less than average_ deaths, _less than average_ active cases, _slightly less than one standard deviation greater_ incidence rate, and _two standard deviations greater_ case-fatality ratio.

Overall, Maryland has done a decent job so far dealing with the coronavirus as only 4 out of the 24 counties have higher-than-average COVID-19 presence and 16 counties are in the cluster with the lowest COVID-19 presence (cluster 1).

If bigger data sample sizes were available for all these counties with Maryland state, it would be helpful to  incorporate how these counties are grouped based on other health metrics, such as the obesity and heart disease mortality rates, the heart disease prevalence rate, etc. It would also be useful to look at other socioeconomic metrics and the clustering therein, such as vehicle availablity or accessibility to food or healthcare. The current data is limited to mortality/morbidity and to mostly income-related metrics; the demographics of a county, such as racial composition, may also provide interesting insights into the existing clusters and may also change how counties are clustered. 

Additionally, COVID-19 rates are not affected only by population sizes, income levels, poverty/unemployment rates, morbidity rates, or mortality; there may be other factors to consider, such as accessbility to healthcare, education regarding hygiene, etc. 
	
Moving forward, our data holds implications for government planning, especially to identify the counties that may require more assistance with alleviating income inequality, reducing poverty/unemployment rates, improving overall health, reducing morbidity/mortality rates, etc. This can take the form of increased funding and aid for counties that are part of a lower-income cluster, for example, or new initiatives being created to reduce morbidity rates across the state. Better health and fewer socioeconomic disparities may lead to improved quality of life, increased productivity across the board, and more. 
