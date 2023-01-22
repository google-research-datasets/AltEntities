# Alternative Entities (AltEntities) dataset: Resolving Indirect Referring Expressions for Entity Selection

## COPYRIGHT NOTICE

This is the work of Mohammad Javad Hosseini, Filip Radlinski, Silvia Pareti, and Annie Louis from Google LLC, made available under the CC-BY SA 3.0 License. A full copy of the license can be found at https://creativecommons.org/licenses/by-sa/3.0/

## The Dataset

AltEntities is a dataset of English-language **alternative questions with their answers**. In these questions, a user is presented with a choice of two entities. The user answer intends to **select one entity from the pair by referring to it in an indirect way, i.e., without referring to its name or position**. For example:

Question: “Do you mean 'Nemesis (Davis novel)' or 'Nemesis (Christie novel)'?”

Answer: “Not the more modern one, the one closer to BC than 2021.”

The entity names are sampled from Wikipedia. The alternative questions are generated using a simple template. The referring expressions are provided by human raters. The dataset contains **6,247 alternative questions in three domains (books, music, and recipes) and 42,529 referring expressions**. The dataset is suitable for building machine learning systems to resolve indirect referring expressions for entity selection.

A full description of the data collection methodology, analyses, human rater instructions, and the performance of the SOTA LLMs can be found in the associated research [paper](https://arxiv.org/abs/2212.10933), which can be cited as:

```
@article{hosseini2022resolving,
  title={Resolving Indirect Referring Expressions for Entity Selection},
  author={Hosseini, Mohammad Javad and Radlinski, Filip and Pareti, Silvia and Louis, Annie},
  journal={arXiv preprint arXiv:2212.10933},
  year={2022}
}
```

Further details about the data are provided in [Data-Description.pdf](Data-Description.pdf)


