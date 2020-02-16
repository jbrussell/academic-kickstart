+++
title = "OBSrange: A New Tool for the Precise Remote Location of Ocean-Bottom Seismometers"
date = 2019-08-01T00:00:00
draft = false

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["**J.B. Russell**", "Z. Eilon", "S.G. Mosher"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference paper
# 2 = Journal article
# 3 = Manuscript
# 4 = Report
# 5 = Book
# 6 = Book section
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "*Seismological Research Letters*"
publication_short = "*Seismological Research Letters*"

# Abstract and optional shortened version.
abstract = "Reliable instrument recoverability and data quality rely on accurate estimates of instrument locations on the seafloor. However, freely available software for this estimation does not currently exist. We present OBSrange, an open-source tool for robustly locating ocean-bottom seismometers (OBSs) on the seafloor using acoustic transponder ranging data. Available in both MATLAB and Python (see Data and Resources), the algorithm inverts two-way acoustic ranging travel-time data for instrument location, depth, and average water sound speed with the ability to accurately account for ship velocity, ray refraction through the water column specific to the region, and a known lateral offset between the ship’s Global Positioning System (GPS) receiver and acoustic transponder. The tool provides comprehensive estimates of model parameter uncertainty including bootstrap uncertainties for all four parameters as well as an F-test grid search providing a 3D confidence ellipsoid around each station. \n\n We validate the tool using a synthetic travel-time dataset and find average horizontal location errors on the order of ∼4 m for an instrument at 5000 m depth. An exploration of survey geometries shows significant variation in location precision depending on the pattern chosen. We explore the trade-off between survey length and location uncertainty to quantitatively inform cruise planning strategies. The optimal survey radius for resolving instrument location depends on water depth and desired precision and nominally ranges from 0.75–1 nautical mile (NM) at 5000 m water depth to ∼0.25 NM at 500 m depth. Radial legs toward and away from the instrument are crucial for resolving the depth-water velocity trade-off, and thus circle surveys should be avoided. Line surveys, common for active source experiments, are unable to resolve the instrument location orthogonal to the survey line. \n\n We apply our tool to the 2018 Young Pacific OBS Research into Convecting Asthenosphere (ORCA) deployment in the south Pacific yielding an average root mean square data misfit of 1.96 ms with an average instrument drift of ∼170 m. Observed drifts reveal a clockwise rotation pattern of ∼500 km diameter that resembles a cyclonic mesoscale gyre observed in the geostrophic flow field, suggesting a potential application of accurate instrument drifts as a novel proxy for depth-integrated flow through the water column."
abstract_short = "We present a new tool for locating seismometers on the seafloor and use it to identify a large-scale gyre in the south Pacific."

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["deep-learning"]` references 
#   `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects = ["OBS_range"]

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["ocean bottom seismology","instrumentation","open-source software"]

# Links (optional).
url_pdf = "pdf/Russell_et_al_2019_SRL.pdf"
url_preprint = ""
url_code = "https://github.com/jbrussell/OBSrange"
url_dataset = "https://seiscode.iris.washington.edu/projects/obsrange/files"
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""

# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
# url_custom = [{name = "Dataset", url = "https://seiscode.iris.washington.edu/projects/obsrange/files"}]

# Digital Object Identifier (DOI)
doi = "10.1785/0220180336"

# Does this page contain LaTeX math? (true/false)
math = true

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
[image]
  # Caption (optional)
  caption = ""

  # Focal point (optional)
  # Options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
  focal_point = "Bottom"
  
  preview_only = false
  
# [header]
#   image = "featured_nomelt.png"

+++
