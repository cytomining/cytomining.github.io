---
title: "iceberg-bioimage"
description: "Data cataloging — scans bioimaging stores and publishes image metadata to Cytomining-compatible Parquet warehouses via Apache Iceberg."
showDate: false
showAuthor: false
logoUrl: "https://raw.githubusercontent.com/WayScience/iceberg-bioimage/main/docs/src/_static/iceberg-bioimage-logo.png"
---

<img src="https://raw.githubusercontent.com/WayScience/iceberg-bioimage/main/docs/src/_static/iceberg-bioimage-logo.png" alt="iceberg-bioimage logo" width="400">

iceberg-bioimage is a Python package that catalogs bioimaging data using Apache Iceberg.
It scans image stores across formats, publishes structured metadata tables, and exports layouts compatible with the Cytomining profiling ecosystem — bridging raw image archives and downstream analysis pipelines.

**Key capabilities:**

- Scan image stores into canonical `ScanResult` objects
- Publish image metadata with PyIceberg for versioned, queryable catalogs
- Export Cytomining-compatible Parquet warehouses for profiling workflows
- Validate profile tables against microscopy join contracts
- Supports Zarr, OME-TIFF, and Parquet source formats

**[View documentation →](https://wayscience.github.io/iceberg-bioimage/)**
