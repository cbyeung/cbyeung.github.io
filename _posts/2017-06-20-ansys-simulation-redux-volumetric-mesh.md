---
layout: post
title:  ANSYS simulation redux---volumetric mesh
date:   2017-06-18
categories: ultrasound confocal clot 3dprint ANSYS youngsModulus simulation FEA
tags: ultrasound confocal clot 3dprint ANSYS youngsModulus simulation FEA
---
Professor Matt Zucker suggested I look into the possibility of importing a volumetric mesh into ANSYS. A volumetric mesh based on my fibrin clot `.stl` files would be a much more true-to-life rendition of the clots I fabricated, compared to my crude stick models. Below I will outline the workflow I have developed to accomplish this goal, largely through trial-and-error.

The first and most crucial step is to convert an `.stl`---which is a shape file---into a filled, solid body. As it turns out, ANSYS is much more punctilious than even the typical 3D printer as regards an error-free input; a file accepted by the printer could still be rejected by ANSYS.

`Solidworks` can perform the surface-to-solid conversion, but sets a hard 20,000-facets limit on the complexity of the shape file it will accept. On my part meeting that requirement necessitates highly aggressive mesh reduction. `MeshLab` unfortunately has trouble retaining the shape of the original file when asked to reduce aggressively, so I turned to `Meshmixer` instead. This software has a function `Edit`&rarr;`Make solid`. Lowering `Solid accuracy` and `Mesh density` usually results in something that at least resembles (if not particularly faithfully) the original shape, *and* does not have too many awkward sharp angles that ANSYS will refuse to mesh.

Next up: repair in `Fiji` and at <https://cloud.netfabb.com>. In particular, make sure to close holes and delete self-intersecting faces. This process could take many iterations. Trial-and-error is our new best friend today.

Now import this repaired `.stl` into Solidworks. In the import dialogue box, select `.stl` as the file type, then within options, choose import as solid body. *N.B. mine may not be the exact wording you will see.* If Solidworks refuses, go back to the previous step. If not, allow Solidworks to run import diagnostics. If errors are detected, also return to the previous step. *Sorry.*

If you have come this far, save the *solid!* as a `.igs` file---remember to select export as solid within the option dialogue box.

Launch ANSYS. Import this `.igs` file. Accept the default import settings unless something goes wrong.

We can begin meshing. Please stay tuned for updates on this front.
