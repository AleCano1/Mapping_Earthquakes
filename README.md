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

## Explore Data
First, for each map we create the html file, there were prepared the page adding an Leaflet CSS and a LEaflet Javascript sections. The Leaflet CSS and JavaScript files we added to the index.html file are referred to as content delivery networks (CDNs). Also we added the next code,
    
    <!-- The div that holds our map -->
    <div id="mapid"></div>
 
 The div element, was added with the id tag for the map. Next, we added a css file to set the style for our map on our index.html page. Finally, for this first part, we need to ask to the html page to read the css file, so we add a link script. 
 Also, we created a two javascript files, one for the API key and one for configure the map, is this last file we created the map object and the tile layer Then we add our 'graymap' tile layer to the map. 


## Results 
* **1.- Simple Map **  

The first map object, was a simple map, created with a zoom and center level.

    let map = L.map('mapid').setView([40.7, -94.5], 4);

In this case, the map's style is mapbox/streets-v11, and the result was:

<img width="401" alt="simple_map" src="https://user-images.githubusercontent.com/96165500/185008392-774ae8ba-0924-4b19-be47-14bbd5db86e2.png">

* 2.- ** Map a single Point**  

## Summary

### Links
For more information of USGS website, visit: 
