---
title: 'Kepler Mapper: A flexible Python implementation of the Mapper algorithm.'
tags:
 - Python
 - Mapper
 - Topological Data Analysis
authors:
 - name: Hendrik Jacob van Veen
   affiliation: 1
 - name: Nathaniel Saul
   orcid: 0000-0002-8549-9810
   affiliation: 2
 - name: David Eargle
   orcid: 0000-0002-4056-8114
   affiliation: 3
 - name: Sam W. Mangham
   orcid: 0000-0001-7511-5652
   affiliation: 4
affiliations:
 - name: Nubank
   index: 1
 - name: Department of Mathematics and Statistics, Washington State University Vancouver
   index: 2
 - name: Leeds School of Business, University of Colorado Boulder
   index: 3
 - name: Department of Electronics & Computer Science, University of Southampton, Southampton, SO17 1BJ, UK
   index: 4
date: 12 February 2018
bibliography: paper.bib
---

# Summary

Topological data analysis (TDA) is a field analysis focused on understanding the shape and structure of complex data. By computing topological descriptors of data such as connected components, loops, and voids, we are better able to find hidden relationships among noisy and high-dimensionality data [@edelsbrunner2010computational], [@carlsson2009topology]. However, raw TDA metrics cannot be readily visualized. To address this gap, [@Singh2007] developed the Mapper algorithm in order to facilitate graphical exploration of data topoloigcal structures. The work of [@Lumetal2013] sparked widespread interest in the Mapper technique by demonstrating its use in multiple domains, including political science, biology, and sports analytics.

This library, Kepler Mapper, is a Python implementation of the Mapper algorithm as first described in the paper “Topological Methods for the Analysis of High Dimensional Data Sets and 3D Object Recognition” [@Singh2007]. Kepler Mapper presents an intuitive interface for the Mapper algorithm along with multiple comprehension methods for visualizing the network graph that Mapper produces.
We leverage Scikit-Learn API-compatible cluster and scaling algorithms to construct network graphs in a flexible and user-friendly way.
We also an provide extensive suite of tutorials detailing the use of Kepler Mapper for simple and complex use cases.

![Example Kepler Mapper graph visualization using the Wisconsin Breast Cancer Dataset [@Dua:2019]](http://i.imgur.com/ewjRodK.png)


# Library Details

Kepler Mapper provides an object-oriented API for constructing lenses and building Mapper. The module employs the [strategy pattern](https://en.wikipedia.org/wiki/Strategy_pattern), giving users control over clustering algorithm, covering scheme, and nerve scheme. This allows the module to be flexible for many use cases. Clustering strategies follow the Scikit-Learn clusterer interface [@scikit-learn]. We provide similar interfaces for `Cover` classes and `Nerve` classes as well as default implementations of those classes that are most commonly found in the literature.

Visual exploration is a critical aspect of Mapper analysis. For this, we provide multiple methods for visualization. For interactive visualization and exploration in the browser, the Mapper class can create a visual HTML interface utilizing [D3.js](https://d3js.org/). For use with [Jupyter](https://jupyter.org/) or other embedded purposes, we provide a visualization interface utilizing [Plotly](https://plot.ly/). For static visualizations, we provide an adapter so that visualization functionality from [networkx](https://networkx.github.io/) and [matplotlib](https://matplotlib.org/) can be used.


# Source Code

The source code for Kepler Mapper is available on Github through the Scikit-TDA organization [github.com/scikit-tda/kepler-mapper](https://github.com/scikit-tda/kepler-mapper). Complete documentation can be found at [kepler-mapper.scikit-tda.org](https://kepler-mapper.scikit-tda.org). 

# Acknowledgements

Nathaniel Saul was partially supported by NSF DBI-1661348 and by Washington NASA Space Grant Consortium, NASA Grant #NNX15AJ98H.

# References
