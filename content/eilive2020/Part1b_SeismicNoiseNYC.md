+++
title = "Seismic Noise in New York City"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "Seismic Noise in NYC"
[menu.eilive2020]
  parent = "Part 1: Data Storytelling in Python"
  weight = 5
+++

\

Anyone who has been to New York City knows it can be a noisy place. The same goes for the ground beneath our feet as cars, trucks, buses, and subways rumble by. Extremely sensitive seismometers that measure ground motion can detect these vibrations. Due to the COVID-19 crisis and the resulting shelter-in-place protocols active around the world, seismic noise [has noticeably decreased worldwide](https://www.nature.com/articles/d41586-020-00965-x). 

Shown below is data from a seismometer currently installed in Central Park as part of the [Lamont-Doherty Cooperative Seismographic Network (LCSN)](https://www.ldeo.columbia.edu/LCSN/intro.php). The vertical axis is the root-mean-square (RMS) ground displacement in nanometers. The data have been processed in 1 hour time windows and filtered from 5-15 Hz. 

The jagged line labeled "hourly noise" shows the average hourly noise levels measured at the seismometer. The thicker, smooth line labeled "daily noise" shows a running 24 hour average of the thin line.

<!-- <iframe src="https://www.google.com/maps/d/embed?mid=1Hz6JR0IILBPtMUiWBPq9jbY7c0U4x630&hl=en" width="640" height="480"></iframe> -->

{{% alert note %}}
* Why is the hourly average jagged?  
* What do the peaks/throughs correspond to?
{{% /alert %}}

{{% alert note %}}
TIP: Double click to toggle legend on/off  
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/NYC_SeismicNoise_and_Electricity/2_plot_noise_interactive.ipynb)

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/LD.CPNY.2020-02-09.2020-05-15.5_15Hz.BHZ.html" >}}

\
\

# Make Your Own Noise Figure

Now, we will remake the figure in a trinket. This will allow us to change the window length of the running average (the "daily average" bold line in the previous figure). The variable `win_hr` in the trinket below is the amount of time in hours that the average will be over. Setting this value to `win_hr = 24` reproduces the figure above. Try out different values.

{{% alert note %}}
* What does a weekly average look like?
{{% /alert %}}

<iframe src="https://trinket.io/embed/python3/02862aa480?start=result" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

\
\

# Comparison With Electricity Consumption

A recent [New York Times article](https://www.nytimes.com/interactive/2020/04/08/upshot/electricity-usage-predict-coronavirus-recession.html) showed a decrease in electricity consumption in NYC due to COVID-19 related shutdowns of businesses. This is important because most economic indicators are slow and require time, but electricity consumption data is typically reported hourly, providing nearly realtime information on economic status.  

Below is a figure showing hourly electricity load pulled from the [public NYISO database](http://mis.nyiso.com/public/) with respect to the average of the previous 4 years (2016-2019), compared with the same seismic noise levels at Central Park from above. 

{{% alert note %}}
TIP: Click legend entries to toggle data on/off
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/NYC_SeismicNoise_and_Electricity/4_plot_noise_NYCusage_interactive.ipynb)

<!-- layouts/partials/bokeh -->
<div>
  {{< importBokeh "bokeh/LD.CPNY.2020-02-09.2020-05-15.5_15Hz.BHZ.load_reduction_hourly_NYC.html">}}
</div>

\

Visually, there is an excellent correlation between the two. Both electricity consumption and noise levels dropped during initial lockdown and have apparently begun to increase toward the pre-lockdown levels. Of course, electricity consumption and ground vibrations are not directly linked to one another. Rather, they are both linked to human activity, and the widespread closing of businesses as people stay home has caused both to decrease.
