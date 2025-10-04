+++
# Project title.
title = "Young ORCA: Searching for small-scale convection in the south Pacific"

# Date this page was created.
date = 2020-02-16T00:00:00

# Project summary to display on homepage.
summary = "Small-scale convection, if it exists, should be detectable using high resolution ocean-bottom seismology. We use surface-wave imaging to investigate mantle flow patterns and evaluate whether SSC persists."

# Tags: can be used for filtering projects.
# Example: `tags = ["machine-learning", "deep-learning"]`
tags = ["Seismic Anisotropy", "Surface Waves", "Ambient Noise"]

# Optional external URL for project (replaces project detail page).
external_link = ""

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

math = true

# Featured image
# To use, add an image named `featured.jpg/png` to your project's folder. 
[image]
  # Caption (optional)
  caption = "Russell et al. (2020)"
  
  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Center"
  
  # Show image only in page previews?
  preview_only = true
+++

## Introduction
At a broad scale, evolution of the oceanic lithosphere-asthenosphere system follows a relatively simple half-space cooling model with a rigid plate overlying weaker asthenosphere that thickens with distance from the ridge. However, in detail observations such as [seafloor shallowing relative to half-space cooling](https://www.nature.com/articles/359123a0) at ages >70 Ma and seafloor [gravity lineations](https://agupubs.onlinelibrary.wiley.com/doi/abs/10.1029/JB091iB03p03507) suggest deviations from this simple model. One candidate to explain these observations is small-scale convection, which has been proposed in the form of so-called ["Richter rolls"](http://www.mantleplumes.org/images3/SSCFig1_550.jpg). These convective cells are estimated to be ~200 km in diameter and bring hot material toward the Earth's surface.

## The YoungORCA experiment
The [YoungORCA](https://pacificorca.wordpress.com/2018/04/09/young-pacific-orca-sets-sail/) project consists of an array of 30 broadband ocean-bottom seismometers (OBS) and aims to directly image small-scale convection.  Located at ~40 Ma seafloor in the south Pacific, the array sits on distinct gravity undulations of ~200 km wavelength that may indicate convective cells in the current-day asthenosphere.
{{< figure src="array.png" title="Map of the YoungORCA array with high-pass filtered free-air gravity anomaly in the background. Note the northwest-southeast trending gravity anomalies." numbered="false" width="50%">}}

My research utilizes surface waves (Rayleigh and Love) to investigate the physical, chemical, and thermal structure of the uppermost mantle beneath the array. These waves range in sensitivity from the crust down to ~300 km depth in the uppermost asthenosphere. From surface-wave observations of phase velocity, we constrain the shear velocity structure in the upper mantle, as well as seismic anisotropy.

## Preliminary findings
We find evidence for small-scale convection beneath the YoungORCA array. Seismic anisotropy in the asthensophere reveals a fast direction rotated significantly (~25º) from the absolute plate motion (APM) direction, at odds with the predicted large-scale mantle circulation pattern. This clockwise rotation in anisotropy relative to APM may be explained by pressure-drive flow associated with the South Pacific Superswell. As hot mantle material upwells and impinges on the lithosphere, mantle should flow radially away from the plume head, producing a secondary flow direction that is consistent with what we observe.

{{< figure src="featured.png" title="Elastic structure of the uppermantle beneath the YoungORCA array. Seismic anisotropy in the asthenosphere is rotated from the absolute plate motion, indicating small-scale convection." numbered="false" width="90%">}}
