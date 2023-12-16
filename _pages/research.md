---
title: "Research lines"
permalink: /research/
layout: single
---

* **Computation of incompressible materials using the  Material Point Method**

	 I am working on large deformation problems in structural mechanics. It is especially interesting because civil structures can suffer deformations, and even fractures, caused by strong impacts. I am using an enriched finite element based technique to solve this problem, called Material Point Method. My research focuses on the development and implementation of the Variational Multiscale Method to get stable formulations to deal with incompressible materials in solid and fluid mechanics problems.

* **Computational fluid dynamics**

	 -<u> Numerical simulations of viscoelastic fluid flow with high elasticity.</u>\
	 The global goal of my thesis was the development of mathematical models and numerical methods to simulate viscoelastic flows with high elasticity using the Finite Element Method. The equations that modelized the viscoelastic fluid flow present a large number of non-linearities and additionally, when the elasticity of the fluid is dominant respect to the convection forces, new instabilities must be treated. Reproducing it accurately is considered one of the biggest challenges in computational rheology, as classical methods fails to reproduce high elasticity levels.\
	 -<u> Numerical analysis of the aerodynamic loads on a tunnel wall separation.</u>\
	 In this project we study the influence of a telescope over another one concerning the optical parameters. To carry out the study, we solved the Navier Stokes equations on real terrain taking into account the temperature and considering the Smagorinsky model to capture the turbulence. And then we calculated the optical parameters that were influenced by the air temperature.\
	 -<u> Numerical analysis of the optical quality over a telescope.</u>\
	  Evaluation of the aerodynamic loads at the end of the constructed sections caused by the transient flows due to the train motion along the Mont-Royal tunnel. We carried out a CFD simulation using moving domains, where the geometry of the tunnel was fixed while the train was moving inside it. We used an arbitrary Lagrangian-Eulerian strategy, solving the Navier Stokes equations considering this motion.

* **Other projects in computational mechanics**

	 -<u> The numerical simulation of electromagnetic processes with hysteresis.</u>\
	  The goal was the study and the numerical simulation of electromagnetic processes with hysteresis, with specific application on crankshafts. In this project I had to simulate the magnetisation process of the crankshafts and, subsequently, the demagnetisation process. This process is commonly used in automotive factories to detect fractures in crankshafts, using fluorescent metal shavings.\
	 -<u> Numerical solver based on spectral methods, in order to reproduce the sound wave propagation in a well.</u>

<!--[1. Computational fluid dynamics](#1-numerical-simulations-of-viscoelastic-fluid-flow-with-high-elasticity)\
[2. Incompressible materials in the implicit Material Point Method](#2-material-point-method)
[3. Other problems in computational mechanics](#2-material-point-method)-->
<!--
## 1. Numerical simulations of viscoelastic fluid flow with high elasticity
(For information about the papers resulted see [Publications page](https://lauramoremar.github.io/publications/))\
This research line was addressed overall in my predoctoral stage. The study was performed in a Finite Element (FE) framework, and the formulations were stabilized using the Variational MultiScale Method (VMS), developed originally by Hughes et al. 1998.\
All the implementations were performed in Femuss,  an object-oriented finite element code developed in Fortran and able of solving three-dimensional fluid dynamics, solid mechanics, fluid-structure interaction problems or coupled thermal problems among others, in a high performance environment.\
The main points studied are the following:

### 1.1. Log-conformation reformulation
The log-conformation reformulation (Fattal and Kupferman 2004) is implemented to treat the instability resulting in the equations when the elasticity is high. It is a reformulation of  traditional constitutive equations of viscoelastic fluids, which eliminates this instability and linearizes the exponential stress profiles near the stress singularities. Therefore, the formulation seeks to treat the exponential growth of the elastic stresses, allowing to extend the range of Weissenberg numbers for which a numerical solution can be obtained.

### 1.2. Thermal coupling
Thermal coupling with the viscoelastic fluid flow is also a relevant topic in many industrial processes. In comparison with Newtonian cases, now we will need to consider a dependence of temperature in the viscoelastic properties. On the other hand, the study of the effect of viscous dissipation will be particularly interesting, due to the fact that fluids reach higher temperatures caused by the internal work. This effect is displayed as a term in the energy equation which accounts for the mechanical part of the viscoelastic fluid that is transformed into heat, i.e., Joule’s effect. To address the coupled problem we have to consider an iterative algorithm which updates the parameters needed at each time step, due to the four variables being strongly coupled.

### 1.3. Dynamic sub-grid scales
Recent studies indicate that classical residual-based stabilized methods for unsteady incompressible flows may experience difficulties when the time step is small relative to the spatial grid size. These problems can happen, for instance, when small time steps result from the necessity of accuracy to solve transient problems due to the presence of non-linear terms in the differential equations, a very common issue in viscoelastic flow formulations.
The approximations used in Variational Multiscale (VMS) methods usually neglect the time derivative of the sub-grid scales, consequently, anisotropic space-time discretizations cannot guarantee stability. We propose the design of stabilization techniques that allow one to compute time-dependent viscoelastic flow problems with high elasticity (or Weissenberg number) and with an anisotropic space-time discretization.

### 1.4. The purely elastic instabilities
The flow patterns in viscoelastic fluids can be highly dynamic and in some cases chaotic, due to the elastic component of the fluid and the convective nature of the constitutive equation, even in quasi non-inertial flows, where non-linear rheological effects can manifest through the generation of large normal stresses which result in complex flow phenomena causing a purely elastic instability, and in some cases producing elastic instability. Here, problems which exhibit the purely elastic instability phenomena have been studied, and different tools have been employed to obtain an accurate and efficient solution.

### 1.5. Numerical analysis of stability and convergence
An important topic in numerical analysis is the study of stability and convergence of the applied methods, such a the logarithmic reformulation stabilized using subgrid scales. Due to the fact that a complete analysis of the non-linear problem requires more exhaustive and deep study, we restrict ourselves to analyze the linearized problem.

### 1.6. Fluid-Structure Interaction
Fluid-structure interaction (FSI) is frequently found in several applications, in particular in biomedical research. For example, the blood flow in arteries and veins, where information generated by investigation of blood vessel-wall interaction is useful for medical evaluation.
In these cases fluids usually have non-Newtonian fluid properties and, in particular, viscoelastic behavior. For such viscoelastic fluid-structure interaction (VFSI) problems the effect of viscoelasticity may play a crucial role when it is comparable to dominant inertial effects and this is the line that could be explored. One of the main difficulties to afford this problem is the stability problem, when elasticity of the fluid is dominant.


## 2. Material Point Method

Currently, I'm developing new stabilized algorithms for incompressible materials using the Material Point Method. All the implementations are performed in [Kratos Multiphysics](https://github.com/KratosMultiphysics), an open-source code prepared for running multiphysics problems written in C++ and Python.-->
