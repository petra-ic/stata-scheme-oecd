# Overview

These two stata schemes efficiently implement a look that is consistent with the OECD visual identity. They are based on the modern scheme by mdroste and the internal R scheme by Mauricio Vargas.

# Installation

Installing and using these schemes is straightforward. Install from this GitHub repository and load by typing the following command at the command lines:

1. Dark blue theme

net install scheme-oecddarkblue, from("https://raw.githubusercontent.com/petra-ic/stata-scheme-oecd/main/")
set scheme oecddarkblue, perm

2. Colourful theme

net install scheme-oecdcolourful, from("https://raw.githubusercontent.com/petra-ic/stata-scheme-oecd/main/")
set scheme oecdcolourful, perm


# Fonts

The R scheme uses Arial narrow, you can set this as follows:

graph set window fontface "Arial Narrow"

Other nice fonts for web and latex papers respectively are: 

graph set window fontface "Mullish"
graph set window fontface "LMRoman10-regular"

They have to be downloaded separately.

# Two-way bar chart

For stacked two way bar charts, add this to prevent them from hovering above the axis and from the x-axis ticks showing:

xlabel(2010(1)2020, tposition(outside)) plotregion(margin(b = 0))
