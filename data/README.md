# Data

The notebooks load their data from the web, not from this folder:

- **Day 1 morning (4f):** the [de Varda, Marelli & Amenta (2024)](https://doi.org/10.3758/s13428-023-02261-8) file from [GitHub](https://github.com/Andrea-de-Varda/prediction-resource), or the eye-tracking file of the [Provo Corpus](https://osf.io/sjefs/) ([Luke & Christianson 2018](https://doi.org/10.3758/s13428-017-0908-4)) from OSF.
- **Day 1 afternoon:** [TinyStories](https://huggingface.co/datasets/roneneldan/TinyStories) to train the tiny GPT; our trained checkpoints ([bylin/clabl-tiny-gpt](https://huggingface.co/bylin/clabl-tiny-gpt)) if you have no GPU; [Pythia](https://huggingface.co/EleutherAI/pythia-70m) checkpoints; phrase counts in the Pile through [infini-gram](https://infini-gram.io/).
- **Day 2 morning:** TinyStories in VO and OV order, in four languages, with VO/OV test pairs ([bylin/clabl-tinystories-wordorder](https://huggingface.co/datasets/bylin/clabl-tinystories-wordorder)); the byte-level models trained on them, with all checkpoints and scores ([bylin/clabl-byte-gpt](https://huggingface.co/bylin/clabl-byte-gpt)); parses from [jennhu/tinystories_parsed](https://huggingface.co/datasets/jennhu/tinystories_parsed); [Grambank](https://grambank.clld.org/) 1.0.3.
- **Day 2 afternoon:** the de Varda et al. (2024) file again, with the full cloze answers; the 50 parallel stories of the morning (`nb_sample`); word lists from [NorthEuraLex](https://github.com/lexibank/northeuralex) 0.9 with semantic fields from [Concepticon](https://concepticon.clld.org/).

This folder has one small file, [`example_stimuli.csv`](example_stimuli.csv), in the format described below.

## Using your own stimuli

**Paste sentences** (Day 1 morning, 4e): one sentence per line. You get the surprisal of every word; the download cell saves the table as a CSV file.

**Load a CSV file** (Day 1 morning, 4f-1): from a link (GitHub, OSF, a shared Google Drive file), from a path on your Google Drive, or by uploading it. One row per target word:

| column | required | description |
|---|---|---|
| `sentence` | yes | the whole sentence (or passage) as participants saw it, repeated on every row that belongs to it |
| `word` | recommended | the target word; with or without its punctuation |
| `context_length` | recommended | how many words come before the target in `sentence` |
| any other columns | no | item, condition, your measures: they are kept, so the result merges straight back into your data |

4f-2 adds one surprisal column per model (in bits), named `surprisal: <model>`. Without `context_length`, the target is found by its first occurrence in the sentence, so add `context_length` if a word occurs twice. Without `word`, you get every word of every sentence instead, one row each.

The same cell also reads the Provo eye-tracking file as it comes from OSF and turns it into this format. For a private OSF file, save a personal access token in Colab Secrets as `OSF_TOKEN`.

**In R** (Day 1 morning, R notebook, 4f): the cell is written for the de Varda file, so it expects its column names (`sent_id`, `sentence`, `word`, `context_length`).

**Minimal pairs** (Day 1 afternoon, 3a′): type one grammatical and one ungrammatical sentence. The notebook does not read pairs from a file.

## Format notes

- Save the file as UTF-8 if you can (in Excel: *CSV UTF-8*). The Python notebook also reads older Windows and Mac encodings, and `;` or tab as the separator.
- Words are split at spaces, so punctuation stays attached to its word. This matches how word regions are usually defined in reading studies. `context_length` counts these space-separated words.
- Any language the model knows: the default models include multilingual ones (Qwen2.5, EuroLLM).
- Leave sentence-initial words out of your analysis: the model sees no context for them.
