---
title: "buscar"
description: "Hit calling — identifies biologically active perturbations from single-cell morphological profiles using distribution-level scoring."
problem: "Population-level hit calling averages away cell-to-cell variation, hiding heterogeneous responses and rare subpopulations."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/WayScience/buscar/main/logo/just-icon.png"
---

<img class="logo-light" src="https://raw.githubusercontent.com/WayScience/buscar/main/logo/with-text-for-light-bg.png" alt="buscar logo" width="400">
<img class="logo-dark" src="https://raw.githubusercontent.com/WayScience/buscar/main/logo/with-text-for-dark-bg.png" alt="buscar logo" width="400">

`buscar` scores perturbations directly on single-cell distributions using Earth Mover's Distance, preserving heterogeneity throughout hit calling.

**Problem:** Population-level hit calling averages away biologically meaningful cell-to-cell variation, making heterogeneous responses and rare subpopulations invisible to standard metrics.

**Key capabilities:**

- Define on-target and off-target morphology signatures from reference profiles
- Score perturbation efficacy via Earth Mover's Distance
- Assess specificity with off-target scoring to reduce false positives
- Preserve single-cell heterogeneity throughout hit calling
- Integrates directly with `Pycytominer`, `coSMicQC`, and `CytoTable` workflows

**[View on GitHub →](https://github.com/WayScience/buscar)**
