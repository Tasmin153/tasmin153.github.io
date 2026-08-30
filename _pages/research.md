---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

{% include base_path %}

I am broadly interested in **interpretable machine learning for biological discovery**, with a focus on **genomic resistance prediction** in *Mycobacterium tuberculosis*. My work bridges **protein sequence modeling**, **evolutionary augmentation**, and **causal variant discovery**, aiming to make machine learning models biologically faithful and practically useful for antimicrobial resistance surveillance.

---

##  BIG-TB Benchmark
The **BIG-TB Benchmark** is a large-scale, multimodal dataset of over **17,000 *M. tuberculosis* isolates** spanning **11 WHO-priority antibiotics**.  
It standardizes resistance prediction as a unified ML task and enables fair comparison across DNA-, protein-, and structure-based models.

- Designed a cross-validated benchmark for resistance prediction and interpretability  
- Integrated genomic, proteomic, and evolutionary features across drug pathways  
- Evaluated CNN, Transformer, and foundation model embeddings (ESM2, DNABERT)  

📄 *Manuscript submitted, under revision following peer review:* “**BIG-TB: A Benchmark for Prediction and Interpretability of Sequence-Based Machine Learning Using *M. tuberculosis* Genomes**,” bioRxiv (2026).

---

##  Resistance Forecast Project
The **Resistance Forecast** project combines **structural bioinformatics**, **machine learning**, and **evolutionary constraints** to identify causal variants driving resistance.  

We integrate:
- ΔΔG stability changes from *Rosetta* and *FoldX*  
- 3D-structure-aware proximity metrics and fused-ridge feature models  
- SHAP-based variant attribution for explainability  

 *Goal:* Bridge **mechanistic biology** with **interpretable ML**, yielding causal insights into mutation effects.

📄 *Manuscript under review at PNAS:* “**FARM: Forecasting Antibiotic Resistance in *Mycobacterium tuberculosis* Using Biophysics and Machine Learning**,” bioRxiv (2026).

---

##  Evolutionary Augmentation
I develop **phylogenetic data augmentation** techniques that extend supervised ML datasets using **multi-species homologous sequences** (via UniProt and InterPro).  
This method increases diversity and robustness in low-data antibiotic resistance settings.

- Treats homologs as weakly-labeled susceptible sequences  
- Uses evolutionary embeddings (ESM2, InterProScan) for fine-tuning  
- Improves generalization and variant recovery on rare-mutation datasets  

 *Related work:* “Beyond Sequence-Only Models: Leveraging Structural Constraints for Antibiotic Resistance Prediction” (ICLR MLGenX 2025 Workshop)

---

## Software and Data Resources

<div class="highlight">
<p class="highlight-title">BIG-TB Benchmark</p>
<p>Open-source pipelines for preprocessing, training, cross-validation, robustness analysis, and interpretability evaluation across classical ML, deep neural networks, and biological foundation-model representations.</p>
<img src="/images/big_tb_schematic.PNG" alt="BIG-TB pipeline schematic" style="margin-top:12px; border-radius:6px; border:1px solid var(--global-border-color); max-width:100%;">
</div>

<div class="highlight">
<p class="highlight-title">Structure-Aware Variant Analysis Toolkit</p>
<p>Research code for mapping mutations to protein structures, quantifying spatial clustering, and supporting structure-informed prediction and mechanistic interpretation.</p>
</div>

<div class="highlight">
<p class="highlight-title">Resistance Forecasting in <em>Mycobacterium tuberculosis</em></p>
<p>Reproducible data-preparation, multimodal feature-engineering, model-training, and temporal-evaluation workflows for prioritizing antibiotic-resistance variants of uncertain significance.</p>
</div>

---

##  Other Interests
I’m also exploring:
- Multi-modal integration of protein and genomic embeddings  
- Transfer learning for cross-species resistance prediction  
- Benchmark design and interpretability evaluation pipelines  

For full paper details, see my [Publications](/publications/) page.
