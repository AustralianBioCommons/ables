---
title: School of Agriculture, Food and Wine, The University of Adelaide
description: Quantify how drought (rainfed) vs irrigation shapes the functional capacity of wheat-field soil microbiomes at global scale, and then “zoom in” on a deep-sequenced Australian transect to resolve fine-grained pathways, genomes (MAGs), and ecological indicators.
toc: false
type: ABLeS Participant
---

## Project title

Global Functional Shifts in Wheat-Field Soils Under Drought vs Irrigation

## Collaborators and funding

[School of Agriculture, Food and Wine](https://set.adelaide.edu.au/agriculture-food-wine/), The University of Adelaide, Urrbrae, SA, Australia

## Contact(s)

-   Jiayu Li, School of Agriculture, Food and Wine, The University of Adelaide, <Jiayu.li02@adelaide.edu.au>

## Project description and aims

1) Project summary
Goal. Quantify how drought (rainfed) vs irrigation shapes the functional capacity of wheat-field soil microbiomes at global scale, then zoom in on a deep-sequenced Australian transect to resolve fine-grained pathways, genomes (MAGs), and ecological indicators.
Datasets.
Global set: ~300 bulk-soil metagenomes (each ~20 Gb) from wheat fields worldwide (rainfed vs irrigated), plus amplicons (16S/ITS) where available.
Australian transect: 68 bulk-soil samples spanning west→east; each ~40 Gb metagenome (+ matched amplicons).
Overall approach. Harmonise metadata and processing; perform function- and genome-resolved metagenomics; build drought/irrigation classifiers and indicator gene panels; validate patterns with the Australian transect; release an open resource (MAGs, gene catalogues, reproducible workflows).
2) Aims & testable hypotheses
**Aim 1** Global functional contrasts.
Quantify differences in metabolic potential between rainfed vs irrigated wheat soils.
H1: Droughted (rainfed) sites show enrichment of osmoprotection (e.g., trehalose/betaine), EPS/aggregate formation, ROS mitigation, and water-use efficiency-linked nitrogen cycling routes; irrigated sites show higher denitrification potential and copiotrophic traits.
**Aim 2** Genome-resolved ecology.
Recover and compare MAGs and strain populations associated with drought vs irrigation.
H2: Distinct DefenceBiome-like consortia (e.g., Actinobacteria, Streptomyces, Microbacteriaceae) increase in drought and encode exudate-responsive transporters and stress regulons.
**Aim 3** Indicator panels & predictive models.
Develop gene/pathway and MAG indicator sets that predict water regime and agronomic context across continents.
H3: A small panel of functions (≤50 KOs/CAZymes) plus a handful of sentinel MAGs will classify water regime with high accuracy (AUC > 0.85) after controlling for soil/climate covariates.
**Aim 4** Australian transect validation & mechanistic resolution.
Use the 68-site transect to (i) validate global signatures; (ii) resolve fine-grained pathway variants, strain microdiversity, and ecological thresholds along rainfall/irrigation gradients.
3) Significance & impact
- Agronomic relevance: actionable microbiome indicators for drought-smart management, informing irrigation scheduling, residue/cover practices, and microbial amendments.
- Scientific advance: links host water regime → exudates → microbial functions/MAGs, uniting community and genome-resolved views at continental scale.
- Community resource: openly released MAG catalogue, non-redundant gene set, and reproducible pipelines, enabling re-use in wheat microbiome, soil health, and climate-adaptation studies.
4) Planned analyses 
- 4.1 Data audit & harmonisation
    - Inventory all cohorts; standardise metadata schema (soil chem/texture, climate, management, cultivar, water regime, geography).
    - Define inclusion criteria; handle licence/consent; map to MIxS-Soil fields.
Deliverable: harmonised metadata table; PRISMA-style flow diagram.
- 4.2 Read processing & profiling
    - QC: FastQC/MultiQC → adapter/quality trimming → host (wheat) removal.
    - Taxon/function profiling (reads): Kraken2/Bracken (or centrifuge) + HUMAnN/eggNOG-mapper for KO/EC pathways
    - ShortBRED for targeted marker sets (e.g., osmolyte genes).
Deliverable: per-sample taxon and functional tables + QC reports.
- 4.3 Assembly & gene catalogues
    - Strategy chosen per cohort (single/co-assembly by eco-region); MEGAHIT/metaSPAdes with k-mer sweeps; protein prediction (Prodigal).
    - Non-redundant gene catalogue via MMseqs2; function annotation (KEGG/KO, EC, COG, CAZy, antiSMASH/BGCs); resistome where relevant.
Deliverable: gene catalogue (FASTA + annotation TSV), abundance matrices.
- 4.4 MAG reconstruction & curation
    - Binning with MetaBAT2, CONCOCT, VAMB; refinement (DASTool); quality via CheckM2; dereplication (dRep); taxonomy (GTDB-Tk).
    - Abundance/coverage via coverM; SNP/strain tracking (inStrain).
Deliverable: dereplicated MAG set (≥50% comp, ≤10% contam; high-quality subset ≥90/≤5), per-MAG metadata.
- 4.5 Pathway & network ecology
    - Targeted pathways: osmolytes (proline/betaine/trehalose), EPS, antioxidant systems, nitrogen (nitrification, denitrification, DNRA), sulfur shunts, phosphorus solubilisation, ACC deaminase, transporters for key exudates.
    - Co-occurrence & guild inference (FastSpar/SpiecEasi) → stability/robustness tests.
Deliverable: pathway differential analyses, guild maps, effect sizes.
- 4.6 Statistics & causal controls
    - Compositional methods (ALDEx2/ANCOM-BC) with covariate control (soil pH, texture, organic C, MAP/MAT, continent, cultivar) via mixed-effects models.
    - Counterfactual checks (matching/propensity) to mitigate irrigation vs region confounding.
Deliverable: adjusted global contrasts with uncertainty quantification.
- 4.7 Predictive modelling & indicators
    - ML (elastic net / random forest / XGBoost) to predict water regime and agronomic outcomes from functions + MAGs; nested CV and external validation (Australian transect).
    - Derive minimal indicator panels for field diagnostics.
Deliverable: classifiers (AUC/PR curves), top features, portable panels.
- 4.8 Australian transect deep-dive
    - High-resolution assembly, strain-level microdiversity, fine-scale pathway variants; change-point analyses along rainfall/irrigation; link to soil properties.
Deliverable: Australia-focused paper validating global signals.


## How is ABLeS supporting this work?



## Expected outputs enabled by participation in ABLeS

- D1. Global non-redundant gene catalogue for wheat-field soils (KO/EC/CAZy/BGC).
- D2. Curated MAG set with habitat preferences and trait annotations.
- D3. Indicator panels (genes/MAGs) and validated predictive models of water regime.
- D4. Reproducible Nextflow workflows and environment recipes (Apptainer).
- D5. High impact papers: (i) global functional contrasts; (ii) genome-resolved validation on the Australian transect; (iii) workflow/methods.
- D6. FAIR-compliant data/metadata releases with DOIs.

<br/>

> _These details have been provided by project members at project initiation. For more information on the project, please consult the contact(s) or project links above._