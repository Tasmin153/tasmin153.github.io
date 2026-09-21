---
layout: archive
title: "Research"
permalink: /research/
---

{% include base_path %}

I am broadly interested in **interpretable machine learning for biological discovery**, with a focus on **genomic resistance prediction** in *Mycobacterium tuberculosis*. My work bridges **protein sequence modeling**, **evolutionary augmentation**, and **causal variant discovery**, aiming to make machine learning models biologically faithful and practically useful for antimicrobial resistance surveillance.

---

##  BIG-TB Benchmark
_Question: can sequence-based models predict drug resistance in *M. tuberculosis* — and do their attributions recover the known causal loci, or just fit the phenotype?_

The **BIG-TB Benchmark** is a large-scale, multimodal dataset of **17,942 *M. tuberculosis* isolates** spanning **11 WHO-priority antibiotics**.  
It standardizes resistance prediction as a unified ML task and enables fair comparison across DNA- and protein-based models.

- Led the protein-side benchmark: custom CNN and Transformer architectures alongside regression baselines and frozen ESM-2 embeddings  
- Leave-one-lineage-out splits test whether performance survives population-structure shift rather than fitting clonal lineage signal  
- SHAP attributions scored against WHO-catalogue resistance loci (precision and recall at the top-*k* residues), with one evaluation harness shared across every model family  

📄 *Manuscript submitted, under revision following peer review:* “**BIG-TB: A Benchmark for Prediction and Interpretability of Sequence-Based Machine Learning Using *M. tuberculosis* Genomes**,” bioRxiv (2026).

---

##  Resistance Forecast Project (FARM)
*Question: trained on one snapshot of the WHO resistance catalogue, can a model forecast which uncertain variants will later be reclassified as resistance-causing?*

**FARM** learns only from variants with known effects in the 2021 WHO catalogue, then is evaluated prospectively on the "uncertain significance" variants that WHO reclassified in 2023. Each variant is described by 25 features from four families:

- 3D structural proximity to known resistance sites  
- *Rosetta* biophysical energetics, including ΔΔG stability changes  
- ESM-2 protein language model features  
- AAIndex physicochemical descriptors  

Random forest and logistic regression classifiers are interpreted with SHAP. The model recovered 80.7% of the retrospectively resolved variants that WHO later reclassified as resistant, and it now scores 4,525 uncertain-significance variants to prioritize candidates for experimental follow-up (Supplementary Data 1).

📄 *Manuscript under review at PNAS:* “**FARM: Forecasting Antibiotic Resistance in *Mycobacterium tuberculosis* Using Biophysics and Machine Learning**,” bioRxiv (2026).

---

##  Structure-Aware Models
*Question: does knowing where a mutation sits in 3D make resistance prediction better, and more interpretable?*

- **Fused Ridge** (ICLR MLGenX 2025, first author): a linear model with a structure-based fusion penalty that pulls the coefficients of spatially adjacent residues toward each other. Across nine resistance genes it reached a mean AUC of 0.766, versus 0.755 for plain ridge regression and 0.603 for zero-shot ESM-2 scoring.  
- **3D mutational clustering** (*eLife* 2025, with Anna Green, Rodrigo Vargas Jr., and Maha Farhat): I built the supervised classifier that compares three resistance predictors: 3D structural proximity, 1D sequence proximity, and the Getis-Ord spatial-clustering score. Across 641 labeled variants, 3D proximity reached F1 = 94.6%, versus 92.8% for sequence distance and 80.8% for the clustering score.  

📄 *Published:* “Beyond Sequence-Only Models: Leveraging Structural Constraints for Antibiotic Resistance Prediction” (ICLR MLGenX 2025 Workshop) and “The Structural Context of Mutations in Proteins Predicts Their Effect on Antibiotic Resistance” (*eLife* 2025). See [Publications](/publications/).

---

##  Evolutionary Augmentation
Ongoing dissertation work on overcoming sparse training data in protein-level resistance models by using evolutionary information: homologous sequences from UniProt, protein language-model scoring, and language-model adaptation.

- Uses multi-species protein homologs and language-model plausibility scores to expand small training sets  
- Evaluated with leakage-aware protocols (homology-filtered test sets and nested cross-validation) so that real gains can be told apart from benchmark artifacts  
- Goal: establish when augmentation genuinely helps, not just whether it can  

---

## Software and Data Resources

<div class="highlight">
<p class="highlight-title">BIG-TB Benchmark</p>
<p>Open-source pipelines for preprocessing, training, cross-validation, robustness analysis, and interpretability evaluation across classical ML, deep neural networks, and biological foundation-model representations. <a href="https://github.com/SAGE-Lab-UMass/Big-TB-benchmark">Code on GitHub</a>.</p>
<img src="/images/bigtb_dataset_pipeline.png" alt="BIG-TB phenotype dataset pipeline: extracting VCFs, reconstructing DNA, and translating to protein sequence" style="margin-top:12px; border-radius:6px; border:1px solid var(--global-border-color); max-width:100%;">
<img src="/images/bigtb_training_pipeline.png" alt="BIG-TB training and evaluation pipeline across data encodings, training data, and ML models" style="margin-top:10px; border-radius:6px; border:1px solid var(--global-border-color); max-width:100%;">
</div>

<div class="highlight">
<p class="highlight-title">Structure-Aware Variant Analysis Toolkit</p>
<p>Research code for mapping mutations to protein structures, quantifying spatial clustering, and supporting structure-informed prediction and mechanistic interpretation. <a href="https://github.com/aggreen/MTB_Mut_Clust">Code on GitHub</a>.</p>
<img src="/images/elife_structural_clustering_fig2.png" alt="Figure from Green, Tasmin et al. eLife 2025 showing the Getis-Ord statistic revealing 3D structural clustering of resistance mutations in KatG, RpoB, PncA, and RsmG" style="margin-top:12px; border-radius:6px; border:1px solid var(--global-border-color); max-width:100%;">
<p style="font-size:13px; color:var(--global-text-color-light); margin-top:8px;">Figure from Green, Tasmin, Vargas Jr., Farhat, <em>eLife</em> 14:RP109450 (2025), CC BY 4.0.</p>
</div>

<div class="highlight">
<p class="highlight-title">Resistance Forecasting in <em>Mycobacterium tuberculosis</em></p>
<p>Reproducible data-preparation, multimodal feature-engineering, model-training, and temporal-evaluation workflows for prioritizing antibiotic-resistance variants of uncertain significance. <a href="https://github.com/SAGE-Lab-UMass/resistance_forecast">Code on GitHub</a>.</p>
<img src="/images/farm_framework_figure.png" alt="FARM framework: multimodal feature integration, TB mutation resistance forecasting, and performance evaluation" style="margin-top:12px; border-radius:6px; border:1px solid var(--global-border-color); max-width:100%;">
</div>

---

##  Other Interests
I’m also exploring:
- Multi-modal integration of protein and genomic embeddings  
- Transfer learning for cross-species resistance prediction  
- Benchmark design and interpretability evaluation pipelines  

For full paper details, see my [Publications](/publications/) page.
