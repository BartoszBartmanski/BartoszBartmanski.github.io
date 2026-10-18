---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

## Work experience

### Senior Staff Scientist
European Molecular Biology Laboratory (EMBL), Heidelberg, Germany - (Nov 2021 to present)

- Released Maphelios, a Python package and Streamlit app for gain-of-function screen analysis, on PyPI with GitLab CI/CD and Kubernetes deployment (27 releases, ~20 users across 5 groups)
- Built and ran 20+ tested Snakemake/Nextflow pipelines on SLURM (Docker, Apptainer) used by 3 teams, processing ~10k samples per month
- Cut processing of 1 TB of microscopy images from 4 days to 10 hours using chunked OME-Zarr and Dask
- Harmonised genomic, transcriptomic and proteomic data into analysis-ready Parquet/HDF5 and deposited 5 datasets in ENA, PRIDE and MetaboLights
- Developed an ML framework that classifies structural and residual misspecification of population PK models from fit output, and a PBPK parent-metabolite model of brivudine fitted to mouse data
- Built an LLM-based agentic system that turned ~2,300 scientific documents into structured records at 97% precision, with human-in-the-loop review
- Trained XGBoost and PLS-DA models with SHAP interpretability to link molecular features to phenotypes

### Research Software Engineer
Institute for Computational Biomedicine, University Hospital, Heidelberg, Germany - (Jan to Nov 2021)

- Halved run time of a mechanistic modelling codebase on HPC by switching the solver from CPLEX to Gurobi, enabling analyses across 100 drug perturbations
- Built reproducible benchmarking pipelines (Snakemake) comparing modelling approaches and solvers on common tasks
- Introduced version control, automated testing, documentation and monthly code reviews

### Assistant Programmer
European Molecular Biology Laboratory (EMBL), Heidelberg, Germany - (Oct 2019 to Dec 2020)

- Integrated ChEMBL, DrugBank and MetaboLights into harmonised ML training datasets, reconciling sources with different identifiers and standards
- Built a Snakemake pipeline for metabolomics data (104 GB, 1,700 samples) that extracts features for ML training
- Analysed drug metabolism and drug-microbiome interactions in close collaboration with experimental scientists

### Teaching Assistant
University of Oxford, Oxford, UK - (Oct 2016 to Oct 2019)

Taught stochastic differential equations, computational biology and high-performance computing

## Education

PhD in Applied Mathematics  
University of Oxford, Oxford, United Kingdom  

Thesis: Efficient methods for simulating stochastic reaction-diffusion models on evolving domains

Master’s Degree in Mathematics  (MMath integrated with Bachelor’s)  
Durham University, Durham, United Kingdom  

Key subjects: PDEs, ODEs, Statistics, Numerical Analysis

## Key skills

**Modelling and statistics:** population PK/PD and PBPK (nlmixr2, rxode2, Monolix), nonlinear mixed-effects models, ODE/PDE and stochastic systems, model diagnostics, XGBoost, SHAP, PLS-DA, PyTorch  
**Pipelines and data:** Snakemake, Nextflow, SLURM/HPC, Dask, Parquet, HDF5, OME-Zarr, SQL, FAIR data standards, multi-omics integration (ChEMBL, DrugBank, MetaboLights)  
**Software engineering:** Python packaging and PyPI, pytest, GitLab CI/CD, GitHub Actions, Docker, Apptainer, Kubernetes, reproducible environments (uv, pixi, lockfiles)  
**AI and applications:** LLM-based agentic extraction with schema-constrained output and human review, Streamlit, R Shiny  
**Languages:** Python (11 yrs), R (6 yrs), C++ (5 yrs), Bash/Linux (10 yrs), Git (10 yrs)
