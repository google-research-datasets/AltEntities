# Alternative Entities (AltEntities) dataset: Resolving Indirect Referring Expressions for Entity Selection

## COPYRIGHT NOTICE

This is the work of Mohammad Javad Hosseini, Filip Radlinski, Silvia Pareti, and Annie Louis from Google LLC, made available under the CC-BY SA 3.0 License. A full copy of the license can be found at https://creativecommons.org/licenses/by-sa/3.0/

## The Dataset

AltEntities is a dataset of English-language **alternative questions with their answers**. In these questions, a user is presented with a choice of two entities. The user answer intends to **select one entity from the pair by referring to it in an indirect way, i.e., without referring to its name or position**. For example:

Question: “Do you mean 'Nemesis (Davis novel)' or 'Nemesis (Christie novel)'?”

Answer: “Not the more modern one, the one closer to BC than 2021.”

The entity names are sampled from Wikipedia. The alternative questions are generated using a simple template. The referring expressions are provided by human raters. The dataset contains **6,247 alternative questions in three domains--books, songs (music), and recipes--and 42,529 referring expressions**. The dataset is suitable for building machine learning systems to resolve indirect referring expressions for entity selection.

A full description of the data collection methodology, analyses, human rater instructions, and the performance of the SOTA LLMs can be found in the associated research [paper](https://arxiv.org/abs/2212.10933).

Further details about the data are provided in [Data-Description.pdf](Data-Description.pdf)

## Explanation of the Data Files

The data is released in a json format with each example (json object) representing one alternative question along with its referring expressions. Each example has the following fields:

* domain: The domain of the example: “BOOKS”, “RECIPES”, or “SONGS”.
* question: An alternative question providing two choices.
* target: The URL of the target entity.
* target_index: The index (position) of the target entity in the question (0 or 1).
* sampling_method: The sampling method used to sample the entities in the question (e.g., SAME_NAME, SIMILAR_NAME, or SIMILAR_DESCRIPTION).
* description_section: The title of the Wikipedia section shown to crowd workers. If empty, indicates the first section. This does not apply to the "SONGS" domain.
* choices: Information about the two choices. See below fields for more information.
* choice/name: The name of the choice.
* choice/wikipedia_url: The Wikipedia URL of the choice.
* choice/description: The choice description shown to crowd workers.
* choice/infobox: Textual representation of the choice’s Wikipedia infobox.
* choice/unshown_background: The choice/infobox above concatenated with Wikipedia sections that were *not* shown to annotators.
* expressions: Referring expressions written by crowd workers to select the target entity.

The ``data'' directory contains the full set of examples (all.json). For each domain (books, recipes, and songs), a subdirectory contains all its examples which are split into train.json, dev.json, and test.json. In addition, the mixed subdirectory contains the mix of examples in the three domains.

## Citation
The dataset can be cited as:

```
@article{hosseini2022resolving,
  title={Resolving Indirect Referring Expressions for Entity Selection},
  author={Hosseini, Mohammad Javad and Radlinski, Filip and Pareti, Silvia and Louis, Annie},
  journal={arXiv preprint arXiv:2212.10933},
  year={2022}
}
```
