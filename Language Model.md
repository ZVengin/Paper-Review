#### [StructBERT: Incorporating Language Structures into Pre-training for Deep Language Understanding](https://arxiv.org/abs/1908.04577)
- they force bert model to capture structure information by training bert on two  auxiliary tasks including predicting the text sequence when the order of some input words are shuffled or the order of some input sentences are shuffled.

#### [Learning Structured Text Representations](https://www.aclweb.org/anthology/Q18-1005.pdf)
- this paper tries to learn the representation of documents while incorporating the document structures into representation. the document structures are represented by Rhetorical Structure Theory, which depicts the dependency relations between setences, and it is non-projective dependency tree. Therefore, they propose a model to handle the RST tree of documents.

#### [Towards Generating Long and Coherent Text with Multi-Level Latent Variable Models](https://www.aclweb.org/anthology/P19-1200/)
- this paper tries to capture the structures of text using multi-level latent variables. they adopt two variables to extract text structures in different levels, z2 is infered from input text and z1 is infered from z2. so z2 captures more high-level structure information than z1. they also use two level decoders including word-level decoder and sentence level decoder to decode text hierarchically.

#### [Towards coherent and cohesive long-form text generation](https://www.aclweb.org/anthology/W19-2401.pdf)
- this paper tries to generate coherent and cohesive long text using the evaluation score of the generated text on cohesion and coherence as rewards. they train two discriminators to assign cohesion score and coherence score on the given source text and target text pairs. these pretrained discriminators are used to return evaluation scores on the generated text during training.
