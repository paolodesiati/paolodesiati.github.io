---
title: Particle Propagation
authors:
- admin
- Juan Carlos Díaz Vélez
date: 2025-02-07
external_link: https://paolodesiati.github.io/project/particle
tags:
  - particle propagation
  - magnetic fields
  - anisotropy
---

### Introduction

The propagation of relativistic charged particles in the heliosphere and interstellar magnetic fields is calculated using the
_ptracing_ code. This code was originally developed for the studies described in [Desiati & Zweibel (2014)](https://iopscience.iop.org/article/10.1088/0004-637X/791/1/51). It includes several
analytical magnetic and electric field configurations and interfaces to different heliospheric numerical models. Additionally,
it supports multithreading, allowing it to take full advantage of computers with a large number of CPU cores and shared memory. 

Trajectories are calculated by numerically integrating the following set of 6--dimensional ordinary differential equations
$$\frac{d\mathbf{p}}{dt} = q \left(\mathbf{v}\times\mathbf{B} \right), \, \frac{d\mathbf{r}}{dt} = \mathbf{v},$$
describing the Lorentz force exerted by the magnetic field $\mathbf{B}(\mathbf{r})$ on particles with electric charge $q$ and
velocity $\mathbf{v}$, where $\mathbf{r}$ is their position vector and $\mathbf{p}$ the momentum. 
Momentum is expressed in units of $mc$; $\hat{\mathbf{p}}\equiv\mathbf{p}/mc$. The particle velocity $\mathbf{v}$ is 
related to $\hat{\mathbf{p}}$ by $\mathbf{v} = \hat{\mathbf{p}}/\sqrt{1+\hat p^2}$ and the particle Lorentz factor 
$\gamma = \sqrt{1+\hat p^2}$. In these units, the dimensionless particle gyroradius is $\hat r_g = \hat p_{\perp}$, 
and the dimensionless gyro-frequency is $\hat \omega_g = 1/\gamma$.  %We denote normalized variables with a hat. 

The equations of motion can be numerically integrated using various stepping algorithms. The code supports an adaptive 
time step size in these calculations, with a tolerance level denoted by a parameter $\epsilon$ to ensure that truncation 
errors remain sufficiently small. 
The integration of particle trajectories concludes when either the maximum integration time, $t_\mathrm{max}$, is reached 
or when the particles have attained a radius of $r_\mathrm{max}$. The figure demonstrates how protons are 
affected by the heliosphere and the modified magnetic field near its boundary.

One challenge in calculating trajectories within open boundary systems is that particles propagating from outside the heliosphere have a very low probability of reaching Earth or passing near it. To address this, we plan to generate 100 million anti-proton trajectories, propagating backward from Earth to a distance of 50,000 AU from the Sun.

We compute the trajectories using the Boris Push stepping method. This algorithm has become a standard for this purpose.
Although the Boris algorithm is not symplectic, it does conserve phase space volume, and its energy error is globally bounded,
comparable to that of symplectic algorithms. To ensure the accuracy of our results and as part of our
validation procedure, we will perform additional checks by varying the integration tolerance parameters and comparing the
outcomes with the explicit fourth-order Runge-Kutta method. Additionally, we will conduct cross-validation with limited
statistics using third-party tools such as CRPropa.

We calculate trajectories using heliospheric models provided by our collaborator, Prof. Nikolai Pogorelov, to investigate
the systematic effects of model parameters on our data interpretation. According to Liouville's Theorem, we can interpret the
calculated back-propagated anti-proton trajectories as protons traveling from the ISM to Earth.

A [preliminary study](https://pos.sissa.it/358/1076/) utilized numerically computed particle trajectories from a computational heliospheric model to assess the experimental biases introduced by ground-based experiments and their impact on interpretations. Our intention is to conduct thorough investigations into this experimental dimension of cosmic-ray physics, which will aid in developing the analytical tools needed to explore the origins of cosmic-ray anisotropy and its propagation through the interstellar medium and the heliosphere.


<!--more-->
