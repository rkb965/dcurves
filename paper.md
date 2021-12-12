---
title: 'dcurves: An R package for model evaluation'
tags:
  - R
  - model evaluation
  - decision theory
authors:
  - name: Daniel D. Sjoberg
    orcid: 0000-0003-0862-2018
    affiliation: 1
  - name: Emily Vertosick
    affiliation: 1
affiliations:
 - name: Memorial Sloan Kettering Cancer Center
   index: 1
date: 11 December 2021
bibliography: paper.bib
---

# Summary

Diagnostic and prognostic models are typically evaluated with measures of accuracy, such as the area-under-the-curve or the Brier score, that do not address clinical consequences.
Decision-analytic techniques allow assessment of clinical outcomes but generally require collection of extensive additional information and are cumbersome to apply to models that yield a risk estimate on a continuous scale from zero to one. 
Decision curve analysis (DCA) allows incorporation of clinical consequences, thus addressing the question of whether a model would do more good than harm, but is able to do so without excessive extraneous data.
The result of a DCA is a graph drawn by plotting threshold probability on the x-axis and net benefit on y-axis, illustrating the trade-offs between benefit (true positives) and harm (false positives) as the threshold probability is varied across a range of reasonable threshold probabilities.
The evaluation of a model is compared on the graph to two competing strategies, 1. a "treat all" strategy where the model is ignored and the decision is to treat for all patients, and 2. a "treat none" where the model results are once again ignored an no intervention is made.

![](https://github.com/ddsjoberg/dcurves/raw/joss/data-raw/dca-example.png)

``dcurves`` is an R package for model evaluation using DCA.
The package includes functionality for evaluating models predicting binary endpoints described in the initial DCA publication [@vickers2006decision].
The package also includes extensions for survival and competing event endpoints [@vickers2008extensions] and case-control study designs [@pfeiffer2020estimating].

DCA has been used in thousands research publications.
Previously, users needed to download unpublished scripts from [decisioncurveanalysis.org](decisioncurveanalysis.org) and implement the methods in R, SAS, or Stata (all software written by the authors of the ``dcurves`` package).
The ``dcurves`` R package represents an evolutionary jump in the previous scripts available, with improved API, thorough documentation, unit testing, and a release of the package on CRAN. 


# Acknowledgements

We acknowledge Dr Andrew Vickers for developing the methods and theory for performing decision curve analysis.

# References
