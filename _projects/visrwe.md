---
title: "VisRWE: RNA-Modification Enzymes in the 3D DepMap"
date: 2026-10-09
period: "2026"
excerpt: "An interactive resource for looking up how cancer models depend on the enzymes that write, read and erase RNA modifications, comparing the new DepMap organoid screens with the original 2D DepMap gene by gene and partner by partner."
keywords: [epitranscriptomics, DepMap, CRISPR screens, organoids, co-dependency, data resource]
image: projects/visrwe.svg
links:
  - name: Explorer
    url: https://shuyang-zhao.github.io/VisRWE_DepMap/
  - name: Code
    url: https://github.com/shuyang-zhao/VisRWE_DepMap
  - name: Methods
    url: https://github.com/shuyang-zhao/VisRWE_DepMap/blob/main/docs/methods.md
---

## The question

Writers, readers and erasers of RNA modifications (m6A, pseudouridine, m5C, m7G,
2′-O-methylation, the many tRNA modifications and others) are often proposed as cancer
dependencies. The Cancer Dependency Map (DepMap) recently added 147 genome-scale CRISPR
screens in organoids and neurospheres ("NextGen", Neiswender, Maffa, Brenan *et al.*,
*Nature* 2026). Do these enzymes behave the same way in 3D models as in the classic 2D
cell lines, and which genes move together with them?

## What the resource contains

* **217 RNA-modification enzymes and cofactors**, each annotated with the modification it
  installs, removes or reads, its substrates, and known caveats.
* **Single-gene dependencies** in NextGen and in 597 lineage-matched 2D screens: how often
  each gene is essential, organoid versus 2D, and lineage-selective dependencies.
* **A co-dependency map of 5,693 dependency genes**, computed the same way in both datasets
  (16 million gene pairs each), so every pair can be labelled as found in both datasets,
  only in organoids, or only in 2D.
* **Functional modules and known partners**, scored with one rule for every gene and every
  modification family, so the resource does not favour any particular machinery.

## The explorer

The explorer is a single web page that runs entirely in the browser. You can start from any gene,
hover over a node to preview its partners and click to add them, so the network grows one step at a
time. Switching between the organoid data, the 2D data and a side-by-side comparison takes one click.
Opening any pair shows how the correlation splits across tumour lineages, with scatter plots of both
datasets next to each other and a check against 2D lines screened with the same CRISPR library as the
organoids. Module enrichment is shown as a heat map. The interface is in English and Chinese.

## How it is built

The statistics follow the published code of the NextGen paper. I first reproduced two of the
paper's own results from the raw data (a biomarker table and the gene dependency classes) to make
sure the data handling matches, then applied the same conventions to the co-dependency map and to the
2D comparison. The whole analysis reruns with a single command, and every number in the report is
read from the generated tables.

## What it shows so far

Roughly a third of these enzymes are essential in almost every model, in both datasets. Well-known
partners, such as METTL3 and METTL14, are found together far less often in the organoid screens than
in 2D. That difference persists when the 2D data are cut down to the same number of screens, so it
reflects the organoid data rather than the statistics.
