# Summary

Universal Dependencies corpus for Eastern Armenian, developed for UD version 2.1 originally,  
by the ArmTDP team led by Marat M. Yavrumyan at the Yerevan State University.


# Introduction

UD_Armenian is based on the ՀայՇտեմ-ArmTDP-East dataset (version 1.0), a mix of random sentences sampled from different sources and representing different genres and domains, released in several formats (local on-line newspaper and journal articles, contemporary fiction dated between 1980 and 2018).

The annotation scheme was developed in according to the UD guidelines. All data were checked manually. The tokenization and POS-tagging process was carried out through alternating steps of automatic scripting and manual revision, and finally with some out-of-domain parsing modules in the YerevaNN research lab. Parsing results also underwent a manual revision.

The treebank is so far the only human-corrected corpus of Eastern Armenian supplied with comprehensive morphological annotation and syntactic annotation in the form of a complete dependency tree provided for every sentence.

## References

* Marat M. Yavrumyan, Hrant H. Khachatrian, Anna S. Danielyan, Gor D. Arakelyan. “ArmTDP: Eastern Armenian Treebank and Dependency Parser.” XI International Conference on Armenian Linguistics, Abstracts. Yerevan, 2017

# Acknowledgments

This work became possible in part by a research grant from the Armenian National Science and Education Fund (ANSEF) based in New York, USA. We are deeply grateful to ANSEF, also to Lragir.am, 1in.am and Yavruhrat Publishing for letting us download and exploit their articles as text material under the terms of educational use.

The team behind the UD_Armenian: Marat M. Yavrumyan, Hrant H. Khachatrian, Anna S. Danielyan, Gor D. Arakelyan.

# Basic stats

| set   | sentences | ~tokens |
| ----- |----------:| -------:|
| train |     ---   |    --K  |
| test  |     ---   |    --K  |
| TOTAL |    ----   |   ---K  |

# Data split

Data is split between train and test. There are no larger treebanks of Eastern Armenian. We have kept almost everything as test data but set aside a small sample as “train”. This includes also the translated and annotated 20 examples from the Cairo Cicling Corpus (CCC).

# Format

UD Armenian data conforms to [CoNLL-U](http://universaldependencies.org/format.html) format with the following specifics:
* Sentence-level comments:
  * Document boundaries are present as `# newdoc id = xxxx`.
  * Sentence-level paragraph boundaries are present as `# newpar id = xxxx`.
  * Document titles are present as `# doc_title = Ագռավները.fiction`.
* XPOSTAG column is currently unused.
* No enhanced dependencies or empty nodes present in DEPS column.
* MISC column:
  * `SpaceAfter=No` markers are present.
* Document, paragraph, sentence, and token ids are 4-character base-32 numbers. They survive treebank updates.

## Contact

[myavrum@ysu.am](mailto:myavrum@ysu.am)

# Changelog

* 2018-30-03 **v2.1**
  * First release in UD containing ---K tokens of news examples and fiction.


=== Machine-readable metadata (DO NOT REMOVE!) ================================
Data available since: UD v2.1
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
Data contributors: Yavrumyan, Marat M.; Khachatrian, Hrant H.; Danielyan, Anna S.; Arakelyan, Gor D.
Documentation contributors: Yavrumyan, Marat M.; Danielyan, Anna S.
https://github.com/armtreebank
