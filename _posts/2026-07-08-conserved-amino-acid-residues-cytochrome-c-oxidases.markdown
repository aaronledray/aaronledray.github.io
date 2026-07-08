---
layout: post
title: "Conserved Amino Acid Residues Amongst Cytochrome c Oxidases"
date: 2026-07-08 09:00:00 -0500
categories: cofactors enzymes coordination-networks
---

I have been mapping conserved amino acid residues across Cytochrome c Oxidases to see which positions remain most invariant across the family and how those residues distribute around the catalytic core. The motivation here is to identify which residues matter most for de novo design, including whether AlphaFold models built from only the conserved residues can produce structural mimics of Cytochrome c Oxidase (CcO).

<figure class="art-figure art-center">
  <img class="art-img art-shadow" src="/assets/images/20260708_HCO_residues_in_coordination_network.png" alt="Conserved residues overlayed on Cytochrome c Oxidase 1v54 subunit 1" width="900">
  <figcaption class="art-caption">Conserved residues shown from red-orange-yellow, low to high conservation, overlaid on prototypical Cytochrome c Oxidase 1v54 subunit 1.</figcaption>
</figure>

<figure class="art-figure art-center">
  <video class="art-img art-shadow" controls playsinline preload="auto" poster="/assets/images/20260708_heme-copper-oxidase_heatmap_poster.png" style="max-width: 100%; height: auto;" width="900">
    <source src="/assets/videos/20260708_heme-copper-oxidase_heatmap_websafe.mp4" type="video/mp4">
    Your browser does not support embedded video.
  </video>
  <figcaption class="art-caption">Video version of the residue conservation heatmap for the heme-copper oxidase structure.</figcaption>
</figure>

<figure class="art-figure art-center">
  <img class="art-img art-shadow" src="/assets/images/20260708_Frequencies.png" alt="Residue frequency summary for Cytochrome c Oxidases" width="900">
  <figcaption class="art-caption">Residue frequency summary across Cytochrome c Oxidases.</figcaption>
</figure>

I would like to make these scripts public as part of a webapp tool. The current method is to fetch and align all structures in a set, perform residue-interaction analysis on a single template structure, and then query the aligned structures for the amino acid identity at each template residue position. That produces a frequency map and colors the template structure according to residue conservation.
