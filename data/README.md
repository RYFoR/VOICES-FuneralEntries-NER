# 📁 Funeral Entries Data Overview

This folder contains curated and other data files supporting the assessment of Named Entity Recognition (NER) and Handwritten Text Recognition (HTR) on historical Funeral Entries manuscripts, as part of the ERC-funded VOICES project.

## 🗂️ Folder Structure

The data directory is organized into the following subfolders, each representing a key stage in the NER and transcription workflow:

- **annotation/** – Contains annotated files for the HTR Upload
- **displacy/** – Includes NER visualization outputs in displacy JSON format for each transcription variant.
- **ner/** – Reserved for NER outputs, models.
- **transcriptions/** – Contains transcription CSV files for each variant.
- **validation/** – Holds the standardized validated entity files for assesment and evaluation.

## 📑 Transcription Variants

Five transcription variants of the Funeral Entries subset were produced:

- **Manual transcription (MAN):** A historian-generated version retaining early modern spellings while correcting obvious errors.
- **EyeCR transcription (EYE):** Produced using an internal transcription tool that can connect to different LLMs, developed at the ADAPT Centre. For this case study, the LLM connected to EyeCR was the GPT-4.1-mini model.
- **Transkribus transcription (TRA):** Raw HTR output exported directly from Transkribus.
- **Curated Transkribus transcription (CUR):** A diplomatically curated version of TRA, correcting clear HTR errors while preserving original orthography.
- **Transkribus + VARD transcription (TKV):** The TRA version processed with the software VARD2 to normalise historical spelling variants.

## 📷 Funeral Entry Images

Each entry includes images with crest and coat of arms from NLI GO MS 66, numbered FE 1–11, with Transkribus page files, volume reference, and folio pagination (e.g., 1 recto, 1 verso). FE 6 spans f. 2r–2v.
