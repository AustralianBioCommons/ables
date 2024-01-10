---
title: Parabricks and GATK benchmarking
description: Benchmarking for NVIDIA Parabricks and GATK RNA-Seq variant calling workflows.
toc: false
type: projects
---

## Bioinformatics leads

- Locedie Mansueto <l.mansueto.10@student.scu.edu.au >


## Details

This project is for an updated analysis for NVIDIA Parabricks and GATK benchmarking for RNA-Seq, based on NVIDIA recommendations.

Workflows included are RNA-Seq variant calling pipelines:
- [GATK RNA-Seq variant discovery](https://gatk.broadinstitute.org/hc/en-us/articles/360035531192-RNAseq-short-variant-discovery-SNPs-Indels-), and 
- [Parabricks rna_fq2bam](https://docs.nvidia.com/clara/parabricks/3.8.0/Documentation/ToolDocs/man_rna_fq2bam.html)

The number of discovered variants, service unit (SU) usage and runtime will be compared.

This is a follow-up run based on the recommendation from NVIDIA to use specific versions (`Parabricks 3.8`, `GATK v4.2.0.0`, `STAR v2.7.2`) for compatibility. 

The test data are from 21 RNA-Seq Cannabis samples and cs10 genome assembly.
