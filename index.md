---
permalink: /
title: "Computational Biology & Machine Learning"
layout: home
eyebrow: "Ph.D. Candidate · Computer Science · UMass Amherst"
kicker: "Computational biology · ML for genomics"
headline: "Machine learning for the biology of *antibiotic resistance*"
role: "Ph.D. candidate studying drug resistance in *Mycobacterium tuberculosis*. Advised by [Prof. Anna Green](https://people.cs.umass.edu/~annagreen/), SAGE Lab."
status_badge: "Open to postdoctoral & research scientist roles · flexible start, 2027"
band_left: "Protein language models · TB drug-resistance genomics · Structural ML"
band_right: "Research ↘"
description: "Computational Biologist | ML for Genomics — building generalizable, interpretable models with biological signal. Protein language models, TB drug-resistance genomics, structural ML."
redirect_from:
  - /about/
  - /about.html
---

<section class="home-stats home-wrap" aria-label="Work at a glance">
<div><span class="home-stat__num">17,942</span><span class="home-stat__label"><em>M. tuberculosis</em> isolates in BIG-TB</span></div>
<div><span class="home-stat__num">11</span><span class="home-stat__label">WHO-priority antibiotics</span></div>
<div><span class="home-stat__num">4,525</span><span class="home-stat__label">Uncertain variants scored by FARM</span></div>
<div><span class="home-stat__num">{{ site.publications | size }}</span><span class="home-stat__label">Papers, preprints &amp; abstracts</span></div>
</section>

<section class="home-quote">
<div class="home-wrap">
<p class="home-why"><span class="home-label">Why it matters</span>In 2023, an estimated 410,000 people developed drug-resistant tuberculosis, and only 43% were diagnosed and started on appropriate treatment. <cite>WHO, 2024</cite></p>
<blockquote class="pull-quote">Sequence-only ML models in genomics look impressive on benchmarks and then fail on new lineages, new genes, new populations. I build models that stay accurate and explainable by injecting the biology we already know — protein structure, evolutionary constraint, multi-omic context — into the model itself.</blockquote>
</div>
</section>

<section class="home-section home-wrap" id="research">
<div class="home-section__head">
<div><p class="home-label">Research highlights</p><h2>What I'm working on</h2></div>
<a class="home-link" href="/research/">All research &#8599;</a>
</div>
<div class="home-proj-list">
<div class="home-proj">
<div><p class="home-proj__kind">Benchmark</p><h3>BIG-TB</h3></div>
<div><p>A unified dataset and evaluation framework spanning 17,942 isolates and 11 drugs. I led the protein-side benchmark, built to compare resistance-prediction models on equal footing, including on lineages they never saw in training.</p><ul class="tags"><li class="tag">PyTorch</li><li class="tag">ESM-2</li><li class="tag">SHAP</li><li class="tag">SLURM</li></ul><a href="/research/"><img class="home-proj__fig" src="/images/home_bigtb_thumb.jpg" alt="BIG-TB phenotype dataset pipeline: extracting VCFs, reconstructing DNA, and translating to protein sequence" loading="lazy"></a></div>
</div>
<div class="home-proj">
<div><p class="home-proj__kind">Forecasting</p><h3>FARM</h3></div>
<div><p>Forecasting which uncertain variants will later be reclassified as resistance-causing, by combining 3D structure, Rosetta energetics, and protein-language-model features, then scoring 4,525 variants for follow-up.</p><ul class="tags"><li class="tag">Rosetta</li><li class="tag">Random forest</li><li class="tag">Protein LMs</li></ul><a href="/research/"><img class="home-proj__fig" src="/images/home_farm_thumb.jpg" alt="FARM framework: multimodal feature integration, TB mutation resistance forecasting, and performance evaluation" loading="lazy"></a></div>
</div>
<div class="home-proj">
<div><p class="home-proj__kind">Data augmentation</p><h3>Evolutionary augmentation</h3></div>
<div><p>Leveraging multi-species protein homologs to enhance sparse training data for structure-aware, protein-level models.</p><ul class="tags"><li class="tag">UniProt</li><li class="tag">ESM-2</li><li class="tag">Leakage-aware evaluation</li></ul></div>
</div>
</div>
</section>

<section class="home-section home-wrap" id="publications">
<div class="home-section__head">
<div><p class="home-label">Selected publications</p><h2>Recent papers</h2></div>
<a class="home-link" href="/publications/">All publications &#8599;</a>
</div>
<ol class="home-pubs">
<li class="home-pub">
<div class="home-pub__year">2026</div>
<div><p class="home-pub__venue">bioRxiv <span class="home-pub__kind">Preprint · under review at PNAS</span></p><h3><a href="https://www.biorxiv.org/content/10.64898/2026.07.23.740359v1" target="_blank" rel="noopener">FARM: Forecasting Antibiotic Resistance in <em>Mycobacterium tuberculosis</em> Using Biophysics and Machine Learning</a></h3><p class="home-pub__authors"><strong>Tasmin, M.</strong>, Barethiya, S., Wang, Y., Kang, L., Chen, J., &amp; Green, A. G.</p></div>
</li>
<li class="home-pub">
<div class="home-pub__year">2026</div>
<div><p class="home-pub__venue">bioRxiv <span class="home-pub__kind">Preprint · under revision</span></p><h3><a href="https://www.biorxiv.org/content/10.64898/2026.01.30.702134v1.abstract" target="_blank" rel="noopener">BIG-TB: A Benchmark for Prediction and Interpretability of Sequence-Based Machine Learning Using <em>Mycobacterium tuberculosis</em> Genomes</a></h3><p class="home-pub__authors"><strong>Tasmin, M.</strong>, Mohanty, S., Kulkarni, S., Farhat, M. R., &amp; Green, A. G.</p></div>
</li>
<li class="home-pub">
<div class="home-pub__year">2025</div>
<div><p class="home-pub__venue">eLife <span class="home-pub__kind">Journal article</span></p><h3><a href="https://doi.org/10.7554/eLife.109450.1" target="_blank" rel="noopener">The Structural Context of Mutations in Proteins Predicts Their Effect on Antibiotic Resistance</a></h3><p class="home-pub__authors">Green, A. G., <strong>Tasmin, M.</strong>, Vargas Jr., R., &amp; Farhat, M. R. &middot; <em>eLife</em> 14:RP109450</p></div>
</li>
<li class="home-pub">
<div class="home-pub__year">2025</div>
<div><p class="home-pub__venue">ICLR 2025 MLGenX Workshop <span class="home-pub__kind">Workshop paper</span></p><h3><a href="https://openreview.net/pdf?id=cwi0o5rrVG" target="_blank" rel="noopener">Beyond Sequence-Only Models: Leveraging Structural Constraints for Antibiotic Resistance Prediction in Sparse Genomic Datasets</a></h3><p class="home-pub__authors"><strong>Tasmin, M.</strong> &amp; Green, A. G.</p></div>
</li>
</ol>
</section>

<section class="home-section home-wrap" id="media">
<div class="home-section__head">
<div><p class="home-label">Talks &amp; media</p><h2>Watch</h2></div>
<a class="home-link" href="/talks/">All talks &#8599;</a>
</div>
<div class="home-media">
<a class="home-video" href="https://www.youtube.com/watch?v=O0k0XMh18G8" target="_blank" rel="noopener">
<span class="home-video__frame"><img src="/images/ai_at_umass_still.jpg" alt="Mahbuba Tasmin speaking in the AI at UMass feature video" loading="lazy"><span class="home-video__play" aria-hidden="true">&#9654;</span></span>
<span class="home-video__title">Featured in UMass Amherst's AI at UMass campaign</span>
<span class="home-video__meta">UMass Amherst &middot; 2026 &middot; Video</span>
</a>
<a class="home-video" href="https://www.youtube.com/watch?v=oi-ibb6Snrw" target="_blank" rel="noopener">
<span class="home-video__frame"><span class="home-video__play" aria-hidden="true">&#9654;</span></span>
<span class="home-video__title">BIG-TB spotlight talk at MLCB 2025</span>
<span class="home-video__meta">Machine Learning for Computational Biology &middot; Talk</span>
</a>
</div>
</section>

<section class="home-section home-wrap" id="milestones">
<div class="home-section__head">
<div><p class="home-label">Since 2025</p><h2>Recent milestones</h2></div>
</div>
<ul class="home-tl">
<li><span class="home-tl__when">Next</span><span>Preparing to propose my dissertation, <em>"Integrating Biological Signal to Improve Generalizability and Interpretability of Machine Learning in Genomics,"</em> in early Fall 2026.</span></li>
<li><span class="home-tl__when">2026</span><span>Submitted the <strong>FARM</strong> manuscript (biophysics-aware resistance forecasting) — under review at PNAS.</span></li>
<li><span class="home-tl__when">2026</span><span>Selected as a fully funded graduate participant for the Tapia Conference.</span></li>
<li><span class="home-tl__when">2026</span><span>Featured as a graduate researcher in UMass's <a href="https://www.youtube.com/watch?v=O0k0XMh18G8">AI at UMass</a> public-engagement campaign.</span></li>
<li><span class="home-tl__when">2025–26</span><span>Serving as elected Ph.D. Graduate Representative, Faculty Senate / CICS, UMass Amherst.</span></li>
<li><span class="home-tl__when">2026</span><span>Reviewing for <em>Bioinformatics Advances</em> and MLCSB (ISMB).</span></li>
<li><span class="home-tl__when">2025</span><span>Published a <a href="https://doi.org/10.7554/eLife.109450.1">research article</a> in eLife on predicting antibiotic resistance using protein structural context.</span></li>
<li><span class="home-tl__when">2025</span><span>Presented work at the ICLR MLGenX workshop and delivered a spotlight talk at MLCB.</span></li>
<li><span class="home-tl__when">2025</span><span>Completed my Master's in Computer Science and advanced to Ph.D. candidacy.</span></li>
</ul>
</section>

<section class="home-contact" id="contact">
<div class="home-wrap">
<p class="home-label">Contact</p>
<div class="home-contact__grid">
<div>
<h2>Research &amp; collaboration</h2>
<p>Want to talk research, collaboration, or TB genomics? Book 30 minutes, no agenda required.</p>
<div class="home-plinks">
{% include home-links.html %}
</div>
</div>
<div class="home-scheduler">
<iframe src="https://scheduler.zoom.us/mahbuba-tasmin/30-mins-with-mahbuba?embed=true" title="Book 30 minutes with Mahbuba Tasmin" frameborder="0"></iframe>
</div>
</div>
</div>
</section>
