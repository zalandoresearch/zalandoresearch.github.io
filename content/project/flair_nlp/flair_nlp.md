+++
date = "2018-09-01T00:00:00+02:00"
description = ""
external_link = ""
image = ""
project_id = "flair_nlp"
short_description = "State-of-the-Art Natural Language Processing (NLP)"
title = "Flair"
+++

## State-of-the-Art Natural Language Processing (NLP)
### Research Project by Alan Akbik (ex-member)
Can we teach machines to read and understand human language? And in the future, can we teach them to perform language AI tasks with little training data, across over 20 different human languages? At Zalando Research, we’re investigating answers to these questions.

We are researching a novel approach that leverages neural language modeling to learn powerful, contextualized representations of human language from large corpora. These representations contain a wealth of syntactic and semantic information that can be used to directly improve downstream natural language processing (NLP) tasks.

In particular, [our recent paper](https://www.google.com/url?q=http://alanakbik.github.io/papers/coling2018.pdf&sa=D&ust=1536756403667000) proposes a sequence labeling architecture built on top of neural language modeling that sets new state-of-the-art scores for a range of classical NLP tasks, such as named entity recognition (NER) and part-of-speech (PoS) tagging.

![image2](img/image2.png)

Example of named entity recognition in the domain of fashion. Our approach identifies and highlights fashion-related entities such as colors, looks, designs and brands in text.

Illustration of our approach. A sentence (bottom) is input as a character sequence into a pre-trained bidirectional character language model (LM, yellow in Figure. From this LM, we retrieve for each word a contextual embedding by extracting the first and last character cell states. This word embedding is then passed into a vanilla BiLSTM-CRF sequence labeler (blue in Figure), achieving robust state-of-the-art results on downstream tasks (NER in this example).

![image1](img/image1.png)

We make our state-of-the-art NLP framework – called [Flair](https://github.com/flairNLP/flair) – openly available. The framework is already in use by multiple research groups that have used it to reach new state-of-the-art scores for a range of NLP tasks across different languages.

We are actively developing [Flair](https://github.com/flairNLP/flair) to encompass a growing range of NLP task and languages – and keep pushing the state-of-the-art in NLP!


#### References:

[1] [Contextual String Embeddings for Sequence Labeling.](http://alanakbik.github.io/papers/coling2018.pdf). (Akbik et al., 2018)

[2] [The Flair NLP framework](https://github.com/flairNLP/flair)
