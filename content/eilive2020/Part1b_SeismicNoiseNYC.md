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
  weight = 2
+++

<iframe src="https://trinket.io/embed/python3/600f40f1cf" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>


``` python
import bokeh
from bokeh.models import Line, Span, ColumnDataSource, DatetimeTickFormatter
from bokeh.plotting import figure, output_notebook, show, output_file
import time

# Define figure attributes
p = figure(x_axis_type='datetime',plot_width=800, plot_height=400, sizing_mode = 'scale_width',
           x_range=(df.t_cent.min(),df.t_cent.max()), y_range=([0, df.daily_average.max()*1e9*2]),
           x_axis_label='Date', y_axis_label='Average Ground Displacement (nm)', title='NYC Seismic Noise',
           tools=['save','box_zoom','ywheel_zoom','xwheel_zoom','reset','crosshair','pan'])

# Plot lines for hourly and daily displacement
p.multi_line([df.t_cent,       df.t_cent],
             [df.disp_avg*1e9, df.daily_average*1e9],
             line_color=["lightsteelblue","steelblue"],
             line_width=[2, 4])

# Plot vertical lines marking stay at home and first nyc death
# First need to convert datetime to milliseconds for some reason...
nyc_SAH_ms = time.mktime(nyc_SAH.timetuple())*1000
nyc_1st_ms = time.mktime(nyc_1st.timetuple())*1000
nyc_SAH_start = Span(location=nyc_SAH_ms, dimension='height', line_color='firebrick', line_width=3)
p.add_layout(nyc_SAH_start)
nyc_1st_start = Span(location=nyc_1st_ms, dimension='height', line_color='firebrick', line_width=3)
p.add_layout(nyc_1st_start)

# Show plot in browser
show(p)
# Save local file
output_file(fname+'.html')
```

<!-- layouts/partials/bokeh -->
{{< importBokeh "bokeh/LD.CPNY.2020-02-09.2020-05-07.5_15Hz_1min.BHZ.csv.html" >}}
