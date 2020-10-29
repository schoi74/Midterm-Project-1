# Midterm-Project-1

## Background

## Business Question

## Data Analysis

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
 
## Summary

