---
layout: post
title:  Recipe for making blood clots in vitro and confocal imaging
date:   2017-05-16
categories: ultrasound confocal clot 3dprint fiji
tags: ultrasound confocal clot 3dprint fiji
---
This is a detailed recipe containing the techniques I first trialled in the summer of 2017 to fabricate blood clots *in vitro*, from pure fibrinogen rather than human plasma, and later refined in the summer of 2018. Alternatives may exist for many of the reagents and tools listed below; the ones I mentioned are the only ones I tested.

### Preparing fibrin clots and mounting on microscope slides
*Based extensively on the recipe originally provided by Irina Chernysh in the Department of Cell and Developmental Biology at the University of Pennsylvania.*

Buy fibrinogen from Hyphen Biomed, catalogue number PP002K or PP002B fibrinogen 5 mg/mL. Mix with 37&deg;C distilled water as per instructions on the provided data sheet; keep at 37°C in an incubator.  Agitate the solution by drawing it up and down in a micropipette. Do not vortex-mix: fibrinogen is sensitive to turbulence. Complete dissolution could take several hours with occasional mixing.  Once prepared, 30&mu;L aliquots of fibrinogen can be frozen in -20&deg;C freezer until desired day of use.

Buy AlexaFluor 488 fluorescently-labelled fibrinogen from ThermoFisher, catalogue number F13191 (1.5 mg/mL).  Place a small magnetic stirrer in the vial. Add 3.33mL of 0.1M sodium bicarbonate (pH 8.3) as per data sheet found online and stir gently on magnetic base. As before, do not vortex-mix.

Prepare a 1L stock solution of 140 mM NaCl plus 50 mM Tris (pH 7.4) for use in dialysis. [Sigma-Aldrich](https://www.sigmaaldrich.com/content/dam/sigma-aldrich/docs/Sigma/Bulletin/1/106bbul.pdf) provides a handy guide for mixing Tris. *N.B. see note on dialysis below*.

Prepare a 1.5 mL stock solution of 0.1 M CaCl<sub>2</sub>.

Thrombin is to be prepared according to instructions from supplier, except stock solution should be made to a concentration of 10 un/mL *not* 100 un/mL. Add liquid to vial and agitate only by pipette.  Thrombin stock solution may be frozen in -20&deg;C freezer until the desired day of use. When out of freezer, thrombin must be kept on ice at all times---it is very sensitive to heat.

---
<br>
On day of use, remove reagents from freezer but keep them on ice.

Prepare a chamber on a microscope slide: seal left and right sides of the chamber with 3 layers of double-sided tape on each side. (May need to wipe the slide with KimWipes for the tape to adhere securely.) Lower the cover slip onto the tape and gently press on the taped sides to ensure proper sealing. Seal the bottom side with a generous amount of *Sally Hansen Hard as Nails* nail polish. Apply layer by layer, and harden each layer by blowing with a hairdryer before applying a new layer.

Dialyse to exchange buffer: mix 4% (final concentration) of Alexa Fluor 488 into fibrinogen (e.g. 4 µL Alexa for every 100&mu;L of final fibrin sample).  Place the mixture into a dialysis bag (Dialysis Cassette G2, package of 10, ThermoFisher catalog number 87728, 340 kiloDalton cutoff) floating on NaCl-Tris buffer overnight.  *Optional* for our purposes: use a spectrophotometer to measure the final concentration of fibrinogen: correct the final concentration (e.g. 4.6 mg/mL) back to 5 mg/mL if necessary.

*Note: In my experience success rate is much lower when fibrinogen is dialysed, possibly due to fibrinogen’s sensitivity to heat. Forgoing dialysis, simply mix 30&mu;L fibrinogen with 4&mu;L Alexa and the required volume of Tris needed to make up 100&mu;L of final sample volume---62&mu;L for 0.1 un/mL thrombin, 58&mu;L for 0.5 un/mL thrombin or 53&mu;L for 1.0 un/mL thrombin.*

Mix 3&mu;L of CaCl<sub>2</sub> into the fibrinogen. Now, when everything else is ready, mix the required volume of thrombin into the fibrinogen; 1&mu;L for a 0.1un/mL final concentration (which forms thick fibres/large pores/the least dense mesh), or 10&mu;L for a 1.0un/mL final concentration (which forms thin fibres/small pores/the densest mesh). With a pipette, rapidly aspirate and dispense three times to mix. Then, rapidly transfer the mixture into the slide chamber. With 1.0un/mL thrombin, we have a window of about 5 seconds; at 0.1un/mL, the window could be stretched to as much as 10 seconds. Beyond that, the fibrin could clot inside the pipette tip.

Seal the remaining opening of the slide with nail polish. Sandwich the slide between wet towels and incubate at 37&deg;C for up to 30 minutes. Once the clot sets, we can view it under a confocal microscope or freeze (in -20&deg;C freezer to prevent the defroster cycle in household freezers from causing sample evaporation) the slide for later viewing.  Slides will last several weeks, though their lifetimes are shortened each time they are thawed.

Here is a summary of the amount of reagents required to make a 100&mu;L fibrin sample:
  - 30&mu;L of fibrinogen at 1.5mg/mL
  - 4&mu;L of Alexa Fluor 488 at 4%
  - 53--62&mu;L of Tris buffer
  - 3&mu;L of CaCl<sub>2</sub> at 3mM
  - 1--10&mu;L of thrombin at 0.1-1.0un/mL.

### Confocal microscopy
Click on the I3 filter button and the shutter button. Look through the eyepiece and scan around with the smart controllers to find a “good” z-depth to see fibrin. Photobleaching can be very severe, so keep the shutter closed (or the Argon laser off) as much as possible.

Choose `Alexa 488-flybackground` (494-525nm) as the PMT preset. Set Argon laser to 25% and the laser power in beam path setting to 50%. Only PMT 2 should be active. Choose 20x dry objective lens. Format 1024x1024 pixels, 400Hz. Switch line average to 2 and frame average to 4 and turn on bidirectional scanning *after* choosing a good spot and depth range to image a z-stack. Use z-compensation (linear by PMT; add a reasonable number of interpolation points) to correct for some photobleaching, though it will still be necessary to manually adjust the `smart gain` and `smart offset` during stack-imaging. Use a zoom of 4.0 when taking z-stacks---this will cover an area of approximately 193x193 microns. Choose 0.2 microns for z-step size and image over a depth range of 50 microns---this will give an approximately cubic volume of 50x50x50 microns when exporting to STL (more on this later), with approximately equal resolution in every spatial direction. Imaging such a stack takes 40 minutes.

Alternatively, to obtain more z-resolution---which may be desirable due to difficulties associated with interpolation---reduce the z-step size to 0.04 microns. Reduce the depth range from 50 microns to 10 microns; otherwise imaging takes too long.

### Exporting to STL, repairing, 3D printing
*N.B. I used `Fiji` (is just ImageJ) on a computer with 8GB of RAM. Your mileage may vary; more memory enables a larger volume of fibrin to be processed.*

Open Leica’s `.lif` file in `Fiji`. Set `color mode` to `Grayscale` and check `Autoscale`. Whether to crop the stack depends on the memory constraints of the computer. If cropping is necessary, close and reopen the `.lif` file and select `crop on import` under `memory management`. Enter appropriate values in pixels for the width and height.

Under `Image`&rarr;`Adjust`, perform `Bleach correction` by `Histogram matching`. This equalises brightness and contrast across the stack while generating the least (but potentially still problematic) amount of noise. The last slice of the stack tends to have a catastrophic amount of noise; if so, delete the last slice with `Image`&rarr;`Stacks`&rarr;`Delete Slice`.

If noise is an issue, try the de-noising functions under `Process`&rarr;`Noise`, particularly `Despeckle` and `Remove outliers`. Pumping up the brightness and contrast could also reduce noise, though this is not recommended as it also brightens out-of-focus light.

Go to `Process`&rarr;`Binary`&rarr;`Make binary`. Choose the default thresholding method and set `Background` to `Dark`. Click on `Apply`.

Use `3D viewer` under `Plugins` to view the stack as `surface` not `volume` (the latter is selected by default). Export as binary STL shape file (binary STL has a smaller file size than ASCII STL).

---
<br>
Open the `.stl` file in `MeshLab`. Under `Filters`&rarr;`Cleaning and repairing`, perform every repair operation except `Merge close vertices` (which will be performed later using a more specialised function). Of particular importance is `Remove isolated pieces by diameter`---set percentage to 99% to remove all isolated pieces. The `.stl` file should be slightly smaller in size after exporting the repaired file.

Go to `Filters`&rarr;`Remeshing...`&rarr;`Simplication: Quadric Edge Collapse Decimation`. Later we need to use an online repair tool that imposes a 100MB limit on file size, so choose a percentage reduction (1.0 being no reduction at all) to bring the file size below that limit. As of the writing of this post, the tool will fail unless the mesh is simplified, so if the file size is already below 100MB, choose 0.99 percent reduction. Check `Preserve Boundary...`, `Preserve Topology`, `Optimal position...` and `Post simplification cleaning`.

Visit <https://cloud.netfabb.com>. Upload the `.stl` file to be automatically corrected for common errors such as watertightness, inverted normals, etc. *N.B. Netfabb sometimes experiences temporary interruptions of service, including changing the server on which it is hosted. The future of the tool appears nebulous.*

Print the mesh. Dissolve support material. Complete dissolution may take several days, longer for denser clots. The precise steps will depend on the 3D printer used.

### Analysis
`Fiji` includes the function `Analyze`&rarr;`Analyze particles`. After making slices binary, by ensuring that pores are dark and fibrils are bright, we can trick `Analyze particles` into thinking the pores are the particles. Fiji then counts the number of black pixels in each pore, and subsequently converts them to areas in units of micron<sup>2</sup>.

Results can be exported as an Excel file and analysed further, such as creating histograms and calculating mean pore sizes.
