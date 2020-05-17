+++
title = "Earthquake Magnitude and Depth"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "Earthquake Magnitude and Depth"
[menu.eilive2020]
  parent = "Part 1: Data Storytelling in Python"
  weight = 3
+++

\

Magnitude and depth are two key features of an earthquake that are especially important for hazards. Typically, the shallower the earthquake and larger the magnitude, the more potential for destruction.

In the two figures below, we can explore relationships between earthquake magnitude and depth using what's sometimes called "linking and brushing". Selecting data in one figure will highlight the corresponding points on the other. This helps to gain a grasp of complicated multidimensional datasets. 

For our purposes, this allows us to select earthquakes in the map and see where they fall in magnitude-depth space. It also works the other way around – select earthquakes of a desired magnitude and depth to see where they occur on the map. 

{{% alert note %}}
* Where do deep earthquakes most commonly occur? Why?
* Are there more large or small magnitude earthquakes?
{{% /alert %}}

<!-- layouts/partials/bokeh -->
<div>
  {{< importBokeh "bokeh/a1_globalEQ_MagDepth.html" >}}
</div>
