---
title: "OME-arrow"
description: "Image storage — stores microscopy images alongside metadata and derived data in a unified, queryable Apache Arrow format."
problem: "Images and feature tables live in separate systems — linking a numeric outlier back to its source cell requires error-prone manual joins across formats."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/WayScience/OME-arrow/main/docs/src/_static/ome-arrow-logo.png"
---

<img src="https://raw.githubusercontent.com/WayScience/OME-arrow/main/docs/src/_static/ome-arrow-logo.png" alt="OME-arrow logo" width="400">

**Problem:** Images and feature tables live in separate systems — linking a numeric outlier back to its source cell requires error-prone manual joins across formats.
`OME-arrow` embeds images as first-class columns in Apache Arrow tables, so features, metadata, and pixel data travel together and can be queried or exported as tensors.

**Key capabilities:**

- Store images, metadata, and derived features together in a single table
- Support for TIFF, OME-Zarr, NumPy, and Parquet source formats
- Lazy reading and region-of-interest (ROI) access for large datasets
- Tensor-focused output compatible with PyTorch, JAX, and DLPack
- Visualization integrations for matplotlib, PyVista, and Napari

**[View documentation →](https://wayscience.github.io/ome-arrow/)**
