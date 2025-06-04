---
title: 'Geodynamic code development'
weight: 40
#subtitle: ''
summary: Aims to improve DES3D (Dynamic Earth Solver in 3D), an open-source geodynamic modeling code by extending the code's functionality and accelerating its performance.
authors:
# - admin
- icon: people
  icon_pack: fab
  name: GeoFLAC developers
  url: https://github.com/orgs/GeoFLAC/people
tags:
- DES3D
- High-Performance Computing
- GPU
- Non-linear rheologies
- rate-and-state friction
- Adaptive Mesh Refinement
categories:
- research, geodynamic code development

date: ""
lastmod: "2023-12-13"
featured: true
draft: false

# Optional external URL for project (replaces project detail page).
external_link: ""

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
image:
  placement: 1
  caption: Three-dimensional model for core complex formation created with DES3D. Accelerated on NVidia V100 graphics card.
  focal_point: ""
  preview_only: false
  
links:
  - icon: github
    icon_pack: fab
    name: GeoFLAC GitHub Organization
    url: https://github.com/GeoFLAC/
  - icon: code-branch
    icon_pack: fas
    name: DynEarthSol
    url: https://geoflac.github.io/DynEarthSol/
  - icon: code-branch
    icon_pack: fas
    name: Laghost
    url: https://github.com/GeoFLAC/Laghost/
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
slides: ""
---

The main goal of this project is to improve [DES3D (Dynamic Earth Solver in 3D)](https://github.com/tan2/dynearthsol), an open-source geodynamic modeling code. in terms of the types of physical processes it can model and the speed 

## Performance

DynEarthSol (DES) is multithread-parallel through OpenMP. The parallel performance scales well up to 16 threads on recent multi-core CPUs and will be tested on newer CPUs models whenever possible.

DES has been enabled to run on NVIDIA GPUs through CUDA and then on other hardware through OpenACC. The overall parallelization is illustrated in the figure below.
{{< figure src="/img/DES3DFlowChart.png" title="How DES3D works when using GPU" >}}
With the CUDA version, a three-dimensional model for core complex formation showed speedup of 40-60 relative to the performance on a 16-thread CPU. The speedup varies according to the problem size, which tends to increase over the course due to mesh refinement.
{{< figure src="/img/GPUacceleration.png" title="Core complex model and performance on GPU relative to CPU" >}}
[This video](https://youtu.be/zr-4HIg7_14) shows the code in action.

## Functionality

In additional to its core function to simulate large deformation in temperature-dependent elasto-visco-plastic material, we are adding other useful capabilities:

- **Rate-and-state friction law** by [Tong and Lavier (Nature Comm., 2018)](https://dx.doi.org/10.1038/s41467-018-06390-z). With this new friction law, we can better model an entire earthquake cycle as well as the consequences of its numerous repetition.
{{< figure src="/img/EqCycle.png" title="Earthquake cycles modeled with a rate-and-friction law implemented in DES3D" >}}
- **Pseudo-transient method**, an efficient extension of [Cundall's damping scheme for dynamic relaxation](https://geoflac.github.io/des3d/docs/theory/dynamicrelaxation)
- **Structured meshing** that will complement the default unstructured meshing with P1 elements and provide convenience in some types of models
- **Laghost: Migration of code base to MFEM**. MFEM is an arbitrary-order finite element library for extreme-scale parallel computation. [Laghost](https://github.com/GeoFLAC/Laghost/) is an effort to build DES's main algorithm on MFEM.

