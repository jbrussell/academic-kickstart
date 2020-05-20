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

\

Hundreds of earthquakes occur across the globe every day, but most of them are too small for us to feel. Here, we will dive into earthquake data and explore some of the larger magnitude earthquakes (greater than M5.0) that have occurred over the past several years.

We start by looking at where earthquakes occur spatially. The interactive map below shows the past 5 years of earthquakes, where each circle represents a single earthquake. Circles increase in size with increasing earthquake magnitude and the color indicates depth. Use the toolbar to zoom in and out and pan the page. Hover over points with the cursor to see information about each earthquake.

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/ExploreEarthquakes/a1_plot_global_eqs.ipynb)

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/a1_global_seismicity.html" >}}


\
\

# 45 Years of Earthquake Data

Next, we gather all available data for earthquakes larger than M5.0 from the past nearly 45 years (1976–2020) from the [USGS catalogue](https://earthquake.usgs.gov/earthquakes/map/) and the [GCMT Project](https://www.globalcmt.org/). 

This would be far too many points to interactively load into your web browser (more than 50,000 earthquakes), so here we are using a tool that gathers the data within pixels on the map and counts how many earthquakes occur in each. We can think of this as earthquake density as indicated by the color: dark colored points have few or no earthquakes and bright colors show regions with many earthquakes. In this view, you can clearly see the boundaries of the tectonic plates!

{{% alert note %}}
* What are the bright spots in the middle of the oceans?
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/ExploreEarthquakes/a2_plot_eqdensity_heatmap.ipynb)

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/a2_global_seismicity_heatmap.html" >}}
