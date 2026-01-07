## NER Validation (BERT/Stanford) Protocol and Observations

This protocol details the validation process for the first trial of the Stanford and BERT NER models on the first three folios of the Funeral Entries volume NLI GO MS 66.

Transcriptions of individual entries were generated and extracted from Transkribus before being passed unprocessed through the Stanford and BERT models both in a combined and separate capacity. In the combined scenario, if any model identified an entity (either person = PER or location = LOC) with >70% certainty, that entity was captured. Duplicates were dropped with only the higher certainty score being retained. In the separate scenarios, all PER and LOC entities were preserved regardless of the confidence score.

Each entity was recorded and validated in a CSV file of the following format:

| text    | start | end | label | confidence | method   | file_name                | validation |
| ------- | ----- | --- | ----- | ---------- | -------- | ------------------------ | ---------- |
| Dublin  | 303   | 309 | LOC   | 0.9988     | stanford | 0001_NLI_GO_MS_66_0001r  | 1          |
| Phoebe  | 192   | 198 | PER   | 0.997      | BERT     | 0001_NLI_GO_MS_66_0001   | 1          |

### Validating Results

Four categories were used in validating these off-the-shelf NER results:

- **0 = False.** NER inaccurate.

  Example sentence: “Shee was buried.”

  &rarr; where “Shee” is identified as PER: **0**

- **1 = True.** NER is accurate, and Transkribus transcription too.

  Example sentence: “Shee was buried in Dublin.”

  &rarr; where “Dublin” is identified as LOC: **1**

- **2 = Improve.** NER is partially accurate, but the models have either grabbed an entity only partially or grabbed more text than was necessary. This may be because of either the models themselves or be caused by a transcription error.

  Example sentence: “Nicholas Cusake Knight was Buried in St. Patrickes.”

  &rarr; where “Nicholas Cusake Knight” is identified as PER and “St. Patricke” is identified as LOC. These are both technically correct answers. However, we are not grabbing titles (Knight, Lady, Mayor, Dame etc) as part of PER entities and the models cut through “St. Patrickes”, removing the “s”. Both results are therefore marked as **2**.