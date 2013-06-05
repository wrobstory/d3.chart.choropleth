d3.chart.choropleth
===================

A d3.chart based choropleth map generator with an easily modified domain and built-in color-brewer colors based on a quantize scale.

YlGnBu color brew:

![YlGnBu](http://farm4.staticflickr.com/3734/8955684925_da4d2c2c85_o.png)

OrRd color brew:

![OrRd](http://farm8.staticflickr.com/7385/8955684907_3167f47886_o.png)

### Sample Use

```javascript
// YlGnBu color brew, custom domain
var chart_1 = d3.select('#map1')
  .append("svg")
  .attr("height", 500)
  .attr("width", 480)
  .chart("Choropleth")
  .domain([0, 15])
  .range('YlGnBu')
  .projection(d3.geo.albersUsa())
  .scale(500);

// OrRd color brew, wider domain
var chart_2 = d3.select('#map2')
  .append("svg")
  .attr("height", 500)
  .attr("width", 480)
  .chart("Choropleth")
  .domain([0, 25])
  .range('OrRd')
  .projection(d3.geo.albersUsa())
  .scale(500);

### API

Sample API Documentation:

#### `<instance>.height(newHeight)`

**Description:**

When value provided sets the height of the SVG. If no value provided, defaults to 500 for bl.ocks integration.

**Parameters:**

* `newHeight` - Integer, optional, new height

**Uses:**

Example:

```javascript
var map = d3.select("#map")
  .append("svg")
  .chart("Choropleth")
  .height(500);
```

#### `<instance>.width(newWidth)`

**Description:**

When value provided sets the width of the SVG. If no value provided, defaults to 960 for bl.ocks integration.

**Parameters:**

* `newWidth` - Integer, optional, new width

**Uses:**

Example:

```javascript
var map = d3.select("#map")
  .append("svg")
  .chart("Choropleth")
  .width(900);
```

#### `<instance>.range(newRange)`

**Description:**

When value provided sets the color range for the map, based on the [color brewer](http://colorbrewer2.org/) colors. Must pass one of the following:
* BuGn
* BuPu
* GnBu
* OrRd
* PuBu
* PuBuGn
* PuRd
* RdPu
* YlGn
* YlGnBu
* YlOrBr
* YlOrRd

Defaults to YlGnBu

**Parameters:**

* `newRange` - String, optional, new color range

**Uses:**

Example:

```javascript
var map = d3.select("#map")
  .append("svg")
  .chart("Choropleth")
  .width(900);
```

