# Data

Small example files used in the notebooks. Larger datasets and trained models are hosted on the Hugging Face Hub; links are given in the notebooks.

## Using your own stimuli

The notebooks read a CSV file with one sentence per row:

| column | required | description |
|---|---|---|
| `item` | yes | item ID |
| `condition` | yes | condition label |
| `text` | yes | the full sentence, as presented to participants |
| `language` | no | ISO 639-3 code, e.g. `nob`, `sme`, `rus` |

For minimal pairs, give both members of a pair the same `item` ID and different `condition` labels.

Save the file as UTF-8. Words are split on whitespace, so punctuation attached to a word stays with that word, which matches how word regions are usually defined in reading studies.

<!-- TODO: add example_stimuli.csv -->
