---
title: "zedprofiler"
description: "3D feature extraction — extracts morphological features from volumetric microscopy images for CPU-efficient high-content profiling."
problem: "Classical profiling tools only extract 2D features, leaving organoid and z-stack experiments without a CPU-efficient extractor."
showDate: false
showAuthor: false
---

**Problem:** Classical profiling tools extract only 2D features, leaving organoid, cleared-tissue, and z-stack experiments without a CPU-efficient extractor.
`zedprofiler` extracts morphological features directly from 3D volumetric images, including anisotropic voxel spacing correction — no GPU required.

**Key capabilities:**

- Extract features from 3D volumetric (z-stack) single-cell images
- Multi-channel fluorescence microscopy support
- Anisotropic voxel spacing correction for accurate 3D measurements
- Modular, extensible architecture for custom feature sets
- CPU-optimized for high-throughput processing without GPU dependency

**[View on GitHub →](https://github.com/WayScience/zedprofiler)**
