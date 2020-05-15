+++
title = "Global Seismicity"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "Global Earthquakes"
[menu.eilive2020]
  parent = "Part 1: Data Storytelling in Python"
  weight = 2
+++

Hundreds of earthquakes occur across the globe every day, but most of them are too small for people to feel. Here, we will dive into the data and explore some of the larger earthquakes (greater than M5.0) that have occurred over the past several years.

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/a1_global_seismicity.html" >}}

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/a1_globalEQ_MagDepth.html" >}}

\
## 45 Years of Seismicity

Finally, we have gathered all the seismicity data for all earthquakes larger than M5.0 from the past nearly 45 years (1976–2020). This would be far too many points to interactively load into your web browser (more than 26,000 earthquakes), so here we are using a tool that automatically bins data and shows data density based on color; dark colors have no data and bright colors denote lots of data.

``` python
# Load the holoviews datashader tool to quickly calculate earthquake density
from holoviews.operation.datashader import rasterize

plot = rasterize(earthquakes).opts(plot=dict(fig_size=200, aspect=2)).opts(title="Earthquake Density > M5.0 (1976-2020)").opts(opts.Image(tools=['hover']))
```

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/a2_global_seismicity_heatmap.html" >}}

