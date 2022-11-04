---
layout: page
title: Rotorcraft
description: Learn more about rotorcraft and propellor simulations simulations using WAKE3D.
img: assets/img/publication_preview/S76Rotor-WAKE3D.jpg
importance: 1
category: Applications
---

Simulating rotorcraft such as helicoptors or quadcoptors is essentially the same process as simulating wind turbines. 
Here we study rotors in hover formation to understand performance and fluid dynamics which cause the turbulent structures in the waterfall-like wake.

<h2>Sikorsky S76 Rotorcraft Blade and Hub Simulation</h2>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
	{% include youtube.html id='VqLgTunM7i4' class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Isocontour visualization of the rotor wash colored by velocity magnitude.
</div>
The hover performance of a four-bladed Sikorsky S76 rotor is studied using the high-order discontinuous Galerkin (DG) method. Time accurate Navier-Stokes calculations are performed using the WAKE3D code, which combines solution technologies in a multi-mesh, multi-solver paradigm through a dynamic overset framework that employs a finite-volume unstructured mesh Navier-Stokes method as a near-body solver (NSU3D) and a high-order adaptive discontinuous Galerkin discretization as an off-body solver (dg4est). The rotor with a swept-tapered tip is simulated at tip Mach number 0.65 and Reynolds number 1.2 million based on the reference chord. A constant coning angle of 3.5-degrees is applied. In this framework, we study the effect of time step size and sub-iterations on the integrated force parameters. The effect of the maximum order of accuracy of the hp-adaptive discretization in the off-body solver on solution accuracy and efficiency is also investigated. Thrust coefficient, torque coefficient, and figure of merit are calculated and compared with available data in the literature, and demonstrate strong agreement. In general, higher-order off-body simulations are found to result in a better accuracy and computation cost metrics.

<h2>Helicopter-Ship Wake Interaction on SFS2 Geometry.</h2>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include vimeo.html id='256818241?h=c7ac07cb95&loop=1' %}
    </div>
</div>
Within our WAKE3D framework, we can add multiple static or dyanamic bodies, forming complex flow interactions such as those found of a ship mast wake propagating into the inflow of rotor blades. Here we see isosurfaces of vorticity magnitude illuminating the Simple Frigate Shape (SFS2) wake impinging on UH60A rotorcraft blades. This scenario is very common in Naval aircraft/helicopter landings at sea. Additionally, the WAKE3D framework can incorporate atmospheric inflow conditions through precursor simulations done by WRF or NREL's SOWFA.

<article>
    {%- include Rotorcraft_papers.html %}
</article>
