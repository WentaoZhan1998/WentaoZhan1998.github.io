---
layout: page
title: Research
permalink: /research/
nav: true
nav_order: 3
display_categories: [work, fun]
horizontal: false
---

<!-- pages/projects.md -->

With the rapid advancement of modern technology, data containing spatial information is being generated in increasingly larger volumes and more complex structures, presenting significant statistical challenges to the scientific community. However, I believe that rather than being a burden, the spatial nature represents a valuable opportunity, imbuing datasets with elegance and smoothness. By employing appropriate formulations, we can unlock the full potential of spatial knowledge and extract unique, highly valuable insights from the data. My research has been motivated by the statistical challenges at the forefront of science across various different spatial contexts, which require novel and efficient methodology.

---

## Tensor Covariance Estimation via Kronecker-Structured Sparse Inverse Cholesky

High-dimensional multi-way (tensor) data, examplified by space-time data, pose significant challenges for covariance estimation due to the curse of dimensionality. We introduce a unified framework for scalable estimation of tensor covariances based on a Kronecker-structured sparse inverse Cholesky (KSIC) projection. By leveraging physical or data-driven nearest-neighbor sparsity, KSIC provides a geometry-aware representation that is both statistically interpretable and computationally efficient. Our framework integrates two estimation regimes: a nonparametric estimator that projects the empirical covariance directly onto the manifold; and a parametric estimator that fits generative covariance models.

Theoretically, we establish the conditions for the existence of the KSIC projection and finite-sample concentration rates for the nonparametric regime, proving that the KSIC estimator gainfully exploits cross-mode information and is robust to data scarcity. 

Numerical experiments demonstrate that the proposed KSIC estimators achieve state-of-the-art accuracy and scalability, particularly in settings with high dimensionality and limited sample sizes. We apply KSIC to spatiotemporal temperature anomalies and functional MRI data, demonstrating its broad applicability across diverse multi-way data domains.

**Related publications**
- Zhan, W., & Katzfuss, M. (2026+). Tensor Covariance Estimation via Kronecker-Structured Sparse Inverse Cholesky (Submitted to JASA T&M) [link](https://arxiv.org/abs/2608.14887)

{% include figure.liquid path="assets/img/KSIC.png" caption='Temperature anomalies analysis by KSIC' width="95%" %}

---

## Neural Networks for Geospatial Data

Analysis of geospatial data has traditionally been model-based, with a fixed mean model, customarily specified as a linear regression on the covariates, and a Gaussian process covariance model, encoding the spatial dependence. We propose [NN-GLS](https://www.tandfonline.com/doi/full/10.1080/01621459.2024.2356293) that embeds neural networks directly within the traditional Gaussian process (GP) geostatistical model to accommodate non-linear mean functions while retaining all other advantages of GP, like explicit modeling of the spatial covariance and predicting at new locations via kriging.

We provide the first large-sample results for any neural network algorithm for irregular spatial data, including the consistency and finite sample concentration rates which quantifies the need to accurately model the spatial covariance in neural networks for dependent data. 

NN-GLS admits a representation as a special type of graph neural network, which takes kriging weights for graph convolution. The idea can be easily generalized to a wider range of deep-learning approach, which led to "spatially-informed deep-learning" as a promising future direction.

**Related publications**
- Zhan, W., & Datta, A. (2025). Neural networks for geospatial data. Journal of the American Statistical Association 120 (549), 535-547. [link](https://www.tandfonline.com/doi/full/10.1080/01621459.2024.2356293)


{% include figure.liquid path="assets/img/NN-GLS.png" caption='NN-GLS' width="95%" %}

---

## GeospaNN: A python implementation for NN-GLS

[GeospaNN](https://wentaozhan1998.github.io/geospaNN-doc/) is a package for geospatial analysis using neural networks that explicitly accounts for spatial correlation in the data. The package implements the NN-GLS method and is developed using PyTorch and under the framework of PyG library. GeospaNN is a geographically-informed Graph Neural Network (GNN) for analyzing large and irregular geospatial data, that combines multi-layer perceptrons, Gaussian processes, and generalized least squares (GLS) loss. GeospaNN offers both regression function estimation and spatial prediction. The sparse approximation in NN-GLS allows efficient computation in geospaNN, which scale up to sample sizes of hundreds of thousands.

**Related publications**
- Zhan, W., & Datta, A. (2026). GeospaNN: a Python package for geospatial neural networks. Journal of Open Source Software 11 (117), 8389. [link](https://joss.theoj.org/papers/10.21105/joss.08389.pdf)

{% include figure.liquid path="assets/img/updated_NN_figure.png" width="95%" caption='Architecture of geospaNN' %}

---



<!--
## Multispa: a multi-sample cell-microenvironment analysis tool 

The development of spatial transcriptomics allows for single-cell (or near-single-cell) level sequencing of tissues while preserving spatial information. This technique represents an unprecedented advancement in medical and biological research. For instance, in immunology, immune cells interact with tumor cells through antibody signaling, and the fate of a tumor cell is influenced by the density of immune cells in its microenvironment, which can only depicted by introducing "spatial distance."

In this project, we hypothesize that the relationship between the expression of gene A in tumor cells and the expression of gene B in immune cells within their microenvironment may differ across patient groups (e.g., treatment vs. control).

We introduce Multispa, a statistical tool that leverages spatial information to identify differentially associated gene pairs between groups. Multispa uncovers distinct gene regulatory mechanisms across these groups and holds significant implications for immunotherapy research.

**Related publications**
- Zhan, W., & Ji, H (2025+). Multispa: a Multi-sample Cell-microenvironment Tool for Spatial Transcriptomics  (Manuscript in prepartion)

{% include figure.liquid path="assets/img/Spatial.png" caption='Differential gene regulation' width="95%" %}
-->
