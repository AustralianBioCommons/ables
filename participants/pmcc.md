---
title: Transcriptome Methods Development at Peter MacCallum Cancer Centre
description: The dysregulation of splicing is a hallmark of cancer. Comparing local RNA-seq cohort data to large-scale global splicing databases remains challenging due to incompatible and specialised processing pipelines. This project aims to uniformly process local reference cohort data to allow efficient comparison with major international pre-computed datasets.
toc: false
type: ABLeS Participant
---

## Project title

Standardised processing of cancer cohort RNA-seq data for streamlined analysis and discovery

## Collaborators and funding

-   [Peter MacCallum Cancer Centre](https://www.petermac.org/)
-   [Children’s Cancer Institute](https://www.ccia.org.au/)

## Contact(s)

Andrew Lonsdale, Peter MacCallum Cancer Centre, <andrew.lonsdale@petermac.org>

## Project description and aims

Leveraging these summarised databases effectively with patient and research cohorts requires private RNA-seq samples to be processed using the same pipelines. The Snapcount and Recount3 common backend workflow differs from clinical and standard pipelines, and requires raw data to be reanalyzed and processed to directly comparable with the pre-computed public databases. The goal of this project is to develop a systematic method to: transfer files to national compute, process private samples using a common workflow, summarise at cohort level, and export results back for analysis. 

## How is ABLeS supporting this work?

Quarterly allocation of 50000 SU and 5TB of long term storage. 

## Expected outputs enabled by participation in ABLeS

The major outcome of this project would be a Snapcount3 compatible resource via a Snaptron server. This will give an API for querying splicing and metadata across across. paediatric caner cohorts for researchers to use. This will result in both a web accessible database for querying, and an associated paper disseminating key findings.  A Snaptron web service running under Docker will be deployed on institutional virtual machines  to store and disseminate the data.

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
