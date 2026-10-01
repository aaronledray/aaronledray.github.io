---
layout: post
title: "One Protein, Two Copper Sites, and a Surprising Role for Tyrosine"
description: >-
  How I used a common protein scaffold to compare CuB and CuSiR sites and examine the role of a nearby tyrosine in oxygen and sulfite reduction.
date: 2026-10-01 09:00:00 -0500
permalink: /posts/cub-vs-cusir-apx/
categories: cofactors enzymes protein-design
published: true
---

In a recently published study, I compared two copper sites that sit beside heme but support different chemistry: the Cu<sub>B</sub> site from heme–copper oxidases and the Cu<sub>SiR</sub> site from sulfite reductase type A. The central challenge was that the native enzymes differ in much more than their copper sites. They have different protein scaffolds, surrounding residues, access channels, and heme environments.

To make the comparison more direct, we built both types of site in the same protein scaffold, soybean ascorbate peroxidase, or APX. This gave us a way to ask which features of the local metal environment influence oxygen reduction and sulfite reduction, and what changes when a nearby tyrosine is added to the design.

## Motivation:

Heme–copper oxidases use a Cu<sub>B</sub> center next to heme to reduce oxygen to water. Sulfite reductase type A uses a related heme–copper arrangement, called Cu<sub>SiR</sub>, to reduce sulfite to sulfide. Both sites place copper near heme, but the reactions involve different substrates and different overall chemistry.

Comparing the two native enzymes directly makes it difficult to identify the source of that difference. Nearly every part of the active site is changing at once. A common scaffold cannot remove every variable, but it can make the comparison more controlled and the design logic more explicit.

## Building both sites in APX

We chose APX because its distal heme pocket provided a useful scaffold for introducing either a Cu<sub>B</sub>-like or Cu<sub>SiR</sub>-like site. The designs were guided by structural comparisons rather than by residue numbering alone. The relevant question was whether residues occupied comparable positions relative to the heme, copper, and neighboring groups.

<figure class="art-figure art-center">
  <picture>
    <source srcset="{{ '/assets/images/APX_Mutation_Sites.webp' | relative_url }}" type="image/webp">
    <img class="art-img art-shadow" src="{{ '/assets/images/APX_Mutation_Sites.png' | relative_url }}" alt="Native APX heme pocket showing His42 and Leu131, the positions used in the engineered designs" width="534" height="544" loading="lazy" decoding="async">
  </picture>
  <figcaption class="art-caption">Native APX heme pocket showing His42 and Leu131, the positions later altered or tested in the engineered designs.</figcaption>
</figure>

<figure class="art-figure art-center">
  <picture>
    <source srcset="{{ '/assets/images/HCO_CuB_ActiveSite.webp' | relative_url }}" type="image/webp">
    <img class="art-img art-shadow" src="{{ '/assets/images/HCO_CuB_ActiveSite.png' | relative_url }}" alt="Heme-CuB active site in bovine cytochrome c oxidase structure 1V54, showing the copper center, histidine ligands, and nearby tyrosine" width="510" height="660" loading="lazy" decoding="async">
  </picture>
  <figcaption class="art-caption">Reference heme–Cu<sub>B</sub> active site from bovine cytochrome c oxidase structure 1V54, highlighting the copper center, three histidine ligands, and nearby Tyr244.</figcaption>
</figure>

For the Cu<sub>B</sub>-like design, we introduced three histidines to create a copper-binding environment modeled on the three histidine ligands in heme–copper oxidases. We also changed APX His42 to alanine so that it would not dominate the engineered site. This construct is called Cu<sub>B</sub>APX.

For the Cu<sub>SiR</sub>-like design, we replaced two APX residues with cysteines and included the same H42A change. This created a site modeled on the two cysteine ligands of Cu<sub>SiR</sub>. We called this construct Cu<sub>SiR</sub>APX.

<figure class="art-figure art-center">
  <picture>
    <source srcset="{{ '/assets/images/SiR_CuSiR_ActiveSite.webp' | relative_url }}" type="image/webp">
    <img class="art-img art-shadow" src="{{ '/assets/images/SiR_CuSiR_ActiveSite.png' | relative_url }}" alt="Heme-CuSiR active site in sulfite reductase type A structure 4RKN, showing copper, cysteine ligands, and nearby tyrosine residues" width="1078" height="994" loading="lazy" decoding="async">
  </picture>
  <figcaption class="art-caption">Reference heme–Cu<sub>SiR</sub> active site from sulfite reductase type A structure 4RKN, highlighting the copper center, cysteine ligands, and nearby tyrosine residues.</figcaption>
</figure>

Both designs were also used to test the effect of a nearby tyrosine. In the native systems, a conserved tyrosine sits near the heme–copper center. We introduced the corresponding L131Y substitution into the APX designs to ask whether this residue changed activity beyond the primary copper coordination sphere.

## Testing the designs

We measured both oxygen reduction and sulfite reduction. Oxygen reduction was monitored with a Clark-type oxygen electrode. Sulfite reduction was measured with a methyl viologen-based anaerobic assay.

The comparison included native APX, the Cu<sub>B</sub>APX and Cu<sub>SiR</sub>APX designs, and the corresponding L131Y variants, with and without added copper where appropriate. This made it possible to separate several effects that are often mixed together: the protein scaffold, the engineered coordination environment, the presence of copper, and the nearby tyrosine.

## What the comparison showed

The Cu<sub>B</sub>-like site increased oxygen-reduction activity in APX, and adding copper produced a further increase. The Cu<sub>SiR</sub>-like site could also support oxygen reduction, but copper had a smaller effect than it did in the Cu<sub>B</sub>-like design. This shows that Cu<sub>SiR</sub> is not simply inactive toward oxygen, while also showing why a Cu<sub>B</sub>-like environment is better suited to the oxygen-reduction reaction.

The contrast was stronger for sulfite reduction. Cu<sub>B</sub>APX showed little sulfite-reduction activity, whereas Cu<sub>SiR</sub>APX displayed substantially higher activity that increased when copper was added. In this common scaffold, the Cu<sub>SiR</sub>-like coordination environment established a much stronger baseline for sulfite reduction than the Cu<sub>B</sub>-like environment.

The tyrosine results were the most surprising part of the study. Adding L131Y enhanced oxygen reduction when copper was present in both designs. It also strongly increased sulfite reduction. In particular, Cu<sub>B</sub>APX-L131Y displayed unexpectedly high sulfite-reduction activity even though the Cu<sub>B</sub>-like site alone was not effective at that reaction.

This result argues against a simple rule in which copper coordination alone determines reaction identity. The nearby tyrosine can reshape the activity landscape, but its effect depends on the surrounding coordination environment and on the presence of copper.

The high sulfite-reduction activity of Cu<sub>B</sub>APX-L131Y does not mean that native heme–copper oxidases should reduce sulfite in the same way. Under the conditions tested in the study, native heme–copper oxidase did not show sulfite-reduction activity.

One likely explanation is substrate access. Native heme–copper oxidases have deeply buried catalytic centers and channels specialized for oxygen. The APX scaffold has a more solvent-exposed distal heme pocket, which may give sulfite better access to the engineered site. The surrounding protein therefore remains part of the chemistry, even when the metal-binding residues have been redesigned.

The common-scaffold strategy helped separate two ideas that are easy to conflate:

- The primary coordination environment influences which reactions a designed site can support.
- Secondary-sphere residues and scaffold geometry can determine how effectively those reactions proceed.

The work does not establish a universal rule for native Cu<sub>B</sub> or Cu<sub>SiR</sub> enzymes. It demonstrates what can happen when related metal sites are placed in a shared, experimentally accessible scaffold. That distinction matters for both mechanistic interpretation and protein design.

For me, the most useful outcome was a better design principle: a metal site should not be treated as a list of ligands. The nearby hydrogen-bonding network, substrate access, and geometry of the surrounding protein can be just as important as the atoms directly attached to the metal.

## Read the paper!

The full study is available through the [PubMed record](https://pubmed.ncbi.nlm.nih.gov/42619153/) and the [Journal of the American Chemical Society article](https://doi.org/10.1021/jacs.6c00223).
