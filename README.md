# COVID-19-Data-Animated-Visualization

Goal: Visualize COVID-19 cases on a map of the United States over time. I worked on this on April when my school decided to transition to online school. By then, I saw the impact of COVID-19 around the world, and realized how big of an impact it was going to be in the US. So I wanted to see if I could visualize the impact (through number of cases over time) on a map. I created one map based on number of cases in a day by state and another animated map of number of cases over time based on county.

## Data Collection

I gathered my data from [New York Times' covid-19-data repository](https://github.com/nytimes/covid-19-data). It provided series of data files with cumulative counts of coronavirus cases in the United States, at the **state and county level** -- which would work well for me as I wanted to know the number of cases based on **location**. I also found data that gives the geocode location of counties on the map.

## Process

### Number of cases in a day by state
Using R's ggmap and maps packages, I got info about each state's position on a map and I joined that data with my state level data. With that, I plotted a geom_polygon map with ggplot and specified a specific date to see the number of cases on that day.

![map_bystate](https://github.com/justinezth/COVID-19-Data-Animated-Visualization/blob/master/map_bystate.png)

### Number of cases over time by county
Using the geocode location of counties and the county level COVID data, I joined them together and plotted them on a map with scatterplot dots. Then I used gganimate in order to show the animation of cases over time.

![map_animation](https://github.com/justinezth/COVID-19-Data-Animated-Visualization/blob/master/map_animation.gif)
