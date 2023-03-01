# Computing, Culture & Creativity

Various explorations and assorted materials related to course planning for future "Computing, Culture & Creativity" course.

## poemBot

Documentation and instructional materials forked from @evanwill's [poemBot](https://github.com/evanwill/poemBot) repository.

- [Overview](https://github.com/kwaldenphd/poemBot/blob/master/overview.md)
- [poemsMain.py](https://github.com/kwaldenphd/poemBot/blob/master/poemsMain.py)
- [thermalPrinter.py](https://github.com/kwaldenphd/poemBot/blob/master/thermalPrinter.py)
- [Hardware setup](https://github.com/kwaldenphd/poemBot/tree/master/pi-hardware)
- [Deployed versions](https://github.com/kwaldenphd/poemBot/tree/master/deployed_versions)

## Corpora

### Project Gutenberg

Allison Parish materials
- [Gutenberg, dammit](https://github.com/aparrish/gutenberg-dammit/) (full corpus)
- [Gutenberg corpus](https://github.com/aparrish/gutenberg-poetry-corpus) (poetry corpus)
  - ["Quick Experiments" Jupyter Notebook](https://github.com/aparrish/gutenberg-poetry-corpus/blob/master/quick-experiments.ipynb)
  - ["Plot to Poem" 2017 NoPaGenMo Jupyter Notebook](https://github.com/aparrish/plot-to-poem/blob/master/plot-to-poem.ipynb)
- [Gutenberg Poetry Autocomplete](http://gutenberg-poetry.decontextualize.com/)
  
[KW "gutenberg-explorations" Jupyter Notebook](https://colab.research.google.com/drive/1PfqleS2Bh4-I3CnOt7tKV-Lc4CHtmhGT?usp=sharing)
- Builds Allison Parrish's `Gutenberg Poetry` corpus
- Combines separate lines to create `poem` field
- Loads metadata from [gutenberg.org](https://www.gutenberg.org/cache/epub/feeds/pg_catalog.csv)
- Joins Gutenberg corpus & metadata using `pd.merge()`

### Golden Treasury

Evan did some data wrangling/cleaning with web scraping from Gutenberg HTML for a specific collection (Palgrave Golden Treasury)
- Source: https://www.gutenberg.org/ebooks/19221
- Data: https://github.com/evanwill/poemBot/blob/master/goldenTreasuryPoems.csv

### Poetry Foundation

Data looks identical:
- Web scraping program that uses Selenium: https://github.com/TGDivy/WebScrapping-PoetryFoundation
- Kaggle dataset: https://www.kaggle.com/datasets/tgdivy/poetry-foundation-poems

Files:
- [KW "other-data-sources" Jupyter Notebook](https://colab.research.google.com/drive/1Gv8vd51xug1tKX8Mkn5H3T9G6eWI4VIe?usp=sharing)
- [pfound.csv](https://github.com/kwaldenphd/poemBot/blob/master/corpora/pFound.csv)

- [KW "data-wrangling" Jupyter Notebook](https://colab.research.google.com/drive/1ifEg5impzAyJPipg6oNQ6EBHv2wn-Ah6?usp=sharing)
- [pFound_subset.csv](https://github.com/kwaldenphd/poemBot/blob/master/corpora/pFound_subset.csv)

### Poets.org

Jacob Heil taught a DH class at Wooster and built a script that scraped `poets.org`
- Class: https://github.com/WoosterDH/poemBot-Scripts
- Data: https://github.com/WoosterDH/poemBot-Scripts/blob/master/poem_scrape_cleaning.csv

Built a program that uses `BeautifulSoup` to scrape `Poets.org`.
- [KW "other-data-sources" Jupyter Notebook](https://colab.research.google.com/drive/1Gv8vd51xug1tKX8Mkn5H3T9G6eWI4VIe?usp=sharing)
- [poetsOrg.csv](https://github.com/kwaldenphd/poemBot/blob/master/corpora/poetsOrg.csv)

- [KW "data-wrangling" Jupyter Notebook](https://colab.research.google.com/drive/1ifEg5impzAyJPipg6oNQ6EBHv2wn-Ah6?usp=sharing)
- [pOrg.csv](https://github.com/kwaldenphd/poemBot/blob/master/corpora/pOrg_subset.csv)

### PoetryDB

Some kind of API situation
- https://github.com/thundercomb/poetrydb
- https://poetrydb.org/index.html

Built a program that scrapes all titles included in the API.
- [KW "other-data-sources" Jupyter Notebook](https://colab.research.google.com/drive/1Gv8vd51xug1tKX8Mkn5H3T9G6eWI4VIe?usp=sharing)
- [poemDB.csv](https://github.com/kwaldenphd/poemBot/blob/master/corpora/poemDB.csv)

- [KW "data-wrangling" Jupyter Notebook](https://colab.research.google.com/drive/1ifEg5impzAyJPipg6oNQ6EBHv2wn-Ah6?usp=sharing)
- [poemDB_subset.csv](https://github.com/kwaldenphd/poemBot/blob/master/corpora/poemDB_subset.csv)

## Data Wrangling

[KW "data-wrangling" Jupyter notebook](https://colab.research.google.com/drive/1ifEg5impzAyJPipg6oNQ6EBHv2wn-Ah6?usp=sharing)
- Loads separate corpora, creates common column structure (`title`, `text`, `author`, `source`)
- Filters out extraneous regular expression content/characters
- Adds `lineCount` value that counts # of lines in each poem
- Adds `avgChar` value that counts the total # of characters in the poem & divides by the number of lines
- Merges individual corpora dataframes using `pd.concat()`

[KW "filtering-poems" Jupyter notebook](https://colab.research.google.com/drive/1iFEAXZu58O22BLPva5xBJWEI8EFVMlU0?usp=sharing)
- Filters out poems with more than 20 lines 
- Filters out poems that average more than 40 characters per line
- Criteria modeled on Evan Will's [Golden Treasury Corpus](https://github.com/evanwill/poemBot/blob/master/goldenTreasuryPoems.csv)

## Test Balloon

[KW Jupyter Notebook](https://colab.research.google.com/drive/1zQhl36ph35K-dO_mzTWrme5np804yo0I?usp=sharing)
- Loads data from `CSV`
- Function that selects and outputs random poem
- Function that selects and outputs random poem based on keyword input

## Jupyter Notebooks

Exploring Allison Parrish's materials/resources
- [allison-parrish](https://colab.research.google.com/drive/1DiWHgo5ugK_mEaAbCWNS_y2YKB3YgNQQ?usp=share_link)
- [project-gutenberg-parrish](https://colab.research.google.com/drive/168SXWCO_NI7uvbTLZRHYQNU7Rbe7KnwF?usp=share_link)
- [gutenberg-explorations](https://colab.research.google.com/drive/1PfqleS2Bh4-I3CnOt7tKV-Lc4CHtmhGT?usp=share_link)
- [magic-words](https://colab.research.google.com/drive/1tAP5tSJStzFvJaudzcpaesRKVkFD6ykk?usp=share_link)
- [spacy](https://colab.research.google.com/drive/1IQXIkK9KZdfG3gT8dszh1NG-Dzc-sMCF?usp=share_link)

Data wrangling/filtering, test interface
- [data-wrangling](https://colab.research.google.com/drive/1DiWHgo5ugK_mEaAbCWNS_y2YKB3YgNQQ?usp=share_link)
- [other-data-sources](https://colab.research.google.com/drive/1Gv8vd51xug1tKX8Mkn5H3T9G6eWI4VIe?usp=share_link)
- [filtering-poems](https://colab.research.google.com/drive/1iFEAXZu58O22BLPva5xBJWEI8EFVMlU0?usp=share_link)
- [test-interface](https://colab.research.google.com/drive/1zQhl36ph35K-dO_mzTWrme5np804yo0I?usp=share_link)

Other
- [olipy](https://colab.research.google.com/drive/1LOyjlVh2zI96xjm3epkiqUiomPCL2xOl?usp=share_link)
- [original-combined](https://colab.research.google.com/drive/1h8qgWMNcY7NAn2J5_qxFZvuk34PCR1dA?usp=share_link)
- [speech-to-text](https://colab.research.google.com/drive/1pcfCcOmZfq_43QNeJIL574ik8cjIFmKJ?usp=share_link)

## All the Allison Parrish Things
