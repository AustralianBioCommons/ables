---
title:  Southern Cross University
description: Benchmarking for NVIDIA Parabricks and GATK RNA-Seq variant calling workflows.
toc: false
type: ABLeS Participant
---

## Project title
Parabricks and GATK benchmarking

## Collaborators and funding


## Contact(s)

- Locedie Mansueto <l.mansueto.10@student.scu.edu.au>

## Project description and aims

This project is for an updated analysis for NVIDIA Parabricks and GATK benchmarking for RNA-Seq, based on NVIDIA recommendations.

Workflows included are RNA-Seq variant calling pipelines:
- [GATK RNA-Seq variant discovery](https://gatk.broadinstitute.org/hc/en-us/articles/360035531192-RNAseq-short-variant-discovery-SNPs-Indels-), and 
- [Parabricks rna_fq2bam](https://docs.nvidia.com/clara/parabricks/3.8.0/Documentation/ToolDocs/man_rna_fq2bam.html)

The number of discovered variants, service unit (SU) usage and runtime will be compared.

This is a follow-up run based on the recommendation from NVIDIA to use specific versions (`Parabricks 3.8`, `GATK v4.2.0.0`, `STAR v2.7.2`) for compatibility. 

The test data are from 21 RNA-Seq Cannabis samples and cs10 genome assembly.


## How is ABLeS supporting this work?

This work is supported through Software accelerator scheme provided by ABLeS. The support includes 2 TB long term storage, 5 TB temoprary storage on scratch and 20 KSUs per quarter.

## Expected outputs enabled by participation in ABLeS

<br/>

> *These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above.*
