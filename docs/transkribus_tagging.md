## Using Transkribus to transcribe NLI GO MS 66

### Background

[Transkribus](https://www.transkribus.org/) is a tool for Handwritten Text Recognition (HTR). In the [VOICES project](https://voicesproject.ie), it transforms digital images of early modern texts into machine-readable digital text.

Historians review and manually correct these transcriptions before being processed for statistical analysis and entity extraction. This will populate the VOICES Knowledge Graph (KG), which is the heart of the project and will expose the entities for future research.

NLI GO MS 66 (also known as Funeral Entries volume 3) is one of the 16 Funeral Entries volumes being analysed by the VOICES project. The benchmarking experimentation conducted for the publication associated with this dataset focused on the first three folios of the volume.

### Principles

The Funeral Entries (FE) memorialise deceased people in early modern Ireland, often mentioning their family relations. The collection is held at the Genealogical Office of the National Library of Ireland (NLI), where it has been digitised in full. Digital copies were given to the VOICES project for analysis.

Before ingestion into Transkribus, these files had to be manually renamed according to their archival reference number whereby the document given shelfmark GO MS66 in the NLI catalogue would be renamed `NLI_GO_MS_66_0001r`. Retention of this archival information in the metadata of each image is particularly important since the images were being uploaded en masse to Transkribus and the resulting transcriptions would retain the metadata associated with the corresponding image.

Most Funeral Entries consists of a header, a crest or sigil, and a main entry. For the purpose of transcription, the drawings will be ignored, and only text will be considered.

Once the “Recognise” button is clicked, Transkribus will start converting the image of the text to machine-readable text. As part of this step, the markup process will identify lines on which the text is found. The automated recognition worked without problems for our collection, so manual correction wasn’t necessary.

Commonly, the Funeral Entries collection features two entries per page. As the export for further processing requires the entries to be separated, a decision was made to use markup in the documents to identify the individual entries. The markup was done using the manual drawing of “regions” on the image, identifying a “heading” and a “paragraph”. The heading would later be identified in the XML-export so that it could be used as a separator between entries.

For this reason, each entry is required to have a “heading”, even if the page doesn’t contain any (see: [Exceptions](#exceptions)).

It may also have addendum added by the original scribe or other writers at a later point in time. This additional script that does not form part of the Funeral Entry proper will be marked as [marginalia](#4-marginalia).

### Exceptions

The Funeral Entries corpus consists of heterogenosu and messy data. The hands used in the manuscripts change drastically between and even within volumes. Moreover, several crucial data points are often missing from the source altogether. Names, places, and/or dates of death are often ommitted, or scribbled only in part. Some entries are empty altogether. Entries can also span multiple pages or contain elaborate depictions of funerary processions. This data messiness complicates the use of HTR to automatically transcribe the text.

### Markup process

As a complex historical artifact hinting at the struggles of a nascent bureaucracy, finding a one-size-fits-all solution to the HTRing of the Funeral Entries corpus is complicated. The following tagging process allows for a great degree of flexibility for the pre-processing of the manuscripts before HTR.

#### 1. Mark up process

1. In a first step, individual entries will be manually identified by the user, following which the entry’s regions will be highlighted. All areas with text are considered regions.
2. In a second step, tags will be assigned to the regions for each entry, with the options to tag a region as [heading](#2-heading), [paragraph](#3-paragraph) or [marginalia](#4-marginalia). Each individual entry must have at least one heading and one paragraph, even if those are left blank.

#### 2. Heading

1. Creating a heading region. Where possible, this is the one or two names above the crest.
2. When there are no names on top of the crest, but there are names to the left and right, these will make up the header. To avoid confusing the model with designs in the coat of arms, two separate heading regions will be created, which will then be processed together post-extraction. This is done by ensuring that the heading regions are together in the sorting phase.
3. When no names can be identified as a heading for the subsequent entry, a blank space on the page will be created.

#### 3. Paragraph

1. Paragraphs correspond to the main text of the Funeral Entry. Some FEs will only have one, others will have multiple. Some will even have blocks of text spread across the layout of the page which need to be captured individually, as Transkribus reads from left to right.
2. The text needs to be examined to determine whether one paragraph suffices, or whether the FE’s main body of text needs to be split into multiple paragraphs. Where multiple paragraphs belong to one entry, it is essential that they are combined together in the sorting phase.
3. Paragraphs must always be assigned to a heading (or combined headings). Only textual elements should be captured as to avoid throwing off the model upon transcription.

#### 4. Marginalia

1. Occasionally, the pages carry additional text that cannot be identified as a heading or as paragraphs. This can be additional names of houses in the crests, notes by the scribes, a numbering system within the volume, or annotations such as references to other FEs in the collection.
2. These items will be labelled using the Marginalia tag. This ensures that the information is not lost during the extraction process, even though it is not immediately relevant for the purpose of this project.

#### 5. Dealing with multiple pages

1. Some entries are spread across two or more pages. Where an entry continues from the previous page, new paragraph and marginalia regions should be created as appropriate.
2. New heading regions should not be indicated until a new entry is encountered.

#### 6. Sorting

1. The regions appear in the right column next to the image. Extra care is required to ensure that the regions are in the correct order. For that reason, it is recommended to tag one FE with all its elements first, then adjust the order before proceeding to the next FE on the same page.
2. When sorting, the heading (or combined headings) must always be on top, as it serves as a separator to identify the belonging elements. Even if marginalia occasionally may be higher or left of the heading, the outline in the right panel must have the heading(s) leading all other related entries.

#### 7. Transcription process

1. After marking up all entries in the collection, the historian will proceed with the transcription process. This includes selecting the best-suited transcription model. The process will consume paid tokens within Transkribus.
2. Following the automated transcription, the FEs will undergo manual inspection, and the transcription will be refined. Any errors identified in steps 1 through 5 may also be addressed and corrected at this stage.