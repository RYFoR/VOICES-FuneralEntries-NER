# 🛠️ Instructions for Using the RYFoR Dataset Template

This guide walks you through the steps required to use, adapt, and share your own dataset based on this template. The goal is to help you stay aligned with FAIR principles and good research data practices.

## 📚 Table of Contents

0. [🚀 Getting Started](#-getting-started)
1. [📁 Organize Your Dataset](#-1-organize-your-dataset)
2. [📝 Document Your Dataset](#-2-document-your-dataset)
3. [📊 Explore and Analyze](#-3-explore-and-analyze)
4. [🧬 Declare Metadata](#-4-declare-metadata)
5. [♻️ Reuse and Share](#-5-reuse-and-share)
6. [🤝 Collaborate](#-6-collaborate)

---

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Pandas (for CSV handling)
- Git, Markdown, and basic knowledge of metadata standards

### Installation

```bash
# Clone the repository
git clone https://github.com/ryfor/RYFOR-data-template.git
cd RYFOR-data-template

# Create environment
conda env create -f environment.yml
conda activate ryfor-data-template
```

---

## 📁 1. Organize Your Dataset

Place your raw data files into:

```
data/raw/
```

If needed, you can add `data/processed/` for cleaned or transformed versions.

---

## 📝 2. Document Your Dataset

Update the following files inside the `docs/` folder:

- `codebook.md`: Define variables and controlled vocabularies.
- `data_dictionary.md`: Describe each column and data type.
- `methodology.md`: Explain how the data was collected or generated.
- `quality_report.md`: Highlight data issues, cleaning steps, and completeness.

---

## 📊 3. Explore and Analyze

Use the notebooks in the `notebooks/` folder:

- `01-explore_raw_data.ipynb`: Automatically summarizes and visualizes your dataset.
- Add your own notebooks like `02-preprocessing.ipynb`, `03-analysis.ipynb`, etc.

You can run them using:

```bash
jupyter notebook
```

---

## 🧬 4. Declare Metadata

Your dataset includes several machine-readable metadata files:

- `datapackage.json`: For validation with Frictionless Data tools
- `.zenodo.json`: For automatic metadata ingestion when publishing on Zenodo
- `schemaorg.jsonld`: Embedded JSON-LD for discoverability in Google Dataset Search
- `dcat.ttl`: DCAT-compliant RDF metadata for data catalogs
- `CITATION.cff`: Citation metadata (DOI, version, authors)

These help ensure your dataset is **FAIR**: Findable, Accessible, Interoperable, and Reusable.

---

## ♻️ 5. Reuse and Share

- Publish on [Zenodo](https://zenodo.org/) or [MendeleyData](https://data.mendeley.com/)
- Register a DOI (automatically with `.zenodo.json`)
- Share with institutions or platforms that support DCAT or Frictionless metadata
- Reference your dataset using the `CITATION.cff` format

---

## 🤝 6. Collaborate

Encourage contributions with:

- `CONTRIBUTING.md`
- `CODE_OF_CONDUCT.md`
- Open issues or pull requests for improvement.

---

## 🗂️ Project Structure

```
dataset-template/
│
├── .github/                      # Community health files (issues, templates, policies)
│   └── ISSUE_TEMPLATE.md         # Template for reporting issues or suggestions
│
├── data/                         # All dataset files are stored here
│   ├── external/                 # External data sources (raw, unaltered)
│   ├── processed/                # Cleaned and transformed data ready for analysis
│   └── raw/                      # Primary raw data (e.g., metadata.csv, data.csv)
│
├── docs/                         # Human-readable documentation
│   ├── data_dictionary.md        # Description of each dataset variable
│   ├── ethical_considerations.md # Ethical checklist and research compliance notes
│   ├── methodology.md            # Data collection and processing methodology
│   ├── quality_report.md         # Data quality insights and validation output
│   └── README.md                 # Description of the documentation module
│
├── fair/                         # FAIR compliance statements and evidence
│   └── README.md                 # Summary of FAIR alignment strategies
│
├── metadata/                     # Machine-readable metadata for catalogs
│   ├── dcat.ttl                  # DCAT RDF file for semantic catalogs
│   └── schemaorg.jsonld          # Schema.org metadata for Google Dataset Search
│
├── notebooks/                    # Interactive notebooks for data analysis
│   ├── 00-quality_report.ipynb   # Quality control and summary statistics
│   ├── 01-explore_raw_data.ipynb # Initial data exploration
│   ├── 02-preprocessing.ipynb    # Cleaning and preprocessing steps
│   └── 03-analysis.ipynb         # Main analysis workflows
│
├── .gitignore                    # Git exclusions
├── .zenodo.json                  # Zenodo-compatible metadata file
├── CHANGELOG.md                  # Version history and changes
├── CITATION.cff                  # Citation metadata (DOI, author, version)
├── CODE_OF_CONDUCT.md            # Contributor behavior expectations
├── CONTRIBUTING.md               # Guidelines for contributions
├── datapackage.json              # Frictionless Data metadata descriptor
├── LICENSE                       # Licensing terms (e.g., MIT)
├── README.md                     # Main description of the dataset and usage
├── trinity.win.commit.cmd        # Helper script (customizable for internal use)
└── USAGE.md                      # How to use and adapt this dataset template
```
