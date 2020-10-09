+++
# Project title.
title = "Visualizing Earth's Free Oscillations"

# Date this page was created.
date = 2018-10-30T00:00:00

# Project summary to display on homepage.
summary = "After a large earthquake, Earth's normal modes vibrate like waves on a guitar string. If the earthquake is large enough, the Earth can 'ring' for days or weeks. This video demonstrates both visually and sonically these free oscillations of the Earth."

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Data Visualization", "Data Sonification", "Suface Waves", "Free Oscillations", "Normal Modes"]

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references 
#   `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides = ""

# Links (optional).
url_pdf = ""
url_slides = ""
url_video = ""
url_code = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
#url_custom = [{icon_pack = "fab", icon="twitter", name="Follow", url = "https://twitter.com/JBRussell_"}]

# Optional external URL for project (replaces project detail page).
external_link = ""

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
[image]
  # Caption (optional)
  caption = ""
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Center"
  
  # Show image only in page previews?
  preview_only = true
+++

This video is a contribution by [Celia Eddy](https://www.celiaeddy.com/) and I to the [Seismic Sound Lab](http://www.seismicsoundlab.org/), run by Ben Holtzman at the Lamont-Doherty Earth Observatory. 

{{< vimeo 215665951 >}}
\

After a large earthquake, the Earth vibrates like waves on a guitar string -- These discrete modes of vibration are called normal modes or free oscillations. If the earthquake is large enough, the Earth can 'ring' for days or weeks. This video uses synthetic waveform simulations to demonstrate both visually and sonically these free oscillations of the Earth after the [M6.9](https://earthquake.usgs.gov/earthquakes/eventpage/us20008m3t/executive#executive) earthquake that occurred off the coast of Fiji on 2/24/2017.

The video is composed of three separate-but-related animations. Each animation show how the waves travel along the surface of the earth, displayed as a circular ring. This 2-dimensional ring is made up of 2,000 points on the Earth's surface that display ground motion for 48 hours after the earthquake.

## Animation 1: Surface and Body Waves
We are *listening* to a waveform at the antipode of the Earth from the M6.9 in Fiji. The synthetic waveforms are calculated using [Instaseis](http://instaseis.net/). To make the sound, many narrow band filters are used to decompose the seismic waveform into its constituent frequency components (**Fig. 1**). Each individual waveform is then assigned to an oscillator of a specific frequency.

{{< figure src="comb.jpg" title="Narrow band filtered seismograms." numbered="true" width="100%">}}


## Animation 2: Normal Modes
The first 8 gravest (lowest frequency) spheroidal modes are extracted from 48 hour seismograms (**Fig. 2**). This animation shows the shapes of these modes in color and the superposition of the modes in white, starting from the lowest frequency and incrementally adding higher modes. Each mode is mapped to a tone that we can hear, where the relative frequencies of the tones are preserved. By the end of the animation, you can begin to see surface waves propagating back and forth.

{{< figure src="peaks.jpg" title="Discrete frequencies for the 8 gravest modes." numbered="true" width="100%">}}


## Animation 3: Attenuation
This animation is similar to **Animation 2** except this time, all the modes are played at once. The tone of each mode is modulated in time by the amplitude envelopes in **Fig. 3**. Through time, the high frequencies die out due to anelastic attenuation and all that is left are the lowest frequency modes. In this video, you can actually hear this attenuation!

{{< figure src="envelopes.jpg" title="Amplitude envelopes for each of the modes in Fig 2." numbered="true" width="100%">}}


