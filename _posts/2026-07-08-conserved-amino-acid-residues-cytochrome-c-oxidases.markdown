---
layout: post
title: "Conserved Amino Acid Residues Among Cytochrome c Oxidases"
description: >-
  A preliminary analysis of conserved residues across cytochrome c oxidases and their distribution around the catalytic core.
date: 2026-07-08 09:00:00 -0500
categories: cofactors enzymes coordination-networks
---

I am mapping conserved amino acid residues across cytochrome c oxidases to ask two related questions: which positions remain most invariant across the family, and how are those positions distributed around the catalytic core?

### Why this matters

Cytochrome c oxidase is a useful system for thinking about how a protein environment supports metal-centered chemistry. Conserved residues can provide clues about which parts of that environment are shared across the enzyme family. They may also provide useful design constraints, although conservation by itself does not establish that a residue is catalytic or functionally sufficient.

The longer-term goal is to understand whether a model built around conserved residues can reproduce important structural features of cytochrome c oxidase, and which parts of the surrounding environment are needed to preserve function.

The figures below show the current analysis from several complementary views. The first overlays residue conservation on a representative structure. The video shows the same type of map as a rotating heatmap, and the final figure summarizes residue frequencies across the 200-structure dataset.

<figure class="art-figure art-center">
  <picture>
    <source srcset="{{ '/assets/images/20260708_HCO_residues_in_coordination_network.webp' | relative_url }}" type="image/webp">
    <img class="art-img art-shadow" src="{{ '/assets/images/20260708_HCO_residues_in_coordination_network.png' | relative_url }}" alt="Conserved residues overlaid on cytochrome c oxidase structure 1V54, subunit I" width="900" height="618" loading="lazy" decoding="async">
  </picture>
  <figcaption class="art-caption">Conserved residues shown from red–orange–yellow, low to high conservation, overlaid on subunit I of cytochrome c oxidase structure 1V54.</figcaption>
</figure>

<figure class="art-figure art-center">
  <video class="art-img art-shadow" controls playsinline preload="metadata" poster="{{ '/assets/images/20260708_heme-copper-oxidase_heatmap_poster.png' | relative_url }}" style="max-width: 100%; height: auto;" width="900">
    <source src="{{ '/assets/videos/20260708_heme-copper-oxidase_heatmap.web.mp4' | relative_url }}" type="video/mp4">
    Your browser does not support embedded video.
  </video>
  <figcaption class="art-caption">Video version of the residue-conservation heatmap for the heme–copper oxidase structure.</figcaption>
</figure>

<figure class="art-figure art-center">
  <picture>
    <source srcset="{{ '/assets/images/20260708_Frequencies.webp' | relative_url }}" type="image/webp">
    <img class="art-img art-shadow" src="{{ '/assets/images/20260708_Frequencies.png' | relative_url }}" alt="Residue frequency summary across cytochrome c oxidases" width="900" height="651" loading="lazy" decoding="async">
  </picture>
  <figcaption class="art-caption">Residue-frequency summary across the cytochrome c oxidase set.</figcaption>
</figure>

## Current workflow

I analyzed 200 structures in total. The dataset includes every structure I could find annotated as cytochrome c oxidase, along with several AlphaFold structures annotated similarly. The color scale reports how conserved each residue was across the full dataset, from lower to higher conservation.

The current method follows four broad steps:

1. Fetch and align the 200 structures in the cytochrome c oxidase dataset.
2. Perform residue-interaction analysis on a single template structure.
3. Query the aligned structures for the amino acid identity at each template-residue position.
4. Generate a frequency map and color the template structure according to residue conservation.

This produces both a structural visualization and a position-by-position view of sequence variation in the aligned set. The template structure provides the coordinate system, while the alignment provides the comparison across the family.

## Interpretations:

The current figures are best treated as an exploratory map. A highly conserved position is a candidate for closer inspection, especially when it lies near a metal center or another feature of interest. It is not, on its own, evidence that the position controls activity, determines selectivity, or can be used in isolation to build a functional enzyme.

The interpretation will also depend on the structural set, the quality of the alignment, the choice of template, and the conservation threshold. These are therefore important parts of the analysis rather than invisible preprocessing steps.

## Toward a design workflow

The code is not published yet because I am still finishing it. The next step is to make the analysis more systematic and eventually make the scripts available as part of a web-based tool. I want that workflow to make it easier to inspect conserved positions, compare coordination environments, and test which features are preserved when moving from a natural enzyme family toward a designed model.

For now, this is an active analysis rather than a finished design rule. The structural set, conservation criteria, and design tests will need to become more complete before stronger conclusions are warranted.
