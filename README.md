# Overview

These three stata schemes efficiently implement a look that is consistent with the OECD visual identity guidelines and the existing Excel and R schemes. They are based on the modern scheme by mdroste and the internal R scheme by Mauricio Vargas.

# Installation

Installing and using these schemes is straightforward. Install from this GitHub repository and load by typing the following commands:

1. Dark blue scheme

```stata
net install scheme-oecddarkblue, from("https://raw.githubusercontent.com/petra-ic/stata-scheme-oecd/main/")
set scheme oecddarkblue, perm
```

2. GG dark blue scheme - charts have a grey background and white gridlines, otherwise same as 1.)

```stata
net install scheme-ggoecddarkblue, from("https://raw.githubusercontent.com/petra-ic/stata-scheme-oecd/main/")
set scheme ggoecddarkblue, perm
```

3. Colourful scheme

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

# Two-way bar chart and other add-ons

Some features are unfortunately impossible to regulate within the scheme itself but can be easily fixed with add-on code on the fly.

For stacked two-way bar charts, add this to prevent them from hovering above the axis and the x-axis ticks from showing:

```stata
xlabel(, tposition(outside)) plotregion(margin(b = 0))
```

For the 'ggplot' inspired scheme with dark background, add this if you also want the legend to have grey background. 

```stata
region(color(gs14))
```
