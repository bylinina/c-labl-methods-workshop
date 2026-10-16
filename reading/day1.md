# Reading list · Day 1 (Tuesday 20 October 2026)

*Language models for linguistic research* · C-LaBL Methods Workshop, UiT The Arctic University of Norway, Tromsø · [Lisa Bylinina](https://bylinina.github.io)

**Morning:** LLM anatomy and computation (tokens, probabilities, attention, decoding) and surprisal; practical session 1, *Language models up close*.

**Afternoon:** training and post-training (objective, loss, data and scale), evaluation, training data and generalisation; practical session 2, *Watch a model learn, then test it*.

This list has every source cited on the Day 1 slides and in the two Day 1 notebooks, grouped by topic. Start with the first section; the rest is there to look things up.

## Start here

- **Jurafsky & Martin.** *Speech and Language Processing* (3rd ed. draft), [Ch. 7: Transformers and Pretraining](https://web.stanford.edu/~jurafsky/slp3/7.pdf). The whole morning lecture in one chapter, from attention to perplexity. Then [Ch. 8](https://web.stanford.edu/~jurafsky/slp3/8.pdf) for post-training (the afternoon), [Ch. 9](https://web.stanford.edu/~jurafsky/slp3/9.pdf) for masked language models and [Ch. 10](https://web.stanford.edu/~jurafsky/slp3/10.pdf) for interpretability (Day 2).
- **Alammar.** [The Illustrated Transformer](https://jalammar.github.io/illustrated-transformer/) and [The Illustrated GPT-2](https://jalammar.github.io/illustrated-gpt2/). Visual walk-throughs of the same material; several slides are drawn after them.
- **Pimentel & Meister (2024).** How to compute the probability of a word. *EMNLP*. [link](https://aclanthology.org/2024.emnlp-main.1020/). Why the surprisal of a word is not simply the sum of its tokens' surprisals, and how to correct it.
- **Oh & Schuler (2023).** Why does surprisal from larger transformer-based language models provide a poorer fit to human reading times? *TACL* 11. [link](https://aclanthology.org/2023.tacl-1.20/). Bigger is not better for psycholinguistic measures.
- **Hu & Levy (2023).** Prompting is not a substitute for probability measurements in large language models. *EMNLP*. [link](https://aclanthology.org/2023.emnlp-main.306/). Reading off a model's probabilities and asking it for a judgment give different answers.
- **Kuribayashi, Oseki & Baldwin (2024).** Psychometric predictive power of large language models. *Findings of NAACL*. [link](https://aclanthology.org/2024.findings-naacl.129/). Instruction-tuned models predict reading times worse than base models: use base models for surprisal.
- **Warstadt, Parrish, Liu, Mohananey, Peng, Wang & Bowman (2020).** BLiMP: The benchmark of linguistic minimal pairs for English. *TACL* 8. [link](https://aclanthology.org/2020.tacl-1.25/). Minimal pairs as a test of what a model has learned.
- **Chang & Bergen (2022).** Word acquisition in neural language models. *TACL* 10. [link](https://aclanthology.org/2022.tacl-1.1/). Learning trajectories: the same test at every checkpoint, compared with children's age of acquisition.

## Morning · LLM anatomy and surprisal

### Language models and people

- Jones & Bergen (2026). Large language models pass a standard three-party Turing test. *PNAS* 123(21), e2524472123. [doi](https://doi.org/10.1073/pnas.2524472123)
- Hu, Mahowald, Lupyan, Ivanova & Levy (2024). Language models align with human judgments on key grammatical constructions. *PNAS* 121(36), e2400917121. [doi](https://doi.org/10.1073/pnas.2400917121)
- de Varda, Marelli & Amenta (2024). Cloze probability, predictability ratings, and computational estimates for 205 English sentences, aligned with existing EEG and reading time data. *Behavior Research Methods* 56. [doi](https://doi.org/10.3758/s13428-023-02261-8)
- Warstadt et al. (2023). Findings of the BabyLM Challenge: Sample-efficient pretraining on developmentally plausible corpora. *BabyLM Challenge at CoNLL*. [link](https://aclanthology.org/2023.conll-babylm.1/) · [babylm.github.io](https://babylm.github.io)
- What LLMs Can(not) Do: a living survey of what language models can and cannot do, and how it was tested. [what-llms-can-not-do.org](https://what-llms-can-not-do.org)

### Tokenization

- Sennrich, Haddow & Birch (2016). Neural machine translation of rare words with subword units. *ACL*. [link](https://aclanthology.org/P16-1162/) (byte pair encoding)
- Cognetta, Pinter et al. (2026). Tokenization: A survey for modern NLP. [link](https://www.alphaxiv.org/abs/2609.tokenization-survey-modern-nlp)
- Edman, Schmid & Fraser (2024). CUTE: Measuring LLMs' understanding of their tokens. *EMNLP*. [link](https://aclanthology.org/2024.emnlp-main.177/)
- Abagyan et al. (2026). One tokenizer to rule them all: Emergent language plasticity via multilingual tokenizers. *ACL*. [link](https://aclanthology.org/2026.acl-long.141/)
- Xue, Barua, Constant, Al-Rfou, Narang, Kale, Roberts & Raffel (2022). ByT5: Towards a token-free future with pre-trained byte-to-byte models. *TACL* 10. [link](https://aclanthology.org/2022.tacl-1.17/)

### Inside the model

- Vaswani, Shazeer, Parmar, Uszkoreit, Jones, Gomez, Kaiser & Polosukhin (2017). Attention is all you need. *NeurIPS*. [link](https://arxiv.org/abs/1706.03762)
- Geva, Schuster, Berant & Levy (2021). Transformer feed-forward layers are key-value memories. *EMNLP*. [link](https://aclanthology.org/2021.emnlp-main.446/)
- Meng, Bau, Andonian & Belinkov (2022). Locating and editing factual associations in GPT. *NeurIPS*. [link](https://arxiv.org/abs/2202.05262)
- Qwen Team (2024). Qwen2.5 technical report. *arXiv*. [link](https://arxiv.org/abs/2412.15115) (the model on the slides: Qwen2.5-0.5B)

### Surprisal: theory and evidence

- Hale (2001). A probabilistic Earley parser as a psycholinguistic model. *NAACL*. [link](https://aclanthology.org/N01-1021/)
- Levy (2008). Expectation-based syntactic comprehension. *Cognition* 106(3). [doi](https://doi.org/10.1016/j.cognition.2007.05.006)
- Smith & Levy (2013). The effect of word predictability on reading time is logarithmic. *Cognition* 128(3). [doi](https://doi.org/10.1016/j.cognition.2013.02.013)
- Shain, Meister, Pimentel, Cotterell & Levy (2024). Large-scale evidence for logarithmic effects of word predictability on reading time. *PNAS* 121(10). [doi](https://doi.org/10.1073/pnas.2307876121)
- Oh & Schuler (2023): see *Start here*.

### From tokens to words, and from probabilities to judgments

- Pimentel & Meister (2024): see *Start here*.
- Oh & Schuler (2024). Leading whitespaces of language models' subword vocabulary pose a confound for calculating word probabilities. *EMNLP*. [link](https://aclanthology.org/2024.emnlp-main.202/)
- Hu & Levy (2023): see *Start here*.

### Practical session 1 · *Language models up close*: data, models and tools

Structural priming (section 4c):

- Sinclair, Jumelet, Zuidema & Fernández (2022). Structural persistence in language models: Priming as a window into abstract language representations. *TACL* 10. [link](https://aclanthology.org/2022.tacl-1.60/)
- Jumelet, Zuidema & Sinclair (2024). Do language models exhibit human-like structural priming effects? *Findings of ACL*. [link](https://aclanthology.org/2024.findings-acl.877/)

Data (section 4f):

- de Varda, Marelli & Amenta (2024): see above. Data: [github.com/Andrea-de-Varda/prediction-resource](https://github.com/Andrea-de-Varda/prediction-resource)
- Frank, Monsalve, Thompson & Vigliocco (2013). Reading time data for evaluating broad-coverage models of English sentence processing. *Behavior Research Methods* 45. [doi](https://doi.org/10.3758/s13428-012-0313-y)
- Frank, Otten, Galli & Vigliocco (2015). The ERP response to the amount of information conveyed by words in sentences. *Brain and Language* 140. [doi](https://doi.org/10.1016/j.bandl.2014.10.006)
- Luke & Christianson (2018). The Provo Corpus: A large eye-tracking corpus with predictability norms. *Behavior Research Methods* 50. [doi](https://doi.org/10.3758/s13428-017-0908-4) · data: [osf.io/sjefs](https://osf.io/sjefs/)

Tools:

- minicons: Misra (2022). minicons: Enabling flexible behavioral and representational analyses of transformer language models. *arXiv*. [link](https://arxiv.org/abs/2203.13112) · [github.com/kanishkamisra/minicons](https://github.com/kanishkamisra/minicons)
- wordsprobability, by the authors of Pimentel & Meister (2024): [pypi.org/project/wordsprobability](https://pypi.org/project/wordsprobability/)
- pangoling (R), by Bruno Nicenboim: [docs.ropensci.org/pangoling](https://docs.ropensci.org/pangoling/)

Models:

- Qwen2.5: Qwen Team (2024), see above.
- GPT-2: Radford, Wu, Child, Luan, Amodei & Sutskever (2019). Language models are unsupervised multitask learners. *OpenAI report*. [pdf](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
- Pythia: Biderman et al. (2023). Pythia: A suite for analyzing large language models across training and scaling. *ICML*. [link](https://arxiv.org/abs/2304.01373)
- SmolLM2: Allal et al. (2025). SmolLM2: When smol goes big. Data-centric training of a small language model. *arXiv*. [link](https://arxiv.org/abs/2502.02737)
- EuroLLM: Martins et al. (2024). EuroLLM: Multilingual language models for Europe. *arXiv*. [link](https://arxiv.org/abs/2409.16235)

## Afternoon · Training, post-training, evaluation

### Model families and training objectives

- Vaswani et al. (2017): see above (the original encoder–decoder transformer).
- Devlin, Chang, Lee & Toutanova (2019). BERT: Pre-training of deep bidirectional transformers for language understanding. *NAACL*. [link](https://aclanthology.org/N19-1423/)
- Brown et al. (2020). Language models are few-shot learners. *NeurIPS*. [link](https://arxiv.org/abs/2005.14165) (GPT-3: fine-tuning vs in-context learning)
- Gradient descent, hands on: [playground.tensorflow.org](https://playground.tensorflow.org)

### Post-training

- Ouyang et al. (2022). Training language models to follow instructions with human feedback. *NeurIPS*. [link](https://arxiv.org/abs/2203.02155) (InstructGPT)
- Lambert, Castricato, von Werra & Havrilla (2022). Illustrating reinforcement learning from human feedback (RLHF). *Hugging Face blog*. [link](https://huggingface.co/blog/rlhf)
- Kuribayashi, Oseki & Baldwin (2024) and Hu & Levy (2023): see *Start here*.

### Evaluation and learning trajectories

- Warstadt et al. (2020), BLiMP: see *Start here*.
- Jumelet, Weissweiler & Bisazza (2026). MultiBLiMP 1.0: A massively multilingual benchmark of linguistic minimal pairs. *TACL*. [link](https://aclanthology.org/2026.tacl-1.10/) (preprint 2025)
- Misra (2022), minicons: see above (minimal-pair scoring).
- Chang & Bergen (2022): see *Start here*.
- Biderman et al. (2023), Pythia: see above (154 public checkpoints per model).
- Groeneveld et al. (2024). OLMo: Accelerating the science of language models. *ACL*. [link](https://arxiv.org/abs/2402.00838)

### Case study: adjective order (our work)

- Jumelet, Bylinina, Zuidema & Szymanik (under review). Black Big Boxes: Tracing adjective order preferences in large language models.
- Jumelet\*, Misra\*, Bylinina, Szymanik, Mahowald & Culbertson (in preparation). Higher-order distributional similarities drive nominal word order generalization in language models. (\*equal contribution)

### Training data: how much, and what is in it

- Kaplan et al. (2020). Scaling laws for neural language models. *arXiv*. [link](https://arxiv.org/abs/2001.08361)
- Hoffmann et al. (2022). Training compute-optimal large language models. *NeurIPS*. [link](https://arxiv.org/abs/2203.15556)
- Warstadt et al. (2023), BabyLM: see above (≤ 100M words).
- Gao et al. (2020). The Pile: An 800GB dataset of diverse text for language modeling. *arXiv*. [link](https://arxiv.org/abs/2101.00027) (Pythia's training data)
- GPT-3 training data by language: [github.com/openai/gpt-3](https://github.com/openai/gpt-3/tree/master/dataset_statistics)
- Touvron et al. (2023). Llama 2: Open foundation and fine-tuned chat models. *arXiv*. [link](https://arxiv.org/abs/2307.09288) (Table 10: languages)
- BigScience Workshop: Le Scao et al. (2022). BLOOM: A 176B-parameter open-access multilingual language model. *arXiv*. [link](https://arxiv.org/abs/2211.05100)
- Laurençon et al. (2022). The BigScience ROOTS corpus: A 1.6TB composite multilingual dataset. *NeurIPS Datasets and Benchmarks*. [link](https://arxiv.org/abs/2303.03915)

### Looking inside the training data

- Elazar et al. (2024). What's in my big data? *ICLR*. [link](https://arxiv.org/abs/2310.20707) · [github.com/allenai/wimbd](https://github.com/allenai/wimbd)
- Liu, Min, Zettlemoyer, Choi & Hajishirzi (2024). Infini-gram: Scaling unbounded n-gram language models to a trillion tokens. *COLM*. [link](https://arxiv.org/abs/2401.17377) · demo: [infini-gram.io/demo](https://infini-gram.io/demo)
- Liu et al. (2025). OLMoTrace: Tracing language model outputs back to trillions of training tokens. *ACL System Demonstrations*. [link](https://arxiv.org/abs/2504.07096) · try it: [playground.allenai.org](https://playground.allenai.org) ("Show OLMoTrace")
- Grosse et al. (2023). Studying large language model generalization with influence functions. *arXiv*. [link](https://arxiv.org/abs/2308.03296)
- Ruis et al. (2024). Procedural knowledge in pretraining drives reasoning in large language models. *arXiv*. [link](https://arxiv.org/abs/2411.12580)
- Hupkes et al. (2023). A taxonomy and review of generalization research in NLP. *Nature Machine Intelligence* 5. [link](https://arxiv.org/abs/2210.03050) · [genbench.org](https://genbench.org/)

### Practical session 2 · *Watch a model learn, then test it*: data, models and tools

- TinyStories: Eldan & Li (2023). TinyStories: How small can language models be and still speak coherent English? *arXiv*. [link](https://arxiv.org/abs/2305.07759) · data: [roneneldan/TinyStories](https://huggingface.co/datasets/roneneldan/TinyStories)
- Our trained tiny GPT, for runs without a GPU: [bylin/clabl-tiny-gpt](https://huggingface.co/bylin/clabl-tiny-gpt)
- Pythia-70m and its checkpoints: [EleutherAI/pythia-70m](https://huggingface.co/EleutherAI/pythia-70m)
- BLiMP data: [nyu-mll/blimp](https://huggingface.co/datasets/nyu-mll/blimp)
- Phrase counts in the Pile: infini-gram (Liu et al. 2024, above)
- Base vs instruction-tuned: [Qwen/Qwen2.5-0.5B](https://huggingface.co/Qwen/Qwen2.5-0.5B) and [Qwen/Qwen2.5-0.5B-Instruct](https://huggingface.co/Qwen/Qwen2.5-0.5B-Instruct)

## More to read

- Singh et al. (2025). The leaderboard illusion. *NeurIPS Datasets and Benchmarks*. [link](https://proceedings.neurips.cc/paper_files/paper/2025/file/70a93f260a51123b3c0e33ecd1b4de97-Paper-Datasets_and_Benchmarks_Track.pdf). An audit of Chatbot Arena: why a leaderboard rank is weak evidence of what a model can do.

## Citing these materials

If you use or adapt the workshop materials, please cite them as:

Bylinina, L. (2026). *Language models for linguistic research: Materials for the C-LaBL Methods Workshop*. UiT The Arctic University of Norway, Tromsø, 20 and 22 October 2026. https://github.com/bylinina/c-labl-methods-workshop

A BibTeX entry is in the [README](../README.md#how-to-cite). Please also cite the papers, datasets and tools you use from this list.
