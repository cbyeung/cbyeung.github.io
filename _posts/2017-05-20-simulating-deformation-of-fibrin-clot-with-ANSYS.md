---
layout: post
title:  Simulating deformation of fibrin clot with ANSYS
date:   2017-05-20
categories: ultrasound confocal clot 3dprint fiji ANSYS youngsModulus simulation
tags: ultrasound confocal clot 3dprint fiji ANSYS youngsModulus simulation
---
In the same spirit as my [last post]({{ site.baseurl }}{% link _posts/2017-05-19-fabricating-and-3d-printing-fibrin-clots-to-understand-sonothrombolysis.md %}), which is an almost verbatim transcript of a poster I presented at Swarthmore College, this post is a reproduction of the final report I wrote for a solid mechanics course, originally titled "E59 Project: Simulating deformation of fibrin clot using ANSYS."

## Abstract
A 3D printed scale model of a blood clot was mapped. Nodal coordinates, along with empirically determined material properties, were entered into ANSYS (Release 17.2). The model was simulated using ANSYS `Beam4` elements, and solved for nodal displacements in the x, y and z-directions. These displacements were subsequently used to calculate stress and strain and the bulk Young’s moduli of the clot: E<sub>x</sub>, E<sub>y</sub> and E<sub>z</sub>. Results are summarised in table 1.

E<sub>x</sub> (Pa) | E<sub>y</sub> (Pa) | E<sub>z</sub> (Pa)
--- | --- | ---
113.5 | 109.1 | 16.17
{:.table}
<center>Table 1: Young's moduli.</center>
<br>
All three moduli fell within the range 0.1--1500 MPa obtained from past literature.
