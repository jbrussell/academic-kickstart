+++
title = "Exploring Earthquake Magnitude and Depth"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "Earthquake Magnitude and Depth"
[menu.eilive2020]
  parent = "Part 1: Data Storytelling in Python"
  weight = 4
+++

\

Magnitude and depth are two basic features of an earthquake that are important for understanding plate tectonics as well as earthquake hazard. Typically, the shallower the earthquake and larger the magnitude, the more potential for destruction.

In the two interactive figures below, we will explore relationships between earthquake magnitude and depth using what's called "linking and brushing". Selecting data in one figure will highlight the corresponding points in the other. This technique is useful for grasping complex multidimensional datasets. 

For our purposes, this allows us to select earthquakes in the map and see where they fall in magnitude-depth space. It also works the other way around – select earthquakes of a desired magnitude and depth to see where they occur on the map. 

{{% alert note %}}
TIP: Data in the two figures below are linked. Highlight points in one using the "Box Select" or "Lasso Select" tool to see where they occur in the other.
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/ExploreEarthquakes/a1_plot_global_eqs.ipynb)

<!-- layouts/partials/bokeh -->  
{{< importBokeh "bokeh/a1_globalEQ_MagDepth.html" >}}

\
\

The questions asked in the previous section are much easier to answer now:  

{{% alert note %}}
* Where do deep earthquakes most commonly occur? Why?  
{{% /alert %}}

> Along the edges of the oceanic plates! This is direct evidence for plate tectonics –-- the cold dense oceanic lithosphere subducting beneath the less dense, buoyant continents.
 
{{% alert note %}}
* Are there more large or small magnitude earthquakes? 
{{% /alert %}} 

> There are many more small magnitude earthquakes than large. How many more? We will explore that next!

\
\

# Magnitude Distribution of Earthquakes

One of the most fundamental equations in earthquake seismology is the **Gutenberg-Richter relation**, [published in 1956](https://authors.library.caltech.edu/43574/1/Gutenberg_1956.pdf). It is an empirical formula that describes how earthquakes vary in number from small to large:

$$ \log_{10}N = a - bM $$

where $M$ is earthquake magnitude, and $N$ is the number of earthquakes with magnitude greater than or equal to $M$. The parameters $a$ and $b$ are trickier to attribute a physical meaning to, but describe how earthquakes distribute themselves from small to large. On average, $b$ tends to be close to 1. It is a logarithmic relationship and therefore appears as a straight line when plotted with a logarithmic axis.

Below is a graph showing the number of earthquakes $N$ of at least a given magnitude versus magnitude $M$. The blue circles are from data for all earthquakes >M5.0 from 2015-2020, as in the previous section. The red line shows the Gutenberg-Richter relation assuming $b = 1$ and $a = 8.7$. 

The figure shows that each unit increase of magnitude corresponds to approximately 10 times fewer earthquakes in the same amount of time. For example, for every earthquake M7.0 or greater there are approximately 100 M5.0 or greater earthquakes.

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/ExploreEarthquakes/a1_plot_global_eqs.ipynb)

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/a1_GutenbergRichter.html" >}}

