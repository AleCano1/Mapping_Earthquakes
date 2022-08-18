# Mapping_Earthquakes

## Overview of Project 
### Purpose
The purpose of this project is to visually show the differences between the magnitudes of earthquakes all over the world for the last seven days.

### Tools and Tecnologies
* GeoJSON earthquake data from the USGS website
* JavaScript and the D3.js library
* Leaflet library 
* Mapbox map
* API request

## Create a Map 

For each map we create the html file, there were prepared the page adding an Leaflet CSS and a Leaflet Javascript sections. The Leaflet CSS and JavaScript files we added to the index.html file are referred to as content delivery networks (CDNs). Also we added the next code:
    
    <!-- The div that holds our map -->
    <div id="mapid"></div>
 
 The div element, was added with the id tag for the map. Also, we added a css file to set the style for our map on our index.html page. Then, we need to ask to the html page to read the css file, so we add a link script. 
 Also, we created a two javascript files, one for the API key and one for configure the map, is this last file we created the map object and the tile layer Then we add our 'graymap' tile layer to the map. 
 
 The structure of the folder for eah map is:
 
 <img width="211" alt="structure" src="https://user-images.githubusercontent.com/96165500/185016412-88e99017-fce5-4140-987f-568f6fcf9ce1.png">
 
 Other option is using a GeoJSON data, JavaScript Object Notation(JSON), specially to host graphical information, for this project is reprsented by a geometry object, features object, or collection of features like the next code, is a features object that has a geometry object.
 
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
* **1.- Simple Map**  

The first map object, was a simple map, created with a zoom and center level.

    let map = L.map('mapid').setView([40.7, -94.5], 4);

In this case, the map's style is mapbox/streets-v11, and the result was:

<img width="401" alt="simple_map" src="https://user-images.githubusercontent.com/96165500/185008392-774ae8ba-0924-4b19-be47-14bbd5db86e2.png">

* **2.-Map a single Point** 
The second map object, was a map witha single point created with a zoom and center level but also, add a circle marker to the map.

        //  Add a marker to the map for Los Angeles, California.
        L.circleMarker([34.0522, -118.2437], {
           radius: 300,
           color: 'black',
           fillColor: '#fffa1'
        }).addTo(map);

In this case, the map's style is mapbox/dark-v10, and the result was:

<img width="551" alt="single_point" src="https://user-images.githubusercontent.com/96165500/185013992-a218d3d5-797d-4a58-92b3-a5424ddffa90.png">

* **3.-Map with multiple Points** 

In this map, we added a javascript file called cities.js and we add an array of cities, this is part of the code:

        // An array containing each city's location, state, and population.
        let cities = [{
         location: [40.7128, -74.0059],
         city: "New York City",
         state: "NY",
         population: 8398748
         },

then, we replace the marker variable(which we use d to map one location) with the cities variable, for used the reference of five most populous cities array. Next, we need to iterate through each city object and add each city location to the marker() function, which will, in turn, be added to the map. Then, we added each city's location to the map by adding the location to the marker() function. To add data from each object in the cities array, we'll use Leaflet's bindPopup() method on the marker() function. and format the population with a thousands separator by using the toLocaleString() method on the city.population in the bindPopup() method, like this:

        // Get data from cities.js
        let cityData = cities;

        // Loop through the cities array and create one marker for each city.
        cityData.forEach(function(city) {
           console.log(city)
           L.circleMarker(city.location,{
                radius: city.population/100000,
                color: 'orange',
                lineweight: 4
           })
           .bindPopup("<h2>" + city.city + ", " + city.state + "</h2> <hr> <h3>Population " + city.population.toLocaleString() + "</h3>")
           .addTo(map);
        });
        
  As before, the map's style is mapbox/dark-v10, and the result was:
  
  <img width="524" alt="multiple points" src="https://user-images.githubusercontent.com/96165500/185016119-840dc5ed-2dc3-4df7-ad98-15d36f71eb87.png">
  
* **4.-Map Lines** 
For map Line, we created a code with the coordinates for each point to be used in the polyline.

        // Coordinates for each point to be used in the line.
        let line = [
            [37.6213, -122.3790],
            [30.1974292,-97.6663058],
            [43.681727, -79.612049]
        ];
In this case, we used the style mapbox/satellite-streets-v11, the result is:

<img width="829" alt="map lines" src="https://user-images.githubusercontent.com/96165500/185264410-f1048e20-4524-4efb-95ea-2ee9e057665e.png">

* **5.-Mapping GeoJSON Points** 

In this map we choose the style mapbox/navigation-night-v1:

<img width="557" alt="Los Angeles" src="https://user-images.githubusercontent.com/96165500/185266526-776c1abd-d9d1-4ed3-a08b-55a268bcb300.png">

* **5.-Mapping GeoJSON Multiple Points** 

For this map we added a part of code that the user can choose between two tile layer, one was the background of the ma and the other is the option of the map.
And then create a base layer to hold both maps.

// Create a base layer that holds both maps.
let baseMaps = {
  Street: streets,
  Dark: dark
};

For the backgrpund of the map we used mapbox/streets-v11/ that is the "street" variable and mapbox/dark-v10/ is the option "dark", the map are these:


The same map but with dark option:

## Summary

### Links
For more information of USGS website, visit: 
