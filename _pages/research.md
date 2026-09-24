---
layout: wide
title: "Research"
permalink: /research/
---

<p class="rs-intro">I work on <strong>interpretable machine learning for biological discovery</strong>, with a focus on <strong>drug-resistance prediction</strong> in <em>Mycobacterium tuberculosis</em>. My models put known biology, such as protein structure and evolutionary constraint, into the model itself, so that they stay accurate and explainable on new lineages, genes and populations.</p>

<div class="rs-grid">
<nav class="rs-toc" aria-label="Projects">
<a href="#bigtb">BIG-TB benchmark</a>
<a href="#farm">FARM forecasting</a>
<a href="#structure">Structure-aware models</a>
<a href="#augmentation">Evolutionary augmentation</a>
<a href="#interests">Other interests</a>
</nav>
<div class="rs-body">
<section class="rs-sec" id="bigtb">
<h2 class="rs-label">BIG-TB benchmark &middot; Under revision</h2>
<p class="rs-q">Can sequence-based models predict resistance, and do their attributions recover the known causal loci, or just fit the phenotype?</p>
<p>A large, multimodal benchmark of 17,942 <em>M. tuberculosis</em> isolates across 11 WHO-priority antibiotics that puts DNA- and protein-based models on equal footing.</p>
<div class="rs-result"><span class="rs-result__n">17,942</span><span class="rs-result__t">isolates scored on 11 antibiotics, including lineages the models never saw in training</span></div>
<p class="rs-did-label">What I did</p>
<ul class="rs-did">
<li>Led the protein-side benchmark: CNN and Transformer models, regression baselines and frozen ESM-2 embeddings</li>
<li>Leave-one-lineage-out splits test whether performance survives a shift in population structure instead of fitting clonal lineage signal</li>
<li>SHAP attributions scored against WHO-catalogue resistance loci (precision and recall at the top-<em>k</em> residues), with one evaluation harness shared across every model family</li>
</ul>
<img class="research-figure" src="/images/bigtb_dataset_pipeline.png" alt="BIG-TB phenotype dataset pipeline: extracting VCFs, reconstructing DNA, and translating to protein sequence">
<img class="research-figure" src="/images/bigtb_training_pipeline.png" alt="BIG-TB training and evaluation pipeline across data encodings, training data, and ML models">
<p class="research-links"><a class="btn" href="https://www.biorxiv.org/content/10.64898/2026.01.30.702134v1.abstract" target="_blank" rel="noopener">Paper</a><a class="btn" href="https://github.com/SAGE-Lab-UMass/Big-TB-benchmark" target="_blank" rel="noopener">Code on GitHub</a></p>
</section>
<section class="rs-sec" id="farm">
<h2 class="rs-label">FARM forecasting &middot; Under review at PNAS</h2>
<p class="rs-q">Trained on one snapshot of the WHO resistance catalogue, can a model forecast which uncertain variants will later be called resistance-causing?</p>
<p>FARM learns only from variants with known effects in the 2021 WHO catalogue, then is tested prospectively on the &ldquo;uncertain significance&rdquo; variants that WHO reclassified in 2023.</p>
<div class="rs-result"><span class="rs-result__n">80.7%</span><span class="rs-result__t">of the variants later reclassified as resistant were recovered in that prospective test</span></div>
<p class="rs-did-label">What I did</p>
<ul class="rs-did">
<li>Built 25 features per variant: 3D structural proximity, <em>Rosetta</em> energetics including &Delta;&Delta;G, ESM-2 protein language model features and AAIndex physicochemical descriptors</li>
<li>Random forest and logistic regression classifiers, interpreted with SHAP</li>
<li>The model now scores 4,525 uncertain-significance variants to prioritize candidates for experimental follow-up (Supplementary Data 1)</li>
</ul>
<img class="research-figure" src="/images/farm_framework_figure.png" alt="FARM framework: multimodal feature integration, TB mutation resistance forecasting, and performance evaluation">
<p class="research-links"><a class="btn" href="https://www.biorxiv.org/content/10.64898/2026.07.23.740359v1" target="_blank" rel="noopener">Paper</a><a class="btn" href="https://github.com/SAGE-Lab-UMass/resistance_forecast" target="_blank" rel="noopener">Code on GitHub</a></p>
</section>
<section class="rs-sec" id="structure">
<h2 class="rs-label">Structure-aware models &middot; Published</h2>
<p class="rs-q">Does knowing where a mutation sits in 3D make resistance prediction better, and more interpretable?</p>
<p>Two published papers on putting protein structure into the model: Fused Ridge (ICLR MLGenX 2025) and 3D mutational clustering (<em>eLife</em> 2025).</p>
<div class="rs-result"><span class="rs-result__n">94.6%</span><span class="rs-result__t">F1 for 3D proximity, against 92.8% for sequence distance and 80.8% for the clustering score (<em>eLife</em> 2025)</span></div>
<p class="rs-did-label">What I did</p>
<ul class="rs-did">
<li><strong>Fused Ridge</strong> (first author): a linear model whose structure-based penalty pulls the coefficients of neighbouring residues together. Across nine resistance genes it reached a mean AUC of 0.766, against 0.755 for plain ridge and 0.603 for zero-shot ESM-2 scoring</li>
<li><strong>3D mutational clustering</strong> (with Anna Green, Rodrigo Vargas Jr. and Maha Farhat): I built the classifier comparing 3D proximity, 1D sequence proximity and the Getis-Ord clustering score across 641 labeled variants</li>
</ul>
<img class="research-figure" src="/images/home_elife_thumb.jpg" alt="Figure from Green, Tasmin et al., eLife 2025: the Getis-Ord workflow and the clustering of resistance mutations on the KatG structure">
<p class="research-caption">Cropped from Figure 2 of Green, Tasmin, Vargas Jr., Farhat, <em>eLife</em> 14:RP109450 (2025), CC BY 4.0. The full figure is in the paper.</p>
<p class="research-links"><a class="btn" href="https://openreview.net/pdf?id=cwi0o5rrVG" target="_blank" rel="noopener">Fused Ridge paper</a><a class="btn" href="https://doi.org/10.7554/eLife.109450.1" target="_blank" rel="noopener">eLife paper</a><a class="btn" href="https://github.com/aggreen/MTB_Mut_Clust" target="_blank" rel="noopener">Clustering code on GitHub</a></p>
</section>
<section class="rs-sec" id="augmentation">
<h2 class="rs-label">Evolutionary augmentation &middot; Ongoing dissertation work</h2>
<p class="rs-q">When does evolutionary information genuinely help protein-level models trained on sparse data?</p>
<p>Multi-species protein homologs and language-model scoring, used to enrich the small training sets that resistance prediction usually has to work with.</p>
<p class="rs-did-label">What I do</p>
<ul class="rs-did">
<li>Use homologs from UniProt and language-model plausibility scores to expand small training sets</li>
<li>Evaluate with leakage-aware protocols (homology-filtered test sets and nested cross-validation), so that real gains can be told apart from benchmark artifacts</li>
<li>Goal: establish when augmentation helps, not just whether it can</li>
</ul>
</section>
<section class="rs-sec" id="interests">
<h2 class="rs-label">Other interests</h2>
<ul class="rs-did">
<li>Multi-modal integration of protein and genomic embeddings</li>
<li>Transfer learning for cross-species resistance prediction</li>
<li>Benchmark design and interpretability evaluation pipelines</li>
</ul>
<p>For full paper details, see my <a href="/publications/">publications</a>.</p>
</section>
</div>
</div>

<script>
(function () {
  var links = document.querySelectorAll('.rs-toc a');
  if (!links.length || !('IntersectionObserver' in window)) return;
  function mark(id) {
    for (var i = 0; i < links.length; i++) {
      links[i].setAttribute('aria-current', links[i].getAttribute('href') === '#' + id ? 'true' : 'false');
    }
  }
  var io = new IntersectionObserver(function (entries) {
    entries.forEach(function (e) { if (e.isIntersecting) mark(e.target.id); });
  }, { rootMargin: '-20% 0px -65% 0px' });
  document.querySelectorAll('.rs-sec').forEach(function (s) { io.observe(s); });
  mark('bigtb');
})();
</script>
