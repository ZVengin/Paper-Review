## Dialogue  System Summary

### Task-oriented Dialogue System

#### Multi-domain

##### [Towards Scalable Multi-domain Conversational Agents: The Schema-Guided Dialogue Dataset](https://arxiv.org/abs/1909.05855)

- Problem
  1. most datasets focusing on a single domain
  2. existing multi-domain datasets are relatively small
  3. existing task-oriented dialogue systems cannot generalize to unseen tasks
- Motivation
  1. practical virtual assistants should be capable of handling large-scale tasks.
  2. Based on the observation that most tasks have the overlapping of functionality. so dialogue system should be able to handle unseen tasks by leveraging the experience of other similar tasks.
  3. some tasks have little or no training data, which requires dialogue system to leverage their knowledge learned from other tasks. 
- Contributions
  1. build a large-scale multi-domain datasets, including 16 domains, 26 services and  16000 dialogues.
  2. they try to predict intentions and slot values on some unseen domains or services and obtain promising results.

##### [Goal-Oriented Multi-Task BERT-Based Dialogue State Tracker](https://arxiv.org/abs/2002.02450)

- Problem
  1. existing task-oriented dialogue systems cannot generalize to unseen tasks
- Contribution
  - reformulate the dialogue state tracking task in the form of QA, where the dialogue history, slot, service and intent description correspond to the question and the dialogue state corresponds to the answer
 
##### [Towards Knowledge-Based Recommender Dialog System](https://arxiv.org/abs/1908.05391)
 - Problem
    1. conventional recommendation systems recommend items only depend on previous selected items, which makes the recommendation not accurate
 - Contribution
    1. combine the recommendation system with dialogue system
    2. use knowledge graph to find the items to be recommended
 - Motivations
    1. during conversation, users may convey some information about the desirable items. we can use these information to improve the recommendation accuracy
    2. the information conveyed in conversations can be connected with desirable items in knowledge graphs. So using knowledge graph can help find the desirable items according to the information in dialogues. 

[Building Task-Oriented Dialogue Systems for Online Shopping]([file:///home/vengin/Downloads/14261-66459-1-PB.pdf](file:///home/vengin/Downloads/14261-66459-1-PB.pdf))

