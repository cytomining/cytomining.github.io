---
title: "OME-arrow"
description: "Image storage — stores microscopy images alongside metadata and derived data in a unified, queryable Apache Arrow format."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/WayScience/OME-arrow/main/docs/src/_static/ome-arrow-logo.png"
---

<img src="https://raw.githubusercontent.com/WayScience/OME-arrow/main/docs/src/_static/ome-arrow-logo.png" alt="OME-arrow logo" width="400">

OME-arrow brings Open Microscopy Environment (OME) specifications to Apache Arrow, enabling microscopy images to be stored directly in data tables alongside their metadata and derived features as multilayer structs.
This makes bioimaging data fast to query, easy to share, and compatible with modern tensor-based ML workflows.

**Key capabilities:**

- Store images, metadata, and derived features together in a single table
- Support for TIFF, OME-Zarr, NumPy, and Parquet source formats
- Lazy reading and region-of-interest (ROI) access for large datasets
- Tensor-focused output compatible with PyTorch, JAX, and DLPack
- Visualization integrations for matplotlib, PyVista, and Napari

**[View documentation →](https://wayscience.github.io/ome-arrow/)**
