# Reading list · Day 2 (Thursday 22 October 2026)

*Language models for linguistic research* · C-LaBL Methods Workshop, UiT The Arctic University of Norway, Tromsø · [Lisa Bylinina](https://bylinina.github.io)

**Morning:** models as learners: input, controlled rearing, multilinguality, grounding; practical session 3, *Controlled rearing with tiny models*.

**Afternoon:** opening the black box: entropy, attribution, probing and intervening, similarity across languages and the logit lens; practical session 4, the same methods hands-on.

This list has all sources cited on the Day 2 slides and in the two Day 2 notebooks, grouped by topic. Start with the first section; the rest is there to look things up. Studies with human participants that the slides cite are listed separately at the end of each half-day.

## Start here

- **Warstadt & Bowman (2022).** What artificial neural networks can tell us about human language acquisition. In *Algebraic Structures in Natural Language*. CRC Press. [link](https://arxiv.org/abs/2208.07998). What a model learner can show about learnability, and what it cannot.
- **Misra & Mahowald (2024).** Language models learn rare phenomena from less rare phenomena: The case of the missing AANNs. *EMNLP*. [link](https://aclanthology.org/2024.emnlp-main.53/). A controlled-rearing study from start to finish: remove a construction from the training data, retrain, test. Our adjective-order case study uses the same setup.
- **Kallini, Papadimitriou, Futrell, Mahowald & Potts (2024).** Mission: Impossible language models. *ACL*. [link](https://aclanthology.org/2024.acl-long.787/). Change the language instead of removing evidence: which languages does this learner learn easily?
- **Pimentel, Meister, Wilcox, Levy & Cotterell (2023).** On the effect of anticipation on reading times. *TACL* 11. [doi](https://doi.org/10.1162/tacl_a_00603). Next-word entropy as a predictor of reading times, beyond surprisal.
- **Belinkov (2022).** Probing classifiers: Promises, shortcomings, and advances. *Computational Linguistics* 48(1). [link](https://aclanthology.org/2022.cl-1.7/). What a probe shows, and what it does not.
- **Ferrando, Sarti, Bisazza & Costa-jussà (2024).** A primer on the inner workings of transformer-based language models. *arXiv*. [link](https://arxiv.org/abs/2405.00208). One survey for the whole afternoon: attribution, probing, the logit lens, activation patching.
- **Wendler, Veselovsky, Monea & West (2024).** Do Llamas work in English? On the latent language of multilingual transformers. *ACL*. [link](https://aclanthology.org/2024.acl-long.820/). The logit lens applied across languages.

## Morning · Models as learners

### How much input, and what a model learner can tell us

- Grattafiori et al. (2024). The Llama 3 herd of models. *arXiv*. [link](https://arxiv.org/abs/2407.21783) (15T training tokens)
- Yang et al. (2025). Qwen3 technical report. *arXiv*. [link](https://arxiv.org/abs/2505.09388) (36T training tokens)
- Warstadt & Bowman (2022): see *Start here*.
- Frank (2023). Bridging the data gap between children and large language models. *Trends in Cognitive Sciences* 27(11). [doi](https://doi.org/10.1016/j.tics.2023.08.007)
- Lan, Chemla & Katzir (2024). Large language models and the argument from the poverty of the stimulus. *Linguistic Inquiry*. [doi](https://doi.org/10.1162/ling_a_00533)

### BabyLM: training at human scale

- Warstadt et al. (2023). Findings of the BabyLM Challenge: Sample-efficient pretraining on developmentally plausible corpora. *BabyLM Challenge at CoNLL*. [link](https://aclanthology.org/2023.conll-babylm.1/)
- BabyLM 2026, including the new multilingual track: [babylm.github.io](https://babylm.github.io)
- Evaluation sets used in BabyLM: EWoK, Ivanova et al. (2024). Elements of World Knowledge (EWoK): A cognition-inspired framework for evaluating basic world knowledge in language models. *arXiv*. [link](https://arxiv.org/abs/2405.09605) · COMPS, Misra, Rayz & Ettinger (2023). COMPS: Conceptual minimal pair sentences for testing robust property knowledge and its inheritance in pre-trained language models. *EACL*. [link](https://aclanthology.org/2023.eacl-main.213/)

### Controlled rearing: remove the evidence

- Lee, Gujarathi & Wood (2021). Controlled-rearing studies of newborn chicks and deep neural networks. *NeurIPS workshop on Shared Visual Representations in Human and Machine Intelligence*. [link](https://arxiv.org/abs/2112.06106)
- Misra & Mahowald (2024): see *Start here*.
- Patil et al. (2024). Filtered corpus training (FiCT) shows that language models can generalize from indirect evidence. *TACL*. [link](https://arxiv.org/abs/2405.15750)
- Leong & Linzen (2026). Manipulating language models' training data to study syntactic constraint learning: The case of English passivization. *Journal of Memory and Language*. [link](https://arxiv.org/abs/2407.04593)
- Yao, Misra, Weissweiler & Mahowald (2025). Both direct and indirect evidence contribute to dative alternation preferences in language models. *COLM*. [link](https://arxiv.org/abs/2503.20850)
- Scivetti et al. (2025). Unpacking *let alone*: Human-scale models generalize to a rare construction in form but not meaning. *EMNLP*. [link](https://aclanthology.org/2025.emnlp-main.1399/)

### Controlled rearing: change the language

- Ravfogel, Goldberg & Linzen (2019). Studying the inductive biases of RNNs through synthetic variations of natural languages. *NAACL*. [link](https://aclanthology.org/N19-1356/)
- Kallini et al. (2024): see *Start here*.
- Yang, Aoyama, Yao & Wilcox (2025). Anything goes? A crosslinguistic study of (im)possible language learning in LMs. *ACL*. [link](https://aclanthology.org/2025.acl-long.1264/)
- Papadimitriou & Jurafsky (2020). Learning music helps you read: Using transfer to study linguistic structure in language models. *EMNLP*. [link](https://aclanthology.org/2020.emnlp-main.554/)

### Controlled rearing: control the language exposure

- Constantinescu, Pimentel, Cotterell & Warstadt (2025). Investigating critical period effects in language acquisition through neural language models. *TACL*. [link](https://aclanthology.org/2025.tacl-1.5/)
- Arnett, Chang, Michaelov & Bergen (2025). On the acquisition of shared grammatical representations in bilingual language models. *ACL*. [link](https://aclanthology.org/2025.acl-long.1010/)
- Sinclair, Jumelet, Zuidema & Fernández (2022). Structural persistence in language models: Priming as a window into abstract language representations. *TACL* 10. [link](https://aclanthology.org/2022.tacl-1.60/)
- Michaelov, Arnett, Chang & Bergen (2023). Structural priming demonstrates abstract grammatical representations in multilingual language models. *EMNLP*. [link](https://aclanthology.org/2023.emnlp-main.227/)
- Škrjanec, Winther, Demberg & Frank (2026). Is cross-lingual transfer in bilingual models human-like? A study with overlapping word forms in Dutch and English. *CMCL*. [link](https://aclanthology.org/2026.cmcl-1.10/)
- Pires, Schlinger & Garrette (2019). How multilingual is Multilingual BERT? *ACL*. [link](https://aclanthology.org/P19-1493/)
- Deshpande, Talukdar & Narasimhan (2022). When is BERT multilingual? Isolating crucial ingredients for cross-lingual transfer. *NAACL*. [link](https://arxiv.org/abs/2110.14782)

### Case study: what transfers to German case (our work)

- Kiziloglu, Di Marco, Bylinina & Edman (in progress). Disentangling structural and lexical information in cross-lingual transfer.
- Training data: NLLB Team (2022). No language left behind: Scaling human-centered machine translation. *arXiv*. [link](https://arxiv.org/abs/2207.04672). Test pairs from [UD German-GSD](https://universaldependencies.org/treebanks/de_gsd/index.html).

### Case study: adjective order without direct evidence (our work)

- Jumelet\*, Misra\*, Bylinina, Szymanik, Mahowald & Culbertson (in preparation). Higher-order distributional similarities drive nominal word order generalization in language models. (\*equal contribution)
- Scott (2002). Stacked adjectival modification and the structure of nominal phrases. In G. Cinque (ed.), *Functional Structure in DP and IP*. Oxford University Press.
- Cinque (2005). Deriving Greenberg's Universal 20 and its exceptions. *Linguistic Inquiry* 36(3).
- Hahn, Degen, Goodman, Jurafsky & Futrell (2018). An information-theoretic explanation of adjective ordering preferences. *Proceedings of CogSci*.
- Futrell, Dyer & Scontras (2020). What determines the order of adjectives in English? Comparing efficiency-based theories using dependency treebanks. *ACL*. [link](https://aclanthology.org/2020.acl-main.181/)
- Dagan, Pereira & Lee (1994). Similarity-based estimation of word cooccurrence probabilities. *ACL*. [link](https://aclanthology.org/P94-1038/)
- Schütze (1998). Automatic word sense discrimination. *Computational Linguistics* 24(1). [link](https://aclanthology.org/J98-1004/)

### Grounding

- Bylinina (2026). Augustinian BabyLM: What ostensive definition can and cannot teach a small language model. *arXiv*. [link](https://arxiv.org/abs/2609.11870)
- He, Liu, Gao & Chen (2021). DeBERTa: Decoding-enhanced BERT with disentangled attention. *ICLR*. [link](https://arxiv.org/abs/2006.03654)
- Lin, Rust, Villar Corrales et al. (2026). EgoBabyVLM: Benchmarking cross-modal learning from naturalistic egocentric video data. *arXiv*. [link](https://arxiv.org/abs/2605.19130) (the VP-Swap test)
- Augustine, *Confessions* I.8, as quoted in Wittgenstein (1953), *Philosophical Investigations* §1.

### Practical session 3 · *Controlled rearing with tiny models*: data, models and tools

- Our dataset and models: [bylin/clabl-tinystories-wordorder](https://huggingface.co/datasets/bylin/clabl-tinystories-wordorder) · [bylin/clabl-byte-gpt](https://huggingface.co/bylin/clabl-byte-gpt)
- Eldan & Li (2023). TinyStories: How small can language models be and still speak coherent English? *arXiv*. [link](https://arxiv.org/abs/2305.07759)
- Parses: [jennhu/tinystories_parsed](https://huggingface.co/datasets/jennhu/tinystories_parsed), made with the Berkeley Neural Parser: Kitaev & Klein (2018). Constituency parsing with a self-attentive encoder. *ACL*. [link](https://aclanthology.org/P18-1249/)
- Translations: Japanese [shibatch/TinyStories-JA](https://huggingface.co/datasets/shibatch/TinyStories-JA); Arabic [sboughorbel/tinystories_dataset_arabic](https://huggingface.co/datasets/sboughorbel/tinystories_dataset_arabic); Norwegian by OPUS-MT ([Helsinki-NLP/opus-mt-tc-big-en-gmq](https://huggingface.co/Helsinki-NLP/opus-mt-tc-big-en-gmq)): Tiedemann & Thottingal (2020). OPUS-MT: Building open translation services for the World. *EAMT*. [link](https://aclanthology.org/2020.eamt-1.61/)
- Hudson Kam & Newport (2005). Regularizing unpredictable variation: The roles of adult and child learners in language formation and change. *Language Learning and Development* 1(2). [doi](https://doi.org/10.1207/s15473341lld0102_3) (regularising vs matching frequencies, section 2)
- Grambank: Skirgård et al. (2023). Grambank reveals the importance of genealogical constraints on linguistic diversity and highlights the impact of language loss. *Science Advances* 9(16). [doi](https://doi.org/10.1126/sciadv.adg6175) · [grambank.clld.org](https://grambank.clld.org/)
- Littell, Mortensen, Lin, Kairis, Turner & Levin (2017). URIEL and lang2vec: Representing languages as typological, geographical, and phylogenetic vectors. *EACL*. [link](https://aclanthology.org/E17-2002/)
- Petrov, La Malfa, Torr & Bibi (2023). Language model tokenizers introduce unfairness between languages. *NeurIPS*. [link](https://arxiv.org/abs/2305.15425)
- Tokenizers compared: GPT-2, Radford et al. (2019), [pdf](https://cdn.openai.com/better-language-models/language_models_are_unsupervised_multitask_learners.pdf); Qwen2.5, Qwen Team (2024), [link](https://arxiv.org/abs/2412.15115); XLM-R, Conneau et al. (2020). Unsupervised cross-lingual representation learning at scale. *ACL*, [link](https://aclanthology.org/2020.acl-main.747/); bytes, Xue et al. (2022). ByT5. *TACL*, [link](https://aclanthology.org/2022.tacl-1.17/)
- Warstadt et al. (2020). BLiMP: The benchmark of linguistic minimal pairs for English. *TACL* 8. [link](https://aclanthology.org/2020.tacl-1.25/)

### Studies with people (and chickens) cited this morning

- Gilkerson et al. (2017). Mapping the early language environment using all-day recordings and automated analysis. *American Journal of Speech-Language Pathology* 26(2). [doi](https://doi.org/10.1044/2016_AJSLP-15-0169) (≈ 100M words by age 13, via BabyLM)
- Wood (2013). Newborn chickens generate invariant object representations at the onset of visual object experience. *PNAS* 110(34).
- Bultena, Dijkstra & van Hell (2014). Cognate effects in sentence context depend on word class, L2 proficiency, and task. *Quarterly Journal of Experimental Psychology* 67(6).
- Huisman (2025), on false friends in bilingual reading, as cited in Škrjanec et al. (2026).
- Bar-Sever, Lee, Scontras & Pearl (2018). Little lexical learners: Quantitatively assessing the development of adjective ordering preferences. *Proceedings of BUCLD 42*.
- Martin, Holtz, Abels, Adger & Culbertson (2020). Experimental evidence for the influence of structure and meaning on linear order in the noun phrase. *Glossa* 5(1).
- Martin, Adger, Abels, Kanampiu & Culbertson (2024). A universal cognitive bias in word order: Evidence from speakers whose language goes against it. *Psychological Science* 35(3).
- Culbertson, Schouwstra & Kirby (2020). From the world to word order: Deriving biases in noun phrase order from statistical properties of the world. *Language* 96(3).

## Afternoon · Opening the black box

### Entropy

- Hale (2003). The information conveyed by words in sentences. *Journal of Psycholinguistic Research* 32(2). [doi](https://doi.org/10.1023/A:1022492123056)
- Hale (2006). Uncertainty about the rest of the sentence. *Cognitive Science* 30(4). [doi](https://doi.org/10.1207/s15516709cog0000_64)
- Frank (2013). Uncertainty reduction as a measure of cognitive load in sentence comprehension. *Topics in Cognitive Science* 5(3). [doi](https://doi.org/10.1111/tops.12025)
- Linzen & Jaeger (2016). Uncertainty and expectation in sentence processing: Evidence from subcategorization distributions. *Cognitive Science* 40(6). [doi](https://doi.org/10.1111/cogs.12274)
- Pimentel et al. (2023): see *Start here*.
- Frank, Otten, Galli & Vigliocco (2015). The ERP response to the amount of information conveyed by words in sentences. *Brain and Language* 140. [doi](https://doi.org/10.1016/j.bandl.2014.10.006)
- Jacobs, Grobol & Tsang (2024). Large-scale cloze evaluation reveals that token prediction tasks are neither lexically nor semantically aligned. *arXiv*. [link](https://arxiv.org/abs/2410.12057)
- Pimentel & Meister (2024). How to compute the probability of a word. *EMNLP*. [link](https://aclanthology.org/2024.emnlp-main.1020/) (word-level measures from tokens)

### Attribution

- Sundararajan, Taly & Yan (2017). Axiomatic attribution for deep networks. *ICML*. [link](https://arxiv.org/abs/1703.01365) (integrated gradients)
- Li, Monroe & Jurafsky (2016). Understanding neural networks through representation erasure. *arXiv*. [link](https://arxiv.org/abs/1612.08220) (removing words to measure their effect: our "word removal")
- Jumelet, Bylinina, Zuidema & Szymanik (under review). Black Big Boxes: Tracing adjective order preferences in large language models. (case study: context cues for adjective order)
- DeYoung, Jain, Rajani, Lehman, Xiong, Socher & Wallace (2020). ERASER: A benchmark to evaluate rationalized NLP models. *ACL*. [link](https://aclanthology.org/2020.acl-main.408/)
- Krishna et al. (2022). The disagreement problem in explainable machine learning: A practitioner's perspective. *arXiv*. [link](https://arxiv.org/abs/2202.01602)
- Neely, Schouten, Bleeker & Lucic (2022). A song of (dis)agreement: Evaluating the evaluation of explainable artificial intelligence in natural language processing. *HHAI*. [link](https://arxiv.org/abs/2205.04559)
- Jacovi & Goldberg (2020). Towards faithfully interpretable NLP systems: How should we define and evaluate faithfulness? *ACL*. [link](https://aclanthology.org/2020.acl-main.386/)

### Probing and intervening

- Alain & Bengio (2016). Understanding intermediate layers using linear classifier probes. *arXiv*. [link](https://arxiv.org/abs/1610.01644)
- Tenney, Das & Pavlick (2019). BERT rediscovers the classical NLP pipeline. *ACL*. [link](https://aclanthology.org/P19-1452/)
- Belinkov (2022): see *Start here*.
- Hewitt & Liang (2019). Designing and interpreting probes with control tasks. *EMNLP*. [link](https://aclanthology.org/D19-1275/)
- Elazar, Ravfogel, Jacovi & Goldberg (2021). Amnesic probing: Behavioral explanation with amnesic counterfactuals. *TACL* 9. [link](https://arxiv.org/abs/2006.00995)
- Lasri, Pimentel, Lenci, Poibeau & Cotterell (2022). Probing for the usage of grammatical number. *ACL*. [link](https://aclanthology.org/2022.acl-long.603/)
- Adjective classes in the practical: Dixon (1982). *Where Have All the Adjectives Gone? and Other Essays in Semantics and Syntax*. Mouton · Scontras, Degen & Goodman (2017). Subjectivity predicts adjective ordering preferences. *Open Mind* 1(1). [doi](https://doi.org/10.1162/OPMI_a_00005)

### The logit lens

- nostalgebraist (2020). Interpreting GPT: The logit lens. *LessWrong*. [link](https://www.lesswrong.com/posts/AcKRB8wDpdaN6v6ru/interpreting-gpt-the-logit-lens)
- Wendler et al. (2024): see *Start here*.
- Belrose, Furman, Smith, Halawi, Ostrovsky, McKinney, Biderman & Steinhardt (2023). Eliciting latent predictions from transformers with the tuned lens. *arXiv*. [link](https://arxiv.org/abs/2303.08112)

### Comparing languages inside one model

Design 1, one vector per language:

- Rama, Beinborn & Eger (2020). Probing multilingual BERT for genetic and typological signals. *COLING*. [link](https://aclanthology.org/2020.coling-main.105/)
- Lin, Hu, Zhang, Martins & Schütze (2024). mPLM-Sim: Better cross-lingual similarity and transfer in multilingual pretrained language models. *Findings of EACL*. [link](https://aclanthology.org/2024.findings-eacl.20/)
- Östling & Kurfalı (2023). Language embeddings sometimes contain typological generalizations. *Computational Linguistics* 49(4). [link](https://aclanthology.org/2023.cl-4.6/)
- Chang, Tu & Bergen (2022). The geometry of multilingual language model representations. *EMNLP*. [link](https://aclanthology.org/2022.emnlp-main.9/) (each language around its own mean, and a shared space once the means are removed: practical 4a–4b)
- To compare with: Skirgård et al. (2023), Grambank, and Littell et al. (2017), URIEL: see the morning.

Design 2, how each language arranges the same concepts:

- Kriegeskorte, Mur & Bandettini (2008). Representational similarity analysis: Connecting the branches of systems neuroscience. *Frontiers in Systems Neuroscience* 2. [doi](https://doi.org/10.3389/neuro.06.004.2008)
- Thompson, Roberts & Lupyan (2020). Cultural influences on word meanings revealed through large-scale semantic alignment. *Nature Human Behaviour* 4. [doi](https://doi.org/10.1038/s41562-020-0924-8)
- Beinborn & Choenni (2020). Semantic drift in multilingual representations. *Computational Linguistics* 46(3). [link](https://aclanthology.org/2020.cl-3.2/)
- Peng & Søgaard (2024). Concept space alignment in multilingual LLMs. *EMNLP*. [link](https://aclanthology.org/2024.emnlp-main.315/)

Design 3, one grammatical category:

- Papadimitriou, Chi, Futrell & Mahowald (2021). Deep subjecthood: Higher-order grammatical features in multilingual BERT. *EACL*. [link](https://aclanthology.org/2021.eacl-main.215/)
- Brinkmann, Wendler, Bartelt & Mueller (2025). Large language models share representations of latent grammatical concepts across typologically diverse languages. *NAACL*. [link](https://aclanthology.org/2025.naacl-long.312/)
- Gidi, Almudévar, Park, Saphra & Marxer (2026). Shared circuits for shared grammar: Tracing subject-verb agreement across languages. *COLM*. [link](https://arxiv.org/abs/2608.18545)

### Shared circuits: activation patching

- Vig, Gehrmann, Belinkov, Qian, Nevo, Singer & Shieber (2020). Investigating gender bias in language models using causal mediation analysis. *NeurIPS*. [link](https://arxiv.org/abs/2004.12265)
- Meng, Bau, Andonian & Belinkov (2022). Locating and editing factual associations in GPT. *NeurIPS*. [link](https://arxiv.org/abs/2202.05262)
- Heimersheim & Nanda (2024). How to use and interpret activation patching. *arXiv*. [link](https://arxiv.org/abs/2404.15255)
- Gidi et al. (2026): see above.

### Practical session 4 · *Opening the black box*: data, models and tools

- nnsight: Fiotto-Kaufman et al. (2025). NNsight and NDIF: Democratizing access to open-weight foundation model internals. *ICLR*. [link](https://arxiv.org/abs/2407.14561) · tutorials (activation patching, attribution patching, logit lens and more): [nnsight.net](https://nnsight.net)
- Model: [Qwen/Qwen2.5-0.5B](https://huggingface.co/Qwen/Qwen2.5-0.5B); Qwen Team (2024). Qwen2.5 technical report. *arXiv*. [link](https://arxiv.org/abs/2412.15115)
- Data for entropy: de Varda, Marelli & Amenta (2024). Cloze probability, predictability ratings, and computational estimates for 205 English sentences, aligned with existing EEG and reading time data. *Behavior Research Methods* 56. [doi](https://doi.org/10.3758/s13428-023-02261-8) · [github.com/Andrea-de-Varda/prediction-resource](https://github.com/Andrea-de-Varda/prediction-resource), with the reading times of Frank, Monsalve, Thompson & Vigliocco (2013), *Behavior Research Methods* 45, [doi](https://doi.org/10.3758/s13428-012-0313-y), and the EEG of Frank et al. (2015), above
- Data for similarity: the 50 parallel stories of this morning (`nb_sample` in [bylin/clabl-tinystories-wordorder](https://huggingface.co/datasets/bylin/clabl-tinystories-wordorder))
- Word lists for design 2: Dellert, Daneyko, Münch, Ladygina, Buch, Clarius, Grigorjew, Balabel, Boga, Baysarova, Mühlenbernd, Wahle & Jäger (2020). NorthEuraLex: A wide-coverage lexical database of Northern Eurasia. *Language Resources and Evaluation* 54. [doi](https://doi.org/10.1007/s10579-019-09480-6) · version 0.9 in CLDF: [github.com/lexibank/northeuralex](https://github.com/lexibank/northeuralex)
- Semantic fields: List, Cysouw & Forkel (2016). Concepticon: A resource for the linking of concept lists. *LREC*. [link](https://aclanthology.org/L16-1379/) · [concepticon.clld.org](https://concepticon.clld.org/)

### Studies with people cited this afternoon

- Federmeier, Wlotko, De Ochoa-Dewald & Kutas (2007). Multiple effects of sentential constraint on word processing. *Brain Research* 1146.
- Stone, Nicenboim, Vasishth & Rösler (2023). Understanding the effects of constraint and predictability in ERP. *Neurobiology of Language* 4(2). [link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC10205153/)
- Ankener, Sekicki & Staudte (2018). The influence of visual uncertainty on word surprisal and processing effort. *Frontiers in Psychology* 9, 2387. [doi](https://doi.org/10.3389/fpsyg.2018.02387)
- Allopenna, Magnuson & Tanenhaus (1998). Tracking the time course of spoken word recognition using eye movements: Evidence for continuous mapping models. *Journal of Memory and Language* 38(4). [doi](https://doi.org/10.1006/jmla.1997.2558)

## More to read

- Giulianelli, Harding, Mohnert, Hupkes & Zuidema (2018). Under the hood: Using diagnostic classifiers to investigate and improve how language models track agreement information. *BlackboxNLP*. [link](https://aclanthology.org/W18-5426/). An early probe-then-intervene study, on subject–verb agreement.
- Jurafsky & Martin. *Speech and Language Processing* (3rd ed. draft), [Ch. 10](https://web.stanford.edu/~jurafsky/slp3/10.pdf), on interpretability.
