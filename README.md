# Summary

The ArmTDP Eastern Armenian UD treebank is based on the ՀայՇտեմ-ArmTDP-East dataset (2.0), created by the ArmTDP team led by Marat M. Yavrumyan at the Yerevan State University.

# Introduction

UD_Armenian is based on the ՀայՇտեմ-ArmTDP-East dataset (version 2.0), a mix of random sentences sampled from different sources and representing different genres and domains, released in several formats (local on-line newspaper and journal articles, contemporary fiction dated between 1976 and 2018). The treebank consists 1030 sentences (~2.3k tokens).

The annotation scheme was developed in according to the UD guidelines. The original data was manually annotated by the ArmTDP team. The tokenization and POS-tagging process was carried out through alternating steps of automatic scripting and manual revision in the YerevaNN research lab (led by Hrant H. Khachatrian). The treebank is so far the only manual verificated corpus of Eastern Armenian supplied with comprehensive morphological annotation and syntactic annotation in the form of a complete dependency tree provided for every sentence.

# Acknowledgments

This work became possible in part by a research grant from the Armenian National Science and Education Fund (ANSEF) based in New York, USA. We are deeply grateful to ANSEF, also to Lragir.am, 1in.am and Yavruhrat Publishing for letting us download and exploit their articles as text material under the terms of educational use.

The team behind the UD_Armenian: Marat M. Yavrumyan, Hrant H. Khachatrian, Anna S. Danielyan, Gor D. Arakelyan.

## References

* Marat M. Yavrumyan, Hrant H. Khachatrian, Anna S. Danielyan, Gor D. Arakelyan. “ArmTDP: Eastern Armenian Treebank and Dependency Parser.” XI International Conference on Armenian Linguistics, Abstracts. Yerevan, 2017

# Data split

The data was split into Train and Test.

## Format

UD_Armenian data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specifics:
* Sentence-level comments:
  * Document titles are present as `# doc_title = Ագռավները Նոյից առաջ`.
  * Document boundaries are present as `# newdoc id = fiction/news-xxxx`.
  * Sentence-level paragraph boundaries are present as `# newpar id = newdoc-xxxx`.
  * Sentence boundaries are present as `# sent_id = newdoc-newparxxxx`.
* XPOSTAG column is currently unused.
* No enhanced dependencies or empty nodes present in DEPS column.
* MISC column:
  * `SpaceAfter=No` markers are present.
* Document, paragraph, sentence, and token ids are 4-character base-32 numbers. They survive treebank updates.


# Changelog

* 2018-31-10 **v2.3**
  * expl added
  * Reconsidered Animacy
  * Improved advmod vs. obl distinction
  * Improved treatment of comparative complements
* 2018-30-03 **v2.2**
  * Initial release

```
=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.3
License: CC BY-SA 4.0
Documentation status: full
Includes text: yes
Genre: news fiction
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
