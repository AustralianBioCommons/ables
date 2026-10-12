---
title: Translational Intelligence, The Kids Research Institute Australia
description: This project aims to build a unified AI-assisted workflow that takes a single genetic variant and limited, non-identifiable patient information as input and returns curated, evidence-backed report to guide rare disease research. Over 12 months, we will evaluate at least 50 rare disease variants and release the workflow, examples and benchmark for reuse by Australian life science researchers.

toc: false
type: ABLeS Participant
page_id: thekids-4
---

## Project title

Agentic workflows for variant interpretation and evidence integration in rare disease

## Collaborators and funding

Leading institution: [The Kids Research Institute Australia](https://www.thekids.org.au/)

Funding: [Stan Perron Charitable Foundation](https://www.perronfoundation.org.au/)

## Contact(s)

- Isabelle Bond, The Kids Research Institute Australia, <isabelle.bond@thekids.org.au>

- Rafael Peres da Silva, The Kids Research Institute Australia, <Rafael.PeresdaSilva@thekids.org.au>

## Project description and aims

This project aims to build one unified workflow for genetic variant interpretation in rare disease that takes a single genetic variant and available patient information (phenotype/HPO terms and relevant clinical context) as input and returns curated evidence about that variant. A vast amount of relevant open-source data already exists, but it is scattered across many sources and often underused. Our group has previously published tools for literature search (https://doi.org/10.64898/2026.07.07.736901), RNA sequencing re-analysis (https://doi.org/10.1101/2025.11.04.686647) and gene set interpretation (https://doi.org/10.1371/journal.pcbi.1014500). This project will connect these tools alongside other in-house modules and relevant external opensource software through agentic systems. These systems will focus on orchestration and evaluation of existing tools with local LLM inference where needed.

The workflow will standardise the input before collecting evidence from the literature, public RNA sequencing studies, gene function data and variant annotations. It will then output a clear report combining this evidence and adhering in full to the FAIR guiding principles (https://www.gofair.foundation/fair-principles). We will then test the workflow on at least 50 rare disease variants with public or synthetic patient context.

The specific aims of this project are:

- Build databases and knowledge graphs that standardise the retrieval and storage of open-source data.

- Develop a trustworthy workflow that takes a genetic variant as input and reports evidence about literature, previous variant curation, biological mechanism and pathogenicity.

- Measure report accuracy, completeness, analyst time and compute cost against the current manual workflow.
The project repository will be hosted at: https://github.com/orgs/tkria/translationalintelligence 

## How is ABLeS supporting this work?

This work is supported through the Production Bioinformatics scheme provided by ABLeS.

## Expected outputs enabled by participation in ABLeS

A publicly hosted instance of MicrobialExplorer, accessible via a web URL for use by researchers at The Kids Research Institute Australia and external collaborators. The application and its source code will be maintained on GitHub (agudeloromero/MicrobialExplorer) for transparency and reproducibility. A methods publication describing the application is also planned (target journal TBC).

Hosting MicrobialExplorer through ABLeS will also support upcoming funding applications, including an ARC Future Fellowship and WA Department of Health grant opportunities.

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
