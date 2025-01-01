Part-of-Speech Tagging
=======================

Flair Tagger
------------

This is ELIT's replication of `Flair <https://github.com/zalandoresearch/flair/>`_ tagger using contextual string embeddings. 
It is ported from the PyTorch implementation of Flair version 0.2.

- **Source**: `https://github.com/zalandoresearch/flair <https://github.com/zalandoresearch/flair>`_
- **Associated models**: ``elit_pos_flair_en_mixed``
- **Decode parameters**: ``none``
- **Voice source**: `technolati <https://www.technolati.com/sound-of-text-wanita-manja-di-wa-di-hp-android/>`_

Web API
------------

.. code-block:: json

   {
       "model": "elit_pos_flair_en_mixed"
   }

Python API
------------

.. code-block:: python

   from elit.structure import Document, Sentence, TOK
   from elit.component import POSFlairTagger

   tokens = ['Jinho', 'Choi', 'is', 'a', 'professor', 'at', 'Emory', 'University', 'in', 'Atlanta', ',', 'Georgia', '.']
   doc = Document()
   doc.add_sentence(Sentence({TOK: tokens}))

   pos = POSFlairTagger()
   pos.decode([doc])
   print(doc.sentences[0])

Output
------------

.. code-block:: json

   {
       "sid": 0,
       "tok": ["Jinho", "Choi", "is", "a", "professor", "at", "Emory", "University", "in", "Atlanta", ",", "Georgia", "."], 
       "pos": ["NNP", "NNP", "VBZ", "DT", "NN", "IN", "NNP", "NNP", "IN", "NNP", ",", "NNP", "."]
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
