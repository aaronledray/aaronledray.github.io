---
layout: post
title:  "Defining Coordination Networks VERY GENERALLY in Metalloenzymes"
date:   2025-09-12 02:21:37 -0500
categories: cofactors enzymes coordination-networks
published: false
---







Title: Mapping Protein–Cofactor Coordination Networks (and Why I Built This)

I’ve been spending a lot of time manually tracing which atoms around a cofactor are actually coordinating it — and I finally got tired of doing that by hand. So I built a small toolkit to extract and compare coordination networks across protein structures.

What it does:

- Parses PDB/mmCIF structures and identifies primary/secondary coordination spheres around a cofactor.
- Outputs CSV + HTML visualizations for quick inspection (I’m using these to sanity‑check OEC and nitrogenase networks).
- Supports template‑to‑query alignment to compare networks and compute RMSD for shared atoms.
- Includes a chain deduplication helper for cleaning multi‑chain structures.

I’m starting with single‑structure analysis and template‑query matching, but I want this to grow into a broader set of tools for cofactor‑focused protein design workflows.

GitHub: <YOUR_REPO_LINK>

If you want to try it, the repo has example commands and sample outputs. The HTML network views are especially handy for quick inspection.






Send me the repo URL and I’ll finalize the post with the live link and adjust tone/length for your audience.







---












### Coordination of metallocofactors




### The extended coordination network




In metalloenzymes, the placement of metal ions within a protein is never arbitrary. Coordinating residues direct directly with the metal or metallocofactor, but the residues which interact with the coordinating residues __themselves__ are part of the larger **coordinaiton network**. The complete coordination network describes the amino acid side chains, solvent molecules, and secondary structural elements that together define how a metallocofacor behaves through influencing its geometry and electronics, and ultimately modulating its reactivity.



















---

### Establishing Definitions

In my framework, a **coordination network** is:

1. **Primary coordination sphere**  
   Direct ligands bound to the metal (e.g., His, Cys, Asp).

2. **Secondary sphere**  
   Residues and motifs which themselves interact with the primary coordination sphere. 

---

### Looking Ahead

The goal is to assemble a **taxonomy of coordination networks** that spans oxidoreductases, hydrolases, and transferases.  
This will
 form the foundation for comparing enzyme families, visualizing conserved motifs, and even guiding computational models of proton-coupled electron transfer.

---





 

---






