---
layout: post
title:  Numerically solving Rayleigh-Plesset in Mathematica
date:   2017-06-01
categories: acoustics ultrasound wave bubble cavitation nonlinear mathematica
tags: acoustics ultrasound wave bubble cavitation nonlinear mathematica
---
Luke Barbano, a fellow Swarthmore student who previously worked under the guidance of Professor Carr Everbach, laid the groundwork for the results of my post. His goal was to simulate the radial oscillation of a single bubble when subjected to a sinusoidal ultrasound field. Though his results did not quite match literature, which he was attempting to replicate, it was an essential part of modelling sonothrombolysis. The holy grail of any research, as Carr put it, is to reproduce the same results empirically, analytically, and numerically. If one achieves that, the problem is considered fully understood and *solved*; time to move on to the next enterprise, to uncharted waters. The enterprise I have been tasked with however, is much less ambitious: model ultrasound- and microbubble-assisted clot dissolution *numerically*.

Two sides of the same coin: modelling a blood clot numerically---relative to which my [E59 project]({{ site.baseurl }}{% link _posts/2017-05-20-simulating-deformation-of-fibrin-clot-with-ANSYS.md %}) is but a droplet in a haemal ocean; and modelling microbubbles numerically. Luke's work is the basis for the latter.

The summer one year prior, I made some ad hoc changes to Luke's `Matlab` and `Mathematica` scripts but still failed to replicate literature results. Carr suggested, rather than hacking away at the same code, that I start afresh. I returned to *The Acoustic Bubble* (Leighton, 1994) and transferred the Rayleigh-Plesset equation

$$\begin{equation*}
R\ddot{R}+\frac{3\dot{R}^2}{2} = \frac{1}{\rho}\left\{ \left( p_0+\frac{2\sigma}{R_0}-p_v \right)\left( \frac{R_0}{R} \right)^{3\kappa}+p_v-\frac{2\sigma}{R}-\frac{4\eta\dot{R}}{R}-p_0-P(t) \right\}.
\end{equation*}$$

into a Mathematica script, shown below.
~~~
Clear[R, R0, \[Rho], P0, \[Sigma], Pv, \[Eta], P, \[Kappa]]
(*initial radius 2mm*)
R0 := 0.002
(*density of water 1000 kg/m^3*)
\[Rho] := 1000
(*static pressure 101325 Pa*)
P0 := 101325
(*surface tension of water 0.07286 N/m; source: "Surface-tension \
values" Wikipedia*)
\[Sigma] := 0.07286
(*Vapour pressure of water 2338.8 Pa*)
Pv := 2338.8
(*Shear or dynamic viscosity of water 0.001002 Pa-s*)
\[Eta] := \
0.001002
(*10kHz sound field of pressure amplitude 2.7 bar*)

P[t] := 270000*Sin[2*\[Pi]*10000*t]
(*Polytropic index 1.4 since adiabatic*)
\[Kappa] := 1.4
NDSolve[{R[t]*R''[t] + (3 (R'[t])^2)/2 ==
   1/\[Rho]*((P0 + (2*\[Sigma])/R0 - Pv)*(R0/R[t])^(3*\[Kappa]) +
      Pv - (2*\[Sigma])/R[t] - (4*\[Eta]*R'[t])/R[t] - P0 - P[t]),
  R[0] == R0, R'[0] == 0}, R, {t, 0, 0.001}]
Plot[Evaluate[R[t] /. %], {t, 0, 0.001},
 AxesLabel -> {"Time (s)", "Bubble radius R (m)"}]
~~~

Apologies for the absence of syntax highlighting; `Rouge` currently does not support Mathematica---a massive oversight in my opinion.
