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

📄 *Manuscript in preparation:* “**BIG-TB: A Benchmark Dataset for Genomic Resistance Prediction and Interpretability in *M. tuberculosis***”

---

##  Resistance Forecast Project
The **Resistance Forecast** project combines **structural bioinformatics**, **machine learning**, and **evolutionary constraints** to identify causal variants driving resistance.  

We integrate:
- ΔΔG stability changes from *Rosetta* and *FoldX*  
- 3D-structure-aware proximity metrics and fused-ridge feature models  
- SHAP-based variant attribution for explainability  

 *Goal:* Bridge **mechanistic biology** with **interpretable ML**, yielding causal insights into mutation effects.

---

##  Evolutionary Augmentation
I develop **phylogenetic data augmentation** techniques that extend supervised ML datasets using **multi-species homologous sequences** (via UniProt and InterPro).  
This method increases diversity and robustness in low-data antibiotic resistance settings.

- Treats homologs as weakly-labeled susceptible sequences  
- Uses evolutionary embeddings (ESM2, InterProScan) for fine-tuning  
- Improves generalization and variant recovery on rare-mutation datasets  

 *Related work:* “Beyond Sequence-Only Models: Leveraging Structural Constraints for Antibiotic Resistance Prediction” (ICLR MLGenX 2025 Workshop)

---

##  Other Interests
I’m also exploring:
- Multi-modal integration of protein and genomic embeddings  
- Transfer learning for cross-species resistance prediction  
- Benchmark design and interpretability evaluation pipelines  

For full paper details, see my [Publications](/publications/) page.
