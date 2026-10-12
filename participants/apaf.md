---
title: Australian Proteome Analysis Facility, Macquarie University
description: This project develops and benchmarks a novel, groundbreaking mathematical framework that leverages topological data analysis and optimal transport to align disparate spatial modalities while strictly preserving full tissue mass and cellular topology across severe physical deformations.
toc: false
type: ABLeS Participant
---

## Project title

Scalable Multi-Modal Spatial Omics Integration via a novel mathematical algorithm

## Collaborators and funding

Australian Proteome Facility, Macquarie University.

## Contact(s)

- Ignatius Pang, Australian Proteome Analysis Facility (APAF), <ignatius.pang@mq.edu.au>


## Project description and aims

### Scientific Context & Challenge

Spatial biology has accelerated from single-modality experiments to complex multi-omics assays that measure spatial gene expression, targeted antibody panels, and untargeted metabolite/lipid distributions within the same tissue specimen. Reconstructing three-dimensional tissue structures and harmonizing cross-technology experiments requires robust pairwise and multi-slice registration. 

Current computational approaches face severe limitations:

1. **Extrinsic Metric Sensitivity**: Methods relying on Cartesian Euclidean coordinates (e.g., standard Fused Gromov–Wasserstein / PASTE) fail when slices experience non-isometric shear or non-linear elastic stretching during histological sectioning.

2. **Artificial Margin Discarding**: Partial optimal transport methods (e.g., PASTE2) achieve nominal accuracy by mathematically dropping 15–20% of spots, selectively pruning ambiguous border cells and damaged margins rather than solving the true registration problem.

3. **Cross-Modality Incompatibility**: Methods that require shared gene features cannot align spatial transcriptomics with mass spectrometry imaging or antibody-based proteomics.

### Project Aims

- **Aim 1: Topological Data Analysis and Optimal Transport**: Develop, implement, and optimise our novel algorithm that is robust to different types of stresses and damage applied to the tissue samples, including non-linear warping and tissue lacerations.

- **Aim 2: Rigorous Combinatorial Benchmarking on Pawsey Setonix**: Deploy a reproducible Nextflow DSL2 pipeline on Setonix to evaluate SC-FGW against 12 state-of-the-art algorithms that operate on spatial coordinates and molecular feature matrices (PASTE, PASTE2, MOSCOT, GPSA, SLAT, STalign, etc.) across:
  - 13 biological datasets (Human DLPFC, Andersson Breast Cancer, Mouse Olfactory Bulb, Stereo-seq Whole Embryo MOSTA, MALDI brain serial sections, and CODEX colorectal cancer).
  - 4 synthetic stress-testing regimes (anisotropic shear, planar rotation, non-linear elastic deformation, and tissue tearing).
  - Two resolution tiers (Tier 1 downscaled grids and Tier 2 native resolution exceeding 2,000 spots per slice).

- **Aim 3: Formal Mathematical Verification**: Provide machine-checked formal verification of all underlying optimal transport theorems, metric properties, and convergence bounds in the Lean 4 interactive theorem prover, guaranteeing zero algorithmic failure states.

### High-Performance Computing Justification

Native-scale spatial alignment problems require optimizing quadratic assignment problems over thousands of cells with non-convex manifold constraints. Individual full-scale tasks require up to 32 cores and 128 GB RAM to compute toplogical data analysis and optimal transport calculation iterations. The full multi-donor combinatorial benchmark requires 12,516 individual process executions (120,000–250,000 core-hours). Pawsey Setonix’s high-speed Lustre scratch filesystem and distributed Slurm scheduling via Nextflow DSL2 provide a viable infrastructure capable of completing this workload at scale.

## How is ABLeS supporting this work?

This work is supported through the production bioinformatics scheme provided by ABLeS. The supports includes storage and compute resources.

## Expected outputs enabled by participation in ABLeS

Participation in ABLeS on Pawsey Setonix directly enables the generation, publication, and FAIR dissemination of the following research outputs:

1. **Open-Source Scientific Software**:
   - ** The Python Package**: Production-grade, vectorized implementation supporting PyTorch and POT backends, released under an open-source MIT license on PyPI and GitHub.
   - **Containerized Nextflow DSL2 Pipeline**: An automated, portable, and nf-core compliant workflow containerized with Singularity and Docker, enabling Australian and international researchers to run robust spatial omics alignment workflows on institutional clusters or cloud environments.

2. **FAIR-Compliant Benchmark Data & Artifacts**:
   - **Standardized Spatial Benchmark Corpus**: Curated, preprocessed AnnData objects across 13 tissue systems with standardized cell annotations and synthetic distortion sets deposited on public data repositories (NCBI GEO and BioStudies).
   - **Comprehensive Evaluation Archive**: Master benchmark records (15,000 evaluated configurations), CSV performance summaries, and runtime Pareto frontiers deposited with permanent, citable DOIs on **Zenodo** in compliance with FAIR data principles.

3. **High-Impact Scientific Publications**:
   - A lead manuscript submitted to a peer-reviewed computational biology journal (e.g. Bioinformatics), citing Australian BioCommons and Pawsey Setonix support.
   - A companion mathematical formalization repository with machine-checked proofs in Lean 4 verifying the novel algorithm in spatial data science.

4. **Australian Research Capability Building**:
   - Workflows, tutorials, and documentation will be shared with the Australian BioCommons community through collaborative webinars, computational biology workshops, and BioCommons workflow registries, empowering Australian researchers to analyze complex spatial multi-omics datasets with state-of-the-art national HPC tools.

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
