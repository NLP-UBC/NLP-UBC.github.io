---
layout: post
date: 2021-12-01
title: Discourse Analysis and Parsing
link: https://nlp.cs.ubc.ca/mega-dt
---

##### Distantly- and Self-Supervised Approaches to Infer Discourse

In our recent line of distantly- and self-supervised approaches for RST-style discourse parsing, we aim to generate robust silver-standard discourse trees informed by related downstream tasks.

<br>

###### Discourse from Sentiment Analysis

|![Image](/assets/img/showcases/mega_dt_pipeline.png){: .showcase_img}|
|*MEGA-DT Disocurse Annotation Pipeline*|
{: .showcase_img_right}

In our [EMNLP 2019](https://aclanthology.org/D19-1235/) and [MEGA-DT](https://aclanthology.org/2020.emnlp-main.603.pdf) (published at EMNLP 2020) papers, we propose a combination of a deep multiple instance learning model (MILNet) with the traditional CKY algorithm to generate nuclearity-attributed discourse structures for large-scale sentiment annotated corpora. We show that while the silver-standard discourse trees cannot outperform in-domain supervised discourse parsers, they do capture highly robust structures, which generalize well between domains, reaching the best inter-domain discourse parsing performance to date. Our generated silver-standard discourse treebank containing over 250.000 complete discourse trees in the review domain can be downloaded <a href='{{ '/mega-dt' | prepend: site.url }}'>here</a>.

<br>

###### Discourse from Topic Segmentation

|![Image](/assets/img/showcases/topic_seg_for_disc.png){: .showcase_img}|
|*Topic Segmentation to Infer High Level Discourse Structures*|
{: .showcase_img_left}

Improving on our work using sentiment augmented data to infer discourse structures, we target high-level (above-sentence) discourse structures in our AAAI 2022 work on [Predicting Above-Sentence Discourse Structure using Distant Supervision from Topic Segmentation](https://arxiv.org/abs/2112.06196). We thereby exploit our top-performing neural topic segmentation model presented in [this paper](https://aclanthology.org/2020.aacl-main.63/) to greedily segment documents, showing that the generated high-level (binary) discourse structures align well with gold-standard discourse annotations, an important factor for many downstream tasks implicitly or explicitly converting constituency trees into dependency representations. 

<br><br>

###### Discourse from Summarization

|![Image](/assets/img/showcases/sum4disc.png){: .showcase_img}|
|*Discourse Inference from Transformer Self-Attention Matrices*|
{: .showcase_img_right}

Extending our work on distantly-supervised discourse parsing, we explore the auxiliary task of summarization, especially focussing on the nuclearity attribute, which has previously been shown to contain importnat information for summarization related tasks. In our [NAACL 2021 paper](https://aclanthology.org/2021.naacl-main.326/), we show that discourse (dependency) structures can be reasonably inferred using the CKY and Eisner algorithms to extract discourse trees from transformer self-attention matrices, marking an important first step to explore state-of-the-art NLP models for their alignment with discourse information.

<br>


###### Discourse from Tree-style Autoencoders

|![Image](/assets/img/showcases/tree_ae.png){: .showcase_img}|
|*Unsupervised Tree Auto-Encoder*|
{: .showcase_img_left_large}

In our AAAI 2021 paper on [Unsupervised Learning of Discourse Structures using a Tree Autoencoder](https://ojs.aaai.org/index.php/AAAI/article/view/17549), we aim to generate discourse structures (without nuclearity and relation labels) from the task of tree-style language modelling. In contrast to many modern approaches interpreting the language modelling task as a sequential problem, we explicitly generate discrete tree structures during training and inference. We show that those tree structures learned purely from existing large-scale datasets can reasonably align with discourse and further also supports important downstream tasks (here: sentiment analysis). While the performance is nowhere close to supervised (or distantly-supervised) models, we show first insights into the value of generating more tree-enabled structures for language modelling, potentially valuable for further research in the future.

<br>

###### W-RST: A weighted Extension of Discourse Theories

|![Image](/assets/img/showcases/wrst.png){: .showcase_img}|
|*The W-RST framework bridging the gap between Linguistics and NLP*|
{: .showcase_img_right}

In a first attempt to bridge the ever growing gap between (Computational) Linguistics and Natural Language Processing, we propose the [Weighted-RST (W-RST) framework](https://aclanthology.org/2021.acl-long.302/) at ACL 2021. In this line of work, we explore the usage of readily available real-valued scores in distantly supervised discourse models, namely the [MEGA-DT](https://aclanthology.org/2020.emnlp-main.603.pdf) and our [NAACL 2021](ttps://aclanthology.org/2021.naacl-main.326/) paper, to generate more fine-grained importance scores between sibling sub-trees (i.e., the RST nuclearity attribute). In our experiments, we show that the weighted RST trees are superior to discourse treuctures with binary nuclearity attributes for most thresholds, and further align well with human annotations.

<br><br>

##### Supervised Discourse Parsers

Our lab further contributed some of the top-performing, completely supervised discourse parsers to date. With the [CODRA discourse parser](https://direct.mit.edu/coli/article/41/3/385/1522/CODRA-A-Novel-Discriminative-Framework-for) reaching state-of-the-art performance at the time using an optimal parsing algorithm with two Conditional Random Fields for intra-sentential and multi-sentential parsing. 

More recently, our neural discourse parser presented at [CODI 2020](https://aclanthology.org/2020.codi-1.17/) based on the shift-reduce paradigm, using SpanBERT and an auxiliary coreference module reached the state-of-the-art performance for RST-style discourse parsing on RST-DT.
