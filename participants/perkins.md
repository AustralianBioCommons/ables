---
title: The Rare Disease Genetics and Functional Genomics Research Group
description: Workflow consolidation, testing and implementation for Rare Disease Genetics and Functional Genomics managed by the Harry Perkins Institute of Medical Research.
toc: false
type: ABLeS Participant
---

## Project title

Rare Disease Genetics and Functional Genomics

## Collaborators and funding

## Contact(s)

- Gina Ravenscroft <gina.ravenscroft@perkins.uwa.edu.au>
- Mridul Johari <mridul.johari@uwa.edu.au>

## Project description and aims

We are analysing DNA and RNA sequencing data from rare disease patients to identify genomic variants that may be contributing to disease. This first requires the processing of the raw sequencing read (FASTQ) files to file formats that are compatibile with variant calling (BAM and VCF).

Downstream analyses include:

- Using variant filtering/prioritisation platforms to identify putatively disease causing SNPs/indels in patient WGS/WES data
- Detection of structural variants in WGS/WES data
- Detection of aberrant splice and expression events using RNAseq data
- Identification of known and novel repeat expansions using STR calling programs, and
- Modelling of mutations on protein structures

Our workflows are currently distributed across multiple compute platforms at multiple institutes as well as on local resources.

Our long-term plan is to consolidate these resources to one location, increase our compute resources with increased demand, and test these workflows.

## Goals:

Briefly, the broad goals of this project are to:

1. Consolidate HPC resources to free up cloud and local compute
2. Provide increased compute resources coinciding with expected increased demand and emergence of new technologies
3. Reanalyse old data using new pipelines

The general workflows/analyses for this project are as follows:

1. Align next generation sequencing (NGS) data from rare disease patients to the reference genome using the [Genome Analysis ToolKit (GATK)](https://bio.tools/gatk), or similar, to facilitate downstream analysis (see below)
2. Call SNPs and indels using GATK and call structural variants using the [Germline-StructuralV-nf pipeline](https://doi.org/10.48546/WORKFLOWHUB.WORKFLOW.431.1)
3. Call STRs using EH, EHdn, and STRipy
4. RNA-seq data processing using [nfcore/rnaseq](https://github.com/nf-core/rnaseq)
5. Detecting aberrant splicing and expression outliers in RNAseq data using the [Detection of RNA Outliers Pipeline (DROP)](https://gagneurlab-drop.readthedocs.io/en/latest/)
6. Model protein structures using [AlphaFold](https://bio.tools/alphafold_2)

## How is ABLeS supporting this work?

This work is supported through Production bioinformatics scheme provided by ABLeS. The supports includes unlimited temporary storage on scratch, 1 TB permenant storage and 50 KSUs per quarter.

## Expected outputs enabled by participation in ABLeS

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
