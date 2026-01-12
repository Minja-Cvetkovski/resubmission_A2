# Documentation 
## Corpus description
The data folder contains seven subdirectories representing the seven Arctic Monkeys studio albums, released between 2006 and 2022. These subdirectories contain all the song lyrics in raw .txt files. This corpus is designed to explore changes in thematic and stylistic changes over time.
## Target audience
This corpus is intended for musicologists and linguists who work with digital tools and are interested in the lyrical evolution of the Arctic Monkeys.
## Text selection
The texts were selected to cover the Arctic Monkeys' complete discography, from their first album to the most recent one. Including all albums will give the most accurate results when examining changes in lyrical style over time.
## Data collection
Lyrics were manually collected from Genius.com by copying and pasting the lyrics into plain .txt files. Each song is stored as a separate .txt file within its corresponding album folder.
Moreover, metadata (title, album, and year) was also manually compiled in a CSV file. An “artist” column was not included, as the corpus consists exclusively of songs by Arctic Monkeys.
## Required modules
- spaCy: used for linguistic annotation, including tokenization, lemmatization, part-of-speech tagging, and named entity recognition
- en_core_web_sm: required to process English text and enable linguistic features
- pandas: used for creating and manipulating DataFrames, merging metadata, and saving annotated CSV files
- plotly: used for creating visualizations to compare linguistic patterns across albums
## Format files 
1. Data folder:
   - Seven subdirectories representing the albums that each contain raw .txt files of all song lyrics. 
2. metadata.csv:
   - Title
   - Album
   - Year
3. corpus_df.csv:
   - Album
   - Filename
   - Title
   - Document (original text)
   - Year
   - Tokens
   - Lemmas
   - POS
   - Proper_nouns
   - NE_labels
   - NE_words
## Quality checks 
The corpus_df.csv file was checked whether it corresponds to original data as well as if spaCy's tools worked. Further, the "en_core_web_sm" is a relatively small model used for computational efficiency, and the quality of annotation may therefore not be perfect. For bigger projects, it is recommended to use "en_core_web_lg".
