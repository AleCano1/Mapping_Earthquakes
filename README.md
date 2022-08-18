# Mapping_Earthquakes

Disaster Reporting Network is a nonprofit company that provides data driven storytelling on disasters around the world.

## Overview of Project 
### Purpose

The purpose of this project is to visualize on a map the differences between the magnitudes of earthquakes all over the world for the last seven days, with two different maps and the earthquake overlay. And then, the visualization of earthquake data in relation to the tectonic plates’ location on the earth, and an additional map that shows the earthquakes with a magnitude greater than 4.5.


### Tools and Tecnologies
* GeoJSON earthquake data from the USGS website
* JavaScript and the D3.js library
* Leaflet library 
* Mapbox map
* API request

## Create a Map 

For a simple map was used the next, files and folders structure:

 <img width="211" alt="structure" src="https://user-images.githubusercontent.com/96165500/185016412-88e99017-fce5-4140-987f-568f6fcf9ce1.png">
 
 Also, there were used GeoJSON data, JavaScript Object Notation(JSON), especially to host graphical information, by a geometry object, features object, or collection of features. For example, the next code is a feature object that has a geometry object.
 
        // Add GeoJSON data.
        let sanFranAirport =
        {"type":"FeatureCollection","features":[{
            "type":"Feature",
            "properties":{
                "id":"3469",
                "name":"San Francisco International Airport",
                "city":"San Francisco",
                "country":"United States",
                "faa":"SFO",
                "icao":"KSFO",
                "alt":"13",
                "tz-offset":"-8",
                "dst":"A",
                "tz":"America/Los_Angeles"},
                "geometry":{
                    "type":"Point",
                    "coordinates":[-122.375,37.61899948120117]}}
        ]};
        
  

## Results 

During the project there were some maps with different styles and parameters, in this case, a **Simple Map** and the map's style is Mapbox/streets-v11, and the result was:


<img width="401" alt="simple_map" src="https://user-images.githubusercontent.com/96165500/185008392-774ae8ba-0924-4b19-be47-14bbd5db86e2.png">


In this **Map with multiple Points**, we added a javascript file called cities.js and we add an array of cities, there were used Leaflet's bindPopup() method on the marker() function, and format the population with a thousand separator by using the toLocaleString() method on the city.population in the bindPopup() method, there were used another style named mapbox/dark-v10 and we got this:
        
  
  <img width="524" alt="multiple points" src="https://user-images.githubusercontent.com/96165500/185016119-840dc5ed-2dc3-4df7-ad98-15d36f71eb87.png">
  
Another option used was **Map Lines** using a code with coordinates for each point in the polyline. In this case, there was used the style mapbox/satellite-streets-v11, and the result was:

<img width="829" alt="map lines" src="https://user-images.githubusercontent.com/96165500/185264410-f1048e20-4524-4efb-95ea-2ee9e057665e.png">

For a **Mapping GeoJSON Points** we collect the coordinates of the airport of San Francisco and used the style mapbox/navigation-night-v1, we got this:

<img width="557" alt="Los Angeles" src="https://user-images.githubusercontent.com/96165500/185266526-776c1abd-d9d1-4ed3-a08b-55a268bcb300.png">

After some maps, there was created a map that shows the differences in magnitudes of earthquakes all over the world for the last seven days, and got the next result:

<img width="612" alt="sevendays" src="https://user-images.githubusercontent.com/96165500/185297842-1b9b5331-7754-40ce-8c3e-db814d7f11ad.png">

The result is in real-time, so the result will change eventually. In the image with can see that the map shows that in México there was an earthquake with a 5.2 magnitude, shown in a red circle, which means a dangerous magnitude. 

In another part of the world in China, there was an Earthquake of 5.5 Magnitude, which is shown in a big circle and in the color red.

<img width="717" alt="last" src="https://user-images.githubusercontent.com/96165500/185297851-713fb37b-9bcf-4ec4-8ae9-8afeee941126.png">

This last map is the most complete map, where we can observe Tectonic plate data visually in a map with multiple lines, and added circle markers based on the magnitude of the earthquake, and as we can see there are not only two options of style maps, there are three options (Streets, Satellite and Navigation Night). In this map with can choose to visualize the Earthquakes, the Tectonic Plates, the Major Earthquakes, only two options or all.

## Summary

As we can see it is a long way to visualize the geographic information and customize the maps, so it depends on what the particular need of the client is, in this project, I started with a simple map and ended with a more complete map that shows different seismic points. Companies can use it to predict future disasters. The Disaster Reporting Network team will have complete information in real-time to upload the data and visualize the changes or simulations that each part of the world has. In the Asian continent, we can observe more orange and red points than in America so it means the zone is more seismic.

### Links
For more information about Earthquakes, visit of USGS website: https://earthquake.usgs.gov/
