# Leaflet, an interactive map

<!-- badges: start -->

[![R build status](https://github.com/rstudio/leaflet/actions/workflows/R-CMD-check.yaml/badge.svg)](https://github.com/rstudio/leaflet/actions) [![CRAN RStudio mirror downloads](https://cranlogs.r-pkg.org/badges/leaflet)](https://www.r-pkg.org/pkg/leaflet) [![](https://www.r-pkg.org/badges/version/leaflet)](https://www.r-pkg.org/pkg/leaflet) [![RStudio community](https://img.shields.io/badge/community-leaflet-blue?style=social&logo=rstudio&logoColor=75AADB)](https://community.rstudio.com/new-topic?title=&tags=leaflet&body=%0A%0A%0A%20%20--------%0A%20%20%0A%20%20%3Csup%3EReferred%20here%20by%20%60leaflet%60%27s%20GitHub%3C/sup%3E%0A&u=barret)

<!-- badges: end -->

Leaflet is developed by Numa Gremling, Paul Crickard III, Paul Crickard, and Mark Lewin. The leaflet package from Github is: <https://github.com/rstudio/leaflet/tree/main>

The website I created for this package is:

My customization of the website:

1.  change the page theme to minty

2.  change the code theme to arrow-dark

3.  change the base font into Roboto, the heading font into Roboto Slab, code font into JetBrains Mono

4.  change navbar background into dark

5.  change the navbar layout into left: [intro, reference, articles, news]; right: [search, github]

## 

## Author of the website

Ziying Yang, first year ScM Biostatistics student at Johns Hopkins University, mainly responsible for the main page development and example analysis.

## Purpose of the package

Leaflet is one of the most popular open-source JavaScript libraries for interactive maps. It's used by GIS specialists like OpenStreetMap, Mapbox, and CartoDB. This R package makes it easy to integrate and control Leaflet maps in R.

## Installation

To install this package from CRAN:

``` r
install.packages('leaflet')
```

We can also install the development version from GitHub:

``` r
if (!require('devtools')) install.packages('devtools')
devtools::install_github('rstudio/leaflet')
```

To begin using `leaflet`, we should first import the package using the `library` command:

``` r
library(leaflet)
```

## Example Usage

``` r
m <- leaflet() %>%
  addTiles() %>% 
  addMarkers(lng=-76.6122, lat=39.2904, popup="The Interactive Map of Baltimore")
m  
```

We can also add pop-ups

``` r
m %>% addPopups(lng=-76.5902, lat=39.2983, "Here is the Bloomberg school of public health</b>, JHU")
rand_lng <- function(n = 10) rnorm(n, -76.5902, .01)
rand_lat <- function(n = 10) rnorm(n, 39.2983, .01)
```

## Exported Functions

addAwesomeMarkers() addGraticule() addLayersControl() layersControlOptions() removeLayersControl() addLegend() labelFormat() addMapPane() addMeasure() addMiniMap() addProviderTiles() providerTileOptions() addRasterImage() projectRasterForLeaflet() Add a raster image as a layer addRasterLegend() addScaleBar() scaleBarOptions() removeScaleBar() addSimpleGraticule() addTerminator() atlStorms2005 awesomeIconList() awesomeIcons() breweries91 colorNumeric() colorBin() colorQuantile() colorFactor() createLeafletMap() leafletMap() Legacy functions derivePoints() derivePolygons() dispatch() invokeMethod() easyButtonState() easyButton() addEasyButton() addEasyButtonBar() evalFormula() expandLimits() expandLimitsBbox() filterNULL() gadmCHE getMapData() groupOptions() iconList() icons() JS %\>% leaflet() leafletOptions() leafletCRS() leafletDependencies leafletProxy() leafletSizingPolicy() makeAwesomeIcon() makeIcon() addControl() addTiles() addWMSTiles() addPopups() addMarkers() addLabelOnlyMarkers() addCircleMarkers() highlightOptions() addCircles() addPolylines() addRectangles() addPolygons() addGeoJSON() addTopoJSON() setView() flyTo() fitBounds() flyToBounds() setMaxBounds() clearBounds() tileOptions() WMSTileOptions() popupOptions() labelOptions() markerOptions() markerClusterOptions() pathOptions() leafletOutput() renderLeaflet() mapOptions() previewColors() removeControl() clearControls() clearGroup() removeImage() clearImages() removeTiles() clearTiles() removePopup() clearPopups() removeMarker() clearMarkers() removeMarkerCluster() clearMarkerClusters() removeMarkerFromCluster() removeShape() clearShapes() removeGeoJSON() clearGeoJSON() removeMeasure() removeTopoJSON() clearTopoJSON() showGroup() hideGroup() validateCoords()
