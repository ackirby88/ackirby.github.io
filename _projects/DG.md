---
layout: page
title: dg4est
description: High-order discretizations for the compressible Navier-Stokes equations with adaptive mesh refinement.
img: assets/img/sphere.png
importance: 1
category: Software
---

My primary research revolves around developing high-fidelity numerical methods for Computional Fluid Dynamics problems with applications to Wind Energy and Aerospace.
This involves principally writing code de novo as the problems we target require leadership-class supercomputing capabilities. 
My research vision is to develop highly-scalable and highly-efficient algorithms coupling scientific computation with data-informed modeling suitable for leadership-class heterogeneous supercomputers and to facilitate industry-ready engineering simulations tools applicable to the fields of aerospace and renewable energy.

The primary software I've developed over the past five years in **dg4est** which is a discontinuous Galerkin method leveraging the [p4est](https://github.com/cburstedde/p4est) framework for managing and adapting the grid topology. **dg4est** is the primary off-body CFD solver within the **WAKE3D** framework and has been utilized in many applications. Some of the features of **dg4est** are outlined here.

## dg4est
  - 2D and 3D Simulations
    - Cartesian and unstructured (high-order curvilinear) quad/hex meshes
    - [gmsh](https://gmsh.info/) mesh reader (binary, ascii): 2.X, 4.X formats
    - Dynamic adaptive mesh refinement (non-conforming) with [p4est](https://github.com/cburstedde/p4est)
  - High-Order Spatial Discretizations: Discontinous Galerkin
    - Nodal tensor-product basis functions: Lagrange polynomials (up to 24th order)
    - Modal tensor-product basis functions: Legendre polynomials
    - Quadrature Integration (collocation/over-integrable): Gauss-Legendre (2p+1 accuracy), Lobatto-Gauss (2p-1 accuracy)
    - Kinetic energy-preserving scheme based on flux differencing: Pirozzoli, Kennedy & Gruber
    - Riemann solvers: Lax Friedrichs, Roe (with entropy fix)
    - Diffusion solvers: SIP, BR2
    - Governing equations
      - compressible Euler equations (inviscid)
      - compressible Navier-Stokes equations (viscous)
    - LES subgrid-scale models
      - constant Smagorinsky
      - dynamic Smagorinksy
      - WALE
    - Sources: gravity, Coriolis
    - Boundary conditions: free-stream, slip wall (symmetry), non-slip wall, characteristic, total inlet, static pressure outlet, periodic
  - High-Order Temporal Discretizations
    - Explicit Time Stepping
      - RK1: Forward Euler
      - RK2: SSP (strong-stability preserving)
      - RK3: SSP
      - RK4: 3/8-rule
    - Implicit Time Stepping (dual time stepping: RK-optimized smoothers)
      - BDF-1
      - BDF-2
      - Space-Time DG (up to 10th order)
      - Preconditioned FIRK 2-stage Gauss-Legendre
      - Preconditioned FIRK 2-stage Radau IIA
  - p-Multigrid Solution Convergence Acceleration (space-time, implicit, steady-state)
      - Full Approximation Scheme (FAS)
      - V-/F-/W-Cycling
  - Acoustic Analysis
    - Ffowcs-Williams Hawkings (FW-H) acoustic-analogy formulation
  - Overset Simulation Infrastructure
    - [TIOGA](https://github.com/jsitaraman/tioga) interface
  - In-situ Data Extraction
    - points, lines, planes, volumes
    - [VisIt Libsim](https://www.visitusers.org/index.php?title=VisIt-tutorial-in-situ) tnterface
    - [SENSEI](https://sensei-insitu.org/) interface
  - VTK Visualization
    - parallel VTU format (VisIt, paraview)
    - High-order VTK Lagrange format (paraview)
  - Post-processing
    - LES SGS TKE
    - Temporal statistics: mean, standard deviation, 95% confidence interval
    - Reynolds stresses
    - Proper Orthogonal Decomposition (POD)/Principal Component Analysis (PCA)
    - MPI wall-clock time histogram viewer
    - Analytical spatial error calculator (order of accuracy verification)
  - Unit Testing (gtest framework) and Regresion Testing

### Future Developments
  - Release the code as open source via GitHub!
  - GPU Implementation using [OCCA](https://github.com/libocca): NVIDIA, AMD, Intel hardware
    - Full GPU offload including AMR (dynamic)
  - Mixed-element meshes (with AMR): tets, pyramids, prisms, hexes
  - Boundary Representation (brep) incorporation for curved-mesh adaption
  - Wall-Modeled Large Eddy Simulation

<h2>Unstructured Curved Geometry</h2>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/NACA0012.P3.Q2.Mach.gif" title="3D NACA0012 curved grid." class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<h2>Adaptive Mesh Refinement</h2>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/sphere.Re10000.vorticity.gif" title="Sphere turbulent wake." class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Adaptive mesh refinement allows for long turbulent wake tracking as illustrated in this flow over a sphere.
</div>

