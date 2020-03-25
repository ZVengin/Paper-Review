# Summary

## Dialogue System

### [Sequence-to-Sequence Generation for Spoken Dialogue via Deep Syntax Trees and Strings](https://www.aclweb.org/anthology/P16-2008.pdf)

- Target: Generating sentences from dialogue meaning representation
- Motivation: Exploring the influence of different generation approaches on the generated sentences 
  - Approach 1: generating sentences in two steps, first generating a syntactic dependency tree of sentence and then linearize it to sentence
  - Approach 2: directly generating sentences from meaning representations
- Setting up: comparing with existing models. In addition, for each proposed model. the author tries beam-search with different size
  - existing models
  - model (approach 1): beam-search size being 5,20,100
  - model (approach 2): beam-search size being 5,20,100
- Evaluation
  - comparing with reference responses using BLEU scores
  - manually checking whether the meaning representation is correctly expressed in generated sentences

## Paraphrase

### [Adversarial Example Generation with Syntactically Controlled Paraphrase Networks](https://arxiv.org/pdf/1804.06059.pdf)

- 

 