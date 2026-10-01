---
layout: post
title: "Mapping Protein–Cofactor Coordination Networks"
description: >-
  A working framework for defining, extracting, and comparing the structural networks that shape metallocofactor reactivity.
date: 2025-09-12 02:21:37 -0500
permalink: /posts/coordination-networks/
categories: cofactors enzymes coordination-networks
published: false
---

**TL;DR:** I am developing a toolkit for extracting and comparing the structural environments around protein cofactors. The goal is to move beyond the directly bound ligands and describe the larger coordination networks that influence cofactor geometry, electronics, and reactivity.

## Why map a coordination network?

The behavior of a metal or metallocofactor is shaped by more than the residues directly attached to it. Nearby side chains, backbone atoms, solvent molecules, and hydrogen-bonding interactions can tune the local environment and alter how a cofactor behaves.

That broader environment is often discussed qualitatively, but it is difficult to compare across structures without a consistent definition and a reproducible analysis workflow. I started building this toolkit because I wanted a way to inspect those relationships systematically rather than trace them manually structure by structure.

## A working definition

For this project, I use **coordination network** to describe the connected structural environment that helps define a cofactor site:

1. **Primary coordination sphere:** the atoms or residues directly coordinated to the metal or cofactor.
2. **Secondary coordination sphere:** residues and motifs that interact with the primary ligands or their immediate environment.
3. **Extended network:** additional structural features, including solvent and surrounding secondary-structure elements, that can influence geometry, proton transfer, electrostatics, or access to the site.

The boundary of the network depends on the question being asked. The useful part is making the criteria explicit so that two structures can be analyzed and compared in the same way.

## What the toolkit does

The current workflow can:

- Parse PDB and mmCIF structures.
- Identify primary and secondary coordination environments around a selected cofactor.
- Export structural relationships as CSV data and interactive HTML visualizations.
- Compare a template structure with aligned query structures.
- Calculate RMSD values for atoms shared between comparable networks.
- Deduplicate chains when multi-chain structures contain repeated copies of the same site.

These outputs are intended to support both quick structural inspection and larger comparative analyses.

## From structure to comparison

The analysis currently follows four broad steps:

1. Select a cofactor and a reference structure.
2. Identify the contacts and residues that define the reference coordination network.
3. Align related structures to the reference and map equivalent positions.
4. Compare the resulting networks using structural measurements and visual summaries.

This separates the definition of a network from the comparison step. That distinction matters because a network can be chemically meaningful in one structure while still requiring careful alignment and correspondence rules before it can be compared with another.

## Why this could be useful

A consistent representation of coordination networks could help organize questions about conserved ligands, variable secondary-sphere interactions, and the relationship between local structure and reactivity. It may also provide a useful language for protein design, where changing a residue outside the primary coordination sphere can still have a substantial effect on a metal site.

## Current status and next steps

The project is still under development. The current implementation focuses on single-structure analysis and template-to-query comparison, with examples centered on metallocofactor sites such as heme and iron–sulfur clusters.

The next steps are to make the analysis criteria more configurable, document the input and output formats, add more test structures, and organize the code for a public release. I also want to expand the framework so that coordination networks can be compared across broader enzyme families rather than only within a small set of example structures.
