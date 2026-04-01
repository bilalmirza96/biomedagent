# BioMedAgent Plugin

Autonomous biomedical data analysis using a multi-agent pipeline inspired by [BioMedAgent](https://www.nature.com/articles/s41551-024-01309-4) (Nature Biomedical Engineering, 2026).

## What it does

BioMedAgent takes natural language instructions about biomedical data and produces complete, executable analyses with results and summarized reports. It follows a three-phase pipeline:

1. **Planning** — Task classification, prompt refinement, file analysis, tool scoring, workflow design
2. **Coding** — Code generation with Python/R library mappings, performance optimization, unit tests
3. **Execution** — Interactive execution with error handling, retry loops, and report generation

## Supported analysis categories

| Category | Examples |
|----------|----------|
| **Omics** | Differential expression, pathway enrichment, single-cell RNA-seq, variant calling |
| **Precision Medicine** | Pathogenic variant identification, pharmacogenomics, clinical annotation |
| **Machine Learning** | Classification, regression, clustering, association rules, deep learning |
| **Statistics** | t-tests, ANOVA, survival analysis, Cox regression, cross-tabulation |
| **Visualization** | Heatmaps, volcano plots, PCA, survival curves, forest plots |

## Installation

### Claude Code CLI

```bash
claude --plugin-dir /path/to/biomedagent
```

### Claude Cowork

Add this plugin from the plugin marketplace, or clone and point to the directory.

### Project-level

Copy the plugin directory into your project's `.claude/plugins/` folder.

## Usage

Just describe your biomedical analysis task in natural language:

- "Analyze my RNA-seq data for differentially expressed genes"
- "Train a random forest to predict heart disease from this CSV"
- "Run a survival analysis with Kaplan-Meier curves"
- "Cluster these patients using k-means and show me the results"
- "Find pathogenic variants in my VCF file"

The plugin handles tool selection, workflow design, code generation, execution, and reporting automatically.

## Features

- **65 biomedical tools** catalogued with automatic selection and scoring
- **Self-evolving memory** — learns from past analyses to accelerate future ones
- **R + Python** — uses whichever language is best for each task
- **Error recovery** — automatic retry with intelligent debugging
- **Publication-ready reports** with biological/clinical interpretation

## Requirements

- Python 3.9+ with common scientific libraries (pandas, scikit-learn, scipy, matplotlib)
- Optional: R with Bioconductor packages (for survival analysis, DESeq2, etc.)
- Optional: System tools (BWA, GATK, samtools) for genomics pipelines

## License

MIT
