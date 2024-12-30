English Models
==============

* **PRE**: tools that need to be run prior to the model.
* **DATA**: the dataset used to build the model.
* **EVAL**: evaluation on the dataset that the model is trained on. 
* **BM**: the standard benchmark evaluation for the task.
* **tokseg**: any :ref:`tokenizer <tokenization>` with sentence segmentation.
* **inmixed**: any dataset in the :ref:`mixed corpus <english_datasets.html#mixed>`.

Tokenization
------------

.. csv-table:: Tokenization Models
   :header: "Model ID"
   :widths: 50

   "`elit_tok_space_un <../tools/tokenization.html#space-tokenizer>`_"
   "`elit_tok_lexrule_en <../tools/tokenization.html#english-tokenizer>`_"

Morphological Analysis
----------------------

.. list-table::
   :header-rows: 1
   :widths: 40 10

   * - **Model ID**
     - PRE
   * - `elit_morph_idprule_en <../tools/morphological_analysis.html#english-analyzer>`_
     - :ref:`tokseg <part-of-speech-tagging>`

Part-of-Speech Tagging
----------------------

.. list-table::
   :header-rows: 1
   :widths: 40 10 15 15 15

   * - **Model ID**
     - PRE
     - DATA
     - EVAL
     - BM
   * - `elit_pos_flair_en_mixed <../tools/part_of_speech_tagging.html#flair-tagger>`_
     - :ref:`tokseg <tokenization>`
     - :ref:`Mixed <english_datasets.html#mixed>`
     - 97.80%
     - 97.72%


* **EVAL**: accuracy.
* **BM**: accuracy on the Wall Street Journal portion of the `Penn Treebank <https://catalog.ldc.upenn.edu/ldc99t42>`_ using the standard split (trn: 0-18; dev: 19-21; tst: 22-24).

Named Entity Recognition
-------------------------

.. list-table::
   :header-rows: 1
   :widths: 40 10 20 15 15

   * - **Model ID**
     - PRE
     - DATA
     - EVAL
     - BM
   * - `elit_ner_flair_en_ontonotes <../tools/named_entity_recognition.html#flair-tagger>`_
     - :ref:`tokseg <tokenization>`
     - :ref:`OntoNotes <english_datasets.html#ontonotes>`
     - 88.75%
     - 92.74%

* **EVAL**: F1-score.
* **BM**: F1-score on the English dataset distributed by the `CoNLL 2003 shared task <https://www.clips.uantwerpen.be/conll2003/ner/>`_.

Dependency Parsing
------------------

.. list-table::
   :header-rows: 1
   :widths: 40 10 20 20 20

   * - **Model ID**
     - PRE
     - DATA
     - EVAL
     - BM
   * - `elit_dep_biaffine_en_mixed <../tools/dependency_parsing.html#biaffine-parser>`_
     - :ref:`tokseg <part-of-speech-tagging>`
     - :ref:`Mixed <english_datasets.html#mixed>`
     - 92.26/91.03
     - 96.08/95.02

* **EVAL**: UAS (unlabeled attachment score) / LAS (labeled attachment score).
* **BM**: UAS/LAS on the Wall Street Journal portion of the `Penn Treebank <https://catalog.ldc.upenn.edu/ldc99t42>`_ using the standard split (trn: 2-21; dev: 22, 24; tst: 23) 
  and the `Stanford typed dependencies <https://nlp.stanford.edu/software/stanford-dependencies.html>`_.

Semantic Dependency Parsing
---------------------------

.. list-table::
   :header-rows: 1
   :widths: 40 10 20 20 20

   * - **Model ID**
     - PRE
     - DATA
     - EVAL
     - BM
   * - `elit_sdp_biaffine_en_mixed <../tools/semantic_dependency_parsing.html#biaffine-parser>`_
     - :ref:`tokseg <part-of-speech-tagging>`
     - :ref:`Mixed <english_datasets.html#mixed>`
     - ?
     - 90.68/85.34

* **EVAL**: Labeled F1 score.
* **BM**: Average labeled F1 scores on the in-domain and out-of-domain test sets distributed by the `SemEval 2015 shared task <http://alt.qcri.org/semeval2015/task18/>`_.
