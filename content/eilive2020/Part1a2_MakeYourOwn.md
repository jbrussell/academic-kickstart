+++
title = "Making Your Own Maps With trinket.io"
date = 2020-05-12T00:00:00
# lastmod = 2018-09-09T00:00:00
draft = false  # Is this a draft? true/false
toc = true  # Show table of contents? true/false
type = "docs"  # Do not modify.
# Add menu entry to sidebar.
linktitle = "Make Your Own Maps"
[menu.eilive2020]
  parent = "Part 1: Data Storytelling in Python"
  weight = 3
+++

\

Now we will use [trinket.io](https://trinket.io/) to make our own earthquake maps with Python. Trinkets allow you to run snippets of Python code directly in your internet browser! Just click the <i class="fas fa-play"></i> button in the top bar to run the code.

\
\

# Starting simple
Our first example is a simple sinusoid with frequency $f$ and amplitude $A$:

$$ y = A \sin (f x) $$

Try making changes to the code and rerunning it to see how the output changes.  
*(We will be returning to waves in Part 2!)*

<iframe src="https://trinket.io/embed/python3/bbda930e37?start=result" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

\
\

# Plotting Earthquakes
Trinkets can also include data files. Here we have added a file called `earthquakes.csv`, which contains a comma-separated list of all earthquakes greater than magnitude 5.0 from 2015--2020. The columns of the data file are `time`, `latitude`, `longitude`, `depth`, and `mag` and can be loaded into a Pandas dataframe using a single line:

``` python
import pandas as pd

# Load earthquake data
df = pd.read_csv("earthquakes.csv")
```
The trinket below loads the data and plots it on top of a PNG image of the Earth. We have the option to filter the data based on depth (`min_depth`, `max_depth`) and magnitude (`min_mag`, `max_mag`).

\

{{% alert note %}}
* Where do deep earthquakes most commonly occur? Why?
* Are there more large or small magnitude earthquakes?
{{% /alert %}}

<iframe src="https://trinket.io/embed/python3/a89c18431a?start=result" width="100%" height="356" frameborder="0" marginwidth="0" marginheight="0" allowfullscreen></iframe>

\
\

{{% alert note %}}
* **CHALLENGE:** Try building your own filter that only shows earthquakes within a specified latitude and longitude range.

Hint: Try modifying these lines in the trinket code to filter `df.latitude` and `df.longitude`
``` python
#--------- FILTER DATA ----------#
index_depth = (df.depth >= min_depth) & (df.depth <= max_depth)
index_mag = (df.mag >= min_mag) & (df.mag <= max_mag)
df_filt = df[index_depth & index_mag]
```
{{% /alert %}}



