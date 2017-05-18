---
layout: post
title:  Recipe for making blood clots in vitro and imaging them
date:   2017-05-16
categories: ultrasound confocal clot 3dprint fiji
tags: ultrasound confocal clot 3dprint fiji
---
This is a detailed recipe of the techniques I first trialled in the summer of 2017 to fabricate blood clots in vitro, from pure fibrinogen rather than human plasma, and later refined in the summer of 2018. Alternatives may exist for many of the reagents and tools listed below; the ones I mentioned are the only ones I tested.

### Preparing fibrin clots and mounting on microscope slides
*Based extensively on the recipe originally provided by Irina Chernysh in the Department of Cell and Developmental Biology at the University of Pennsylvania.*

Buy Fibrinogen from Hyphen Biomed, catalogue number PP002K or PP002B Fibrinogen 5 mg/mL. Mix up using 37&deg;C distilled water as per instructions on the provided data sheet; keep at 37°C in an incubator.  Agitate the solution by drawing it up and down in a micropipette. Do not vortex-mix: fibrinogen is sensitive to turbulence. Complete dissolution could take several hours with occasional mixing.  Once prepared, 30&mu;L aliquots of fibrinogen can be frozen in -20&deg;C freezer until desired day of use.

Buy AlexaFluor 488 fluorescently-labelled fibrinogen from ThermoFisher, catalogue number F13191 (1.5 mg/mL).  Place a small magnetic stirrer in the vial. Add 3.33mL of 0.1M sodium bicarbonate (pH 8.3) as per data sheet found online and stir gently on magnetic base. As before, do not vortex-mix.

Prepare a 1L stock solution of 140 mM NaCl plus 50 mM Tris (pH 7.4) for use in dialysis. [Sigma-Aldrich](https://www.sigmaaldrich.com/content/dam/sigma-aldrich/docs/Sigma/Bulletin/1/106bbul.pdf) provides a handy guide for mixing Tris. *N.B. see note on dialysis below*.

Prepare a 1.5 mL stock solution of 0.1 M CaCl<sub>2</sub>.

Thrombin is to be prepared according to instructions from supplier, except stock solution should be made to a concentration of 10 un/mL *not* 100 un/mL. Add liquid to vial and agitate only by pipette.  Thrombin stock solution may be frozen in -20&deg;C freezer until the desired day of use. When out of freezer, thrombin must be kept on ice at all times.

---
<br>
On day of use, thaw frozen items, but keep them on ice.

Prepare a chamber on a microscope slide: seal left and right sides of the chamber with 3 layers of double-sided tape on each side. (May need to wipe the slide with KimWipes for the tape to adhere securely.) Lower the cover slip onto the tape and gently press on the taped sides to ensure proper sealing. Seal the bottom side with a generous amount of *Sally Hansen Hard as Nails* nail polish. Apply layer by layer, and harden each layer by blowing with a hairdryer before applying a new layer.

Dialyse to exchange buffer: mix 4% (final concentration) of Alexa Fluor 488 into fibrinogen (e.g. 4 µL Alexa for every 100&mu;L of final fibrin sample).  Place the mixture into a dialysis bag (Dialysis Cassette G2, package of 10, ThermoFisher catalog number 87728, 340 kiloDalton cutoff) floating on NaCl-Tris buffer overnight.  *Optional for our purposes: use a spectrophotometer to measure the final concentration of fibrinogen: correct the final concentration (e.g. 4.6 mg/mL) back to 5 mg/mL (final concentration) if necessary.

*Note: In my experience success rate is much lower when fibrinogen is dialysed, possibly due to fibrinogen’s sensitivity to heat. Forgoing dialysis, simply mix 30&mu;L fibrinogen with 4&mu;L Alexa and the required volume of Tris needed to make up 100&mu;L of final sample volume---62&mu;L for 0.1 un/mL thrombin, 58&mu;L for 0.5 un/mL thrombin or 53&mu;L for 1.0 un/mL thrombin.*

Mix 3&mu;L of CaCl<sub>2</sub> into the fibrinogen. Now, when everything else is ready, mix the required volume of thrombin into the fibrinogen; 1&mu;L for a 0.1un/mL final concentration (which forms thick fibres/large pores/the least dense mesh), or 10&mu;L for a 1.0un/mL final concentration (which forms thin fibres/small pores/the densest mesh). With a pipette, rapidly aspirate and dispense three times to mix. Then, rapidly inject the mixture into the slide chamber. With 1.0un/mL thrombin, the window is about 5 seconds; at 0.1un/mL, the window could be stretched to as much as 10 seconds. Beyond that, the fibrin could clot inside the pipette tip.

Seal the remaining opening of the slide with nail polish. Sandwich the slide between wet towels and incubate at 37&deg;C for up to 30 minutes. Once the clot sets, you can view it under a confocal microscope or freeze (in -20&deg;C freezer to prevent the defroster cycle in household freezers from causing sample evaporation) the slide for later viewing.  Slides will last several weeks, though their lifetimes are shortened each time they are thawed.

Here is a summary of the amount of final concentration of reagents required to make a 100&mu;L fibrin sample:
  - 30&mu;L of fibrinogen at 1.5mg/mL
  - 4&mu;L of Alexa Fluor 488 at 4%
  - 53--62&mu;L of Tris buffer
  - 3&mu;L of CaCl<sub>2</sub> at 3mM
  - 1--10&mu;L of thrombin at 0.1-1.0un/mL.

### Confocal microscopy
