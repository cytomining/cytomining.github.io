---
title: "buscar"
description: "Hit calling — identifies biologically active perturbations from single-cell morphological profiles using distribution-level scoring."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/WayScience/buscar/main/logo/just-icon.png"
---

<img class="logo-light" src="https://raw.githubusercontent.com/WayScience/buscar/main/logo/with-text-for-light-bg.png" alt="buscar logo" width="400">
<img class="logo-dark" src="https://raw.githubusercontent.com/WayScience/buscar/main/logo/with-text-for-dark-bg.png" alt="buscar logo" width="400">

buscar is a Python package for reproducible hit calling in high-content screening.
Rather than averaging cells into population-level summaries, it operates on individual cell distributions to preserve biological heterogeneity and identify perturbations with on-target morphological signatures.

**Key capabilities:**

- Define on-target and off-target morphology signatures from reference profiles
- Score perturbation efficacy via Earth Mover's Distance
- Assess specificity with off-target scoring to reduce false positives
- Preserve single-cell heterogeneity throughout hit calling
- Integrates directly with pycytominer, coSMicQC, and CytoTable workflows

**[View on GitHub →](https://github.com/WayScience/buscar)**
