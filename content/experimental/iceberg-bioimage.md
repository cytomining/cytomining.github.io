---
title: "iceberg-bioimage"
description: "Data cataloging — scans bioimaging stores and publishes image metadata to Cytomining-compatible Parquet warehouses via Apache Iceberg."
problem: "Raw bioimaging archives have no standard catalog — finding, versioning, and joining images to downstream data requires bespoke scripts per lab."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/WayScience/iceberg-bioimage/main/docs/src/_static/iceberg-bioimage-logo.png"
---

<img src="https://raw.githubusercontent.com/WayScience/iceberg-bioimage/main/docs/src/_static/iceberg-bioimage-logo.png" alt="iceberg-bioimage logo" width="400">

**Problem:** Raw bioimaging archives have no standard catalog — finding, versioning, and joining images to downstream data requires bespoke scripts per lab.
`iceberg-bioimage` scans any image store into a versioned Apache Iceberg catalog that directly exports Cytomining-compatible Parquet warehouses.

**Key capabilities:**

- Scan image stores into canonical `ScanResult` objects
- Publish image metadata with PyIceberg for versioned, queryable catalogs
- Export Cytomining-compatible Parquet warehouses for profiling workflows
- Validate profile tables against microscopy join contracts
- Supports Zarr, OME-TIFF, and Parquet source formats

**[View documentation →](https://wayscience.github.io/iceberg-bioimage/)**
