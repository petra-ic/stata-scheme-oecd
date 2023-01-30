# Overview

These two stata schemes efficiently implement a look that is consistent with the OECD visual identity. They are based on the modern scheme by mdroste and the internal R scheme by Mauricio Vargas.

# Installation

Installing and using these schemes is straightforward. Install from this GitHub repository and load by typing the following commands:

1. Dark blue theme

```stata
net install scheme-oecddarkblue, from("https://raw.githubusercontent.com/petra-ic/stata-scheme-oecd/main/")
set scheme oecddarkblue, perm
```

2. Colourful theme

```stata
net install scheme-oecdcolourful, from("https://raw.githubusercontent.com/petra-ic/stata-scheme-oecd/main/")
set scheme oecdcolourful, perm
```

# Fonts

The R scheme uses Arial Narrow, which works well in charts. You can set this as follows:


```stata
graph set window fontface "Arial Narrow"
```

Other nice fonts for web and latex papers respectively are: 

```stata
graph set window fontface "Mullish"
graph set window fontface "LMRoman10-regular"
```

They have to be downloaded separately.

# Two-way bar chart

For stacked two-way bar charts, add this to prevent them from hovering above the axis and the x-axis ticks from showing:

```stata
xlabel(, tposition(outside)) plotregion(margin(b = 0))
```

