---
layout: post
title:  A brief history of acoustics
date:   2017-05-29
categories: acoustics ultrasound wave bubble cavitation fibrin clot
tags: acoustics ultrasound wave bubble cavitation fibrin clot
---
This post is a compilation of the mini-lectures Professor Carr Everbach gave during the summer of 2017 to acquaint me with the very basics of acoustics and ultrasonic microbubbles. I will expand this post over time.

## Fibrin
There are no loose ends in a fibrin mesh---all fibrin ropes connect with each other.

tPA (tissue plasminogen activator) is an enzyme that takes apart blood clots. Binding sites on tPA match those present on fibrin, allowing tPA to move across fibrin polymers and cleave them. As with all enzymes, a single molecule of tPA is capable of acting on a large number of fibrin polymers without itself being used up.

Synthetic versions of tPA---called r-tPA (recombinant tPA)---exist. Examples include streptokinase and urokinase.

UAT (ultrasound-accelerated thrombolysis) works via the combined effects of thermal and mechanical action.

## Acoustics
Sound waves are mechanical compression waves. These require a medium unlike light waves. A suitable medium possesses the following properties:
  - mass: provides inertia that carries displaced particles past their equilibrium point
  - stiffness
  - restoring force
  - *optionally* dissipative properties, e.g. friction

An equation of state is almost always an empirical relation, rarely derived from first principles.

The speed of a mechanical wave is given by

$$
\begin{equation*}
  v = k \sqrt{\frac{\text{stiffness}}{\text{mass}}}.
\end{equation*}
$$

For a sound wave, the stiffness arises from the Ideal Gas Law $$P=\rho R T$$, where $$R$$ is the gas constant specific to the gas comprising the medium. The dissipation is proportional to the square of the frequency.

To launch a wave, the surface must move more than a wavelength. The size of the surface must at least be comparable to the wavelength as well.

$$ka$$---where $$k$$ is the wavenumber and has units of inverse length and $$a$$ is the diameter and has units of length---is a dimensionless number that determines acoustic projection, specifically, the shape of the beam (e.g. omnidirectional, hemispheric, etc.) and the efficiency of the beam.

Reflection depends on the size of the object w.r.t wavelength. Smaller objects do not contribute to much reflection or scattering; they mostly cause refraction. We call them *acoustically transparent*.

Acoustical propagation is nonlinear. For small amplitudes, waves stay mostly sinusoidal with little distortion, although amplitude decreases with time due to dissipation.

![Sinusoid]({{ site.url }}/images/acoustics/sinusoid.svg){:.text-width}
<center>Figure 1: A sinusoidal wave. For small amplitudes, P<sub>+</sub> = P<sub>-</sub> .</center>
<br>
In general, due to the Perfect Gas Law, sound waves propagate adiabatically (because sound oscillations tend to be very fast) rather than isothermally. This means compression regions get hotter, rarefactions cooler. As a consequence, speed of sound is faster in the hotter compression regions. Components of a wave move at different speeds, causing a sinusoid to distort and eventually become an N-wave. Since a distorted wave is a superposition of the fundamental *plus* higher harmonics, as a wave is distorted, energy migrates into higher harmonics.

## Surface tension
A liquid is a state of matter which cannot sustain a shear. It deforms continuously. A gas expands to fill all available space, while a liquid does not. Surface tension is a property of all liquids.

All molecules have some affinity for each other. Surface tension is a function of the molecular attraction of the *liquid*, unrelated to what *gas* is inside the bubble. The Laplace pressure P<sub>Laplace</sub> is the additional pressure exerted by this molecular attraction on the surface of a bubble that acts to squeeze the bubble.

$$
\begin{equation*}
  P_\text{inside} = P_\infty + P_\text{Laplace} = P_\infty + \frac{\sigma}{2R},
\end{equation*}
$$

where $$P_\infty$$ is the pressure outside the bubble, $$\sigma$$ is the surface tension and $$R$$ is the bubble radius. Hence a smaller bubble has a larger internal pressure.

## Bubbles
Bubble is gas. Void is vacuum. Both are unstable.

Henry's Law states that 1L of liquid at s.t.p contains exactly 1L of dissolved gases. The higher the pressure, the more gas can be dissolved ($$PV=nRT$$). Higher temperature reduces the amount of gas that can be dissolved.

Suppose there is more gas inside a bubble than outside. Concentration gradient drives gas to diffuse outwards through the bubble wall. As the volume of the bubble decreases, $$\sigma/2R$$ increases, the pressure gradient increases further. This creates positive feedback, whereby the bubble shrinks ever faster, eventually completely dissolving away. Surfactants (e.g. soap) can counteract this effect. Their hydrophobic ends accumulate inside bubbles, stabilising the size of the size of the bubbles through mutual electrostatic repulsion.

When a bubble is compressed, for instance in the compression region of a sound wave, the bubble volume decreases. By the logic above, there exists an elevated concentration of gas inside the bubble. Outside, by Henry's Law, the saturation concentration increases, so the relative gas concentration outside the bubble actually *decreases*. This generates a very large concentration gradient that drives gas out of bubbles.

On each cycle, more gas leaks in during rarefaction than out during compression because the bubble surface area is larger during rarefaction. We call this *rectified diffusion*. Thus bubbles grow. They are initially pinned to the container wall by surface tension, but when they are large enough, they rise by buoyancy to the liquid surface, whereupon the gas exits the liquid. This is called *ultrasonic degassing*.

Biot solids are porous solids. They could account for some non-bubble-related ultrasonic thrombolysis, since a clot could be modelled as a Biot solid.

## Cavitation
Cavitation occurs because bubbles are resonators. Bubbles have a high quality (or Q), i.e. they have a sharp resonance peak and are able to oscillate with little energy input. The momentum of liquid carries a displaced bubble wall past its equilibrium radius.

There are several damping mechanisms:
  - shear viscosity of the liquid
  - bubble is a moving surface that emits its own sound field
  - thermal: heat exchange.

### Stable cavitation
Bubble oscillates in a continuous fashion. Cycles are all similar. Usually arises due to a continuous pressure wave around the resonance frequency range of the bubble.

The Minnaert frequency or resonance frequency is defined thus:

$$
\eqalign{
  f_R &=& \frac{1}{2\pi R_0}\sqrt{\frac{3\gamma P_a}{\rho_l}}\\
  &\approx& \frac{3.26}{R_0}~\text{(for air bubble in water)},
}
$$

where $$R_0$$ is the equilibrium bubble radius, $$\gamma=c_P/c_V$$, $$P_a$$ is the absolute pressure, $$\rho_l$$ is the density of the liquid. This equation is only precise for large bubbles (mm size or larger) with no surface tension.

Logistic map is one way of understanding the complex behaviour of bubbles, especially at large amplitudes.

Bubbles can be modelled as nonlinear, stiffening springs. Large apmlitude pressure waves cause bubbles to higher harmonics in addition to the driving frequency. Broadband emission is a good way to identify stable cavitation.

The stiffness of the gas is important in stable cavitation.

### Inertial cavitation
