---
title: "coSMicQC"
description: "Quality control step — flags and removes low-quality cells before profile processing to prevent artifacts from propagating downstream."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/cytomining/coSMicQC/main/media/logo/just-icon.png"
---

<img class="logo-light" src="https://raw.githubusercontent.com/cytomining/coSMicQC/main/media/logo/with-text-for-light-bg.png" alt="coSMicQC logo" width="400">
<img class="logo-dark" src="https://raw.githubusercontent.com/cytomining/coSMicQC/main/media/logo/with-text-for-dark-bg.png" alt="coSMicQC logo" width="400">

coSMicQC (Single-cell Morphology Quality Control) identifies and removes low-quality cells from image-based profiling datasets before downstream analysis.
It catches common problems such as over-segmented nuclei, poorly segmented cells, and imaging artifacts.

**Key capabilities:**

- Flag over-segmented, under-segmented, and poorly focused cells
- Apply threshold-based or z-score-based QC criteria
- Generate summary reports of QC outcomes
- Integrate seamlessly with CytoTable and pycytominer workflows

**[View documentation →](https://cytomining.github.io/coSMicQC/)**

## Publication

<div style="border: 1px solid #e5e7eb; border-radius: 8px; padding: 1.25rem; margin: 1.5rem 0;">
  <div style="margin-bottom: 0.5rem;">
    <span style="background: #6b7280; color: white; padding: 0.2rem 0.7rem; border-radius: 9999px; font-size: 0.78rem; font-weight: 600;">bioRxiv Preprint · 2025</span>
  </div>
  <p style="font-weight: 600; margin: 0.5rem 0 0.25rem;">
    <a href="https://doi.org/10.1101/2025.10.14.682427">Stellar quality control for single-cell image-based profiling with coSMicQC</a>
  </p>
  <p style="font-size: 0.875rem; margin: 0.25rem 0 0; color: #374151;">
    Tomkinson J, Bunten D, Way GP
  </p>
  <p style="font-size: 0.8rem; margin: 0.25rem 0 0; color: #6b7280;">
    doi: <a href="https://doi.org/10.1101/2025.10.14.682427" style="color: #6b7280;">10.1101/2025.10.14.682427</a>
  </p>
</div>
