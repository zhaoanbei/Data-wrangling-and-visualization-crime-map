# Data-wrangling-and-visualization-crime-map

The final map is consisted of two submaps: the map of rape frequency for each street and the map of non-rape streets (Safe streets) of Philadelphia. Through those two maps, I want to inform audience: 1st, in which areas should we have more police force and 2nd, which areas are safer for females.
![alt text](https://github.com/zhaoanbei/Data-wrangling-and-visualization-crime-map/blob/master/StreetMap.jpg)
Fig.1 Street Map of Rape in Philadelphia in Ten Years

To create the map, firstly I filtered data which has “Rape” for Text_General_Code. The count of rape affairs in Philadelphia ten is around 10200. Then I projected those data on map and noticed that all data fell into Philadelphia boundary so I skipped spatial filter step.
Then I used CREATE INDEX query to create index for all datasets. Thirdly, I used DISTINCT ON/ST_Distance/ORDER function to link every crime to its nearest street and set 1000 as the distance range to reduce computations. Then I used COUNT/GROUP BY to calculate the crime count for each street. 

From these two maps, we notice that: the unsafe areas cluster in University City and middle north Philadelphia, but most dangerous streets scatter in those areas. This indicates that University City and middle north Philadelphia are more dangerous than other areas, and that we need to increase police force in the whole region to make improvement.
