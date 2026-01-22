# Image Data Description

This directory contains representative image samples used exclusively for methodological validation of the proposed Radial Flux Equilibrium (RFE) despeckling framework. All images are either sourced from public-domain repositories or provided as derived regions-of-interest (ROIs) to ensure compliance with licensing and attribution constraints. No proprietary or patient-identifiable data are included.

## Radar (SAR)

The SAR image  is sourced from the NASA Jet Propulsion Laboratory (JPL) Photojournal and is in the public domain. This image exhibits fully developed speckle and strong structural boundaries, making it suitable for evaluating variance regulation, frequency-domain gain allocation, and ENL behavior in coherent radar imagery. The image is used to assess kernel-agnostic ENL control and radiometric consistency under high-speckle conditions.

## Ultrasound

The ultrasound image(s)  consist of cropped regions-of-interest derived from publicly accessible ultrasound image galleries. Only localized ROIs are included to respect source usage terms while retaining statistically homogeneous regions required for calibration and evaluation. These images are used to validate the behavior of the proposed method under multiplicative speckle, directional texture, and modality-specific anisotropy characteristic of medical ultrasound imaging.

## Computed Tomography (CT)

The CT image  is a derived axial ROI extracted from publicly available literature and is provided solely for algorithmic validation. The ROI contains approximately homogeneous soft-tissue regions suitable for assessing variance targeting and radiometric preservation in non-speckle-dominant modalities. The original full-resolution images remain subject to their respective publication copyrights and are not redistributed.

## Usage Scope

All images are employed exclusively for:
- validating variance equilibrium behavior,
- evaluating ENL control and saturation characteristics, and
- demonstrating modality-agnostic statistical consistency.

The data are not intended for clinical interpretation, diagnosis, or training of learning-based models.
