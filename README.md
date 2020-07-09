# Geospatial features for Germany

This repository contains outlines for German counties and states in both TopoJSON and GeoJSON format. The id for the respective objects corresponds to the Community Identification Number ([Amtlicher Gemeindeschlüssel](https://de.wikipedia.org/wiki/Amtlicher_Gemeindeschl%C3%BCssel), AGS).

## TopoJSON
The TopoJSON file of Germany contains its states, counties, important places and furthermore the districts of Berlin in separate objects. Forked from [AliceWi/TopoJSON-Germany](https://github.com/AliceWi/TopoJSON-Germany).

The original shape files are from [the GADM database](https://www.gadm.org). The districts of Berlin are drawn by [AliceWi](https://github.com/AliceWi).

### counties (Landkreise) and Berlin
* id: five digit Community Identification Number (AGS)
* properties: 
    * name
    * state 
    * kfz (=license tag)
    * districtType: 
        * Landkreis (=rural district)
        * Kreis (=rural district), only in Schleswig-Holstein and Nordrhein-Westfalen 
        * kreisfreie Stadt (=urban district)
        * Stadtkreis (=urban district), only in Baden-Württemberg    
        
Note: In the counties the Bodensee is not included.

### states (Bundesländer)
* id: first two digits of the Community Identification Number (AGS)
* properties: 
    * name
    * nameEN (=english name, is null if there is none)
    * short (=abbreviation)
    
### places
* id: name
* properties: 
    * name
    * nameEN (=english name, is null if there is none)
    * state
  
## GeoJSON
The GeoJSON files are derived from the original TopoJSON and converted using [Mapshaper](http://mapshaper.org/) by Matthew Bloch. The files and properties correspond to the list above.

## Alternatives
The repository [deutschlandGeoJSON](https://github.com/isellsoap/deutschlandGeoJSON) contains GeoJSON outlines for German states and districts as well. It offers a choice of different levels of detail but lacks Community Identification Number (AGS) labels.

