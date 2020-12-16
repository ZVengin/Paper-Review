### Hierarchical story generation


#### [Hierarchical Neural Story Generation](https://www.aclweb.org/anthology/P18-1082.pdf)
- this paper solves the problem that the generated story is not closedly related to the given pompt, therefore, they introduce fusion mechansim in their work. So in their work, they first generate the prompt which captures the main contents of the story and generate the story following the prompt using fusion model. They also collect a story generate dataset. 


#### [Narrative Interpolation for Generating and Understanding Stories]()
- this work studies the stories generation by confining its starting and ending sentence. they find that existing storyline based story generation models face the problem of wandering and are sensitive to the selection of keywords in storylines. so they propose to interpolate the story by confining its starting and ending.

#### [A Skeleton-Based Model for Promoting Coherence Among Sentences in Narrative Story Generation](https://www.aclweb.org/anthology/D18-1462.pdf)
- this paper solves the problem that the sentences in generated story should have semantic connections, where semantic connections denote that . so they proposed skeleton-based model for promoting coherence among sentences. in their model, they first learning to generate skeleton using RL and extend skeleton to stories. the skeleton means the key words or phrases in sentences.

#### [Learning to Predict Explainable Plots for Neural Story Generation]()
- this paper also studies the problem of generating stories in a herarchical way where an outline is first generated and then the story is generated conditioned on the outline. the outline in their work is a single sentence which summarizes the main contents of the story.

#### [Consistency and Coherency Enhanced Story Generation](https://arxiv.org/pdf/2010.08822.pdf)
- this paper belongs to the idea that generating story in-two-steps in order to improve the coherence and consistency of story. they first generate an outline of the story which is consist of a set of keywords or an abstract, and then generate story based on the outline and prompt. They also augment the generation model with a disclose relation classifier to distinguish the discourse relation between two consecutive sentence. they suggest that this way can improve story's coherence.

#### [Progressive Generation of Long Text]()
- this paper explores how to generate long text in a herarchical way. they find that existing works only focus on short text generation and the promising long text generation model like GPT facing the problem of incoherence and repeatition. Therefore, they proporse to first generate a backbone of the text which consists of a set of key phrases and then filling the interval between phrases with words to make it become a complete text.

#### [Summarize, Outline, and Elaborate: Long-Text Generation via Hierarchical Supervision from Extractive Summaries]()
- this paper explores how to generate long stories in a hierarchical way. they find that pretrained language models like GPT focuses on predicting local words and ignores the
high-level structure of text. Although existing coarse-to-fine story generation approach which first generate a summary of the story like a set of key words or a single sentece summary and then generate stories following the guidance of the summary. They argue that the keywords and a single-sentence summary are limited in capacity and cannot capture the high-level sturcture of text. Therefore, they propose to generate multi-sentence summaries with each sentence corresponding to a segment of story, and each segment can be generated following its own summary.


### Story-line based story generation
#### [Towards Controllable Story Generation](https://pdfs.semanticscholar.org/f9de/0d4a5adefc59bfb033f162d8a4a5212882cf.pdf?_ga=2.186340393.1437532588.1602585748-917632008.1599084173&_gac=1.159122888.1599460111.CjwKCAjwkdL6BRAREiwA-kiczH95rmO86D0s6vqHi4gsT7dhL-quGeLMV0UDh8OIocXSHdRTGup0PxoCLKsQAvD_BwE)
- this paper attempts to control story generation using some control factors like labels indicating the sentiment of the end of story and keywords indicating the storyline. 

#### [Strategies for Structuring Story Generation](https://arxiv.org/pdf/1902.01109.pdf)
- this paper aims to make long story more coherent and model long-distance dependency among contents. so they generate story in two steps: (1) they generate a sequence of actions from prompt (2) generate story following the guidance of the actions. the action here is represented with a predicate-agrument structure. 
- diversity, repeatition and lacking details are main problem in their results. 

#### [Towards Better Storylines with Sentence-Level Language Models]()
- this paper aims at generating coherent ending for storyline. They find that existing works generate storylines in word-level and cannot learn the dependency between sentences. Therefore, they tries to rank a set of candidate endings and select the most appropriate one as ending, instead of directly generating the ending based on context.

#### [PLOTMACHINES: Outline-Conditioned Generation with Dynamic Plot STate Tracking]()
- this paper also studies coherent story generation. They find that existing works  

#### [Narrative Text Generation with a Latent Discrete Plan]()
- this paper generates short stories using a hierarchical variational auto-encoder. they follow previous works which aims to generate coherent stories using storylines e.g. keywords, phrases, evnt representations and plot graph, but they find that the storylines in previous works are generated using an off-the-shelf tool which is too heuristic and cannot jointly learn during training phase. Therefore, they propose to model the storyline (a sequence of keywords, each keyword corresponds to a sentence) as a sequence of latent variables. during inference phase, the storyline first is sampled from the latent variables and then generate stories conditioning on the sampled story.




### Interaction based story generation
#### [Plan, Write, and Revise: an Interactive System for Open-Domain Story Generation](https://www.aclweb.org/anthology/N19-4016.pdf)
- This paper deveoped an interactive story generation system, where user can control the story generation and revise the generated story through the webpage interface. there are two types of interactions, one is model-cross interaction where user can choose the story generated by different models and control the diversity of story. the other one is inter-model interaction where user can modify both the story line and the story itself of the selected story, including inserting, deleting and modifying.  

#### [Cue Me In: Content-Inducing Approaches to Interactive Story Generation]()
- This paper tries to explore interactively controlling story generation in a conversation by providing the model a hint like a phrase. Existing works always generate stories in a one-shot manner where users cannot control the generation of stories. 

#### [Modeling Protagonist Emotions for Emotion-Aware Storytelling]()
- this paper studies the problem of controlling the emotion flow inside the generated stories. the control signal for emotions is a set of words expressiong emotions like joy-> anger->sadness. 



### Revise story generation
#### [Content Planning for Neural Story Generation with Aristotelian Rescoring](https://arxiv.org/pdf/2009.09870.pdf)
- This paper try to revise the plot of the generated stories. according to the characteristirc of a good story plot, they design a a set of ranking models to assign a score to each possible plot for each given prompt. they find the best story plot by ranking candidate plots according to the average score over all ranking models. the plot of story is represented as a sequence of events and each event is represented with semantic role labelling (SRL).
- from their example, there many repeatition of contents, missing details about events, the order of events may be chaotic.  


### Event to sentence
#### [Story Realization: Expanding Plot Events into Sentences](https://arxiv.org/pdf/1909.03480.pdf)
- This paper forces models to include input event into the sentence using five different models. 


### Script generation
#### [Hierarchical Quantized Representations for Script Generation]()
- this paper explores the problem of generating script for a scenerio. the script describes how a sequence of events is unfold under a specific scenerio. they found that previous works which solely relies on language model cannot generate coherent events as they ignore the hierarchical characteristic of script. therefore, in their work, they propose a hierarchical quantized autoencoder model to implicitly capturing the hierarchical structure of script.

#### [Hierarchical Quantized Representations for Script Generation](https://arxiv.org/abs/1808.09542)
- this paper is about script induction, where they try to predict the next event based on context. in this work, they solved two problems: (1) previous works can only generate locally coherent script (2) previous works ignore the hierachical structure of script. so they proposed a hierachical quatitive autoencoder model to model the script inner structures. but the results are not so illusing and they didn't define their problem clearly. 

#### [Controllable Neural Story Plot Generation via Reward Shaping]()
- this paper aims to control the generation of story plots using reinforcement learning. Previous works generate plots by first manully planning the contents which is controllable but expensive and requires domain knowledge. Recently for neural models althouth they don't require manually planning, we cannot the guide the generation of plots. to remedy this issue, they propose to control story plots generation using reinforcement learning so that the generated plots meet users' goal. In order to deal with sparse reward problem. they design a dense rewards function for their model.

### Analysis
#### [Do Massively Pretrained Language Models Make Better StoryTellers]()
- this paper studies the existing open-domain text generation models.two models including GPT and fusion model are studied on prompt based story generation dataset. They find that GPT model can generate more relevant stories to the given prompt and more coherent than the fusion model as well. But both models achieve similar performance on repeatition , word rareness, syntactic style and complexisty. They also find that sample size of GPT during decoding has an obvious impact on the performance.


### Other
#### [A Knowledge-Enhanced Pretraining Model for Commonsense Story Generation]()
- this paper studies story generation by incorporating external commonsense knowledge base. they find that the stories generated by existing models suffers the problem of repeatition, logical conflicts  and lack of long-range coherence. they assume that these problems are caused by the lack of relevant commonsense knowledge as a result, existing models cannot understand causal relationships and plan entities and events with approporate orders. therefore, they propose to emloy commonsense knowledge from external knowledge base to generate reasonable stories.

#### [Counterfactual Story Reasoning and Generation]()
- this paper explores how to adjust stories to be compitable with counterfactual context. here counterfactual context refers to the case ehere some sentence has logical conflicts with its context. existing works haven't studied this problem formally. therefore they propose this task and release a dataset.

#### [Generating Diverse Story ]


### ToRead
#### [Neural Text Generation in Stories Using Entity Representation as Context]()
#### [Unified Language Model Pre-training for Understanding and Generation]()
#### [Story Ending Generation with Incremental Encoding and Commonsense Knowledge]()
#### [Toward Better Automatic Storytelling]()
#### [Planning Stories]()
#### [Story Generation With Crowdsourced Plot Graphs]()
#### [An Interactive Program Writing Stories]()
#### [Strategies  for Structing Story Generation]()
#### [Unsupervised Hierarchical Story Infilling]()


