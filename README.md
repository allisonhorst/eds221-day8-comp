# EDS 221 - Day 8 Computational Session

Customizing data visualizations with ggplot2

### Required packages: 

#### General use packages:
library(tidyverse)
library(here)
library(janitor)

#### Specifically for plots:
library(patchwork)
library(ggrepel)
library(gghighlight)
library(paletteer)
library(ggExtra)
library(ggbeeswarm)

#### And for another dataset we'll explore:
library(gapminder)

## Lizard size measurement data

Our data are a curated subset from [Jornada Basin Long Term Ecological Research site](https://lter.jornada.nmsu.edu/) in New Mexico, part of the US Long Term Ecological Research (LTER) network: 

- Lightfoot, D. and W.G. Whitford. 2020. Lizard pitfall trap data from 11 NPP study locations at the Jornada Basin LTER site, 1989-2006 ver 37. Environmental Data Initiative. https://doi.org/10.6073/pasta/4a6e258fb49c31e222ecbbcfd128967f

From the data package: "This data package contains data on lizards sampled by pitfall traps located at 11 consumer plots at Jornada Basin LTER site from 1989-2006. The objective of this study is to observe how shifts in vegetation resulting from desertification processes in the Chihuahaun desert have changed the spatial and temporal availability of resources for consumers. Desertification changes in the Jornada Basin include changes from grass to shrub dominated communities and major soil changes. If grassland systems respond to rainfall without significant lags, but shrub systems do not, then consumer species should reflect these differences. In addition, shifts from grassland to shrubland results in greater structural heterogeneity of the habitats. We hypothesized that consumer populations, diversity, and densities of some consumers will be higher in grasslands than in shrublands and will be related to the NPP of the sites. Lizards were captured in pitfall traps at the 11 LTER II/III consumer plots (a subset of NPP plots) quarterly for 2 weeks per quarter. Variables measured include species, sex, recapture status, snout-vent length, total length, weight, and whether tail is broken or whole. This study is complete." 

There are 16 total variables in the `lizards.csv` data we'll read in. The ones we'll use in this workshop are: 

- `date`: data collection date
- `scientific_name`: lizard scientific name
- `common_name`: lizard common name
- `site`: research site code
- `sex`: lizard sex (m = male; f = female; j = juvenile)
- `sv_length`: snout-vent length (millimeters)
- `total_length`: body length (millimeters)
- `toe_num`: toe mark number
- `weight`: body weight (grams)
- `tail`: tail condition (b = broken; w = whole)


