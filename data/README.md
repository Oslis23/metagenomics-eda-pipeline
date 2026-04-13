# CRC Microbiome ML Dataset

## 📊 About This Dataset

This dataset contains **processed gut microbiome data** from 59 samples for **Colorectal Cancer (CRC) detection** using machine learning. The data is derived from 16S rRNA gene sequencing and has been preprocessed using the DADA2 pipeline.

## 📁 Files Included

### 1. `seqtab_nochim_export.xlsx` (1.4 MB)

- **ASV (Amplicon Sequence Variant) abundance table**
- Rows: Patient samples (59 samples)
- Columns: DNA sequences (ASVs) representing different bacterial species
- Values: Read counts (how many times each bacteria was detected)

### 2. `taxa_species_export.xlsx` (511 KB)

- **Taxonomic classification table**
- Maps each ASV to its taxonomic classification
- Includes: Kingdom, Phylum, Class, Order, Family, Genus, Species

### 3. `metadata.csv` (2.8 KB)

- **Patient information**
- Columns:
  - `SampleID`: Unique sample identifier
  - `host_disease`: Disease classification code
  - `SampleName`: Sample name
  - `DiseaseStatus`: Colorectal cancer | Healthy | Adenomatous Polyps
  - `Sex`: Patient gender
  - `Age`: Patient age

## 🎯 Usage

This dataset is ready for machine learning! Use it to:

1. Train classification models to predict CRC from gut microbiome composition
2. Identify bacterial genera associated with CRC
3. Compare microbial diversity between healthy and CRC patients

## 📖 Citation

If you use this dataset, please cite the original study and acknowledge the data source.

## 🔗 Related

- Main repository: [ColorectalCancer-Detection](https://github.com/aramelheni/ColorectalCancer-Detection)
- ML model notebook: See accompanying Kaggle notebook
