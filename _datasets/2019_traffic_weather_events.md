---
title: "LSTW: Large-Scale Traffic and Weather Events Dataset"
collection: datastes
permalink: /datasets/lstw
redirect_from: /datasets/2019_traffic_weather_events
excerpt: This dataset contains country-wide traffic and weather events, which are continuously being collected for the United States from August 2016. Examples of a traffic event are *accident*, *congestion*, and *construction*. Examples of a weather event are *rain*, *snow*, and *storm*. Currently, there are about __37 million__ instances of traffic and weather events in this dataset. 
date: 2021-01-01
---
## Description 
LSTW is a large-scale, country-wide dataset for transportation and traffic research, which contains traffic and weather event data for the United States. In terms of traffic, we have several types of events including accident, congestion, construction, etc. In terms of weather events, we have several types including rain, snow, storm, cold weather event, etc. This dataset is _continuously_ being collected from August 2016, and today it contains about __37 million__ traffic and weather events. Please read below descriptions for further details on this dataset. 

![](/files/BayArea.gif)
*Frequency distribution of traffic events in Bay Area from August 2016 to June 2019 using Kepler.gl*

## Acknowledgment
Please cite the following paper if you use this dataset:

* Moosavi, Sobhan, Mohammad Hossein Samavatian, Arnab Nandi, Srinivasan Parthasarathy, and Rajiv Ramnath. ["Short and Long-term Pattern Discovery Over Large-Scale Geo-Spatiotemporal Data."](https://dl.acm.org/citation.cfm?id=3330755) In proceedings of the 25th ACM SIGKDD International Conference on Knowledge Discovery & Data Mining, ACM, 2019. 

## Usage Policy and Legal Disclaimer
This dataset is being distributed only for __Research__ purposes, under [Creative Commons Attribution-Noncommercial-ShareAlike license (CC BY-NC-SA 4.0)](https://creativecommons.org/licenses/by-nc-sa/4.0/){:target="_blank"}. By clicking on the download buttons below, you are agreeing to use this data only for non-commercial, research, or academic applications. You may cite the above paper if you use this dataset. 


## Download (Version 5, Jan 2021)
<!-- * __Version 1 (Aug 2018):__ In this version, we provide data which is collected from August 2016 to August 2018 for the [Contiguous United States](https://en.wikipedia.org/wiki/Contiguous_United_States){:target="_blank"}. In this set, we have about 13.2 million traffic and 2.3 million weather event records. Download data from [here](https://osu.box.com/v/lstw-traffic-weather){:target="_blank"}. -->

<!--* __Version 2 (June 2019):__ In this version, we provide data which is collected from August 2016 to the end of June 2019 for the [Contiguous United States](https://en.wikipedia.org/wiki/Contiguous_United_States){:target="_blank"}. In this set, we have about 21.3 million traffic and 3.8 million weather event records. Download data from [here](https://osu.app.box.com/v/lstw-traffic-weather-v2){:target="_blank"}. -->

In this version, we provide data which is collected from August 2016 to the end of Dec 2020 for the [Contiguous United States](https://en.wikipedia.org/wiki/Contiguous_United_States){:target="_blank"}. This dataset includes about __31.4 million__ traffic and __5.6 million__ weather events. 

* Download __Traffic__ data from [here](https://drive.google.com/file/d/1IOTGHBPt-0cI8KgHYlwHT62OeAPKpOBc){:target="_blank"}.
* Download __Weather__ data from [here](https://drive.google.com/file/d/1WPWSW0yY5SLzmAYZeey4kA4iwY8Zwcce){:target="_blank"}.
 

<!-- Note that the data format is changed from version 1 to version 2 (some fields are added). -->
The next version will be available by December 2021. 


## Traffic Events
Traffic event is a spatiotemporal entity, where such an entity is associated with location and time. Following is the description of available traffic event types:

* __Accident__: Refers to traffic accident which can involve one or more vehicles.
* __Broken-Vehicle__: Refers to the situation when there is one (or more) disabled vehicle(s) in a road.
* __Congestion__: Refers to the situation when the speed of traffic is lower than the expected speed.
* __Construction__: Refers to an on-going construction, maintenance, or re-paring project in a road.
* __Event__: Refers to the situations such as *sport event*, *concert*, and *demonstration*.
* __Lane-Blocked__: Refers to the cases when we have blocked lane(s) due to traffic or weather condition.
* __Flow-Incident__: Refers to all other types of traffic events. Examples are *broken traffic light* and *animal in the road*.

The traffic data is provided in terms of a __CSV file__ with the following attributes: 

| \# | Attribute | Description | Nullable |
|:-:|:---------:|-------------|:--------:|
| 1 | EventId | This is the identifier of a record | No |
| 2 | Type | The type of an event; examples are *accident* and *congestion*. | No |
| 3 | Severity | The severity is a value between 0 and 4, where 0 indicates the least impact on traffic (i.e., short delay as a result of the event) and 4 indicates a significant impact on traffic (i.e., long delay). | No |
| 4 | TMC | Each traffic event has a [Traffic Message Channel (TMC)](https://wiki.openstreetmap.org/wiki/TMC/Event_Code_List){:target="_blank"} code which provides a more detailed description on type of the event. | No |
| 5 | Description | The natural language description of an event. | No |
| 6 | StartTime (UTC) | The start time of an event in UTC time zone. | No |
| 7 | EndTime (UTC) | The end time of an event in UTC time zone. | No |
| 8 | TimeZone | The US-based timezone based on the location of an event (eastern, central, mountain, and pacific). | No |
| 9 | LocationLat | The latitude in GPS coordinate. | Yes |
| 10 | LocationLng | The longitude in GPS coordinate. | Yes |
| 11 | Distance (mi) | The length of the road extent affected by the event. | Yes |
| 12 | AirportCode | The closest airport station to the location of a traffic event. | Yes |
| 13 | Number | The street number in address record. | Yes |
| 14 | Street | The street name in address record.  | Yes |
| 15 | Side | The relative side of a street (R/L) in address record. | Yes |
| 16 | City | The city in address record. | Yes |
| 17 | County | The county in address record. | Yes |
| 18 | State | The state in address record. | Yes |
| 19 | ZipCode | The zipcode in address record. | Yes |



## Weather Events
Weather event is a spatiotemporal entity, where such an entity is associated with location and time. Following is the description of available weather event types: 

* __Severe-Cold__: The case of having extremely low temperature, with temperature below *-23.7* degrees of Celsius. 
* __Fog__: The case where there is low visibility condition as a result of *fog* or *haze*. 
* __Hail__: The case of having solid precipitation including *ice pellets* and *hail*.
* __Rain__: The case of having rain, ranging from light to heavy. 
* __Snow__: The case of having snow, ranging from light to heavy. 
* __Storm__: The extremely windy condition, where the wind speed is at least *60 km/h*. 
* __Other Precipitation__: Any other type of precipitation which cannot be assigned to previously described event types.

Visit [our paper](https://arxiv.org/abs/1902.06792){:target="_blank"} to learn how we determine type and severity of weather events. 

The weather data is provided in terms of a __CSV file__ with the following attributes: 

| \# | Attribute | Description | Nullable |
|:-:|:---------:|-------------|:--------:|
| 1 | EventId | This is the identifier of a record | No |
| 2 | Type | The type of an event; examples are *rain* and *snow*. | No |
| 3 | Severity | The severity of an event, wherever applicable. | Yes |
| 4 | StartTime (UTC) | The start time of an event in UTC time zone. | No |
| 5 | EndTime (UTC) | The end time of an event in UTC time zone. | No |
| 6 | TimeZone | The US-based timezone based on the location of an event (eastern, central, mountain, and pacific). | No |
| 7 | LocationLat | The latitude in GPS coordinate. | Yes |
| 8 | LocationLng | The longitude in GPS coordinate. | Yes |
| 9 | AirportCode | The airport station that a weather event is reported from. | Yes |
| 10 | City | The city in address record. | Yes |
| 11 | County | The county in address record. | Yes |
| 12 | State | The state in address record. | Yes |
| 13 | ZipCode | The zipcode in address record. | Yes |

## Coverage
The data coverage is country-wide. It currently contains data for the [Contiguous United States](https://en.wikipedia.org/wiki/Contiguous_United_States){:target="_blank"}. Following diagram shows the current frequency distribution of __traffic__ events across 50 difference states in US. 

__Note__: For the following states, we have no traffic data from August 2016 to August 2017: AL, AR, AZ, CO, ID, KS, KY, LA, ME, MN, MS, MT, NC, ND, NH, NM, NV, OK, OR, SD, TN, UT, VT, WI, and WY. 

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~sobhan.mehr84/19.embed" height="525" width="100%"></iframe>


The next diagram shows the current frequency distribution of __weather__ events for the same set of states. 

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~sobhan.mehr84/6.embed" height="525" width="100%"></iframe>

Following diagram shows the current distribution of different __traffic__ event types: 

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~sobhan.mehr84/12.embed" height="525" width="100%"></iframe>


Similarly, current distribution of __weather__ event types is shown in below diagram: 

<iframe id="igraph" scrolling="no" style="border:none;" seamless="seamless" src="https://plotly.com/~sobhan.mehr84/17.embed" height="525" width="100%"></iframe>


## Applications of Dataset
This dataset can be used for plenty of purposes such as traffic analysis and prediction, impact prediction, accident prediction, routing engine optimization, travel time estimation, and many other research applications. 

<br><br>
<p style="color:transparent;"> <a href='https://www.stat-counter.org/'>Page Visits</a> <script type='text/javascript' src='https://www.freevisitorcounters.com/auth.php?id=cb0c83df897583dfb6d8272b30d1adf869fb7ecd'></script>
<script type="text/javascript" src="https://www.freevisitorcounters.com/en/home/counter/487718/t/5"></script> </p>
