# Summary

A Universal Dependencies treebank for Eastern Armenian developed for UD originally by the ArmTDP team led by Marat M. Yavrumyan at the Yerevan State University.

# Introduction

The UD_Armenian-ArmTDP treebank is based on the Eastern Armenian section of the Հայերենի ծառադարան dataset (ArmTDP V2.0), a broad-coverage corpus of general Modern Standard Armenian covering numerous genres.

The annotation scheme was developed in accordance with the UD guidelines. The original data was manually annotated by the ArmTDP team. The tokenization and POS-tagging process was carried out through alternating steps of glossary-based automatic scripting and manual revision. The treebank is so far the largest manually verified corpus of Eastern Armenian supplied with comprehensive morphological and syntactic annotation in the form of a complete dependency tree provided for every sentence.

# Acknowledgments

This work became possible through research grants from the Armenian National Science and Education Fund (ANSEF) based in New York, USA, and partially, from ISTC Foundation, Yerevan, Armenia.

The team behind the UD_Armenian-ArmTDP: Marat M. Yavrumyan, Hrant H. Khachatrian, Anna S. Danielyan, Gor D. Arakelyan, Martin S. Mirakyan, Liana G. Minasyan.

## References

* Marat M. Yavrumyan, Hrant H. Khachatrian, Anna S. Danielyan, Gor D. Arakelyan. “ArmTDP: Eastern Armenian Treebank and Dependency Parser.” XI International Conference on Armenian Linguistics, Abstracts. Yerevan, 2017.
* Marat M. Yavrumyan, “Universal Dependencies for Armenian.” International Conference on Digital Armenian, Abstracts. Inalco, Paris, October 3-5, 2019.
* Marat M. Yavrumyan, "Tokenization and Word Segmentation in the UD_Armenian-ArmTDP Treebank." Bulletin of Yerevan University B: Philology 10, 3(30): 52-65, 2019. (in Armenian)
* Marat M. Yavrumyan, Anna S. Danielyan, “Universal Dependencies and the Armenian Treebank.” Herald of the Social Sciences (2): 231-244, 2020. (in Armenian)
* Anna S. Danielyan, Marat M. Yavrumyan, "Verb Complements in the Eastern Armenian Treebanks UD_Armenian-ArmTDP and UD_Armenian-BSUT." Bulletin of Yerevan University B: Philology 15, 3(45): 139-152, 2024. (in Armenian)

# Data split

Data is split between train/dev/test linearly by hand at 80%/10%/10% to balance in genre and complexity. Some large documents are divided across datasets.

See [stats.xml](https://github.com/UniversalDependencies/UD_Armenian-ArmTDP/blob/dev/stats.xml) for detail.

## Format

UD_Armenian-ArmTDP data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specifics:
* Sentence-level comments:
  * Document titles are present as `# doc_title = Ագռավները Նոյից առաջ`.
  * Document boundaries are present as `# newdoc id = fiction/news-xxxx`.
  * Sentence-level paragraph boundaries are present as `# newpar id = newdoc-xxxx`.
  * Sentence boundaries are present as `# sent_id = newdoc-newparxxxx`.
* XPOSTAG column is currently unused.
* No enhanced dependencies or empty nodes present in DEPS column.
* MISC column:
  * `SpaceAfter=No` markers are present.
  * Form (`Translit`) and lemma (`LTranslit`) transliterations are present.
* Document, paragraph, sentence, and token ids are 4-character base-32 numbers. They survive treebank updates.


# Changelog

* 2023-15-11 **v2.13**
  * Fixed some validation errors.

* 2022-15-05 **v2.10**
  * Fixed some validation errors.

* 2021-15-05 **v2.8**
  * Improved treatment of `Deixis`.
  * Fixed some validation errors.

* 2019-15-11 **v2.5**
  * Fixed annotation errors and added new texts: 36K→52K.
  * `aux:ex` added.
  * `aux` for `AUX` _պիտի_ and _պետք է_.
  * MWE fixed.
  * reflexive pronouns/determiners improved.
  
* 2019-15-05 **v2.4**
  * Fixed annotation errors and added new texts: 23K→36K.
  * `dislocated` added.
  * Improved treatment of case-marking elements, range numbers.
  * Fixed some validation errors.
  * Added transliteration (ISO 9985:1996).
  * Improved consistency by extending annotation guidelines to rarer phenomena.

* 2018-31-10 **v2.3**
  * `expl` added.
  * Reconsidered `Animacy`.
  * Improved `advmod` vs. `obl` distinction.
  * Improved treatment of comparative complements.
  * Fixed various individual annotation errors and inconsistencies, added new texts: 12K→23K.

* 2018-30-03 **v2.2**
  * Initial release

```
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.2
License: CC BY-SA 4.0
Documentation status: full
Includes text: yes
Genre: blog fiction grammar-examples legal news nonfiction  
Lemmas: manual native
UPOS: manual native
XPOS: not available
Features: manual native
Relations: manual native
Contributors: Yavrumyan, Marat M.
Contributing: elsewhere
Contact: myavrum@ysu.am
===============================================================================
Documentation contributors: Yavrumyan, Marat M.; Danielyan, Anna S.
https://github.com/armtreebank
```
