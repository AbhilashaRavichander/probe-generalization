# On the Systematicity of Probing Contextualized Word Representations: The Case of Hypernymy in BERT

This repository contains the diagnostic tests described in the *SEM 2020 paper, [On the Systematicity of Probing Contextualized Word Representations: The Case of Hypernymy in BERT](https://www.aclweb.org/anthology/2020.starsem-1.10/). 
Some of the diagnostic tests have in turn been inspired by the diagnostic tests from [What BERT is not: Lessons from a new suite of psycholinguistic diagnostics for language models](https://www.mitpressjournals.org/doi/full/10.1162/tacl_a_00298), by Allyson Ettinger.

The diagnostic tests comprise of two datasets:
1) [LM Diagnostic](): We use items from the NEG-136 diagnostic from [Ettinger, 2020](https://www.mitpressjournals.org/doi/full/10.1162/tacl_a_00298), selecting the affirmative contexts.
Test items are drawn from Fischler et al. (1983).
2) [LM Diagnostic-Extended](): The LM-Diagnostic datset is expanded by collecting hyponyms from WordNet, corresponding to the nine hypernyms from Fischler et al. (1983).

For each of these datasets, you will find three tab-separated files:
* Singular: Files contain for each item the prompt in singular form, and the target completion.
* Plural: Files contain for each item the prompt in singular form, and the target completion.
* Contextual: Files contain for each item the hyponym to be replaced, the context featuring the hyponym, and the target hypernym.

In addition, we also supply the [paradigmatic]() diagnostic, with three training-validation-test splits to support cross-validation. Each sample consists of
 * a hyponym sentential context
 * a hyponym
 * a hypernym sentential context
 * a hypernym 
 * hypernymy label

This data is licensed under the [MIT License](https://github.com/AbhilashaRavichander/probe-generalization/blob/main/LICENSE).

* Allyson Ettinger. 2020. What BERT is not: Lessons from a new suite of psycholinguistic diagnostics for language models.
* Ira Fischler, Paul A Bloom, Donald G Childers, Salim E Roucos, and Nathan W Perry Jr. 1983. Brain potentials related to stages of sentence verification.

If you make use of our work in your research, we ask that you please cite our paper:

```  
@inproceedings{ravichander-etal-2020-systematicity,
    title = "On the Systematicity of Probing Contextualized Word Representations: The Case of Hypernymy in {BERT}",
    author = "Ravichander, Abhilasha  and
      Hovy, Eduard  and
      Suleman, Kaheer  and
      Trischler, Adam  and
      Cheung, Jackie Chi Kit",
    booktitle = "Proceedings of the Ninth Joint Conference on Lexical and Computational Semantics",
    month = dec,
    year = "2020",
    address = "Barcelona, Spain (Online)",
    publisher = "Association for Computational Linguistics",
    url = "https://www.aclweb.org/anthology/2020.starsem-1.10",
    pages = "88--102",
    abstract = "Contextualized word representations have become a driving force in NLP, motivating widespread interest in understanding their capabilities and the mechanisms by which they operate. Particularly intriguing is their ability to identify and encode conceptual abstractions. Past work has probed BERT representations for this competence, finding that BERT can correctly retrieve noun hypernyms in cloze tasks. In this work, we ask the question: \textit{do probing studies shed light on systematic knowledge in BERT representations?} As a case study, we examine hypernymy knowledge encoded in BERT representations. In particular, we demonstrate through a simple consistency probe that the ability to correctly retrieve hypernyms in cloze tasks, as used in prior work, does not correspond to systematic knowledge in BERT. Our main conclusion is cautionary: even if BERT demonstrates high probing accuracy for a particular competence, it does not necessarily follow that BERT {`}understands{'} a concept, and it cannot be expected to systematically generalize across applicable contexts.",
}
```
