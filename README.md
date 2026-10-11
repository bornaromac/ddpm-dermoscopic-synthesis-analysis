# DDPM for Dermoscopic Image Synthesis and Memorization Analysis

## Overview

This repository contains a proof-of-concept implementation of a class-conditional Denoising Diffusion Probabilistic Model (DDPM) for synthetic dermoscopic image generation using the HAM10000 dataset.

In addition to model training and image sampling, the project includes an exploratory analysis workflow for comparing real and synthetic images. The workflow uses image embeddings, UMAP dimensionality reduction, and nearest-neighbor inspection, with an interactive D3.js visualization.

The project was developed as an initial experiment in diffusion-based medical image synthesis and as a foundation for subsequent research.

## Research objectives

- Explore class-conditional DDPM training for dermoscopic image synthesis.
- Visualize the embedding distributions of real and generated images using UMAP.
- Inspect nearest real-image neighbors of generated samples.
- Explore potential signs of memorization and distribution overlap.

**Important:** UMAP projections and nearest-neighbor inspection are exploratory analysis tools. They do not, by themselves, establish whether a generative model memorizes training data or provide a formal privacy guarantee.

## Dataset

The experiments use HAM10000, a publicly available dataset of dermatoscopic images of pigmented skin lesions.

The dataset is not redistributed in this repository. Users must obtain it from an authorized source and follow the dataset's applicable terms of use.

Dataset preparation, metadata requirements, and expected directory structure should be documented before attempting to reproduce the experiments.

## Project structure

- `configs/` — experiment configuration files
- `src/` — model training, sampling, and analysis scripts
- `d3_viz/` — interactive D3.js visualization
- `viz_export/` — exported artifacts used by the visualization, where applicable
- `requirements.txt` — Python dependencies

Dataset files, model checkpoints, training logs, and generated artifacts are not intended to be committed to the repository.

## Requirements

- Python 3.10 or a compatible version verified against the project dependencies
- PyTorch and a compatible execution environment
- A GPU is recommended for training

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Reproducibility

Before reproducing the experiments, verify the configuration files, dataset layout, preprocessing procedure, and sampling settings.

Detailed instructions for training, sampling, exporting embeddings, and launching the visualization will be added after the corresponding scripts and dependencies have been verified.

## Limitations

This repository represents a proof of concept rather than a validated clinical system or a definitive privacy evaluation. Results depend on the dataset, preprocessing, model configuration, and evaluation procedure.

Synthetic images must not be interpreted as clinical evidence or as a replacement for real medical data.

## Relationship to subsequent work

This repository represents an earlier DDPM experiment. It is separate from the subsequent latent diffusion model experiments conducted at a higher image resolution.

## Citation

If you use this repository in academic work, please cite the repository URL and the relevant dataset and methodological references. A formal citation record can be added when the project is assigned a publication or archival identifier.

## License

A license has not yet been specified. Reuse and redistribution permissions should be clarified before the repository is presented as an open-source project.
