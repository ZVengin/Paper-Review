## Controllable Sentence Generation

### [Toward Controlled Generation of Text](https://arxiv.org/pdf/1703.00955.pdf)

### [Semantically Conditioned LSTM-based Natural Language Generation for Spoken Dialogue Systems](https://arxiv.org/pdf/1508.01745.pdf)

### [Learning to Select Knowledge for Response Generation in Dialog Systems](https://arxiv.org/pdf/1902.04911.pdf)

### [Neural Text Generation from Structured Data with Application to the Biography Domain](https://www.aclweb.org/anthology/D16-1128.pdf)

- Problems:
  - existing datasets for concepts to text are too small
  - traditionally sentence generation experienced three steps: content planning, sentence planning, and surface realization
- Contribution:
  - extend datasets
  - propose a task to generate biography for fact table in info box of wikipedia

### [Learning to Generate Reviews and Discovering Sentiment](https://arxiv.org/pdf/1704.01444.pdf) 

- Contributions:
  - Using unsupervised method to learn the representation of sentences and disentangled the meaning with sentiment.
  - Can control the sentences' sentiment by specifying the sentiment feature to be positive or negative

### [A Context-aware Convolutional Natural Language Generation model for Dialogue Systems](https://www.aclweb.org/anthology/W18-5020.pdf)

- problems:
  - RNN based encoder-decoder model is too slow since it computes in a sequence manner
- Contributions:
  -  developed a CNN based encoder-decoder model 

### [Semantically Conditioned LSTM-based Natural Language Generation for Spoken Dialogue Systems](https://www.aclweb.org/anthology/D15-1199.pdf) 

- a good generator usually depends on several factors: adequacy, fluency, readability, and variation.
- rule-based generator is robust and adequency
- rule-based generator generates frequent repetition of identical
- rule-based generator not easily scale to large open domain
- Contributions:
  - developed a Semantically Conditioned LSTM-based Natural Language Generation for Spoken Dialogue Systems

### [Sequence to Sequence Learning with Neural Networks](https://arxiv.org/pdf/1409.3215.pdf)

- Contribution
  - proposed seq2seq model

### [Style Transfer from Non-Parallel Text by Cross-Alignment](https://arxiv.org/pdf/1705.09655.pdf)

### [Controllable Abstractive Summarization](https://arxiv.org/pdf/1711.05217.pdf)


## Text Editing
#### [Fact-based Text Editing](https://www.aclweb.org/anthology/2020.acl-main.17.pdf)
- in table-to-text task, the generated sentences may miss some facts or include unsupported facts, therefore, they propose a task to revise the generated texts as well as construct a dataset for this task. 
