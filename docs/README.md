# Using QGIS in Mineral Exploration

* [Introduction](main-content/introduction).
* [User Guide](main-content/userguide).

## Have a specific question?

* Use the search bar in the top left to search this documentation
* Check the [FAQ section](other/faq)

## Have an issue?

Raise an issue [Issue Tracker](https://github.com/BritishGeologicalSurvey/Groundhog/issues) 


# Summary

QGIS is an open source GIS program for the display and analysis of GIS data. It has developed significantly in the past few years and is now a valuable tool for the mineral exploration industry, anda viable alternative to the commercially available GIS packages. Although not specifically written for geological applications, QGIS can do most of the required GIS tasks required by today’s geoscientists.The terminology is different to the usual earth sciences programs but many QGIS algorithms do the same thing but with a different name. There is no dedicated drill hole or cross section module available for QGIS currently,but discussions and plans are progressing to develop this module in the future.The Geoscience plugin is a basic drill hole display option that is available as a free plugin.

This manual examines QGIS and how QGIS can assist geoscientists in undertaking mapping and geoscientific tasks in their day-to-day work. The manual has evolved during several years teaching QGIS to geoscientists in Australia and has been produced to offer a go-to document for earth science related GIS activities.

Accessing data from the internet via web map and web feature servers is illustrated to show how using this data can help with compiling available data for an area. Detailed aerial photography and Google Earth can be easily integrated with mapping data to allow the creation of accurate base maps for a variety of geological applications. A wide range of vector and raster (grid and image) data formats can be easily imported into QGIS, including GPS gpx files. 

The presentation options for point, line and polygon data are extensive and easily customised. A variety of geological symbols and pattern fills can be applied to points, lines and polygons.Geochemical and geophysical data can also be presented in a variety of display options. Basic 3D displayof map data is also available via the QGIS2threejsplug-in.QGIS has many plug-ins for specialised tasks and the semi-automatic classification plug-in (SCP), is one example where users can select, download and process ASTER, Landsat and Sentinel 2 satellite data.It is recommended that new users peruse the plugins list to see what plugins are available and for those that may be of use in their work.

Map production is easy in QGIS with the “Print Layout” allowing extensive options for the display and printing of maps.

This document is a working draft and in continuous development. There may be errors and omissions,and these will be rectified as time permits.This manual applies to version 3.14.Please feel free to share this documentand please contact me if you find any errors.

# Introduction

This document is aimed at the exploration geologist,but the techniques outlined are easily transferrable to other areas. The author has been usingQGIS since 2015 and the version used in this documentis version 3.14.

The reader is encouraged to join the international online QGIS user forum at http://lists.osgeo.org/mailman/listinfo/qgis-user. 

This document will not go into the detail that is covered by the official QGIS User Guide and Training Manuals (https://docs.qgis.org/testing/pdf/en/) and other referencebooks (e.g. Graser 2016) on QGIS on topics like editing etc., but will discuss those tools used particularly in geological mapping, mineral exploration and remote sensing.See this video for an explanation of some of the advanced editing functions -https://youtu.be/jZYKGrIyVCA.

[Advanced Editing](https://www.youtube.com/embed/jZYKGrIyVCA ':include :type=iframe width=100% height=400px')

The original default file format for QGIS was the ESRI shape file (*.shp) and this format has been around for many years and can be read by many software products. It is an old format and has limitations, e.g. field names are limited to 10 characters. 

?> QGIS is adopting the new “Geopackage” file format as its default spatial file format. Geopackage files can have different types of vector geometry –points, lines and polygons – and can also include raster images. Geopackage files can be up to 140 TB in size! Layers can be imported into an existing Geopackage by dragging from the Layer panel onto the Geopackage name in the Browser panel. Styling information can be saved into the Geopackage file. When digitising into a Geopackage file, each new feature is auto numbered. Raster images imported into a Geopackage appear to be significantly compressed without any major loss of quality.ESRI and recent MapInfo products can read Geopackage files.

The author has been using QGIS since 2015 after about 20 years using the MapInfo-Discover software.He has been involved in exploration and mining geology for over 40 years, with almost 20 years with CRA Exploration Pty Limited, Argyle Diamonds and Rio Tinto Exploration from 1979 till 1997. The past 20 years (1998 –present) has been engaged in consulting roles to the diamond exploration and mining industry with activities in Australia, Brazil, China, Greenland and India, and exploration for other commodities including base metals, iron ore, and manganese

# About QGIS

QGIS is a user-friendly open source Geographic Information System (GIS) licensed under the GNU General Public License andis an official project of the Open Source Geospatial Foundation (OSGeo). It runs on Linux, Unix, Mac OSX, Windows and Android and supports numerous vector, raster, and database formats.

The Open Geospatial Consortium (OGC) is an international consortium of more than 530 businesses, government agencies, research organizations, and universities driven to make geospatial (location) information and services FAIR -Findable, Accessible, Interoperable, and Reusable. OGC’s members create free geospatial standards. OGC also actively analyses emerging tech trends, and runs an agile, collaborative Research and Development (R&D) lab that builds and tests innovative solutions to members' use cases.For more information visit “ogc.org”.For those users requiring an introduction to GIS, please see this link https://docs.qgis.org/3.4/en/docs/gentle_gis_introduction/.

QGIS is a volunteer driven project. They welcome contributions in the form of code contributions, bug fixes, bug reports, contributed documentation, advocacy and supporting other users on their mailing lists and gis.stackexchange.com. If you are interested in actively supporting the project, you can find more information under the development menu and on the QGIS Wiki.If you find QGIS valuable in your workplace, please donate to the QGIS project –the details are on the website.

QGIS provides a continuously growing number of capabilities provided by core functions and plugins. You can visualize, manage, edit, analyse data, and compose printable maps. 

This document will mainly address workflows for geoscientists but there are many other tools available in QGIS and worthy of some exploration of their functions. Currently QGIS does not have a detailed downhole or cross section display option, but there are groups across the world keen to crowd source the development of the drill hole plug-in. The Geoscience plugin does display drill holes in plan and in cross section but is limited in its features. QGIS does not also handle all the various geophysical processing options, and again there is interest from various groups to develop plug-ins for geophysical processing.

A good explanation of QGIS and where it came from can be found here https://www.youtube.com/watch?v=As4hfPecxoU. 

[QGIS](https://www.youtube.com/embed/As4hfPecxoU ':include :type=iframe width=100% height=400px')

If you find QGIS makes a valuable contribution to your business, please consider making a donation to assist with continual code improvements –see this link https://qgis.org/en/site/getinvolved/donations.html.

Installation options are available on QGIS download page (https://qgis.org/en/site/forusers/download.html) with options to download either the development version (via OS4Geo)orthe standalone installers (recommended).Both 64 and 32 bit versions are available.

QGIS has been using ESRI shapefiles as the default spatial file format but the new “GeoPackage” format is far superior and will probably become the default file format for QGIS in the near future.

!> Shape files have a number of limitations such as field/attribute column names are limited to 10 characters, it lacks a time data type, only supports text fields to 255 characters in length and is limited to 2 GB in size.

GeoPackage files on the other hand allows point, line vector and raster files to be stored in the one file. Formats/styles can be saved into the Geopackage file and it can be up to 140 TB in size.When adding features during digitising, for example, a Geopackage file will automatically populate the id field with sequential numbers.See this web link for further information https://carto.com/blog/fgdb-gpkg/.Note that Geopackage files are single user only and if you need multiple user access at the same timethen PostgreSQL and PostGIS maybe required.