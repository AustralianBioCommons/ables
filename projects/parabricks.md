---
title: Parabricks and GATK benchmarking
contributors: [Ziad Al-Bkhetan, Johan Gustafsson]
description: 
toc: false
type: projects
---

## Bioinfomatics leads

Locedie Mansueto <l.mansueto.10@student.scu.edu.au >

## Details

This project is for an updated analysis for Parabricks and GATK benchmarking for RNA-Seq, based on NVIDIA recommendation.

This is a benchmarking test for two RNA-Seq variant calling pipelines, the [GATK RNA-Seq variant discovery](https://gatk.broadinstitute.org/hc/en-us/articles/360035531192-RNAseq-short-variant-discovery-SNPs-Indels-) and [Parabricks rna_fq2bam pipelines](https://docs.nvidia.com/clara/parabricks/3.8.0/Documentation/ToolDocs/man_rna_fq2bam.html).

The number of discovered variants, service unit usage and runtime will be compared. 
This is a follow-up run based on the reccommedation from NVIDIA to use specific versions (Parabricks 3.8,GATK v4.2.0.0, STAR v2.7.2) for compatibility. 
The test data are from 21 RNA-Seq Cannabis samples will and cs10 genome assembly.
