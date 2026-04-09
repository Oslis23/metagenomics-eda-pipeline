# Metagenomics EDA Pipeline

Exploratory analysis of gut microbiome 16S rRNA data from a colorectal cancer cohort (59 samples: Healthy, Adenomatous Polyps, Colorectal Cancer). The pipeline covers data loading, alpha/beta diversity, and phylum-level differential abundance, building toward ASV-level machine learning classification.

## Tech Stack
- Python 3.11 (Anaconda)
- pandas, numpy, matplotlib, seaborn
- scikit-bio, scikit-learn, SHAP
- Jupyter Notebooks

## Notebooks

| # | Notebook | Description |
|---|----------|-------------|
| 01 | `01_data_loading.ipynb` | Data loading, QC, sparsity analysis, phylum composition barplot and heatmap |
| 02 | `02_alpha_diversity.ipynb` | Observed species, Shannon, Simpson, Chao1 — normality tests, Kruskal-Wallis, Mann-Whitney |
| 03 | `03_beta_diversity.ipynb` | Bray-Curtis dissimilarity, PCoA (2D + 3D), PERMANOVA with post-hoc pairwise tests |
| 04 | `04_diversity_analysis.ipynb` | Phylum-level relative abundance — boxplots, bar charts, Kruskal-Wallis + Mann-Whitney |

## Key Findings

- **Alpha diversity**: No significant differences between groups (Kruskal-Wallis, p > 0.05 for all metrics after Bonferroni correction).
- **Beta diversity**: Community composition differs significantly between groups (PERMANOVA, p < 0.05). Pairwise: Healthy vs CRC and Adenomatous Polyps vs CRC are the main drivers.
- **Phylum-level abundance**: No individual phylum shows significant differential abundance across groups. Phylum-level resolution is too coarse — CRC-associated shifts occur at genus/species level and are masked by aggregation.
- **Overall**: The community *as a whole* differs between disease stages (multivariate signal), but no single broad taxonomic group drives the effect — motivating ASV-level ML classification as the next step.

## Figures

| Figure | Description |
|--------|-------------|
| `figures/phylum_composition_barplot.png` | Stacked barplot of phylum-level relative abundance per sample |
| `figures/phylum_heatmap.png` | Heatmap of phylum-level relative abundance |
| `figures/alpha_diversity_violin.png` | Violin + strip plots for alpha diversity metrics by disease group |
| `figures/braycurtis_heatmap.png` | Bray-Curtis dissimilarity matrix heatmap |
| `figures/pcoa_braycurtis.png` | PCoA ordination (2D) colored by disease status |
| `figures/pcoa_3d.png` | PCoA ordination (3D) colored by disease status |
| `figures/04_phylum_boxplots.png` | Phylum-level boxplots with strip plots by disease group |
| `figures/04_phylum_barplots.png` | Phylum-level mean abundance bar charts with 95% CI by disease group |

## Status
In progress — Phase 1: EDA complete. Next: ASV-level ML classification (notebook 05).
