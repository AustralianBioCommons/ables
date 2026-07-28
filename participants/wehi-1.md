---
title: Papenfuss lab, WEHI
description: This project trains and evaluates sparse autoencoders on single cell foundation model (scFM)'s token embeddings to test whether they encode discriminative biological signals that can be faithfully recovered.
toc: false
type: ABLeS Participant
---

## Project title

Extracting and Evaluating Discriminative Biological Signal in the Sparse Features of Single-Cell Foundation Models

## Collaborators and funding

- [WEHI](https://www.wehi.edu.au)

## Contact(s)

Givanna Putri, WEHI, <putri.g@wehi.edu.au>

## Project description and aims

This project evaluates whether single-cell foundation models (scFMs) such as Geneformer and scGPT encode biological signals in their internal representations that can be recovered as discriminative features, and whether those features can be faithfully interpreted. The current pipeline design includes training sparse autoencoders (SAEs) on scFM token embeddings, selecting discriminating features using AUROC, assigning candidate gene sets via TF-IDF, and generating annotations using ORA and LLM-based methods.

The pipeline has been run in full on Geneformer, across 3 layers, using the K562 CRISPRi Perturb-seq dataset, including a null-model control to confirm the pipeline does not manufacture signal from structureless input. We are now extending the pipeline to scGPT to test whether the pipeline generalises across model architectures.

The project's impact is methodological: as scFMs become more widely used in single-cell analysis, there is limited understanding of whether their internal representations encode useful biological signals, and whether these signals can differentiate biological outcomes. This project aims to establish a generalisable framework for evaluating the faithfulness of such features.

## How is ABLeS supporting this work?

This work is supported through the production bioinformatics scheme provided by ABLeS. The supports includes storage and compute resources.

## Expected outputs enabled by participation in ABLeS

A manuscript describing the evaluation pipeline and results will be submitted to TMLR (Transactions on Machine Learning Research), and the associated code will be made publicly available on GitHub.

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
