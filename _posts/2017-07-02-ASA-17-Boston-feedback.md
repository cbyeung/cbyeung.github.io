---
layout: post
title:  ASA 17 Boston feedback
date:   2017-07-02
categories: ultrasound bubble clot 3dprint ANSYS simulation FEA
tags: ultrasound bubble clot 3dprint ANSYS simulation FEA
---
Paul Barbone of Boston University, the brilliant mathematical modeller, exceedingly patiently explained to me the pitfalls of the simulations I have been running in ANSYS, and gave me suggestions for how to move forward.

Take it away Paul.

# Pitfalls
- When meshing a volumetric mesh in ANSYS, pick a solid element with more nodes, ergo more degrees of freedom. Doing so facilitates approximating nonlinear (e.g. parabolic) internal stresses. Failure to do so could compel ANSYS to use more elements than it can handle.  Oddly this does *not* accord with my experience.
- ANSYS handles Poisson's ratios &le; 0.45 as one would expect, but since materials that possess a Poisson's ratio 0.45 < &nu; &le; 0.5 are unusual, ANSYS behaves erratically if &nu; = 0.4999999. ANSYS gets into a state called "locking," where the object does not deform at all. Look online for a fix. Oddly this does *not* accord with my experience either.

# Going forward towards clot-bubble simulation
- The most rudimentary is probably to add a node to the middle of a rope and apply an oscillatory force in accordance with Rayleigh-Plesset.
- Brute force approach: buy COMSOL, push bubbles and liquid through a clot.
- Boundary element method. I can look this up on the Internet.
- Volume fluid method. Look up "fluid-structure interaction" on the Internet---that's the name of the phenomenon. I can find and download some kind of code, e.g. OpenFOAM.
- Particle method. Probably too difficult.
- Fundamental mathematical approach: model a rope as a cylinder (but then we come full circle back to the limitations of modelling a complex geometry as a collection of cylindrical beams), liquid flow as flow over cylinder, add bubbles to flow, then add more cylinders.
- Hybrid compromise: model flow-over-cylinder-created drag as a damping factor to my stick model or volumetric mesh in ANSYS, (otherwise ropes could go on oscillating forever even after the bubbles are gone,) add bubbles as oscillatory force (P(t) = Rayleigh-Plesset...). In essence this is building a maths model on top of my existing work---probably the most tractable route according to Paul, though starting from scratch in OpenFOAM is also possible.

In short, as Paul said, there is a whole continuum of options, and no right answer.

# List of tools to be vetted
- COMSOL: possible
- OpenFOAM: possible; need a lot of maths to write my own solver though; probably too difficult
- Autodesk Inventor: probably not
- ANSYS Fluent: possible
- Solidworks flow simulation: probably not
- QuickerSim MATLAB: almost definitely not
