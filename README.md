# seurigiotto-st-workflow
"Novel Seurat &amp; Giotto pipelines for Spatial Transcriptomics (ST) data analysis. MSc Thesis project, UB-UOC, 2025."

SeuriGiotto-ST-Workflow
=======================

Optimized pipelines for Spatial Transcriptomics analysis using Seurat & Giotto
Developed for reproducible benchmarking and biological insight in lung cancer research (Visium HD, 10x Genomics)

Project Overview
----------------

This repository provides a reproducible set of pipelines for analyzing Spatial Transcriptomics (ST) data with Seurat and Giotto.
It was developed as part of my Master’s Thesis (TFM) in Bioinformatics and Biostatistics (UB-UOC, 2025), but is designed as a resource for the wider research community.

Key Features

- Independent, fully documented pipelines for Seurat and Giotto using harmonized parameters and robust QC.
- Hybrid pipeline that combines Seurat’s efficiency and Giotto’s granularity, with an automated decision step.
- Benchmarking: memory usage, execution time, clustering resolution and accuracy.
- Downstream analysis: marker gene detection, cell-type signature scoring, deconvolution, and spatial visualization.
- All code, figures, and main results are open for reproducibility.

Repository Structure
--------------------

scripts/        # All R scripts for each workflow and analysis step
data/           # Example/public datasets or download instructions (no private raw data)
results/        # Output figures, tables, and summary statistics
docs/           # Additional documentation, workflow charts, manuscript, slides
env/            # Environment files (renv.lock, requirements.txt, conda, etc.)

Getting Started
---------------

1. Clone the repository

   git clone https://github.com/<your-username>/seurigiotto-st-workflow.git
   cd seurigiotto-st-workflow

2. Install dependencies

   - R version: 4.3 or higher recommended
   - Key packages:
     Seurat (>=5.x), Giotto (>=4.x), ggplot2, dplyr, patchwork, pryr, arrow, data.table, scales, RColorBrewer, viridis

   - Install in R:
     install.packages(c("Seurat", "Giotto", "ggplot2", "dplyr", "patchwork", "pryr", "arrow", "data.table", "scales", "RColorBrewer", "viridis"))

   - Optionally use renv or a conda environment (see /env/ if available).

3. Data

   - All scripts are configured for public datasets (Visium HD, 10x Genomics).
   - For full analysis, download the raw data as described in /data/README.md.

4. Run the analysis

   - See scripts in /scripts for workflow details.
   - Typical usage (in RStudio terminal or shell):

     Rscript scripts/1Seurat.R
     Rscript scripts/2Giotto.R
     Rscript scripts/3ComparativeAnalysis.R
     Rscript scripts/4OptimizedPipeline.R
     Rscript scripts/5IntegratedAnalysis.R

   - Outputs (figures, results, logs) will be saved in /results/ with organized subfolders.

Citation
--------

If you use this workflow or code, please cite this repository and the associated Master Thesis.
Author: Ángel I. Pérez Santiago
MSc in Bioinformatics & Biostatistics (UB-UOC, 2025)
GitHub profile: https://github.com/nuiter

License
-------

This project is licensed under the MIT License. See the LICENSE file for full terms.

Acknowledgements
----------------

- Dataset: Visium HD CytAssist Gene Expression Human Lung Cancer (Fixed Frozen) by 10x Genomics.
- Supervision: Dr. Alfonso Saera Vila (TFM advisor)
- Frameworks: Seurat (https://satijalab.org/seurat/), Giotto (https://giottosuite.com/)

For questions, collaborations, or feedback, please open an issue or contact me directly via GitHub.
