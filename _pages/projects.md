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

## Neural Networks for Geospatial Data

Analysis of geospatial data has traditionally been model-based, with a fixed mean model, customarily specified as a linear regression on the covariates, and a Gaussian process covariance model, encoding the spatial dependence. While non-linear machine learning algorithms like neural networks are increasingly being used for spatial analysis. We propose **NN-GLS** that embeds neural networks directly within the traditional Gaussian process (GP) geostatistical model to accommodate non-linear mean functions while retaining all other advantages of GP, like explicit modeling of the spatial covariance and predicting at new locations via kriging.

We provide the first large-sample results for any neural network algorithm for irregular spatial data, including the consistency and finite sample concentration rates which quantifies the need to accurately model the spatial covariance in neural networks for dependent data. 

In both fixed effect estimation and spatial prediction tasks, NN-GLS provides superior performance over other competing methods.

**Related publications**


<div style="display: flex; justify-content: space-around;">
  <figure>
    {% include figure.liquid path="assets/img/MISE_dim5_main.png" alt="Image 1 description" width="45%" %}
    <figcaption style="display: none;">Image 1 description</figcaption>
  </figure>
  <figure>
    {% include figure.liquid path="assets/img/MISE_dim5_main.png" alt="Image 2 description" width="45%" %}
    <figcaption style="display: none;">Image 2 description</figcaption>
  </figure>
</div>

---

## GeospaNN: a formal implementation of the Neural Networks for geospatial data

  {% include figure.liquid path="assets/img/MISE_dim5_main.png" alt="Image 1 description" width="45%" %}
  {% include figure.liquid path="assets/img/MISE_dim5_main.png" alt="Image 2 description" width="45%" %}

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/updated_NN_figure.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/updated_NN_figure.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
