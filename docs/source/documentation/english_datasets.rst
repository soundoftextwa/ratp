English Datasets
=================

* sc = sentence count.
* tc = token count.

CRAFT
-----

* `Colorado Richly Annotated Full Text Corpus <http://bionlp-corpora.sourceforge.net/CRAFT/>`_
  * Biomedical journal articles (sc = 19,792, tc = 554,539)

BOLT
----

* `Broad Operational Language Translation <https://www.ldc.upenn.edu/collaborations/current-projects/bolt>`_
  * Conversational telephone speech (sc = 11,552, tc = 160,319)
  * Discussion forum (sc = 17,382, tc = 396,584)
  * SMS message (sc = 22,883, tc = 260,431)

EWT
---

* `English Web Treebank <https://catalog.ldc.upenn.edu/LDC2012T13>`_
  * Question-answer (sc = 3,089, tc = 50,404)
  * Email (sc = 3,436, tc = 51,504)
  * Newsgroup (sc = 2,122, tc = 41,891)
  * Review (sc = 2,951, tc = 45,864)
  * Weblog (sc = 1,886, tc = 42,988)

OntoNotes
---------

* `OntoNotes 5.0 <https://catalog.ldc.upenn.edu/LDC2013T19>`_
  * Broadcasting conversation (sc = 14,648, tc = 239,940)
  * Broadcasting news (sc = 11,867, tc = 240,241)
  * News magazine (sc = 7,960, tc = 194,926)
  * Newswire (sc = 40,491, tc = 1,038,190)
  * Pivot text (sc = 24,386, tc = 339,013)
  * Telephone conversation (sc = 10,955, tc = 112,847)
  * Weblog (sc = 11,800, tc = 262,049)

QuestionBank
------------

* `QuestionBank Revised <https://nlp.stanford.edu/data/QuestionBank-Stanford.shtml>`_
  * Question (sc = 3,989, tc = 38,100)

MiPACQ
------

* `Multi-source Integrated Platform for Answering Clinical Questions <http://clear.colorado.edu/compsem/index.php?page=endendsystems&sub=mipacq>`_
  * Clinical note (sc = 9,706, tc = 132,235)
  * Clinical question (sc = 1,980, tc = 37,178)
  * Medpedia (sc = 2,921, tc = 49,252)
  * Pathological note (sc = 1,182, tc = 22,088)

SHARP
-----

* `Strategic Health IT Advanced Research Projects <http://informatics.mayo.edu/sharp/index.php/Main_Page>`_
  * Clinical note (sc = 7,841, tc = 111,789)
  * Seattle group health note (sc = 8,268, tc = 110,208)
  * Stratified (sc = 5,022, tc = 51,629)
  * Stratified Seattle group health note (sc = 15,948, tc = 165,960)

THYME
-----

* `Temporal History of Your Medical Events <http://clear.colorado.edu/compsem/index.php?page=endendsystems&sub=temporal>`_
  * Brain cancer note (sc = 21,284, tc = 263,011)
  * Clinical/Pathological note (sc = 30,090, tc = 448,603)

Mixed
-----

A combined dataset consisting of `CRAFT`, `BOLT`, `EWT`, `OntoNotes`, `QuestionBank`, `MiPACQ`, `SHARP`, and `THYME`.

Part-of-Speech Tags
-------------------

.. csv-table:: Part-of-Speech Tags
   :header-rows: 1

   Tag, Description
   ---, ---
   ADD, Email
   AFX, Affix
   CC, Coordinating conjunction
   CD, Cardinal number
   DT, Determiner
   EX, Existential _there_
   FW, Foreign word
   GW, Go with
   IN, Preposition
   JJ, Adjective
   JJR, Adjective, comparative
   JJS, Adjective, superlative
   LS, List item
   MD, Modal
   NN, Noun, singular or mass
   NNS, Noun, plural
   NNP, Proper noun, singular
   NNPS, Proper noun, plural
   PRP, Pronoun
   PRP$, Pronoun, possessive
   PDT, Predeterminer
   POS, Possessive ending
   RB, Adverb
   RBR, Adverb, comparative
   RBS, Adverb, superlative
   RP, Particle
   TO, To
   UH, Interjection
   VB, Verb, base form
   VBD, Verb, past tense
   VBG, Verb, gerund or present participle
   VBN, Verb, past participle
   VBP, Verb, non-3rd person singular present
   VBZ, Verb, 3rd person singular present
   WDT, _Wh_-determiner
   WP, _Wh_-pronoun
   WP$, _Wh_-pronoun, possessive
   WRB, _Wh_-adverb
   XX, Unknown

.. csv-table:: Punctuation Tags
   :header-rows: 1

   Tag, Description
   ---, ---
   $, Currency
   :, Colon
   ,, Comma
   ., Period
   ``, Left quote
   ``, Right quote
   -LRB-, Left bracket
   -RRB-, Right bracket
   HYPH, Hyphen
   NFP, Superfluous punctuation
   SYM, Symbol
