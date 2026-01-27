# RFE-Variance-Equilibrium-Despeckling

This repository accompanies the manuscript **“Deterministic Locality Algorithm for Structure-Preserving Speckle Suppression via Radial Flux Equilibrium”**, which introduces a deterministic, single-pass despeckling framework for coherent imaging modalities grounded in **Radial Flux Equilibrium (RFE)**.

<p align="center">
  <img src="IMAGE_ULTRASOUND_CT_RADAR/concon" width="620"/>
</p>

**Figure:** Representative Model's graph and results, illustrating variance-equilibrium despeckling and radiometric preservation across modalities.

## Overview

Speckle suppression in coherent imaging is fundamentally challenging due to the multiplicative, signal-dependent nature of speckle noise, which induces spatially heterogeneous statistics and compromises both structural integrity and radiometric consistency. The proposed RFE framework formulates despeckling as a **solved statistical equilibrium problem**, replacing heuristic tuning and iterative correction with analytically derived variance control anchored in measured image statistics.

The method integrates analytic locality with data-driven statistical calibration to achieve predictable variance reduction while preserving edges, ordering, and radiometric relationships. All operations are non-iterative, deterministic, and computationally efficient, enabling reproducible deployment in practical imaging pipelines.

## Methodological Principles

The RFE despeckling pipeline is built on three tightly coupled components:

- **Deterministic Fisher-Motivated ROI Selection**  
  Homogeneous calibration regions are selected automatically by minimizing a Fisher-motivated log-amplitude flatness functional under an explicit edge-density constraint. This eliminates operator bias and yields reproducible estimates of the mean intensity, low- and high-frequency variances, and locality moments required for variance targeting.

- **Closed-Form Variance Targeting Prior to Spatial Blending**  
  Given a user-specified Equivalent Number of Looks (ENL), despeckling strength is imposed analytically through a closed-form variance identity that determines frequency-domain gain factors before any spatial operation. Feasibility is ensured by adaptively constraining the high-frequency budget, transforming noise control from heuristic parameter selection into a deterministic, data-conditioned solution.

- **Radial Flux Equilibrium Locality Coupling**  
  Spatial coherence is enforced using a radial locality kernel whose influence on the output variance is governed exclusively by its first two moments. The kernel shape enters purely as a geometric profile, while the analytically solved variance equilibrium remains invariant, guaranteeing kernel-agnostic ENL control, directional consistency, and predictable saturation behavior.

Radiometric fidelity and edge preservation are further protected via an order-preserving marginal rearrangement within the calibration region, followed by an RFE-consistent blending step.

## Experimental Validation

The framework is validated on real synthetic aperture radar (SAR) and ultrasound imagery, demonstrating:
- predictable ENL trajectories that converge to analytically admissible equilibria,
- radiometric regressions with slopes near unity and negligible intercepts, and
- strong structural and edge preservation at comparable noise levels.

These results establish RFE as a reproducible and practically deployable alternative to iterative, heuristic, or learning-based despeckling approaches when interpretability, statistical traceability, and robustness are required.

## Code Availability

The full implementation of the proposed RFE framework, including ROI selection, variance targeting, locality coupling, and evaluation routines, is available upon reasonable request for academic research and peer-review purposes. This public repository provides methodological documentation, dataset provenance, and access instructions to support transparency and reproducibility.




----

