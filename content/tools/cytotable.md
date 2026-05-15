---
title: "CytoTable"
description: "Upstream ingestion — converts raw CellProfiler, DeepProfiler, and IN Carta outputs into scalable, analysis-ready Parquet tables."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/cytomining/CytoTable/main/logo/just-icon.png"
---

<img class="logo-light" src="https://raw.githubusercontent.com/cytomining/CytoTable/main/logo/with-text-for-light-bg.png" alt="CytoTable logo" width="400">
<img class="logo-dark" src="https://raw.githubusercontent.com/cytomining/CytoTable/main/logo/with-text-for-dark-bg.png" alt="CytoTable logo" width="400">

CytoTable harmonizes output from different high-content image analysis tools — including CellProfiler, DeepProfiler, and IN Carta — into a single, analysis-ready format.
It scales to large datasets using Apache Parquet and DuckDB under the hood.

**Key capabilities:**

- Convert CellProfiler SQLite, CSV, and other formats into Parquet
- Harmonize schema differences across analysis tools
- Scale to datasets with millions of single cells
- Produce outputs compatible with pycytominer and AnnData workflows

**[View documentation →](https://cytomining.github.io/CytoTable/)**

## Publication

<div style="border: 1px solid #e5e7eb; border-radius: 8px; padding: 1.25rem; margin: 1.5rem 0;">
  <div style="margin-bottom: 0.5rem;">
    <span style="background: #7c3aed; color: white; padding: 0.2rem 0.7rem; border-radius: 9999px; font-size: 0.78rem; font-weight: 600;">Patterns (Cell Press) · 2026</span>
  </div>
  <p style="font-weight: 600; margin: 0.5rem 0 0.25rem;">
    <a href="https://doi.org/10.1016/j.patter.2026.101514">Scalable data harmonization for single-cell image-based profiling with CytoTable</a>
  </p>
  <p style="font-size: 0.875rem; margin: 0.25rem 0 0; color: #374151;">
    Bunten D, Tomkinson J, Serrano E, Lippincott MJ, Brewer KI, et al.
  </p>
  <p style="font-size: 0.8rem; margin: 0.25rem 0 0; color: #6b7280;">
    doi: <a href="https://doi.org/10.1016/j.patter.2026.101514" style="color: #6b7280;">10.1016/j.patter.2026.101514</a>
  </p>
</div>
