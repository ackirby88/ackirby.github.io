---
layout: page
title: WAKE3D
description: Learn about our CFD framework for wind energy and aerospace applications.
img: assets/img/WAKE3D.png
importance: 2
category: Software
---

The primary CFD framework we have devoloped is known as WAKE3D, which stands for the Wyoming Wind and Aerospace Applications Komputation Environment.
The framework is derived to have a flexible solver and mesh system paradigm in order to perform simulations for a large class of problems in aerospace and wind energy.
It is designed to support a dynamic overset system using multiple flow solvers and multiple computational meshes, 
where the mesh system generally consists of a collection of near-body and off-body meshes. 
The near-body meshes are inherently unstructured to model the complex geometry and resolve boundary layers of wind turbine or aircraft bodies. 
The off-body mesh is a generally a dynamically adaptive Cartesian grid system, which allows for efficient flow solvers, efficient storage, and ease of AMR implementation. 

<h2>Overset Grids</h2>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sphere.overset.vorticity.png" title="Overset flow over a sphere." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Instantaneous vorticity contours for the Re=10,000 flow over a sphere using the overset mesh paradigm. The near-body mesh (shown) is trimmed to a distance of 2.0R.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/SiemensOversetMeshOverlay.png" title="Overset adaptive mesh of a wind turbine." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Siemens SWT-2.3-93 Wind Turbine overset meshes.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/CRM.AMR.mesh.png" title="Overset adaptive mesh of CRM aircraft." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    NASA Common Research Model (CRM) off-body mesh adapted to outer lining of the trimmed near-body unstructured mesh. dg4est is able to accept point locations for adapting its mesh.
</div>
