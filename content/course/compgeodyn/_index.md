---
title: CERI 8315 Computational Methods for Geodynamics
linkTitle: CERI CompGeodyn
summary: Basic theory and practicals of the finite element method, with applications for modeling geodynamic processes.
date: '2024-09-19'
type: book
tags:
  - current
---

<!-- {{< figure src="featured.jpg" >}} -->

{{< toc hide_on="xl" >}}

## Syllabus

[Fall 2024 Syllabus](/uploads/compgeodyn/CERI73158315_ComputationalMethods_Syllabus.pdf)

## Course Description

This course aims to enable students to understand the basics of the finite element method (FEM), a versatile numerical method for finding an approximate solution to partial differential equations, and to use and modify available open-source tools for applications in various fields in geophysics.

## Course Objectives

After taking this course, students will be able to use or modify as necessary the existing community finite element codes (e.g., CIG codes) for their geophysical research.

To achieve the goal, we will

- review the fundamental governing equations in continuum mechanics,
- have under-the-hood understanding of finite element method,
- gain hands-on experience with common procedure and useful practices in computational research,
- use one of the open-source FEM codes, possibly after modifications, for their term project.

Through a term project, students will

- acquire hands-on experiences with common practices in computational research,
- gain scientific communication skills.

## References and Online Resources

No required textbook but parts of the references listed below will be
used.\

### Reference texts[^1]

[^1]: *means that the UofM Library has an ebook version.

- Fundamental numerical techniques (main reference)

  - *Quarteroni, A., Sacco, R., & Saleri, F. (2007). [Numerical mathematics (2nd ed)](https://link-springer-com.ezproxy.memphis.edu/book/10.1007/b98885). Berlin: Springer.

- Finite element method:
  - *Zienkiewicz, O. C., Zhu, J. Z., and Taylor, R. L. (2013). *The Finite Element Method: Its Basis
and Fundamentals*. Butterworth-Heinemann, 7th edition
  - Belytschko, T., Liu, W. K., Moran, B., & Elkhodary, K. I. (2014). Nonlinear Finite Elements for Continua and Structures (2nd ed.). John Wiley & Sons, Ltd.
  - Hughes, T. J. R. (2000). The Finite Element Method: Linear Static and Dynamic Finite Element Analysis (1st ed.). Dover Publications, Inc.

- Continuum mechanics:

  - *Tadmor, E. B., Elliott, R. S., and Miller, R. E. (2012). *Continuum Mechanics and Thermodynamics: From Fundamental Concepts to Governing Equations*. Cambridge University Press,
Cambridge
  - Holzapfel, G. A. (2000). *Nonlinear solid mechanics : a continuum approach for engineering*.
Wiley, Chichester ; New York
  - Malvern, L. E. (1977). *Introduction to the Mechanics of a Continuous Medium*. Prentice-Hall,
Upper Saddle River, New Jersey

- Geodynamics:

  - *Schubert, G., Turcotte, D. L., and Olson, P. (2001). *Mantle Convection in the Earth and
Planets*. Cambridge University Press, Cambridge
  - Turcotte, D. L. and Schubert, G. (2002). *Geodynamics*. Cambridge University Press, New
York, 2nd edition

### Online resources

- The web sites listed below will help you get familiar with 
the command line-based work environment and other useful tools 
for computational research.

  - How to work on a Linux(-like) system especially when you are new to it: <https://developer.ibm.com/tutorials/l-lpic1-map/>
  - Lessons on BASH, Python and Git by Software Carpentry: <https://software-carpentry.org/lessons/>
  - HPC carpentry: <https://www.hpc-carpentry.org/community-lessons/>
  - Everything needed for using cyberinfrastructure, from programming languages to parallel computing: <https://support.access-ci.org/knowledge-base/resources>

## Term projects

- Students carry out a reasonably small but non-trivial project
    relevant to the course's goal and objectives.

- They should use GitHub to manage their projects and products as
    sharable and reusable resources.

- A project topic will be decided individually based on students' interests and
    needs.

- Possible topics:

  - Consider in a global-scale mantle convection model the effects
      of centrifugal acceleration in addition to the typical
      geocentric gravity

  - Reproduce and possibly improve a published work on computational
      methods.

  - Parallelize an existing code with a directive-based approach
      such as OpenMP and OpenACC and assess the performance
      improvement

  - Introduce recent advances in physics-informed neural networks
      (PINNs)

## Course Outline

- Week 1: [A short review of continuum mechanics](/uploads/compgeodyn/ContinuumMechanicsReview.pdf)

- Week 2: Numerical toolbox - [Principles of numerical mathematics](https://github.com/echoi/compgeodyn/blob/master/Principles.ipynb) [Lecture slides](https://github.com/echoi/compgeodyn/blob/master/Principles.slides.html)

- Week 3: Numerical toolbox - [Interpolation: Lagrange polynomial](https://github.com/echoi/compgeodyn/blob/master/PiecewisePolynomialInterpolation.ipynb) [Lecture slides](https://github.com/echoi/compgeodyn/blob/master/PiecewisePolynomialInterpolation.slides.html)

- Week 4: Numerical toolbox - [Interpolation: Piecewise Lagrange polynomal interpolation in 2D](https://github.com/echoi/compgeodyn/blob/master/PiecewisePolynomialInterpolation.ipynb) [Lecture slides](https://github.com/echoi/compgeodyn/blob/master/PiecewisePolynomialInterpolation.slides.html)

- Week 5: Numerical toolbox - [Solving linear equations: Basic stability analysis and direct method](https://github.com/echoi/compgeodyn/blob/master/LinearSystemSolvers.ipynb)

- Week 6: Numerical toolbox - [Solving linear equations: Iterative methods and conjugate gradient method](https://github.com/echoi/compgeodyn/blob/master/LinearSystemSolvers.ipynb)

- Week 7: Numerical toolbox - [Solving linear equations: Krylov subspace methods](https://github.com/echoi/compgeodyn/blob/master/LinearSystemSolvers.ipynb). Solving non-linear systems

- Week 8: Numerical toolbox - [Approximating function derivatives: Finite difference and interpolation-based approach](https://github.com/echoi/compgeodyn/blob/master/ApproximatingFunctionDerivatives.ipynb)

- Week 9: Numerical toolbox - [Approximating function derivatives: Orthogonal polynomials and weight functions](https://github.com/echoi/compgeodyn/blob/master/ApproximatingFunctionDerivatives.ipynb)

- Week 10: Numerical toolbox - [Numerical integration: Gauss and Gauss-Lobatto quadrature formula](https://github.com/echoi/compgeodyn/blob/master/NumericalIntegration.ipynb)

- Week 11: Basic finite element method - [Examples of PDEs](https://github.com/echoi/compgeodyn/blob/master/Examples_of_PDES.ipynb), [Weak forms and variational principles](https://github.com/echoi/compgeodyn/blob/master/VariationalPrinciple_and_WeakForm.ipynb), [Approximate solution to a weak form](https://github.com/echoi/compgeodyn/blob/master/Approximate_Solution_to_WeakForm.ipynb)

- Week 12: Basic finite element method - [Walkthrough with 1D Poisson Equation](https://github.com/echoi/compgeodyn/blob/master/Solving_1D_Poisson_Equation_with_FEM.ipynb)

- Week 13: Basic finite element method - Extension to 2D and 3D

- Week 14: Basic finite element method - Solving time-dependent PDEs

- Week 15: Selected Topics
  - Elastic deformation: Static and Dynamic
  - Basic parallel computing
  - Introduction to open-source codes: PyLith, ASPECT, FEniCS, or DES3D

## Homework

To be added
<!-- - [Homework 1 on continuum kinematics](/uploads/compgeodyn/CERI8353_Geodynamics_homework1.pdf)
- [Homework 2 on continuum kinematics](/uploads/compgeodyn/CERI8353_Geodynamics_homework2.pdf)
- [Homework 3 on heat transfer](/uploads/compgeodyn/CERI8353_Geodynamics_homework3.pdf) -->

<!--
## Courses in this program

{{< list_children >}}
-->
## Meet your instructor

{{< mention "admin" >}}

## FAQs

<!-- {{< spoiler text="Are there prerequisites?" >}}
There are no prerequisites.
{{< /spoiler >}} -->

<!-- {{< spoiler text="How often do the courses run?" >}}
Designed for one 15-week semester, every otheryear. but Continuously, at your own pace.
{{< /spoiler >}} -->

{{< cta cta_text="Begin the course" cta_link="continuum-mechanics-review" >}}
