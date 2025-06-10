---
title: Southern Cross University
description: Analysis for NVIDIA Parabricks and GATK benchmarking for RNA-Seq, based on NVIDIA recommendations as well as for designing probes for an amplicon-based SNP array genotyping platform.
toc: false
type: ABLeS Participant
---

## Project title

Parabricks and GATK benchmarking, and Cannabis SNPs Genotyping Array Design.

## Collaborators and funding

NVIDIA provided technical assistance and license for Parabricks.

- AUstralian Biocommons and NCI provided the Gadi HPC and GPU hardware infrastructure.

- Cannabis SNPs array genotyping is funded by the Australian Research Council (ARC) Linkage project LP210200606 (New crop on the block: The Genetic control of hempseed nutritional quality)

## Contact(s)

- Locedie Mansueto, Southern Cross University <l.mansueto.10@student.scu.edu.au>

- Ramil Mauleon, Southern Cross University, <ramil.mauleon@scu.edu.au>

- Tobias Kretzschmar, Southern Cross University, <tobias.kretzschmar@scu.edu.au>

## Project description and aims

This project is for an analysis for NVIDIA Parabricks and GATK benchmarking for RNA-Seq, based on NVIDIA recommendations.

Parabricks is a GPU-accelerated variant calling software alternative to the Genome Analysis
Toolkit GATK. Previous benchmarking project compared the GATK Germline and
Parabricks fq2bam workflows, available at [this link](https://github.com/Southern-Cross-Plant-Science/GATK-Parabricks_benchmarking_Gadi_NCI).

This project extended the pipeline and benchmarking to include the:

- [GATK RNA-Seq variant discovery](https://gatk.broadinstitute.org/hc/en-us/articles/360035531192-RNAseq-short-variant-discovery-SNPs-Indels-), and
- [Parabricks rna_fq2bam](https://docs.nvidia.com/clara/parabricks/3.8.0/Documentation/ToolDocs/man_rna_fq2bam.html)

The number of discovered variants, service unit (SU) usage and runtime will be compared.

We will be doing a follow-up run based on the recommendation from NVIDIA to use specific versions (`Parabricks 3.8`, `GATK v4.2.0.0`, `STAR v2.7.2`) for compatibility. The test data are from 21 RNA-Seq Cannabis samples and cs10 genome assembly.

The outputs from variant calling are used to design a SNP genotyping array. The goal is to identify a subset of SNPs to include in an amplicon array. Genotyping arrays are cheaper and faster alternative to whole-genome or GBS sequencing. The array will be used for genetic map construction, QTL discovery, and selection of donors for pre-breeding and
mapping studies. Optimization using classic Integer Linear Programming had been done.

This project will apply machine learning methods to identify the optimal subset. Libraries to
be tested include CPU and GPU-based decision trees (lightGBM, XGBoost), RAPIDS
Random Forrest, and genetic algorithm KNN.

## How is ABLeS supporting this work?

This work is supported through Software accelerator scheme provided by ABLeS. The support includes 2 TB long term storage, 5 TB temoprary storage on scratch and 20 KSUs per quarter.

## Expected outputs enabled by participation in ABLeS

The developed pipeline and benchmarking report are available at this [link](https://github.com/Southern-Cross-Plant-Science/GATK-Parabricks_benchmarking_Gadi_NCI).

The generated Cannabis SNP genotypes are hosted at the [ICGRC - CannSeek Genotype Viewer](https://icgrc.info/genotype_viewer). This resource will be submitted for publication soon.

Pipeline for SNP-Assay design using machine learning methods, and benchmarking between different libraries, and classical constrained mathematical programming.

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
