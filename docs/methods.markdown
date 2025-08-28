---
layout: page
title: Methods
permalink: /methods/
---

## Sampling

We used wildtype ABCxTu zebrafish to carry out our source tracking experiment. These fish were reared at the Huestis Zebrafish Facility at the University of Oregon. Using the standard protocols (as recorded in the The Zebrafish Book), we crossed 10 male/female pairs in individual crossing tanks. The crossing tanks have a false bottom that allows the eggs to fall through a mesh for collection. This prevents adults from eating the eggs, but also limits any contact between eggs and parents post fertilization. To explore the role of water as a source of microbes and as a medium of transmission from parent to egg, we made sure to collect both water from the facility outlet (having no contact with adult fish) and from the crossing tank (more fish-y than the facility water).

![sources](images/sampling_sources.png)

After the adults successfully bred, we euthanized them and removed gut and skin tissues for DNA extraction to explore the adult gut microbiomes and skin microbiomes as potential sources to the offspring. We rinsed fertilized eggs with embryo media (EM) and transferred them to Petri dished (3 per clutch or adult pair).

Sampling occurred at 0 days post fertilization (dpf), 2 dpf, 5 dpf and 7 dpf. At 3 dpf, eggs hatch into larvae. To test for the effect of chorions as a means of transmitting egg microbes to larvae, we removed half of the larvae to new Petri dishes with fresh EM. We started feeding larvae rotifers at 5 dpf, after collecting the 5 dpf samples. Larvae were fed again at 6 dpf. The 5 dpf and 6 dpf rotifer cultures were sampled to determine how food acts as a source the larvae microbiome.

![sampling](images/sampling_times.png)

We used 16S rRNA sequencing to survey the microbiomes of our samples. All data analyses were conducted in R. We used the R package *FEAST*[^1] to estimate the contributions of the different source communities (parents, water, and rotifers) to the sink communties (eggs and larvae). We also examined how previous development stages contribute microbes to later development stages (i.e. 0 dpf eggs to 2 dpf, 5 dpf and 7 dpf) by running FEAST with development stages also considered sources. We used Baysian regression models[^2] to determine whether source contributions changed over development. To identify putatively transmitted taxa, we used the package *indicspecies* to perform an Indicator Species Analysis [^3]. 

[^1]: Shenhav L, Thompson M, Joseph TA, Briscoe L, Furman O, Bogumil D, et al. FEAST: fast expectation-maximization for microbial source tracking. Nat Methods. 2019 Jul;16(7):627–32. 

[^2]: Bürkner PC. brms : An R Package for Bayesian Multilevel Models Using Stan. J Stat Soft. 2017. Available from: http://www.jstatsoft.org/v80/i01/

[^3]: De Cáceres M, Legendre P. Associations between species and groups of sites: indices and statistical inference. Ecology. 2009 Dec;90(12):3566–74. 
