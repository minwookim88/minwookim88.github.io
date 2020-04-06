---
layout: posts
title:  "Useful Data Sources"
date:   2019-04-19 20:00:00 -0700
categories:
  - data_science
  - Tips
tags:
  - tips
  - data
---

Here is a list of public source of data that might come in handy for your own study/research.

<!---  
====================================================================================================
--->

<h4>
<i class="fa fa-database" aria-hidden="true"></i>
Census Data
<button type="button" class="collapsible" id="coll1_button" style="float:right;">Details
<i class="fa fa-arrow-down" aria-hidden="true"></i>
</button>
</h4>

<div>
<b>Demographic</b> and <b>economic data</b> from the U.S published by
<a href="https://www.census.gov/data.html"><b>Census Bureau</b></a> for public use.
</div>

<div class="content" id="coll1">
<!---
Here is a list of some useful links.
--->

<ul>
  <li>Census Bureau Data API Guide:
<a href="https://www.census.gov/data/developers/guidance/api-user-guide.Help_&_Contact_Us.html" target="_blank">Website</a>,
<a href="https://www.census.gov/content/dam/Census/data/developers/api-user-guide/api-guide.pdf" target="_blank">PDF</a>.</li>

  <li>Data List available in Census Bureau API: <a href="https://api.census.gov/data.html" target="_blank">https://api.census.gov/data.html</a></li>

  <li><b>Geographical</b> data (spatial data that encodes coordinates of the boundaries of geographic entities): <br>
<a href="https://www.census.gov/programs-surveys/geography/guidance/tiger-data-products-guide.html" target="_blank">Guide</a>,
<a href="https://www2.census.gov/geo/tiger/TIGER2019/" target="_blank">FTP Server</a>

    <ul>
        <li>List of CRS (Coordinate Reference System) : <a href="http://spatialreference.org/ref/epsg/?search=epsg+4269&srtext=Search" target="_blank">List</a></li>

<!---
@ Ellipsoid : 3D description of surface patch of Earth in real world (varies over time depending on its measurements basis, due to tectonic activity)
@ Datum : Projection function mapping from specified Ellipsoid to 2D map
@ EPSG 4269 : Ellipsoid = GRS80, Datum = NAD83

@ NAD83 : Semimajor axis = 6378137.0 meter, Inverse flattening = 298.257222101
--->


        <li>Reading Shapefile using Python : <a href="http://andrewgaidus.com/Reading_Zipped_Shapefiles/" target="_blank">Reference</a></li>
        <li>Plotting Dot-Density County Map : <a href="http://andrewgaidus.com/Dot_Density_County_Maps/" target="_blank">Reference</a></li>
    </ul>

</li>
</ul>

</div>

<!---  
====================================================================================================
--->





<!---  
====================================================================================================
--->
<h4>
<i class="fa fa-database" aria-hidden="true"></i>
Geocoding API
<button type="button" class="collapsible" id="coll2_button" style="float:right;">Details
<i class="fa fa-arrow-down" aria-hidden="true"></i>
</button>
</h4>

<div>
Geocoding API : <a href="http://www.datasciencetoolkit.org/" target="_blank">http://www.datasciencetoolkit.org/</a>
</div>

<div class="content" id="coll2">
  <ul>
    <li>Converting street address to (latitude, longitude) coordinates: <a href="http://www.datasciencetoolkit.org/" target="_blank">Site</a></li>
    <li>Converting (latitude, longitude) coordinates to political regions:
      <a href="http://www.datasciencetoolkit.org/" target="_blank">Site</a></li>

  </ul>

</div>

<!---  
====================================================================================================
--->



<!---  
====================================================================================================
--->

<h4>
<i class="fa fa-database" aria-hidden="true"></i>
Open Street Map
<button type="button" class="collapsible" id="coll3_button" style="float:right;">Details
<i class="fa fa-arrow-down" aria-hidden="true"></i>
</button>
</h4>

<div>
Open Street Map: <a href="https://www.openstreetmap.org/" target="_blank">https://www.openstreetmap.org/</a>
</div>

<div class="content" id="coll3">
<ul>
  <li>Overpass Query Language & Concepts: <a href="https://wiki.openstreetmap.org/wiki/Overpass_API/Overpass_QL" target="_blank">Wiki</a>
    <ul>
      <li>The list of properties in Overpass: <a href="https://wiki.openstreetmap.org/wiki/Properties" target="_blank">Wiki</a></li>

      <li>Types of relation in Overpass: <a href="https://wiki.openstreetmap.org/wiki/Relation#Types_of_relation" target="_blank">Wiki</a></li>


      <li>Finding OSM tags: <a href="https://wiki.openstreetmap.org/wiki/Tags#Finding_your_tag" target="_blank">Wiki</a></li>

      <li>Python documentation for overpy (Overpass API): <a href="https://python-overpy.readthedocs.io/en/latest/" target="_blank">Docs</a></li>


      <li>Query example: <a href="https://towardsdatascience.com/loading-data-from-openstreetmap-with-python-and-the-overpass-api-513882a27fd0" target="_blank">Reference</a></li>
    </ul>
</li>


</ul>


</div>
<!---  
====================================================================================================
--->


<!---  
====================================================================================================
--->
<h4>
<i class="fa fa-database" aria-hidden="true"></i>
Open Street Map
<button type="button" class="collapsible" id="coll3_button" style="float:right;">Details
<i class="fa fa-arrow-down" aria-hidden="true"></i>
</button>
</h4>



<!---  
====================================================================================================
--->



<!---  
====================================================================================================
--->
<h4>
<i class="fa fa-database" aria-hidden="true"></i>
Additional Data Sources
</h4>

<div>
<ul>
  <li>Highway traffic data: <a href="https://www.fhwa.dot.gov/policyinformation/tables/tmasdata/" target="_blank">https://www.fhwa.dot.gov/policyinformation/tables/tmasdata/</a></li>
  <li><a href="https://wiki.openstreetmap.org/wiki/Potential_Datasources" target="_blank">https://wiki.openstreetmap.org/wiki/Potential_Datasources</a></li>
</ul>
</div>

<!---  
====================================================================================================
--->



<!---
Traffic count data source : http://doc.arcgis.com/en/esri-demographics/data/traffic-counts.htm#ESRI_SECTION1_BBCDB6D779EE4BB5932E6F2A91F01D19
--->

<!---
medicine / CMS
LEIS
...


Music / 

--->

