WIP. Design.

### Quickstart

`geoplot` adds a new `geoplot` extension to the `GeoSeries` and `GeoDataFrame` data structures provided by the
`geopandas` library (itself a geographic extension of `pandas`).

Submethods of `geoplot` provide a number of interesting geographic plot types, from simple to advanced, which extend
the root `geopandas` object's content.

All plots are static plots built using `matplotlib` Basemap facilities, alongside `geopandas` and `mplleaflet`.

Interactive versions of these plots using `leaflet.js` and `d3.js` might be worth investigating as a separate library
 (`mercator`?).

As `pd.DataFrame.plot` extends `matplotlib`, so too should `gdf.GeoDataFrame.geoplot` extend `matplotlib.Basemap`.

As `mpld3` extends `pd.DataFrame` interactively via `d3.js`, so too should `mercator` extend `gdf.GeoDataFrame`
interactively via `d3.js`.

### Features

* `geoplot()` &mdash; Simple extension of the `geopandas`-provided `plot()`.
* `dot()` &mdash; [Dot map](https://raw.githubusercontent.com/andrea-cuttone/geoplotlib/master/examples/screenshots/dotdensity.png).
A simple map type that places a dot wherever a coordinate occurs.
* `marker()` &mdash; An elaboration on `dot()`. Allows any marker type, as well as MultiMarkers.
* `heatmap()` &mdash; [Geo heatmap](https://raw.githubusercontent.com/andrea-cuttone/geoplotlib/master/examples/screenshots/kde1.png).
Fit a KDE or a distance-regular colormap to the map.
* `boundary()` &mdash; [Boundary map](https://raw.githubusercontent.com/andrea-cuttone/geoplotlib/master/examples/screenshots/shapefiles.png).
Draws the boundaries of polygons. Mostly useful in combination.
* `choropleth()` &mdash; [Choropleth](https://raw.githubusercontent.com/andrea-cuttone/geoplotlib/master/examples/screenshots/choropleth.png).
* `voronoi()` &mdash; [Voronoi tesselation](https://raw.githubusercontent.com/andrea-cuttone/geoplotlib/master/examples/screenshots/voronoi-filled.png).
Fits polygons around points that map by minimizing distance.
* `spatial()` &mdash; [Spatial map](https://raw.githubusercontent.com/andrea-cuttone/geoplotlib/master/examples/screenshots/graph-flights.png).
Colors polygons according to data on their number.
* `symbol()` &mdash; [Symbol map](symbol.png). Embed symbols like pies or growing circles into a map.
* `cartogram()` &mdash; Proportional sizing, no idea how that would be implemented.
    * Including [non-contiguous option](http://bl.ocks.org/mbostock/4055908)? Easier to implement.
* Enough to start. Plenty more [here](https://github.com/andrea-cuttone/geoplotlib/tree/master/examples/screenshots).

### To-do

1. Factor out the JavaScript rendering code.
2. Learn the Basemap API.

### Development environment

To set this library up for development in a local virtual environment:

#### Linux, Mac OSX

1. `git clone https://github.com/ResidentMario/geoplot.git`
2. `conda env create`
3. `source activate geoplot`

#### Windows

1. `git clone https://github.com/ResidentMario/geoplot.git`
2. `conda env create` (this will likely partially fail, keep going)
3. `runipy install.ipynb`
4. `activate geoplot`