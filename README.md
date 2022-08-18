# Mapping_Earthquakes

## Overview of Project 
### Purpose

The purpose of this project is to visualize on a map the differences between the magnitudes of earthquakes all over the world for the last seven days, with two different maps and the earthquake overlay. Also, the visualization of earthquake data in relation to the tectonic plates’ location on the earth, and shows all the earthquakes with a magnitude greater than 4.5 on the map, on a third map. 


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

During the project there were done some maps with diferent style and parameters, in this case, is a **Simple Map** and the map's style is mapbox/streets-v11, and the result was:


<img width="401" alt="simple_map" src="https://user-images.githubusercontent.com/96165500/185008392-774ae8ba-0924-4b19-be47-14bbd5db86e2.png">


In this **Map with multiple Points** , we added a javascript file called cities.js and we add an array of cities, there were used Leaflet's bindPopup() method on the marker() function, and format the population with a thousands separator by using the toLocaleString() method on the city.population in the bindPopup() method, use another style named mapbox/dark-v10 and we got this:
        
  
  <img width="524" alt="multiple points" src="https://user-images.githubusercontent.com/96165500/185016119-840dc5ed-2dc3-4df7-ad98-15d36f71eb87.png">
  
Another option were used is **Map Lines** using a code with coordinates for each point in the polyline. In this case, there were used the style mapbox/satellite-streets-v11, the result was:

<img width="829" alt="map lines" src="https://user-images.githubusercontent.com/96165500/185264410-f1048e20-4524-4efb-95ea-2ee9e057665e.png">

For a **Mapping GeoJSON Points** we collect the coordinates of the airport of San Francisco and used the style mapbox/navigation-night-v1, we got this:

<img width="557" alt="Los Angeles" src="https://user-images.githubusercontent.com/96165500/185266526-776c1abd-d9d1-4ed3-a08b-55a268bcb300.png">

After some maps, we got the map that shows the differences between the magnitudes of earthquakes all over the world for the last seven days, having the next result:



## Summary

As we can see is a long way to visualizte the geographical information and customize the maps, so it depends what are particullary the client need, in this project I strated with a simple map and finished with a more complete map that shows different eartquake points that the companies can use to predict future disasters. 

### Links
For more information of USGS website, visit: 
