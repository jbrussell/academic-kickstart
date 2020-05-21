+++
title = "Turning Data Into Sound"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "Turning Data Into Sound"
[menu.eilive2020]
  parent = "Part 2: Earthquake Sonification"
  weight = 4
+++

\

The human ear is hardwired to find patterns within complex sounds. Together with visual cues, we can use data sonification --- or turning data into sound --- to extract new information from complicated datasets that may be missed by just *looking* at the data. The [Seismic Sound Lab](seismicsoundlab.org) at the Lamont-Doherty Earth Observatory works to combine both senses with audio-visuals in order to learn new things about the Earth as well as to communicate that knowledge to the general public. The following sections focus on how these sounds are made directly from seismic data.

\
\

# Understanding Waves

In the previous section <a href="../part1a2_makeyourown/" target="_self">Make Your Own Maps</a>, we introduced a simple sinusoid. In the section, we will explore that further. We will use the same sine wave equation with amplitude $A$ and frequency $f$ (cycles per second), but this time we will also add phase $c$, offset $b$ :

$$ y = A \sin (2 \pi f x + c) + b $$

When we sonify data, we will want to make sure that the data are varying around 0 and therefore we will try our best to ensure that $b = 0$.

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/1_simple_sounds.ipynb)

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/slider.html" >}}

\
\

# Making Your Own Waves With trinket.io

Now, we will try adding waves together. Interesting behavior occurs even when add just two waves together. If you make the frequencies of the two waves close to one another, you will begin to see **beats** --- a sine wave modulated by a lower frequency "envelope". The frequency of the beat that you see is equal to the difference in the frequency of the two waves ($f_{beat} = |f_1-f_2|$). The human ear hears this as a single frequency with its amplitude modulated.

{{% alert note %}}
* Try adjusting `f1` and `f2` up and down to see what happens!  
* What happens when the two frequencies get farther apart? Closer together?

{{% /alert %}}

<iframe src="https://trinket.io/embed/python3/aac225ea55?start=result" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

\
\

# Listening to Sine Waves

Now, we will listen to some of the waves we just made. The following figure shows on top 3 different sine waves, each 2 seconds of length and connected end-to-end. The first one has a frequency of 200 Hz, the second a frequency of 210 Hz, and the third is the sum of the two. In this one you will hear a clear beating sound. Clicking the tab at the top left will show an example for 200 Hz + 300 Hz. These frequencies are far enough apart

The bottom panel is a **spectrogram** that shows the power produced by different frequencies over time. The brighter colors (less negative numbers) represent more power. The numbers are negative because we have taken the $\log_{10}$ to get values in terms of decibels.


{{% alert note %}}
Use the "Wheel Zoom" tool in the top toolbar to expand the horizontal and vertical axes. Click the tabs on the top to change waveforms. Click the "save" button to download your favorite sound wave!
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/1_simple_sounds.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/Beat_hres.html" >}}

\
\

# Sound wave Shape and Compression

Waves come in all shapes and sizes, not just sine waves. Although, sine waves sound the purest and are most pleasing to the ear. In the following example, we will listen to a comparison of the sine wave with the "square wave". Expand the horizontal axes to see what the two waveforms look like in detail.

{{% alert note %}}
  * Can you guess which one is the square wave just by listening to them?
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/1_simple_sounds.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/squarewave_hres.html" >}}

\

Next we will explore the effect of an **envelope** applied to the waveform. Envelopes alter the shape of the waveform and change the amplitude of the tone but have no affect on the frequency. Notice how the power in the spectrogram reflects the amplitude in the waveform. As the waveform amplitude increases, so does the spectral power (it may be difficult to see as the power is shown in $\log_{10}$ units as decibels).

The top left corner shows tabs for different sound duration ranging from 2 to 8 seconds. Notice how the frequency of the tone decreases with increasing duration. This is because the same amount of cycles are being expressed over a larger time interval, leading to a longer wavelength.

{{% alert note %}}
  * What happens to the frequency of the sound as you increase the duration from 2 seconds to 5 seconds?
{{% /alert %}}

[<i class="fab fa-github"></i> view code](https://nbviewer.jupyter.org/github/jbrussell/EI_Live_2020/blob/master/earthquake_sonification/1_bokeh_notebooks/1_simple_sounds.ipynb)
<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/envelope_hres.html" >}}