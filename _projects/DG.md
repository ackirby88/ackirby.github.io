---
layout: page
title: DG Methods
description: High-order discretizations for the compressible Navier-Stokes equations.
img: assets/img/sphere.png
importance: 2
category: Software
---

My primary research revolves around developing high-fidelity numerical methods for Computional Fluid Dynamics problems with applications to Wind Energy and Aerospace.
This involves principally writing code de novo as the problems we target require leadership-class supercomputing capabilities. 
My research vision is to develop highly-scalable and highly-efficient algorithms coupling scientific computation with data-informed modeling suitable for leadership-class heterogeneous supercomputers and to facilitate industry-ready engineering simulations tools applicable to the fields of aerospace and renewable energy. Some of the codes I have developed are outlined here.

<h2>dg4est</h2>


<h3>Unstructured Curved Geometry</h3>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/NACA0012.P3.Q2.Mach.gif" title="3D NACA0012 curved grid." class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<h3>Adaptive Mesh Refinement</h3>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sphere.Re10000.vorticity.gif" title="Sphere turbulent wake." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Adaptive mesh refinement allows for long turbulent wake tracking as illustrated in this flow over a sphere.
</div>

<h2>CartDG</h2>

