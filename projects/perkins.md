---
title: Harry Perkins Institute of Medical Research
contributors: [Ziad Al-Bkhetan, Johan Gustafsson]
description: Rare Disease Genetics and Functional Genomics
toc: false
type: projects
---

## Bioinfomatics leads

Gina Ravenscroft <gina.ravenscroft@perkins.uwa.edu.au> and Mridul Johari <mridul.johari@uwa.edu.au>

## Details

We are analysing DNA and RNA sequencing data from rare disease patients to identify genomic variants that may be contributing to disease. This first requires the processing of the raw sequencing read (FASTQ) files to file formats that are compatibile with variant calling (BAM and VCF). 

Downstream analyses include: using variant filtering/prioritisation platforms to identify putatively diesease causing SNPs/indels in patient WGS/WES data; the detection of structural variants in WGS/WES data; the detection of aberrant splice and expression events using RNAseq data; the identification of known and novel repeat expansions using STR calling programs; and the modelling of mutations on protein structures.

Our workflows are currently distributed across multiple compute platforms at multiple institutes as well as on local resources. 

Our long-term plan is to consolidate these resources to one location, increase our compute resources with increased demand, and test these workflows.

Goals:

Briefly, the broad goals of this project are to:

1. Consolidate HPC resources to free up cloud and local compute
2. Provide increased compute resources coinciding with expected increased demand and emergence of new technologies
3. Reanalyse old data using new pipelinesThe general workflows/analyses for this project are as follows:
4. Align next generation sequencing (NGS) data from rare disease patients to the reference genome using the Genome Analysis ToolKit (GATK) or similar to facilitate downstream analysis (below)
5. Call SNPs and indels using GATK- Call structural variants using the Germline-StructuralV-nf pipeline
6. Call STRs using EH, EHdn, and STRipy
7. RNA-seq data processing using nfcore/rnaseq
8. Detecteing aberrant splicing and expression outliers in RNAseq data using the Detection of RNA Outliers Pipeline (DROP)
9. Model protein structures using AlphaFold
