### Paraphrase

#### [Dictionary-Guided Editing Networks for Paraphrase Generation](https://arxiv.org/abs/1806.08077)
  1. this paper is about paraphrase which aims to paraphrase the input sentence to the target sentence, however, existing works focus on generating the target sentence from scratch, which is different from the way that human does. Following the way of human, they provide a set of paraphrase phrase pairs as candidates to their model, and their model choose the appropriate ones to replace the phrases in the input sentence. 
  2. from their experiment results, it is obvious that not all paraphrase candidates are adopted in target sentence. 

### Dialogue System
  1. this paper is about dialogue response generation. In previous works, the dialogue responses suffer the problem of "safe response" in generation paradigm or the problem of inflexibility in retrieveal paradigm, therefore, this work propose to retrieve a relevant response first from dataset as prototype(template) and then modify its content to adapt it to current dialogue context.
  2. The problem of this work is that the modification of selected prototype depends on the difference between the current context and the context of selected prototype. it is reasonable in some cases where the reponse express similar contents to that of context, while, in other cases, the contents of response may be quite different from the context.
