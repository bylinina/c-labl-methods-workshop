# Language models for linguistic research

Materials for the C-LaBL Methods Workshop (Center for Language, Brain and Learning), UiT The Arctic University of Norway, Tromsø, 20 and 22 October 2026.

Taught by [Lisa Bylinina](https://bylinina.github.io) (Utrecht University).

## About the workshop

Language models are appearing more and more often in experimental and theoretical linguistics, as a source of estimates for psycholinguistic measures, and increasingly as objects of study in their own right. The first part of this workshop covers what these models actually are: how transformers are built, what happens during training and what the training objective optimises for, and how scale, architecture and training data shape the behaviour we observe. No background in machine learning is assumed. Alongside the large models that get most of the attention, we will look at small ones trained on developmentally plausible amounts of text, and at multilingual models — often the more useful instruments for linguistic research, and small enough to run and intervene on.

The second part turns to research practice. We will go through the measures that can be extracted from a model, how to obtain them and how they can be used, working through concrete cases from recent research with an emphasis on methods. We will view language models as learners with controllable linguistic and extralinguistic experience. This allows us to design targeted manipulations of the learning environment — remove a construction from the input, change word order, add or withhold visual grounding — and observe the consequences. This raises the question of observation: how to measure, in a faithful and interpretable way, what a model has learned about language as a result of training — by probing its internal representations, and by modelling its behaviour as a function of its experience. Examining those representations also gives us a way to quantify language similarity on different levels.

The practical sessions run in the browser, with no local installation; no prior experience with Python is required. Participants are welcome to bring their own questions and data.

## Schedule

*Preliminary — may change.*

**Tuesday 20 October** · Room U06, Nedre Lysthus

| Time | Session |
|---|---|
| 10:00–10:50 | **Lecture:** LLM anatomy and computation: tokens, probabilities, attention, decoding |
| 11:05–12:00 | **Practical:** First contact: text generation; surprisal (for real data) |
| 13:00–13:50 | **Lecture:** Training and post-training: training objective, loss, data and scale; evaluation |
| 14:05–15:00 | **Practical:** Train a tiny GPT; evaluate throughout training (learning trajectory) |

**Thursday 22 October** · Room 2.072, ILP building

| Time | Session |
|---|---|
| 10:00–10:50 | **Lecture:** LLMs vs humans: input, grounding, environment, multilinguality |
| 11:05–12:00 | **Practical:** Beyond surprisal: entropy, embeddings, similarity etc. |
| 13:00–13:50 | **Lecture:** Opening the black box: interpretability |
| 14:05–15:00 | **Practical:** Probing, attribution, representational similarity |

Coffee breaks 10:50–11:05 and 13:50–14:05; lunch 12:00–13:00. Both days are also streamed on Teams.

## Materials

| Session | Slides | Colab notebooks |
|---|---|---|
| Day 1 · morning | [Slides](https://docs.google.com/presentation/d/18EjiQ3Q95rrcwtfLRTsic0BgHEVNBNwecFZuTvbXR5E/edit?usp=sharing) | [Python](https://colab.research.google.com/drive/15pMrcr9aITF3wIolI6N0RMB9KcDd_TaU?usp=sharing) · [R](https://colab.research.google.com/drive/1rwPdTQMDvfN_4N8S4QHfduX4qLvSfG7P?usp=sharing) |
| Day 1 · afternoon | [Slides](https://docs.google.com/presentation/d/1IONS_Z85dJ4osFSgYW51RFecN9V9B0Av6ksrJq_zcfU/edit?usp=sharing) | [Python](https://colab.research.google.com/drive/1po-O-olZlpcCI72MNbh1R3la7GrX8DNR?usp=sharing) |
| Day 2 · morning | [Slides](https://docs.google.com/presentation/d/1Ov44Y3gPWT0BVax5FG5wc1vxbtd_rJnXqKh6OEOkIwA/edit?usp=sharing) | [Python](https://colab.research.google.com/drive/1GhoGQAQI_ktxzxZr_v9jKSJXXcTMkf-O?usp=sharing) |

To run a notebook, open it and choose **File → Save a copy in Drive**, then work in your copy.

## Bringing your own data

The notebooks can read your own stimuli from a simple CSV file. See [`data/README.md`](data/README.md) for the format.

## Repository structure

```
notebooks/   Colab notebooks (added as they are developed)
r/           R scripts for analysing the CSV files the notebooks produce
data/        small example datasets and the stimulus file format
slides/      slides (PDF)
```

<!-- TODO: license (e.g. CC BY 4.0 for slides and text, MIT for code) -->
