# 📊 Assessment of Named Entity Recognition (NER) Funeral Entries Manuscripts using NLP techniques

[![DOI](https://zenodo.org/badge/1128349506.svg)](https://doi.org/10.5281/zenodo.18174068)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC--BY--4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

![FAIR Data](https://img.shields.io/badge/FAIR-Compliant-4db8ff)
![Status](https://img.shields.io/badge/status-published-blue)
[![Open Science](https://img.shields.io/badge/open%20science-yes-brightgreen)](https://www.fosteropenscience.eu/)

## Overview

This repository supports research on the recovery of women’s lives from fragmented and underused archives, focusing on the Funeral Entries held in the Genealogical Office of the National Library of Ireland. Compiled by the Ulster King of Arms between the late sixteenth and early eighteenth centuries, these manuscripts document death dates, kinship networks, and social affiliations, and are notable for their unusually high proportion of women (about 38 percent) for the early modern period.

Developed as part of the [**ERC-funded VOICES project**](https://voicesproject.ie/), this resource provides data, code, and documentation for assessment of the combination of out of the box AI-powered methods such as Handwritten Text Recognition (HTR) and Named Entity Recognition (NER) to extract persons, places, and other entities from historical sources.

It aims to support the evaluation of reusable workflows, annotated gold standards, and FAIR-aligned humanities data, ultimately advancing the historiographical understanding of archival visibility and the interpretive potential of genealogical records for women’s history.

---

## 📚 Table of Contents

1. [Overview](#overview)
2. [File and Structture](#-files-and-structure)
3. [FAIR Statement](#fair-statement)
4. [Citation](#-citation)
5. [Contributing](#-contr})
6. [License](#license)
7. [Contact](#contact)

---

## 📁 Files and Structure

```
📦 VOICES-FUNERALENTRIES-NER/
├── data/
│   ├── annotation/        # Annotation files and guidelines
│   ├── displacy/          # NER visualization outputs (displacy JSON)
│   ├── ner/               # NER outputs
│   ├── raw/               # Original, unprocessed data files
│   ├── transcriptions/    # Transcription CSV files for each variant
│   └── validation/        # Validated entity files
├── docs/                      # Documentation and Curation Guides
├── notebooks/                 # Used notebooks
├── metadata/                  # Metadata catalog and schema
├── fair/                      # FAIR machine-readable metadata
├── .zenodo.json
├── datapackage.json
├── LICENSE
├── CITATION.cff
└── README.md
```

---

## 🧬 FAIR Statement

This dataset follows the FAIR data principles:

- **Findable**: It is indexed and published with a DOI.
- **Accessible**: All files are publicly available in open formats.
- **Interoperable**: Metadata and structure follow community standards.
- **Reusable**: Documentation and licensing enable long-term reuse.

Machine-readable metadata is available in the `fair/` and `metadata/` folders.

---

## 📖 Citation

If you use it in your research, please to cite this work, both the dataset and the corresponding paper; the suggested citation in BibTex format is:

```bibtex
@article{VOICES_JOHD_2026,
  author    = {McShane, Bronagh Ann and Rincon-Yanez, Diego and Vanden Borre, Felix and Ohlmeyer, Jane and O'Sullivan, Declan},
  title     = {Digitising Death: Benchmarking Genealogical Data and Recovering Women’s Histories in Early Modern Ireland},
  journal   = {Submitted to Journal of Open Humanities Data},
  keywords  = {digital humanities; benchmarking; named entity recognition; early modern Ireland; women’s history; FAIR data},
  year      = {2026},
  month     = {TBD},
  volume    = {TBD},
  doi       = {TBD},
  url       = {TBD}
}

@dataset{mcshane_2026_18174069,
  author       = {McShane, Bronagh Ann and Rincon-Yanez, Diego and Vanden Borre, Felix and Ohlmeyer, Jane and O'Sullivan, Declan},
  title        = {{Digitising Death (Funeral Entries): Benchmarking Genealogical Data and Recovering Women's Histories in Early Modern Ireland}},
  month        = {jan},
  year         = {2026}
  publisher    = {Zenodo},
  version      = {0.0.2},
  doi          = {10.5281/zenodo.18174069},
  url          = {https://doi.org/10.5281/zenodo.18174069},
}
```


---

## 📜 License

This dataset is shared under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license. 

You are free to reuse, adapt, and distribute it with proper attribution.

This project is licensed under the [CC BY 4.0 License](LICENSE).

## 🤝 Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to contribute to this project.

## 🧾 Code of Conduct

This project adheres to a [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this standard.

## 📬 Contact

For questions or collaboration inquiries, contact the dataset curators listed in the [`CITATION.cff`](./CITATION.cff).
