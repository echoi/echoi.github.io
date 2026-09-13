---
title: "A Study on Rephrasing Large Earthquakes via the Least Action Principle and Evolving Machine Learning"
authors:
- In Ho Cho
- Eunseo Choi
date: '2026'
publishDate: '2026-05-20'
draft: false
publication_types: ["article-journal"]
publication: '*IEEE Access*'
publication_short: '*IEEE Access*'
featured: true
doi: 10.1109/ACCESS.2026.3693178
url_pdf: 'https://ieeexplore.ieee.org/document/11517375/'
rights: 'https://creativecommons.org/licenses/by/4.0/legalcode'
pages: '73744--73764'
issn: '2169-3536'
abstract: "Understanding large earthquakes (EQs) has been a critical endeavor. Recent advancements in machine learning (ML) help this endeavor, yet they face formidable performance ceilings due to our technical limitations, restricted access to seismogenic fault zones, and the lack of large datasets for ML training. This paper introduces a novel approach by conceptualizing the EQ-bearing lithosphere as a chaotic system and investigating whether the least action principle (LAP) from Hamiltonian mechanics can illuminate the potential predictability of large EQ initiation. Leveraging an abstract space defined by time and rupture derivatives, this paper establishes a potential causal pathway between novel LAP-based features and large EQs. An evolving ML framework utilizing parallel evolution strategies was developed to identify hidden rules derived from LAP. The model was trained on data from all EQs in the western U.S. over the past 40 years. Feasibility tests on historical large EQs show promising performance compared to state-of-the-art forecasting methods. While practical applicability requires deeper investigation, these findings suggest a new research direction for large EQ prediction that merges classical physics and evolving ML."
image:
  caption: "The Least Action Principle (LAP) in the Cycle of Earthquake (EQ) Generation and AI-Driven Evolution of Rules. (A) Overall Role of LAP in EQ Cycles: This paper mainly hypothesizes that within any time interval the earth lithosphere satisfies LAP to determine the locations and magnitudes of next ruptures, thus releasing kinetic energy. By the energy conservation, the PE function is shifted to balance the loss of energy by EQs. This constitutes an incessant cycle (dashed box) being fueled by the tectonic plate motions of the Earth. (B) Flow of Training and Inference: The training process employs a parallel Evolution Strategy (ES) to coherently evolve EQ- and LAP-based rules while keeping V and directivity fixed. Conversely, V and directivity are evolved while the rules remain frozen. This two-stage cyclic evolution runs across parallel cores (e.g., >100 CPUs). During inference, the best-so-far LAP-based rules are applied to predict EQs for the future time window. (C) Abstract Space of Time and Derivatives of Rupture Length R(t) of LAP. Example plots of the first derivative of rupture, i.e., rupture velocity (D) and the second derivative of the rupture, rupture acceleration (E). These example plots are drawn from the Ridgecrest EQ (Mw = 7.1, 2019, July 6)."
  focal_point: ""
  preview_only: false
---