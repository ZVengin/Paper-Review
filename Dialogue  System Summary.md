## Dialogue  System Summary

### Dataset

### Multi-Task

#### [Towards Scalable Multi-domain Conversational Agents: The Schema-Guided Dialogue Dataset](https://arxiv.org/abs/1909.05855)
- there are no lagre scale datasets for multi-domain dialogue systems and existing dialogue systems cannot be generalized to unseen domains. Therefore, a [large-scale multi-domain dataset](https://github.com/google-research-datasets/dstc8-schema-guided-dialogue), including 16 domains, 26 services and  16000 dialogues, is constructed.
  

#### [Goal-Oriented Multi-Task BERT-Based Dialogue State Tracker](https://arxiv.org/abs/2002.02450)
- existing task-oriented dialogue systems cannot generalize to unseen tasks, therefore, they reformulate the dialogue state tracking task in the form of QA, where the dialogue history, slot, service and intent description correspond to the question and the dialogue state corresponds to the answer

### Recommendation
#### [Towards Knowledge-Based Recommender Dialog System](https://arxiv.org/abs/1908.05391)
 - conventional recommendation systems recommend items only depend on previous selected items, which makes the recommendation not accurate. So they combine the recommendation system with dialogue system and use knowledge graph to find the items to be recommended
 
#### [Building Task-Oriented Dialogue Systems for Online Shopping]([file:///home/vengin/Downloads/14261-66459-1-PB.pdf](file:///home/vengin/Downloads/14261-66459-1-PB.pdf))

#### [Towards Deep Conversational Recommendations](https://arxiv.org/abs/1908.05391)
- No large scale dataset for recommendation dialogue systems. they release a [dataset](https://redialdata.github.io/website/) for recommendation dialogue systems 
  

### Persona

#### [Generating Persona Consistent Dialogues by Exploiting Natural Language Inference](https://arxiv.org/abs/1911.05889)
- current dialogue systems cannot generate persona consistent responses. they explicitly take persona consistency into consideration during training phase and also adopt natural language inference module to decide whether the generated responses are consistent with the chat-bot's personas.
  
#### [Large Scale Multi-Actor Generative Dialog Modeling](https://www.aclweb.org/anthology/2020.acl-main.8.pdf)
- Existing dialogue systems are faced with the problem of inconsistent personality and averyage personality in conversations. 
  
#### [A Persona-Based Neural Conversation Model](https://www.aclweb.org/anthology/P16-1094/)

#### [Exploring Personalized Neural Conversational Models](https://www.ijcai.org/Proceedings/2017/521)

#### [Personalizing a Dialogue System with Transfer Reinforcement Learning](https://arxiv.org/abs/1610.02891)

#### [Personalizing Dialogue Agents: I have a dog, do you have pets too?](https://arxiv.org/pdf/1801.07243.pdf)

### Negotiation 

#### [Decoupling Strategy and Generation in Negotiation Dialogues](https://arxiv.org/pdf/1808.09637.pdf)
- Problem
  1. end2end model is hard to control and interpret negotiation strategies
  2. directly optimize user's goal using RL with will lead to ungrammartical utterance
- Motivation
  1. freely to adjust negotiation straties in order to achive different negotiation goals without modifying language generation models
- Contribution
  1. propose a framework which decompose strategies and language generation
  2. propose a new negotiation dataset [CRAIGSLISTBARGAIN](https://stanfordnlp.github.io/cocoa/)


### Life-long Learning
#### [Learning from dialogue after deployment: Feed yourself, Chatbot!](https://www.aclweb.org/anthology/P19-1358/)
- it's difficult and expensive to collect enormous amounts of conversation data and conversal models cannot be updated once they have been trained. so they develop a dialogue system which can continously learn dialogue strategies after it has been deployed
  
  
### Emotion
#### [DailyDialog: A Manually Labelled Multi-turn Dialogue Dataset](https://www.aclweb.org/anthology/I17-1099/)
- there is no dataset for buidling a dialogue system for daily conversations and existing dialogue systems are unable to generate response containing spcific emotions. Collecting a large dataset for daily conversations and conversations with emotions
  
### Depression Diagnosis
#### [Predicting Depression in Screening Interviews from Latent Categorization of Interview Prompts](https://www.aclweb.org/anthology/2020.acl-main.2/)
- This work propose a new task to diagnose depression personaility according to the interview conversation transcripts.

### Slot Filling
#### [Coach: A Coarse-to-Fine Approach for Cross-domain Slot Filling](https://www.aclweb.org/anthology/2020.acl-main.3.pdf)
- This work tries to cope with problem of lack of training data in some domains. Therefore, they adopt cross-domain slot filling to solve the problem.


### Evaluation
#### [Designing Precise and Robust Dialogue Response Evaluators](https://www.aclweb.org/anthology/2020.acl-main.4.pdf)
- This work proposes a response evaluator which is independent of reference responses. This evaluator explots the power of semi-supervised learning and pretained language model. The evaluator achieves a promising result on the correlation with human evaluation.



### Knowledge Based
#### [Generating Informative Conversational Response using Recurrent Knowledge-Interaction and Knowledge-Copy](https://www.aclweb.org/anthology/2020.acl-main.6.pdf)
- Existing dialogue systems are unable to merge the multiple knowledge entries into one repsonse. They propose a method recurrent knowledge interaction and a copy mechanism to sovle the problem


### Pretrain Model
#### [PLATO: Pre-trained Dialogue Generation Model with Discrete Latent Variable](https://www.aclweb.org/anthology/2020.acl-main.9.pdf)
- dialogue systems are hevality limited by training data, therefore, they propose a pretraining framework to support various kinds of dialogue systems like chit-chat, knowledge grounded dialogues, and conversational question answering. 
