---
layout: post
title:  Pizza lunch presentation and feedback
date:   2017-06-07
categories: acoustics ultrasound wave bubble cavitation nonlinear mathematica
tags: acoustics ultrasound wave bubble cavitation nonlinear mathematica
---
I presented my cumulative research findings from my work over two-and-a-half summers and one semester (for the E59 Solid Mechanics course). You can access a copy of my presentation [here]({{ site.url }}/images/acoustics/presentationCBYsmall.pdf).

Many members of the audience provided helpful feedback, which I have collated in this post.

Professor Matt Zucker
  - Questioned how fibres could possibly be less stiff axially than flexurally, given that in my 3D prints more fibres are oriented along the z-axis. He cites the example of a spring that is easier to stretch or compress than it is to bend---very unrealistic. Professor Carr Everbach responded that the geometry of the mesh is probably non-trivial because the connections between fibres might be capable of rotation. In other words, conformational changes should not be ignored.
  - Asked if it is possible to measure the effective stiffness of a clot empirically, in order to corroborate my findings. My answer is probably yes, with optical (aka laser) tweezers, to which the physics department at Swarthmore College does have access.
  - Suggested there might be tools to perform a stress analysis directly on a volumetric mesh (i.e. my `.stl` files). ANSYS might be able to do that. This will save me the effort (and avoid the unrealistic aspects) of generating nodes with a ruler and by eye to make a rather crude stick model.

Professor Allan Moser
  - Suggested some companies (e.g. Integral Molecular) might manufacture microscope slides with machined small cavities. That might make it easier for me to make a small cubic sample (roughly 0.3x0.3x0.3mm) to see if fibres in the x- and y-axes look clumpier as a consequence. He also emailed me to the same effect. Carr told me companies that make microfluidic devices (for instane flow modules) may have similar products.

Professor Carr Everbach
  - Mine was an 'A\-' presentation, which is good given I had little preparation.
  - Too long though. It took about 30 minutes. I need to figure out how to squeeze the same amount of information into a circa 10-minute presentation.
  - Regarding making a 0.3x0.3x0.3mm cubic sample: since the bias towards the z-axis *could* be attributed to the microscope's scanning algorithms, one way to eliminate the scope as a cause of the observed anisotropy is to cut (with razor blades spaced 0.3mm apart) a 0.3x0.3mm square from a clot I would prepare normally. There is special equipment that allows one to extract the cube, remove the fragment of coverslip, then reorient the cube on its side and place it on a new slide. This means I can image along the x- and y-axes (as defined by the orientation of the original sample slide) instead. Notwithstanding, this procedure is very difficult, though not impossible.
  - Even though a microbubble only interacts with the fibre it touches, rather than with the clot as a whole, it is still important to know if the overall clot is isotropic, even if knowing this does not help our efforts to model individual bubbles squeezing between individual fibres.

Admonishments to myself
  - On my computer, make sure Energy Saver settings are set such that the display will not go to sleep during my presentation
  - Mute my mobile phone!
