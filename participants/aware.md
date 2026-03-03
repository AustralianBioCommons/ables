---
title: The University of Queensland
description: This project develops GPU-accelerated, uncertainty-aware deep learning models for multimodal medical image segmentation by integrating imaging data with clinical signals and text using large language models (LLMs) and vision–language models (VLMs). The goal is to improve robustness, interpretability, and clinical reliability in computer-assisted diagnosis.
toc: false
type: ABLeS Participant - Completed
page_id: aware
---

## Project title

Uncertainty-aware Medical Data Analysis

## Collaborators and funding

The University of Queensland

## Contact(s)

Dr. Moloud Abdar, <m.abdar@uq.edu.au>

## Project description and aims

This project focuses on advancing medical image segmentation by developing multimodal deep learning frameworks that jointly model medical images (e.g., MRI, CT, ultrasound), auxiliary clinical signals, and textual information such as radiology reports and clinical annotations. The research addresses key challenges in clinical deployment, including limited labeled data, domain variability, and uncertainty in model predictions.

The primary aim is to design GPU-accelerated segmentation models based on CNNs, transformers, and hybrid architectures, enhanced with Bayesian deep learning techniques for uncertainty quantification. Predictive uncertainty will be estimated using methods such as Monte Carlo dropout, Bayesian neural networks, and ensemble strategies to support safer and more interpretable clinical decision-making.

A key innovation of this project is the integration of large language models (LLMs) and vision–language models (VLMs) to incorporate semantic and contextual knowledge from clinical text and multimodal signals. These models will be used for cross-modal alignment, prompt-based conditioning, and weakly supervised learning, enabling improved generalization and robustness in low-data and heterogeneous clinical settings.

Planned analyses include large-scale training and evaluation on clinically relevant datasets, extensive hyperparameter optimization, and repeated stochastic inference to assess segmentation accuracy, calibration, and uncertainty. Performance will be measured using standard metrics such as Dice similarity coefficient and Intersection over Union (IoU), alongside uncertainty-aware evaluation measures.

By leveraging large-scale GPU resources on the Gadi supercomputer, the project aims to deliver a robust, uncertainty-aware, multimodal medical image segmentation framework with significant impact on clinical reliability and real-world deployment.

## How is ABLeS supporting this work?

This work is supported through the Production Bioinformatics scheme provided by ABLeS.

## Expected outputs enabled by participation in ABLeS

Participation in ABLeS will enable the large-scale training and evaluation of GPU-intensive deep learning models for multimodal medical image segmentation and medical data analysis, which would not be feasible without access to national HPC resources. The expected outputs include:

1. Peer-reviewed publications in leading machine learning and medical imaging venues (e.g., ICML, NeurIPS, MICCAI, IEEE TMI), describing novel uncertainty-aware segmentation methods and multimodal LLM/VLM-based frameworks.

2. Open-source code repositories (e.g., GitHub) containing model implementations, training pipelines, and evaluation scripts to support reproducibility and reuse by the research community.

3. Pretrained model checkpoints and configuration files (where permissible) to facilitate downstream research and benchmarking.

4. Curated experimental results and metadata, including uncertainty estimates and evaluation metrics, stored in version-controlled repositories or institutional research data platforms.

5. Technical reports and documentation summarizing experimental findings, best practices for multimodal training on HPC systems, and guidance for uncertainty-aware medical image analysis.

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._
