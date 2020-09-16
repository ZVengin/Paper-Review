### Paraphrase

#### [Dictionary-Guided Editing Networks for Paraphrase Generation](https://arxiv.org/abs/1806.08077)
  1. this paper is about paraphrase which aims to paraphrase the input sentence to the target sentence, however, existing works focus on generating the target sentence from scratch, which is different from the way that human does. Following the way of human, they provide a set of paraphrase phrase pairs as candidates to their model, and their model choose the appropriate ones to replace the phrases in the input sentence. 
  2. from their experiment results, it is obvious that not all paraphrase candidates are adopted in target sentence. 
  3. the paraphrase is limited since they can only paraphrase word-level and phrase level. they cannot do sentence-level paraphrase

### Dialogue System
#### [Response Generation by Context-Aware Prototype Editing](https://arxiv.org/abs/1806.07042)
  1. this paper is about dialogue response generation. In previous works, the dialogue responses suffer the problem of "safe response" in generation paradigm or the problem of inflexibility in retrieveal paradigm, therefore, this work propose to retrieve a relevant response first from dataset as prototype(template) and then modify its content to adapt it to current dialogue context.

### Data-to-Text
#### [Fact-based Text Editing](https://www.aclweb.org/anthology/2020.acl-main.17.pdf)
1. in table-to-text task, the generated sentences may miss some facts or include unsupported facts, therefore, they propose a task to revise the generated texts as well as construct a dataset for this task.
2. this work is so meaningful once the original table-to-text achieves human equivalent performance.

### Post-editing
#### [A Simple and Effective Approach to Automatic Post-Editing with Transfer Learning](https://www.aclweb.org/anthology/P19-1292/)
1. this paper focus on post-editing problem which aims to correct the mistakes in machine translation results. They found that existing works rely on enormous manually labeled data and annoating these data is expensive, moreover, the time of training a APE model with large corpus is equivalent to that training a translation from scracth, which makes the motivation that APE avoids retraining translation model when doing customized edition become meaningless. so they propose to adopt pretrained language model BERT as encoder and decoder in order to alleviate the dependence on labled data. The experiments show that their model adopting BERT can achieve competitive performance with much less labeled training data. 
