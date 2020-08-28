---
title: "Covid-19 Dashboard"
date: 2020-08-20
tags: [data analytics, data science, data visualization] 
excerpt: "It is a Dashboard that visualizes and helps to analyze the covid situation in India. Trends for virus affected cases 
are traced right from its first case on 30th January, 2020 till date. Data is updated daily and the trends are 
visualized accordingly"
mathjax: "true"
---

*[Github code](https://github.com/koshalnirwan/covid_dashboard)*

*[Covid Dashboard for India App](https://covid--dashboard-india.herokuapp.com/)*

It is a Dashboard that visualizes and helps to analyze the covid situation in India. Trends for virus affected cases 
are traced right from its first case on 30th January, 2020 till date. Data is updated daily and the trends are 
visualized accordingly. Data can be analysed and visualized statewise also. 

### Dashboard trace down -
1. Total Cases
2. Recovered Cases
3. Deaths 
4. Active Cases
5. Total Tests

Data is fetched as a json file using an api from official Indian Goverment Health Department website. Data is fetched, 
cleaned and prepared for the visualization. This is the only time consuming part in whole project.

```
resp = requests.get('https://api.covid19india.org/v4/timeseries.json')
df = pd.DataFrame(resp.json())
```

### Stacked bar chart showing covid timeline 

![](https://koshalnirwan.github.io/koshal07/images/covid/bar.JPG)

<img src="https://koshalnirwan.github.io/koshal07/images/covid/bar.JPG" width="500" height="300" />

### Confirmed cases chart for selected States

<img src="https://koshalnirwan.github.io/koshal07/images/covid/confirm.JPG" width=500 height=300>

### Total Tests graph for selected States

<img src="https://koshalnirwan.github.io/koshal07/images/covid/test.JPG" width=500 height=300>
