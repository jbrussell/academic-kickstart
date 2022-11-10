+++
title = "2011 Tohoku Earthquake"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "M9.1 Tohoku Earthquake"
[menu.eilive2020]
  parent = "Part 2: Earthquake Sonification"
  weight = 5
+++

The M9.1 earthquake that occurred in Tohoku, Japan on March 11, 2011 was the largest earthquake ever recorded in Japan and the 4th largest in the world that we have experienced. It produced a catastrophic tsunami that killed over 10,000 people and left many more homeless. It also caused severe damage to the infrastructure of Japan and is quoted as the most costly natural disaster in history, estimated at ~$235 billion. An earthquake of this size generates seismic waves that travel all across the planet and are detected by seismometers.

In this section, we will listen to seismic data at the 3 stations shown in the map below. They represent close, intermediate, and far distances from the earthquake epicenter.

\

<iframe src="https://www.google.com/maps/d/embed?mid=1unzUOXLGZqPxgy6IIU0VanC_nduJ1Fqn&hl=en" width="640" height="480"></iframe>

\
\

# The Background Noise

Before we listen to the earthquakes, we will first listen to the background noise levels at one of the three stations, P39A, in Salisbury, MO.

{{% alert note %}}
* What do you notice about the background noise? Are there any dominant frequencies?
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/2_earthquake_sonification.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/P39A_noise_BHZ_8s.html" >}}

# Listening to a M9.1 Earthquake

Now, we will listen to the M9.1 that shook the earth on March 11, 2011. The tabs on the following figure are ordered from farthest away from the source (over 10,000 miles) to closest (only a few hundred miles).

\

{{% alert note %}}
  * How do the sounds change as you get farther away from the earthquake epicenter?
  * The low frequency waves arriving several hours later -- what are they?
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/2_earthquake_sonification.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/TRQA_M9.1_BHZ.P39A_M9.1_BHZ.MAJO_M9.1_BHZ_3s_hres.html" >}}

\
\

Now we will listen to a smaller magnitude (but still quite large!) M7.3 foreshock that occurred a few days prior to the M9.1 on the same fault. This earthquake produced about 1,000 times less seismic energy than the M9.1.

{{% alert note %}}
* Can you hear any differences from the larger M9.1? Frequency content? Background noise levels?
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/2_earthquake_sonification.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/TRQA_M7.3_BHZ.P39A_M7.3_BHZ.MAJO_M7.3_BHZ_3s_hres.html" >}}

\
\

# Audio-visual Ground Motion Animation

\

What do these seismic waves actually look like? The video below was made at the [Seismic Sound Lab](http://www.seismicsoundlab.org) and shows seismic waves from the M9.1 earthquake that were measured across the United States using seismometers deployed during the [USArray](http://www.usarray.org/) project. Red and blue colors indicate that the ground is moving up or down. This video puts into action all that we have covered in this section!

\

<iframe src="https://player.vimeo.com/video/187740441" width="640" height="360" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
<p><a href="https://vimeo.com/187740441">Ground Motions for Hait and Tohoku Eqs.</a> from <a href="https://vimeo.com/seismicsoundlab">seismicsoundlab</a> on <a href="https://vimeo.com">Vimeo</a>.</p>
