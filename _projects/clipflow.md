---
title: "clipflow: Automated Batch Processing for CLIP-seq"
date: 2026-08-30
period: "2026 – present"
excerpt: "A pipeline that takes a public accession or raw FASTQ files, works out which CLIP protocol produced them, and returns quality-checked, single-nucleotide crosslink maps in one common format, so many datasets can be processed in one batch and compared side by side."
keywords: [CLIP-seq, RNA–protein interactions, bioinformatics pipeline, reproducibility]
image: projects/clipflow.svg
---

## The problem

CLIP-seq (crosslinking and immunoprecipitation followed by sequencing) maps where
RNA-binding proteins touch RNA. Public repositories now hold a large number of CLIP
datasets, but they were produced with many protocol variants (eCLIP, iCLIP, PAR-CLIP and
others). The variants differ in adapter layout, unique molecular identifiers (UMIs), read
structure, and even in where the crosslink site sits relative to a read. Analyzing them
together usually means configuring every dataset by hand, which is slow, easy to get
wrong, and leaves results that are hard to compare across studies.

## The idea

Give clipflow an accession or a set of FASTQ files. It works out how to process them
without being told which protocol they come from:

1. **Fetch and inspect.** Download the raw reads and their metadata.
2. **Infer the method.** Read the protocol off the data itself (adapters, UMIs, read
   structure) and record the evidence and a confidence level for every decision. When
   confidence is low, clipflow stops and says so instead of guessing, and anything the
   user specifies always takes precedence.
3. **Process.** Trim, align, deduplicate, and extract crosslink events. Protocol
   differences are written as data, one profile per method, instead of as special cases
   in the code, so adding a new method means writing a new profile.
4. **Gate.** Each library passes through a series of quality gates. A library that fails
   is stopped with a stated reason. Nothing falls back to a default without saying so.
5. **Standardize.** Every library, whatever its protocol, ends up in the same
   genome-wide, single-nucleotide crosslink table, so later analyses never need to know
   where the data came from. Peak calling can be added on top of that table.

## Built for batches

A cohort mode tracks every library in a registry. One failed sample doesn't stop the rest.
Failures are sorted into categories, and an interrupted run picks up where it stopped. The
aim is that reprocessing a large collection of public CLIP data is a single command.

## Reproducible

Software versions are pinned and the pipeline ships in containers. A built-in self-test
runs a small dataset from start to finish and checks the output against frozen
expectations. A fingerprint command confirms that two machines are running the same
pipeline.

*The code is not public at this time; this page describes the concept only.*
