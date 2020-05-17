+++
title = "Seismic Noise in New York City"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "Seismic Noise NYC"
[menu.eilive2020]
  parent = "Part 1: Data Storytelling in Python"
  weight = 4
+++

\

Anyone who has been to New York City knows it can be a noisy place. The same goes for ground beneath our feet as cars, trucks, buses, and subways rumble by. Extremely sensitive seismometers that measure ground motion can detect these vibrations. Due to the COVID-19 crisis and the resulting shelter-in-place protocols active around the world, seismic noise [has noticeably decreased worldwide](https://www.nature.com/articles/d41586-020-00965-x). 

In this section, we will explore data from a seismometer currently installed in Central Park as part of the [Lamont-Doherty Cooperative Seismographic Network (LCSN)](https://www.ldeo.columbia.edu/LCSN/intro.php).

<!-- <iframe src="https://www.google.com/maps/d/embed?mid=1Hz6JR0IILBPtMUiWBPq9jbY7c0U4x630&hl=en" width="640" height="480"></iframe> -->


<!-- layouts/partials/bokeh -->
<div>
  {{< importBokeh "bokeh/LD.CPNY.2020-02-09.2020-05-15.5_15Hz.BHZ.html" >}}
</div>


# Make your own noise plots

<iframe src="https://trinket.io/embed/python3/600f40f1cf" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

<!-- layouts/partials/bokeh -->
<div>
  {{< importBokeh "bokeh/LD.CPNY.2020-02-09.2020-05-15.5_15Hz.BHZ.load_reduction_hourly_NYC.html">}}
</div>