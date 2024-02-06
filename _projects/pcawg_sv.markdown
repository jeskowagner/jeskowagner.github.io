---
layout: page
title: Predicting gene deficiencies
description: from structural variants
img: /assets/img/ai_symbol.png
importance: 2
category: research
---

| Institute     | UMC Utrecht                       |
| Supervisor    | Jeroen de Ridder, Marleen Nieboer |
| Language      | Python, R, snakemake              |
| Technologies  | WGS, RNA-seq, ML                  | 
| Further links | Unpublished                       |
|               |                                   |

Large troves of cancer genomes have been released in recent years. By performing whole-genome sequencing on cancers, novel insights can be gained into diagnostics and treatment. 
Two notable releases of many cancer genomes came from [The Cancer Genome Atlas](https://www.cancer.gov/about-nci/organization/ccg/research/structural-genomics/tcga) and the [Hartwig Medical Foundation](https://www.hartwigmedicalfoundation.nl/en/). 
Already, these have led to dozen of publications. One observation we made in these genomes was that losing specific genes leads to particular mutational scars.
This is very much in line with [mutational signatures](https://en.wikipedia.org/wiki/Mutational_signatures), which postulate that specific pathway defects lead to specific mutation types, like C>G conversions.

In this project, we investigated whether one such mutation type can be used to predict which cancers had specific pathway defects.
This followed in the footsteps of [CHORD](https://doi.org/10/ghrqr7), which showed that structural variants are predictive of BRCA1/BRCA2 loss.
Similarly, we were interested in whether [tandem-duplications](https://doi.org/10/gd4gb2) can be used to predict CDK12 deficiency.
CDK12 is thought to stabilise RNA polymeraseII and supports transcription elongation.
After re-training CHORD on this dataset, I showed that a novel machine-learning method may be better suited to capture the high-dimensional classification boundary for CDK12 deficient and proficient cancers.

Consequently, I developed a two-step predictor for CDK12 deficiency and showed that area-under-the-precision-recall-curve is ~0.85 on an external dataset, which represents a significant improvement over existing methods.
Interestingly, in cases where the classifier predicted CDK12 deficiency although no severe mutation was detected from WGS, often the genomes harbored benign mutations in the kinase domain of CDK12.
This means the classifier is likely to highlight CDK12 mutations that might otherwise be missed in clinical screenings.
In all, this project provided novel methods to find CDK12-deficient patients which might enable treatment with experimental [approaches](https://doi.org/10/gdqcdw).

<ins>A note on reproducibility</ins>

I am a firm believer of reproducible science, which ensures trust in Science as a whole. In computational subjects especially, this has been lacking in many projects. In this project, like in many of my other projects, I therefore ensured that all methods are reproducible by integrating all methods in a snakemake workflow which can be run without prior experience. To manage dependencies, the workflow was linked to a conda environment file, so that almost no software dependencies had to be installed manually by users. Unfortunately the project has not reached maturity for public release, but do approach me if you are interested to learn more about it.

