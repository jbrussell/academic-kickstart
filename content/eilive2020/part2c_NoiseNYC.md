+++
title = "The Sounds of NYC"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "The Sounds of NYC"
[menu.eilive2020]
  parent = "Part 2: Earthquake Sonification"
  weight = 6
+++

Finally, we return to the ground vibrations measured in Central Park that we looked at in section <a href="../part1b_seismicnoisenyc/" target="_self">Seismic Noise in NYC</a>. However, because we need a waveform that oscillates around zero in order to turn it into sound, we remove the daily running average from the hourly measurements. The resulting waveform and spectrogram is shown below.

The daily signal is the main feature of the waveform and appears as a bright streak in the spectrogram at around 50 Hz in sonified frequency (this is 1 / 24 hours = 1 / 86,400 seconds $\approx$ $1.6 \times 10^{-5}$ Hz).

{{% alert note %}}
  * What are the other bright streaks at approximately 100, 150, 200 Hz, ... ?
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/3_noise_sonification.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/LD.CPNY.2020-02-09.2020-05-15.5_15Hz.BHZ_1hr_4s.html" >}}

\
\

In order to include more sound information, we have reprocessed the dataset to include measurements every minute rather than every hour. The daily noise cycle due to people and traffic can be heard clearly as a beating noise. This is what the daily grind of NYC sounds like!

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/3_noise_sonification.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/LD.CPNY.2020-02-09.2020-05-07.5_15Hz.BHZ_1min_50s.html" >}}



