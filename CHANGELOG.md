# 📦 Changelog

All notable changes to this dataset template are documented in this file.  
This project adheres to [Semantic Versioning](https://semver.org/).

---

## [0.0.2] - 2026/01/07

### Changed
- Updated main README to reflect current data subfolder structure.
- Improved documentation in `docs/README.md` with direct links and usage guidance.
- Enhanced markdown formatting in `docs/transkribus_tagging.md` and `docs/validation_protocol.md` for better rendering.
- Expanded and clarified `data/README.md` to describe all subfolders and workflow.
- Updated `metadata/dcat.ttl` and `metadata/schemaorg.jsonld` to accurately describe data distributions.
- Populated `datapackage.json` with detailed resource entries for all data subfolders.

### Data
- Added and documented the following subfolders in `data/`:
  - `annotation/` for annotation files and guidelines.
  - `displacy/` for NER visualization outputs.
  - `ner/` for NER outputs and models.
  - `raw/` for original, unprocessed data files.
  - `transcriptions/` for transcription CSV files.
  - `validation/` for validated entity files.

### Docs
- Added and improved `docs/README.md` for better navigation and clarity.
- Improved markdown compliance and readability in `docs/transkribus_tagging.md` and `docs/validation_protocol.md`.

### Notebooks
- Added `notebooks/00-NER-Validation.ipynb` for NER validation analysis and experiments.


## [0.0.1] - 2026/01/05

### Added
- Project initialization.
- Basic README and initial folder scaffold.
