Named Entity Recognition
=========================

Flair Tagger
------------

This is ELIT's replication of `Flair <https://github.com/zalandoresearch/flair>`_ tagger using contextual string embeddings. 
It is ported from the PyTorch implementation of Flair version 0.2.

- **Source**: `https://github.com/zalandoresearch/flair <https://github.com/zalandoresearch/flair>`_
- **Associated models**: ``elit_ner_flair_en_ontonotes``
- **Decode parameters**: ``none``

Web API
------------

.. code-block:: json

   {
       "model": "elit_ner_flair_en_ontonotes"
   }

Python API
------------

.. code-block:: python

   from elit.structure import Document, Sentence, TOK
   from elit.component import NERFlairTagger

   tokens = ['Jinho', 'Choi', 'is', 'a', 'professor', 'at', 'Emory', 'University', 'in', 'Atlanta', ',', 'Georgia', '.']
   doc = Document()
   doc.add_sentence(Sentence({TOK: tokens}))

   ner = NERFlairTagger()
   ner.decode([doc])
   print(doc.sentences[0])

Output
------------

.. code-block:: json

   {
       "sid": 0,
       "tok": ["Jinho", "Choi", "is", "a", "professor", "at", "Emory", "University", "in", "Atlanta", ",", "Georgia", "."], 
       "ner": [[0, 2, "PERSON"], [6, 8, "ORG"], [9, 12, "LOC"]]
   }

Citation
------------

.. code-block:: text

   @InProceedings{akbik-blythe-vollgraf:COLING:2018,
     author    = {Akbik, Alan and Blythe, Duncan and Vollgraf, Roland},
     title     = {Contextual String Embeddings for Sequence Labeling},
     booktitle = {Proceedings of the 27th International Conference on Computational Linguistics},
     year      = {2018},
     series    = {COLING'18},
     url       = {http://aclweb.org/anthology/C18-1139}
   }
