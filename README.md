[![DOI](https://zenodo.org/badge/1015390134.svg)](https://doi.org/10.5281/zenodo.15836210)

# htr-front-justice

![characters badge](badges/characters.svg) ![regions badge](badges/regions.svg) ![lines badge](badges/lines.svg) ![files badge](badges/files.svg) 

Some transcriptions of minute books from military court councils during the First World War, as part of the Front-Justice project.

## Content 

The project is organized in two different directories, representing two different phases of the project. The data is mostly useful for automatic transcription purposes. It contains a large sample of different (100+) hands.

### Dir `full_pages`

This directory contains samples of pages taken from multiple armies. The pages are fully transcribed.

| Dossier      | Armée      | Pages | Transcription                  |
|--------------|------------|-------|--------------------------------|
| 11_J_75(2)   | 4e armée   | 10    | Théo Burnel / Giovanni Vitali |
| 11_J_76      | 4e armée   | 10    | Théo Burnel / Giovanni Vitali |
| 11_J_77      | 4e armée   | 10    | Théo Burnel / Giovanni Vitali |
| 11_J_78      | 4e armée   | 10    | Théo Burnel / Giovanni Vitali |
| 11_J_79      | 4e armée   | 10    | Théo Burnel / Giovanni Vitali |
| 11_J_184     | 10e armée  | 60    | Théo Burnel / Giovanni Vitali |
| 11_J_185     | 10e armée  | 39    | Théo Burnel / Giovanni Vitali |
| 11_J_186(1)  | 10e armée  | 40    | Théo Burnel / Giovanni Vitali |
| 11_J_186(2)  | 10e armée  | 40    | Théo Burnel / Giovanni Vitali |
| 11_J_187(1)  | 10e armée  | 21    | Théo Burnel / Giovanni Vitali |


### Dir `selected_pages`

This directory contains pages selected from the whole corpus, based on the needs of the project:
- treating the glosses-like additions (updates on the soldier)
- improving the handwritten text recognition


#### Dir `selected_pages/additions`

This dir contains around 450 pages with additions. Only the additions are annotated. The rest of the lines are ignored. **This subset should not be used for line-segmentation training**.

#### Dir `selected_pages/random_handwritten_sample`

This dir contains around 600 pages focusing on handwriting. It contains almost only manuscript lines and mixed lines (containing both print and handwritten lines). The typescript lines have been automatically identified and removed. **This subset should not be used for line-segmentation training**.

It has been created in several steps:
- by taking a random subset of the whole corpus to get the greatest diversity of hands
- by using a lexicality score for selecting the worst transcribed images based on a first trained model.

## Annotation and Transcription Guidelines

- Layout zones follow the [Segmonto vocabulary](https://github.com/SegmOnto/Guidelines), with minor adaptations.  
- Printed and handwritten text are both transcribed line by line, without distinction.  
- Superscripts are marked with `^` before the text (e.g. `M^e`).  
- Signatures are represented by a `+`.

  
## How to Cite

For citation information, see the [`htr-united.yml`](./htr-united.yml) file.

## Licences

The annotations are licensed under [CC BY](https://creativecommons.org/licenses/by/4.0/).  
The images are the property of the Front-Justice project (see [`CITATION.cff`](./CITATION.cff) for details).
