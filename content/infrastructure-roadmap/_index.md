---
title: "AI-Ready Infrastructure Roadmap"
description: "A 24-month roadmap for unified, scalable, and AI-ready Cytomining data infrastructure."
showDate: false
showAuthor: false
---

<div class="roadmap-doc">

This roadmap defines the next phase of Cytomining infrastructure work. It is organized for two audiences: reviewers who need to understand the purpose and expected outcomes, and developers who need a clear implementation map.

The work focuses on three connected components:

1. Unified multimodal data infrastructure through OME-Arrow.
2. Single-cell scale efficiency through Polars, benchmarking, and iceberg-bioimage.
3. AI-ready image-based profiling through agent-readable APIs, ecosystem skills, and human-in-the-loop checkpoints.

## Roadmap summary

| Component | Main outcome | Primary users | Timeframe |
| --- | --- | --- | --- |
| Unified multimodal data infrastructure | Images, segmentation geometries, morphology profiles, metadata, and QC annotations live in one schema-enforced, queryable representation. | Cell biologists, image analysts, tool developers | Year 1 to Year 2 |
| Single-cell scale efficiency | Researchers can query and process population-scale single-cell datasets without loading full screens into memory. | Profiling teams, data engineers, maintainers | Year 1 to Year 2 |
| AI-ready image-based profiling | Researchers and AI agents can run complete workflows through typed APIs and documented decision points. | New users, expert analysts, agent framework developers | Year 1 to Year 2 |

## Why this work matters

The current Cytomining ecosystem supports high-content microscopy workflows through tools such as [CytoTable](/tools/cytotable/), [coSMicQC](/tools/cosmicqc/), and [Pycytominer](/tools/pycytominer/). These tools make it possible to process single-cell morphology features, but the surrounding data infrastructure still creates friction:

- Images, profiles, segmentation geometries, and QC annotations often live in separate files or stores.
- Large single-cell datasets are difficult to query lazily across plates, projects, and public reference collections.
- Workflow expertise is distributed across documentation, notebooks, and maintainer knowledge rather than encoded as typed APIs and reusable agent guidance.

The roadmap addresses these gaps by making data co-located, queryable, versionable, benchmarked, and easier for both people and AI systems to operate safely.

## Component 1: Unified Multimodal Data Infrastructure

**Goal:** Integrate OME-Arrow across the Cytomining stack so microscopy images, segmentation geometries, morphology profiles, metadata, and QC annotations share a single schema-enforced data model.

**Reviewer view:** This component removes a major source of manual reconciliation. Researchers should be able to trace a morphology measurement back to the source image and segmentation context without fragile joins across independent files.

**Developer execution:**

| Deliverable | Implementation notes | Target |
| --- | --- | --- |
| OME-Arrow schema and CytoTable read/write support | Add native OME-Arrow input and output paths in CytoTable. Verify numerical equivalence against public reference datasets such as JUMP-CP and RxRx19. | Year 1 |
| Pycytominer and coSMicQC integration | Enable Pycytominer to operate directly on OME-Arrow datasets and coSMicQC to write QC annotations back into the same store. | Year 1 |
| Documentation and tutorials | Publish OME-Arrow tutorials and revise Cytomining notebooks to show end-to-end workflows without format conversion. | Year 1 |
| OME community specification | Prepare a formal OME-Arrow specification and participate in OME community review through public issues or pull requests. | Year 2 |
| Project migration | Move OME-Arrow from WayScience to Cytomining once it meets ecosystem maturity expectations. | Year 2 |

**Success indicators:**

- Fewer workflow steps are required to connect source images with morphology profiles compared with a documented baseline workflow.
- End-to-end pipelines run without manual conversion between image, profile, and QC stores.
- At least three external groups adopt OME-Arrow in public workflows, publications, or repositories.
- OME community discussion shows documented progress toward broader standard recognition.

## Component 2: Single-Cell Scale Efficiency

**Goal:** Make Cytomining workflows efficient at population scale through lazy queries, faster dataframe execution, versioned bioimage catalogs, and release-indexed benchmarks.

**Reviewer view:** This component lets researchers work with large-scale morphology data as queryable scientific infrastructure rather than local files that must be fully loaded and copied at each step.

**Developer execution:**

| Deliverable | Implementation notes | Target |
| --- | --- | --- |
| Polars integration | Integrate Polars across Cytomining tools for ingestion, QC, normalization, feature selection, and related table operations. | Year 1 |
| Format and engine benchmark | Compare speed, memory, and storage across AnnData, Zarr, CSV, SQLite, Parquet, DuckDB, Lance, and related approaches. | Year 1 |
| Release benchmark dashboard | Add automated benchmark runs for Cytomining releases and publish version-indexed results. | Year 1 |
| iceberg-bioimage v1.0 | Release cloud-agnostic object storage support with FAIR, version-controlled image cataloging. | Year 2 |
| Cytomining integration for iceberg-bioimage | Connect iceberg-bioimage with CytoTable, coSMicQC, and Pycytominer through a reference pipeline notebook. | Year 2 |
| Project migration | Move iceberg-bioimage from WayScience to Cytomining once it reaches production maturity. | Year 2 |

**Success indicators:**

- Benchmarks show major speed and memory improvements over pandas-based workflows across core pipeline stages.
- At least one population-level reference dataset can be queried lazily without loading the full dataset into memory.
- Benchmark results are published for at least two major Cytomining releases.
- Developers can use benchmark output to identify bottlenecks before releases.

## Component 3: AI-Ready Image-Based Profiling

**Goal:** Make Cytomining workflows executable by both researchers and code-writing agents through typed APIs, reusable workflow knowledge, and explicit human-in-the-loop decision points.

**Reviewer view:** This component lowers the barrier to running image-based profiling while keeping expert biological judgment in the loop. AI systems can help execute workflows, but the roadmap explicitly defines where humans review, choose, and record decisions.

**Developer execution:**

| Deliverable | Implementation notes | Target |
| --- | --- | --- |
| Cytomining ecosystem skill | Publish a versioned skill with tool-specific sections for pipeline orchestration, QC conventions, normalization strategies, and processing decisions. | Year 1 |
| Agent-readable APIs | Validate function signatures, docstrings, and schemas across Cytomining tools using agentic coding systems. | Year 1 |
| Human-in-the-loop taxonomy | Define biological judgment points, starting with QC threshold selection, and log human decisions into provenance records. | Year 1 |
| AI-readiness benchmark suite | Evaluate agent-driven execution with and without the Cytomining skill against expert-validated reference outputs. | Year 2 |
| Ecosystem protocol manuscript | Document the Cytomining ecosystem protocol and supporting technologies in a citable manuscript. | Year 2 |

**Success indicators:**

- Agent-driven workflows complete more accurately and faster when using the Cytomining skill than when using baseline documentation alone.
- Human decisions at biological judgment points are logged and can be reviewed after workflow execution.
- At least two external groups without prior Cytomining expertise complete a profiling workflow using the skill and typed APIs.
- Benchmark reports track correctness, time to completion, and divergence between agent recommendations and human choices.

## Cross-cutting implementation principles

- **Composable tools:** Each component should improve the shared ecosystem without making any single tool monolithic.
- **Public validation:** Outputs should be checked against public reference datasets where possible.
- **Provenance by default:** Data transformations, QC annotations, human decisions, and agent actions should be recorded.
- **Cloud-ready formats:** Storage and query layers should work across local, HPC, and cloud object-storage environments.
- **Maturity before migration:** New projects should move from WayScience to Cytomining only after they have stable releases, documentation, tests, and active maintenance.

## Dependencies and sequencing

| Sequence | Dependency | Rationale |
| --- | --- | --- |
| 1 | Define OME-Arrow schema and CytoTable I/O | The shared representation must exist before downstream tools can rely on it. |
| 2 | Integrate Pycytominer and coSMicQC with OME-Arrow | Processing and QC need to operate on the same data model to remove conversion steps. |
| 3 | Add Polars and benchmark infrastructure | Performance changes should be measured before and after integration across tools. |
| 4 | Release iceberg-bioimage and reference notebooks | Versioned image catalogs should connect to the validated Cytomining data flow. |
| 5 | Publish AI-ready APIs and ecosystem skill | Agent guidance should encode the stabilized workflow, not a moving target. |
| 6 | Run AI-readiness benchmarks | Benchmarks should evaluate the integrated workflow against expert references. |

## What done looks like

By the end of this roadmap, Cytomining should support an end-to-end workflow where a researcher can:

1. Catalog microscopy images into a versioned bioimage store.
2. Co-locate images, segmentation geometries, morphology profiles, metadata, and QC annotations in an OME-Arrow-compatible representation.
3. Query and process large single-cell datasets lazily and reproducibly.
4. Run CytoTable, coSMicQC, and Pycytominer through typed, documented APIs.
5. Use AI-assisted workflow execution while preserving human review at biological decision points.
6. Compare performance and AI-readiness across releases using public benchmark reports.

</div>
