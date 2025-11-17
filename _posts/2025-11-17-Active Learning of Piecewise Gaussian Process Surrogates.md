---
title:  "Active Learning of Piecewise Gaussian Process Surrogates"
header:
    teaser: "/assets/images/Active Learning of Piecewise Gaussian Process Surrogates.png"
excerpt: "New paper has been published"
author: "sangwon"
categories:
  - Paper summary
tags:
  - Piecewise Regression
  - Divide-and-Conquer 
  - Bias–Variance Tradeoff
  - Sequential Design
  - Active Learning
  
last_modified_at: 2025-11-17
---
<img align="center" width="746" height="784" style="border: 1px solid white" src="/assets/images/Active Learning of Piecewise Gaussian Process Surrogates.png">

Title : Active Learning of Piecewise Gaussian Process Surrogates

Authors : Chiwoo Park, Robert Waelder, Bonggwon Kang, Benji Maruyama, Soondo Hong, Robert Gramacy

Abstract : Active learning of Gaussian process (GP) surrogates has been useful for optimizing experimental designs for physical/computer simulation experiments, and for steering data acquisition schemes in machine learning. In this paper, we develop a method for active learning of piecewise, Jump GP surrogates. Jump GPs are continuous within, but discontinuous across, regions of a design space, as required for applications spanning autonomous materials design, configuration of smart factory systems, and many others. Although our active learning heuristics are appropriated from strategies originally designed for ordinary GPs, we demonstrate that additionally accounting for model bias, as opposed to the usual model uncertainty, is essential in the Jump GP context. Toward that end, we develop an estimator for bias and variance of Jump GP models. Illustrations, and evidence of the advantage of our proposed methods, are provided on a suite of synthetic benchmarks, and real-simulation experiments of varying complexity.

[https://doi.org/10.48550/arXiv.2301.08789]