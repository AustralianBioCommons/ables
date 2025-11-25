---
title: Queensland Research Centre for Peripheral Vascular Disease, AITHM, James Cook University
description: This project is an integrative meta-analysis of preexisting scRNA-seq datasets from humans with abdominal aortic aneurysm (AAA) and mouse models of AAA.
toc: false
type: ABLeS Participant
---

## Project title

Using single-cell transcriptomics and genomic biomarkers to drive abdominal aortic aneurysm risk prediction, diagnosis and therapeutic interventions.

## Contact(s)

- Kristen Barratt, JCU, <kristen.barratt@jcu.edu.au>,  <kkbarratt@gmail.com>

## Project description and aims

- Background and context:
Abdominal aortic aneurysm (AAA) occurs due to progressive weakening and expansion of the abdominal aorta. It affects 4-5% of the population 1,2, with males >60 years particularly at risk 3. Despite decades of pre-clinical research aimed at identifying diagnostic biomarkers and drug interventions that limit or prevent AAA growth, the most effective clinical strategies remain early detection and imaging surveillance of small, asymptomatic AAAs. Surgical repair is performed only for large or symptomatic AAA 3. Even with emergency surgical repair, the mortality rate of ruptured AAA remains 76-90% 4–6. These realities underscore the need for new approaches that can advance our mechanistic understanding of AAA and guide therapeutic development.
In this project we will conduct an integrative meta-analysis of publicly available human and mouse single-cell RNA-sequencing (scRNA-seq) AAA datasets to generate a comprehensive analysis of AAA at the transcriptomic level. This will give us new insight into the pathophysiology of AAA, identify novel therapuetic targets, and allow us to recommend the which AAA mouse model recapitulates human AAA the best.  

- Aim: Perform an integrative meta-analysis of publicly available human and mouse single-cell RNA-sequencing AAA datasets
In our recent systematic review of publicly available human and mouse AAA scRNA-seq datasets, we found substantial methodological heterogeneity between studies, including that most sequenced only a single sample per group. This calls into question the results that each study obtained due to limited statistical power. To address this, we will perform an integrative meta-analysis of all eligible datasets, treating individual sequencing samples as ‘pseudo-bulks’ to enable robust statistical analyses. This approach will allow us to identify consistent differentially expressed genes across datasets, detect and characterise previously unrecognised cell types in aortic and aneurysm tissue, and compare mouse AAA models to human disease at the cellular and molecular level. By collating, harmonising, and re-analysing all publicly available datasets across species, we aim to generate a unified, high-resolution map of aneurysm development.

- Methodology: We identified thirteen single-cell RNA sequencing (scRNA-seq) datasets from mouse and human AAA studies in public repositories (e.g., GEO) based on defined inclusion and exclusion criteria. Processed count matrices will be downloaded and analysed using the Seurat pipeline in R. Each dataset will undergo quality control (filtering by mitochondrial %, feature and transcript counts, and removal of doublets and ambient RNA), followed by preliminary cell-type annotation. Datasets will then be integrated by species using Seurat’s Harmony workflow. This is the most computationally intensive step in the pipeline, involving anchor identification and PCA-based dimensionality reduction. The resulting integrated datasets (~60–70 GB each) will be further processed to produce a unified UMAP embedding, re-annotated by cell type, and subdivided for downstream analyses including differential expression, cell proportion analysis, gene set enrichment, and RNA velocity modelling. Comparative analyses will identify conserved and divergent molecular and cellular features between human and mouse AAA datasets.

- Resource requirements:
The analyses proposed involves large datasets and computationally intensive steps that cannot be run solely on a standard desktop computer. While some preprocessing and exploratory analyses will be conducted locally, the HPC will be used for steps that exceed local memory or processing capacity.
The Harmony integration of the single-cell datasets is highly memory-intensive and must be run on a single core with substantial RAM. Downstream analyses, including RNA velocity, differential gene expression, and UMAP embedding, are less memory-intensive but benefit from multi-core processing. The analysis pipeline requires access to R and RStudio, with the ability to install packages such as Seurat and Bioconductor dependencies (e.g. scDblFinder, SingleCellExperiment, DOSE, clusterProfiler, DESeq2, etc). Some steps are more efficiently run in or require Python for analysis (CellPhone and Velocyto), requiring Ubuntu OS and pip also.

## How is ABLeS supporting this work?


This work is supported through the Production Bioinformatics scheme provided by ABLeS. The support includes storage and compute allocation.

## Expected outputs enabled by participation in ABLeS

This project will generate a high-resolution transcriptomic map of AAA, revealing new mechanistic insights into disease development. It will identify conserved and divergent cell types and pathways between human AAA and mouse models, guiding the choice of appropriate preclinical models. The analysis will also uncover candidate genomic and transcriptomic biomarkers to improve risk prediction, diagnosis, and inform therapeutic development.

Using ABLeS and the NCI HPC will allow us to publish the integrative metanalysis in a relatively high impact journal for our field (similar papers have been published in ATVB, IF of 10). Analysis code will be made publicly available in online repositories. The datasets being used are preexisting so will not be re-published. 

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
