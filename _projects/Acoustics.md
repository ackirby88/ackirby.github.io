---
layout: page
title: Acoustics
description: Computation Aeroacoustics via the FW-H formulation.
img: assets/img/sphere.10000.png
importance: 4
category: Software
---

In addition to studying the fluid dynamics of various renewable and aerospace applications, we have developed a computational aeroacoustics capability to predict noise signatures at far-field observers. Our noise-prediction strategy is based on a high-order, adaptive overset mesh flow solver combined with a noise-propagation approach based on the direct integration of the Ffowcs Williams-Hawkings (FW-H) equation.

<h2>Far-field Acoustics of Flow Over a Sphere</h2>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sphere.1000.png" title="Flow at Reynolds number 1,000 over a sphere." class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sphere.10000.png" title="FW-H acoustic comparison." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Instantaneous vorticity contours for the Reynolds numbers 1,000 (left) and 10,000 (right)  flow over a sphere.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sphere.1000.fwh.png" title="FW-H acoustic comparison at Reynolds number 1,000." class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sphere.10000.fwh.png" title="FW-H acoustic comparison at Reynolds number 10,000." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    FW-H acoustic signature reconstruction for Reynolds numbers 1,000 (left) and 10,000 (right) flows over a sphere at Mach 0.3.
</div>

The use of high-order numerical methods helps profoundly in the integration of the FW-H equation enabling accurate noise prediction for various applications.
