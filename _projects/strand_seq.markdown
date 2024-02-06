---
layout: page
title: Modelling cell state changes
description: from single-cell MNase-seq-like data
img: /assets/img/nucleosomes.jpg
importance: 1
category: research
---

| Institute     | EMBL Heidelberg            |
| Supervisor    | Jan Korbel, Hyobin Jeong   |
| Language      | Python, R, snakemake       |
| Technologies  | Strand-seq, WGS, MNase-seq |
| Further links | Unpublished                |
|               |                            |

[Strand-seq](https://doi.org/10/f4c27g) is a single-cell sequencing method enables the detection of large genetic aberrations, termed structural variants (SVs). It works through BrdU-guided degradation of one strand of DNA and a round of mitosis. Through clever computational processing via [scTRIP](https://doi.org/10/ggfwb7) SVs can then be detected bases on integrated phasing of three data tracks. 

In this project, we investigated whether epigenetic differences between cells with and without SVs are also captured with this technique. The motivation for it stems from the experimental protocol. DNA digestion is achieved via MNase digestion, a step that is known to degrade only DNA that is not bound by proteins, most importantly histones. Since histones are associated with inactivate chromatin, we wanted to know whether we can fish out nucleosome positions and detect differences between cells.

To this aim, I developed a novel Python/R/snakemake pipeline that extracted, filtered, analyzed and visualised nucleosome positions and compared groups of cells to find regions of the genome that have differential nucleosome occupancy. Further, I connected this data with knowledge of transcription factor binding sites to link SVs to pathway changes. Since this work is unpublished, please reach out if you are interested about further details.

<ins>A note on reproducibility</ins>

I am a firm believer of reproducible science, which ensures trust in Science as a whole. In computational subjects especially, this has been lacking in many projects. In this project, like in many of my other projects, I therefore ensured that all methods are reproducible by integrating all methods in a snakemake workflow which can be run without prior experience. To manage dependencies, the workflow was linked to a conda environment file, so that almost no software dependencies had to be installed manually by users. Unfortunately the project has not reached maturity for public release, but do approach me if you are interested to learn more about it.

