---
layout: archive
title: "Software"
permalink: /software/
author_profile: true
redirect_from:
  - /software.html
---

{% include base_path %}

I write open-source scientific software, mostly in Python, C++ and R: packages, pipelines and the small apps that make them usable in the lab. Most of my current work lives in the [Zimmermann-Kogadeeva group](https://github.com/zimmermann-kogadeeva-group) organisation at EMBL, where I build and maintain the group's software. Earlier projects are on my [personal GitHub](https://github.com/BartoszBartmanski).

## Featured

### [GEMsembler](https://github.com/zimmermann-kogadeeva-group/GEMsembler)
*Python · co-developed with Elena Matveishina*

[![PyPI](https://img.shields.io/pypi/v/gemsembler)](https://pypi.org/project/gemsembler/)

Assembles and compares genome-scale metabolic models (GEMs) built by different tools, including CarveMe, ModelSEED, gapseq and AGORA. It converts their metabolites, reactions and genes to a common namespace, then builds consensus models and structural comparisons across tools. Includes a test suite and is described in Matveishina et al., *mSystems* (2025).

`pip install gemsembler`

### [Maphelios](https://github.com/zimmermann-kogadeeva-group/Maphelios)
*Python · Streamlit*

[![PyPI](https://img.shields.io/pypi/v/maphelios)](https://pypi.org/project/maphelios/)
[![Downloads](https://img.shields.io/pypi/dm/maphelios)](https://pypistats.org/packages/maphelios)

Finds inserts (for example from gain-of-function screens) and plots them alongside the genome or contigs, using BLAST, pysam and pyCirclize. It comes with a Streamlit app for interactive use. A GitLab CI/CD pipeline publishes each tagged release to PyPI, builds a container image and redeploys the app. The image also runs with Docker or Apptainer.

`pip install maphelios`

### [FRAPPPE](https://github.com/zimmermann-kogadeeva-group/FRAPPPE)
*Python*

[![PyPI](https://img.shields.io/pypi/v/frapppe)](https://pypi.org/project/frapppe/)

¹³C metabolic flux analysis via flux sampling and random-forest prediction. It samples the feasible flux space of a metabolic network and simulates the resulting mass distribution vectors (MDVs). A random-forest model trained on those simulations then predicts intracellular flux ratios from measured labelling data.

[Documentation](https://grp-zimmermann-kogadeeva.pages.embl.de/frapppe/) · `pip install frapppe`

### [StoSpa2](https://github.com/BartoszBartmanski/StoSpa2)
*C++ · Python bindings*

[![JOSS](https://joss.theoj.org/papers/10.21105/joss.02293/status.svg)](https://doi.org/10.21105/joss.02293)
[![PyPI](https://img.shields.io/pypi/v/pystospa)](https://pypi.org/project/pystospa/)

A C++ package for stochastic simulation of models built in the chemical master equation (CME) and reaction–diffusion master equation (RDME) frameworks. It runs on structured and unstructured meshes, and supports uniformly growing domains and time-varying reaction rates through the Extrande method. Python bindings (`pystospa`, built with pybind11) let users run simulations without recompiling. A rewrite of the original [StoSpa](https://github.com/BartoszBartmanski/StoSpa), with unit tests for both the C++ and Python layers.

[Documentation](https://stospa2.readthedocs.io/en/latest/) · [Paper (JOSS, 2020)](https://doi.org/10.21105/joss.02293) · `pip install pystospa`

## Pipelines

* [GEMsPipeline](https://github.com/zimmermann-kogadeeva-group/GEMsPipeline) · *Snakemake*
    - Builds genome-scale metabolic models from genomes with CarveMe and gapseq, then combines them with GEMsembler.

* [MetagenomicsPipeline](https://github.com/zimmermann-kogadeeva-group/MetagenomicsPipeline) · *Snakemake*
    - Runs KneadData and HUMAnN from bioBakery to process metagenomics data. Designed to be imported as a Snakemake module into other projects.

* [ContainerProteoWizard](https://github.com/zimmermann-kogadeeva-group/ContainerProteoWizard) · *Apptainer, Snakemake*
    - Containerised ProteoWizard with a Snakemake workflow for converting proprietary Agilent mass-spectrometry files to open formats on a SLURM cluster.

## Tools and apps

* [PoolingScheme](https://github.com/zimmermann-kogadeeva-group/PoolingScheme) · *Python, Streamlit*
    - Generates combinatorial pooling schemes that assign each sample to a unique set of pools for pooled experiments. Available as a CLI and as a containerised Streamlit app.

* [GrowthCurves](https://github.com/zimmermann-kogadeeva-group/GrowthCurves) · *R, Shiny*
    - R functions for reading and processing plate-reader growth-curve data, plus a Shiny app for uploading data and metadata and exploring the curves interactively.

* [BiGGdb](https://github.com/zimmermann-kogadeeva-group/BiGGdb) · *Python*
    - Builds a JSON lookup of all BiGG database metabolites with their chemical formulas and masses, for annotating metabolomics data.

* [DualMesh](https://github.com/BartoszBartmanski/DualMesh) · *Python*
    - Generates the dual mesh of a triangular mesh read with [meshio](https://github.com/nschloe/meshio). Useful for compartment-based simulations on unstructured meshes. `pip install dualmesh`

* [StoSpa](https://github.com/BartoszBartmanski/StoSpa) · *C++*
    - The original package for stochastic simulation of spatially extended systems using the next subvolume method, including time-dependent propensities via the Extrande algorithm. Superseded by StoSpa2.

## Reproducible analyses

* [PseudomonasAntibioticsResistance](https://github.com/zimmermann-kogadeeva-group/PseudomonasAntibioticsResistance) · *Snakemake, Python*
    - The full pipeline (WGS, RNA-seq, proteomics) and notebooks that reproduce every figure in [Bartmanski et al. (2025)](https://www.biorxiv.org/content/10.1101/2025.01.14.632673) on cross-resistance in *Pseudomonas aeruginosa* clinical isolates. Archived on [Zenodo](https://doi.org/10.5281/zenodo.14648253).

* [13CFluxRatioAnalyisWithFRAPPPE](https://github.com/zimmermann-kogadeeva-group/13CFluxRatioAnalyisWithFRAPPPE) · *Snakemake, pixi*
    - The analysis and figures for the FRAPPPE paper, run as a Snakemake pipeline on SLURM with pixi- and renv-pinned environments.

## Teaching

* [OmicsPredocCourse](https://github.com/zimmermann-kogadeeva-group/OmicsPredocCourse) · *R, Python, Snakemake*
    - A multi-omics practical for the 2025 EMBL predoc course, built on real data on antibiotic resistance in *P. aeruginosa*. Students run bulk RNA-seq on the cluster with Snakemake, do differential expression and PCA, and build simple ML models that predict resistance from expression.

* [KefirCourse](https://github.com/zimmermann-kogadeeva-group/KefirCourse) · *Python, R*
    - Practical sessions and environments for a course on microbial communities: nanopore 16S rRNA analysis with NanoCLUST, metabolomics, flux balance analysis and community modelling.

* [IntroToHDF5](https://github.com/BartoszBartmanski/IntroToHDF5) · *Python, R, C++*
    - A short introduction to reading and writing HDF5 files with h5py (Python), rhdf5 (R) and HighFive (C++).

## Containers

* [DockerCARNIVAL](https://github.com/BartoszBartmanski/DockerCARNIVAL) and [SingularityCARNIVAL](https://github.com/BartoszBartmanski/SingularityCARNIVAL) · *Docker, Singularity*
    - Ready-to-run images of [CARNIVAL](https://github.com/saezlab/CARNIVAL) with example scripts for the lpSolve, CPLEX and Gurobi solvers, published on [Docker Hub](https://hub.docker.com/r/bartoszbartmanski/carnival) and the Sylabs library.

* [SingularityRbase](https://github.com/BartoszBartmanski/SingularityRbase) · *Singularity*
    - Base R images on Ubuntu 20.04 for running R workflows on HPC clusters.

* [WebPlotDigitizer](https://github.com/BartoszBartmanski/WebPlotDigitizer) · *Docker*
    - A container for running [WebPlotDigitizer](https://github.com/ankitrohatgi/WebPlotDigitizer) locally, for extracting data from published figures.

## Contributions to other projects

* [CARNIVAL](https://github.com/saezlab/CARNIVAL) · *R*
    - Added Gurobi as a solver for this causal network inference tool, including distributed solving and retrieval of multiple optimal solutions. Also fixed the CPLEX and CBC interfaces and documented Gurobi usage in the vignette.

* [metaGEM](https://github.com/franciscozorrilla/metaGEM) · *Python, Snakemake*
    - Fixed conda and mamba environment setup.
