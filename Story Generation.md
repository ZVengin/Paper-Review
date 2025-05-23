### Hierarchical story generation

#### [Event Representations for Automated Story Generation with Deep Neural Nets](https://ojs.aaai.org/index.php/AAAI/article/view/11430)(AAAI 2018)
- this paper finds that previous planning story generation works suffer the problem of expensive expert knowledge engineering and also can only generate story in predefined domains. Therefore, they propose to learn story planning and story generation from data corpus generate more openess stories. In order to achieve this purpose, they applied stanford corenlp to extract a sequence events from wikipedia story plot and use them as guideline for story generation. The event is represented as (s,v,o,m), where s is subject, v is verb, o is object and m is supplement components. For story planning, they train a event2event model using the extracted event sequence, which aims to predict the story outline, and for story generation, they train a event2sentence model which aims to tranlate the event sequence into a compelete story.

#### [Hierarchical Neural Story Generation](https://www.aclweb.org/anthology/P18-1082.pdf)(ACL 2018)
- this paper finds that it is very challenging to generate a thematically coherent and creative story. therefore, they propose to generate stories in a hierarchical approach where they first generate a prompt from scratch and then generate the story conditioned on the prompt. the prompt is a short sentence which roughly give a hint on what will be generate in story. In order to achieve this purpose, they collect a writingprompt dataset which has 300000 samples with each sample composed of a prompt and a story. In addition, they also find that seq2seq model tends to ignore the prompt, so they introduce fusion mechansim in their work to balance the dependency on the context and the prompt. 

#### [Towards Controllable Story Generation](https://www.aclweb.org/anthology/W18-1505/)(NAACL 2018)
- this paper focuses on controlling the story generation model to generate stories with specific type of ending or with specified storylines. They find that few existing works try to control the story generation, so they try to extract some control factors like sentiment and storyline from training data and use them to control story generation. For controlling story ending generation, they annotate the end of story with sentiment label and train the model to generate ending with specified sentiment by taking the context and the sentiment label as input. For controlling story generation with storyline, they extract a set of keywords using RAKE from stories and use them as input and try to reconstruct the stories. So in this case, the stories only condition on the storylines.  


#### [Narrative Interpolation for Generating and Understanding Stories]()(CoRR 2020)
- this work studies the stories generation by confining its starting and ending sentence. they find that existing storyline based story generation models face the problem of wandering and are sensitive to the selection of keywords in storylines. so they propose to interpolate the story by confining its starting and ending.


#### [A Skeleton-Based Model for Promoting Coherence Among Sentences in Narrative Story Generation](https://www.aclweb.org/anthology/D18-1462.pdf)(EMNLP 2018)
- this paper focuses on narrative story generation which aims to generate more detailed description for the given scene. the input is a short sentence describing a scene, the output is the extended description for the scene. they find that existing models are easy to fall back to language model and have difficultly in capturing the inter-sentence dependencies. in order to solve the problem, they assume that keyphrases can best keep the main semantics of sentence and can also reduce the redundant information of sentence. and thus they propose to use keyphrases extracted from each sentence of story as the skeleton of story. In this way, without generating redundant information, the model is able to focus more on the semantic connections between sentences. After that, they can extend the skeletons to complete stories.

#### [Learning to Predict Explainable Plots for Neural Story Generation](https://arxiv.org/abs/1912.02395)(CoRR 2019)
- this paper focuses on story generation from a given short title. they find that NLG task including story generation faces a sever problem of information gap that is NLG model has difficulty in generating long text from short input centering the given title and being thematically consistent as well. Although existing works have proposed to use some outlines to bridge the title and the stories, explicitly or implicitly modeling the outlines seems not ideal for story generation task. if implicitly modeling outlines as a latent variable it will be difficult for human to intepret, however, if explicitly modeling outlines as a natural language sentence the model will face exponentional outline search space. Therefore, they propose to represent the outlines as natural language sentences, at the mean while, they regard the outlines as a latent variable and optimize the entire model in a variational autoencode manner.

#### [Strategies for Structuring Story Generation](https://arxiv.org/pdf/1902.01109.pdf)(ACL 2019)
- this paper aims to generate stories from given prompts. they find that existing story generation models sequentially generate text at word-level and cannot plan the plot of stories from high-level. although existing works tried to decompose story generation into serveral steps, there is no comparision between these decomposition approaches. Therefore, in this work, they propose a new decompose approach where they generate the stories from prompts in three steps. they first generate a sequence of events from the prompt. the events here consist of a verb and its arguments like entities. they replace the entities with placeholder when generating event sequences. after that they expand the event sequences into stories and finally replace the placeholders with its correpsonding values. 
- diversity, repeatition and lacking details are main problem in their results. 

#### [Narrative Text Generation with a Latent Discrete Plan](https://www.aclweb.org/anthology/2020.findings-emnlp.325/)(EMNLP 2020)
- this paper generates short stories from a given short title using a hierarchical variational auto-encoder. they follow previous works which aims to generate coherent stories using storylines e.g. keywords, phrases, evnt representations and plot graph, but they find that the storylines in previous works are generated using an off-the-shelf tool which is too heuristic and cannot jointly learn during training phase. Therefore, they propose to model the storyline (a sequence of keywords, each keyword corresponds to a sentence) as a sequence of latent variables. during inference phase, the storyline first is sampled from the latent variables and then generate stories conditioning on the sampled story.


#### [Progressive Generation of Long Text](https://arxiv.org/abs/2006.15720)(CoRR 2020)
- this paper explores how to generate long story with its length being more than 1000 tokens in a hierarchical way. The input is a prompt aand output is a long story. they find that existing pretrained language models performed imperfect when generating long text such as repeatitiona and incoherence between sentences far apart due to the pretrained language models sequentially generating text and as a result have difficulties in planning contents. Based on their observations, they find that some words have decisive impact on the entire text while other words are so dependent on the context. Therefore, they propose to classifiy the words in text into may different levels according to their importance in the text and filling the words into story level by level from the most important level to the less important one. The advantage of their method is that the story generation process can be divided into arbitrary stages depending on how many levels the words have been classified into and these stages can be trained parallelly. For each stage, the model architecture is the same and the input and output setting are also similar.

#### [Summarize, Outline, and Elaborate: Long-Text Generation via Hierarchical Supervision from Extractive Summaries](https://arxiv.org/abs/2010.07074)(CoRR 2020)
- this paper explores how to generate long stories in a hierarchical way. they find that pretrained language models like GPT focuses on predicting local words and ignores the high-level structure of text. Although existing coarse-to-fine story generation approach which first generate a summary of the story like a set of key words or a single sentece summary and then generate stories following the guidance of the summary. They argue that the keywords and a single-sentence summary are limited in capacity and cannot capture the high-level sturcture of text. Therefore, they propose to generate multi-sentence summaries with each sentence corresponding to a segment of story, and each segment can be generated following its own summary.

#### [Consistency and Coherency Enhanced Story Generation](https://arxiv.org/pdf/2010.08822.pdf)(CoRR 2020)
- this paper aims to generate coherent and consistent stories from a given prompt. they find although GPT2 pretrained language model outperforms other baselines but still face the incoherence and inconsistency problem. traditional planning and generating approaches require lots of human efforts in data annotation. Although recently there are some data-driven approaches trying to generate in two-steps where in the first step, a middle meaning representation, such as keywords, keyphrases and sentences, is generated and in the second step, extend the middle meaning representation to a complete stoy. But they didn't make use of the latest language model architectures such as GPT2. Therefore, they adopt transformer architecture as their model backbone and generate the story in two stages. In the first stage, they apply a transformer model to generate an outline from the prompt and in the second stage, they apply the other transformer model to expand the outline to a story.


#### [Outline to Story: Fine-Grained Controllable Story Generation from Cascaded Events](https://arxiv.org/pdf/2101.00822.pdf)(CoRR 2021)
- this paper aims to generate stories from given prompts. they explore generating story from an outline and want to control the story in a fine-granularity level. In their work, they use events as their outline which are extract from dataset. they finetune GPT2 with their dataset in two different ways, one is that events and paragraphs are appeared in sequence interlevaingly, the other one is that the event outlines appears in the beginning of the story.


#### [Plan-And-Write: Towards Better Automatic Storytelling](https://docs.google.com/spreadsheets/d/1rKGZtbIqU5GyLc5VtsS_bO6DWDbcjF-5p6yrL89DGHQ/edit)
- this paper studies open-doamin story generation. they find it is difficult for existing models to generate coherent stories Therefore, they propose to generate stories in tow steps: planning and generate. they represent the planning as a sequence of keywords and they introduce two kinds of planning strategies, one is dynamic(planning while generating stories) and the other is static (planning before story generation). 

#### [Stylized Story Generation with Style-Guided Planning](https://arxiv.org/abs/2105.08625)
- this paper aims to control the style(whether to generate stories with a specified style) of the generated stories. they find existing story generation works focus on generating coherent stories and ignore the style of stoires. Therefore, they propose to control the style of story by generating stories in two steps: planning the keywords and then generating stories conditioning on the context and the keywords. They define the 3 tyoes of style (emotion, event and other) and assign a style label to each story by comparing the relative number of emotional keywords and event keywords.

#### [Content Learning with Structure-Aware Writing: A Graph-Infused Dual Conditional Variational Autoencoder for Automatic Storytelling](https://www.aaai.org/AAAI21Papers/AAAI-10130.YuMH.pdf)
- this paper aims to generate the stories with the guidance of keywords. They find that existing works, when guiding story generation with keywords, they sequentially mapping a keyword to a sentence. However, in practical scene, usually a keyword may appear in multiple sentences and there inner connection between different sentences. So they propose to represent these connections including the keywords-sentence connection and sentence-sentence connection using graphs. When generating a story, they first infer the content information of the story and the graph structure of the story from the keywords, and generate the stories conditioning on the content informtaion and the graph structures.

#### [Content planning for neural story generation with aristotelian rescoring](https://arxiv.org/abs/2009.09870)
- this paper studies story generation with content planning. They find existing pretrained language models canot generate structure and cohension story in global range. They assume this problem can be solved by providing a good plot plan to the model. Therefore, they develop a plot-generation language  model and an assemble of rescore models to rank the generated plots. Their rescore models are designed based on the Aristotle’s Poetics and their plot is represented by semantic role labelling.

#### [Guided Neural Language Generation for Automated Storytelling](https://www.aclweb.org/anthology/W19-3405.pdf)
- this paper aims to guide story generation with event planning. They find existing works focus on generating good planning for events, however, they ignore there are some problems in transformation from the event to sentence since sometimes the transformation from event to sentence may generate grammartically correct but semantically incorrect sentence. Therefore, they propose an ensemble to solve this problem.


#### [Facts2Story: Controlling Text Generation by Key Facts](https://arxiv.org/abs/2012.04332)
- this paper aims to guide story generation with a set of key facts. They find the event representation used as guidance is unnatral for human to use since composing it require expert knowledge. Therefore, they propose to control story generation with a set of key facts which represnted as a set of simple sentenes. They propose a planning and cloze model which first construct the skeleten using the given facts by inserting the space inside facts and then filling the space with details.


#### [Story Generation with Rich Details](https://www.aclweb.org/anthology/2020.coling-main.212/)
- this paper aims to generate story by first planning an outline represented by a sequence of events and then expand each event into a sentence. They find existing event planning based methods lack details. Therefore, they not only expand the event into a sentence but also fill additional details between events.


#### [Graph^based Multi-hop Reasoning for Long Text Generation](https://arxiv.org/abs/2009.13282)
- this paper aims to generate stories focusing on the sentential-level semantic dependencies. They find the existing works can capture semantic dependencies inside sentence, however, they fail to capture that in long text generation. Therefore, they propose to generate long text in two steps;(1) they try to plan text skeleton by reasoning on a knowledge graph in multiple-hops. (2) they try to realize the reaoning path in knowledge graph intp text. 

### Story-line based story generation




#### [Towards Better Storylines with Sentence-Level Language Models](https://arxiv.org/abs/2005.05255)(arxiv 2020)
- this paper aims at generating coherent ending for storyline. They find that existing works generate storylines in word-level and cannot learn the dependency between sentences. Therefore, they tries to rank a set of candidate endings and select the most appropriate one as ending, instead of directly generating the ending based on context.

#### [PLOTMACHINES: Outline-Conditioned Generation with Dynamic Plot STate Tracking](https://www.aclweb.org/anthology/2020.emnlp-main.349/)(EMNLP 2020)
- this paper also studies coherent story generation. They find that existing works  



### Interaction based story generation
#### [Plan, Write, and Revise: an Interactive System for Open-Domain Story Generation](https://www.aclweb.org/anthology/N19-4016.pdf)
- This paper deveoped an interactive story generation system, where user can control the story generation and revise the generated story through the webpage interface. there are two types of interactions, one is model-cross interaction where user can choose the story generated by different models and control the diversity of story. the other one is inter-model interaction where user can modify both the story line and the story itself of the selected story, including inserting, deleting and modifying.  

#### [Cue Me In: Content-Inducing Approaches to Interactive Story Generation]()
- This paper tries to explore interactively controlling story generation in a conversation by providing the model a hint like a phrase. Existing works always generate stories in a one-shot manner where users cannot control the generation of stories. 

#### [Modeling Protagonist Emotions for Emotion-Aware Storytelling]()
- this paper studies the problem of controlling the emotion flow inside the generated stories. the control signal for emotions is a set of words expressiong emotions like joy-> anger->sadness. 

#### [Wordcraft: a Human-AI Collaborative Editor for Story Writing](https://www.seas.upenn.edu/~daphnei/EACL_wordcraft.pdf)
- this paper develop an interactive story generation system where users can ask the system to continue writing story, infilling the missing parts of story, elaborating the specified text or rewriting the specified text. 

#### [STORIUM: A Dataset and Evaluation Platform for Machine-in-the-Loop Story Generation](https://arxiv.org/pdf/2010.01717.pdf)
- this paper propose a new dataset and story evaluation platform for story generation. the existing datasets are too artificial like ROCStories, too unconstraint like the writingPrompts. therefore, they collect a story generation dataset which has 6K longform stories. each story is decomposed into different sceneries. Each scenery has annotation about character introduction, scene introduction, chanllege introduction etc.

#### [Shelley: A Crowd-sourced Collaborative Horror Writer](https://dl.acm.org/doi/pdf/10.1145/3450741.3465251)

#### [Choose Your Own Adventure: Paired Suggestions in Collaborative Writing for Evaluating Story Generation Models](https://aclanthology.org/2021.naacl-main.279.pdf)
- this paper builds a platform for comparing two story generation models and they also studies the interaction experience between users and the story generation models. They ask the users to generate a story following the hint of a given image by collaborating the story generation models. At ech turn, users will give some input and the story generation models will continuing the generation by providing two candidate story for users to choose. After story generation, a set of question related to interaction experience will be asked.

#### [IGA: An Intent-Guided Authoring Assistant](https://arxiv.org/pdf/2104.07000.pdf)
- this paper aims to insert sub sentence satisfying users' intentions such as cause, effect, contrast, description, biography, idiom, and paraphrase. e.g. it was raining [effect] trees. => it was raining, the trees were swaying and the wind was oppresive. They find existing works only focus on compele sentence in word level, therefore, they propose to compelete a sentence by infilling a sub sentence following users' intention. They extract a dataset by using some tools and use it to finetune the GPT2 model. 

#### [Plot-guided Adversarial Example Construction for Evaluating Open-domain Story Generation](https://arxiv.org/pdf/2104.05801.pdf)



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

#### [Decoding Methods for Neural Narrative Generation](https://arxiv.org/abs/2010.07375)
- this paper studies the effect of decoding method on the qulities of story. For nucleus sampling method has been thoroughly been evaluated by human and the recent advanced decoding methods used in dialog field has not been tried in story generation. Therefore, in this paper, they evlauate the effect of threshold p in nucleuns sampling on the story generation and find that the model generate higher quality story when p lies in range from 0.6 to 0.8. They also tried the Maximum  Mutual Information decoding method proposed in dialog field. They find that partially incorporating mutual information (lambda<=0.2) into the loss can benefit the interesting of the story.

### Other
#### [A Knowledge-Enhanced Pretraining Model for Commonsense Story Generation]()
- this paper studies story generation by incorporating external commonsense knowledge base. they find that the stories generated by existing models suffers the problem of repeatition, logical conflicts  and lack of long-range coherence. they assume that these problems are caused by the lack of relevant commonsense knowledge as a result, existing models cannot understand causal relationships and plan entities and events with approporate orders. therefore, they propose to emloy commonsense knowledge from external knowledge base to generate reasonable stories.

#### [Improving neural story generation by targeted common sense grounding](https://arxiv.org/abs/1908.09451)
- this paper aims to inject conmmon sense knowledge into story generation model by finetuning the models using multi-task learning. They find existing large scale can generate style and syntactic consistent text, however, it is difficult to reason about world knowledge. They introduce finetune language generation models with tranditional language modelling loss and they proposed perplexity ranking loss (maxmizing the probability of correct text and lower the probability of incorrect text).

#### [Knowledgeable Storyteller: A Commonsense-Driven Generative Model for Visual Storytelling](https://www.ijcai.org/Proceedings/2019/0744.pdf)
- this paper aims to inject commonsense knowledge into visual storytelling. different from image captioning which simply describe the contents in images, the visual storytelling requires to generate some imaginary concepts which don't appear in images. They find these imaginary concepts and the objects in images are connected by some commonsense, therefore they propose to incorporate commonsense knowledge in visual storytelling. They first extracted a set of realted knowledge graph from knowledge base and apply attention mechanism to incorporate the commonse knowledge into the story.


#### [MEGATRON-CNTRL: Controllable story generation with external knowledge using large-scale language models](https://arxiv.org/abs/2010.00840)
- this paper aims to build a controllable and knowledge grounded story generation model. They find that prevalent pretraned language models lack konwledge and unable to control. Therefore, they propose to control the story generation by incorporating the external knowledge which is extracted from external database using the specified keywords. These extracted knowledge are ranked according to their relevance to the context. The text generator will generate the text conditioning both on the context and the extracted knowledge.

#### [Inferring the Reader: Guiding Automated Story Generation with Commonsense Reasoning](https://www.aaai.org/AAAI21Papers/AAAI-10130.YuMH.pdf)
- this paper aims to generate coherent and multi-character centric stories. They find that existing works will lose coherency when generating long stories. Although some works try to solve the problem by introducing outline to guide story generation, this paper argue that their coherenece is in the outline level, and some other works solve the problem by adding external knowledge, this paper argue that the geberation heavily relies on sampling and lack the process of inference. Therefore, they introduce the inference process during generation phase. They first extract the actions and intentions from the context and the generated candidiate, and then compare whether the actions and intions in the generated story match with that in the context. if match, the candidate story will be outputted, if not, a new candidate will be generated, the above process will be repeated again.

#### [Automated Storytelling via Causal, Commonsense Plot Ordering](https://www.aaai.org/AAAI21Papers/AAAI-5719.AmmanabroluP.pdf)


#### [Counterfactual Story Reasoning and Generation](https://aclanthology.org/D19-1509/)
- this paper explores how to adjust stories to be compitable with counterfactual context. here counterfactual context refers to the case ehere some sentence has logical conflicts with its context. existing works haven't studied this problem formally. therefore they propose this task and release a dataset.

#### [Sketch and Customize: A Counterfactual Story Generator](https://arxiv.org/pdf/2104.00929.pdf)
- this paper studies counterfactual story rewriting task. they find that previous works cannot handle this problem well since they incline to find some spurious relations between the original endings and counterfactual endings. So they propose to implement this task in two stages, first they remove the words which are conflicted with the counterfactual context using Bert model and apply GPT2 model to fill in the removed words.


#### [Transformer-based Conditional Variational Autoencoder for Controllable Story Generation](https://arxiv.org/pdf/2101.00828.pdf)
- this paper explores the effectiveness and the controllability of text generation. The transformer models have achieved effectiveness in text generation while the controllability is left unsolved. Therefore, this work propose a conditional variational autoencoder by incorporating a latent vector representation into transformer.


#### [Story Realization: Exploiting Plot Events into Sentences](https://ojs.aaai.org/index.php/AAAI/article/view/6232)(AAAI 2020)
- this paper focuses on convert event sequence to sentences. they find that in existing heriarchical story plot generation procedure where event sequences are first generated and then story plots are generated conditioned on the event sequeneces, there is a problem that existing event2sentence model tends to igore the event sequence and only generate plots conditioned on its context due to the following two reasons: (1) the existing event2event model tends to generate some unseen events which would be difficult for event2sentence model to translate. (2) the sparsity of training data from events to sentences make the model can only see each type of event for limited times. Therefore, they propose an ensemble-based story generation model which tries to balance the faithfulness to the given event sequence and the interesting degree of the story.

#### [Learning to Control the Fine-grained Sentiment for Story Ending Generation](https://aclanthology.org/P19-1603.pdf)
- this paper aims to control the sentiment of the story endings. they find existing works focus on generating coherent, reasonable and diversified story endings and ignore the sentiment. therefore, they propose to generate story endings with sentiment in different intensities. During training phase, they extract the sentiment intensity using their sentiment analyzer and during the test phase, the sentiment intensity is specified by users. their model generate endings by conditioning on the context and the sentiment intensity.

#### [Finding and generating a missing part for story completion](https://www.aclweb.org/anthology/2020.latechclfl-1.19/)
- this paper studies the story completetion problem. existing works require user to have prior knowledge about the missing position. Therefore, they propose to automatically detect the missing part of the story and then generate the missing part.

#### [T-CVAE: Transformer-Based Conditioned Variational Autoencoder for Story Completion](https://www.ijcai.org/proceedings/2019/0727.pdf)
- this paper aims to generate the missing part in the story. They find the existing works are focus on generating the end of the story, which is different from this task setting and also existing works tend to generate generic and incoherent plots. Therefore, they propose to build model on a variational autoencoder model on transformer model in order to better capture the context clues,

#### [Unsupervised Hierarchical Story Infilling](https://www.aclweb.org/anthology/W19-2405.pdf)
- this paper aims to generate the missing part in the story. They find existing works cannot well balance coherence and fluency with novelty and diversity. Therefore, they propose to infill the missing part of story in a hieracchical way by first predicting the a set of novel words from the context and based on the context and the predicted words to infill the missing part.


#### [Story Ending Generation with Incremental Encoding and Commonsense Knowledge](https://ojs.aaai.org/index.php/AAAI/article/view/4612)
- this paper aims to generate the end of a story. They propose to incremental encoder to encode the context and also the multi-source attention to incorporate the commonse knowledge into the inference of story ending. 

#### [WriterForcing: Generating More Interesting Story Endings](https://arxiv.org/abs/1907.08259)
- this paper focus on story ending generation task. they find existing seq2seq model tend to generate generic endings because of the MLE training objective. Therefore, they propose to training the model with different type of objectives, including converging loss, keyphrase-loss and inverse token frequency loss in order to encourage model to generate rare words in the story.

#### [Learning to write stories with thematic consistency and wording novelty](https://ojs.aaai.org/index.php/AAAI/article/view/3993)
- this paper aims to generate thematic consistency and novelty story. They find there is gap between the stories generated by existing models and that by humans, especially at the thematic consistency and story novelty. Therefpre, they propose to augment the CVAE with a cache module to allievate the above problems. The cache module is used to remember the text generated so far in order to solve the thematic consistency problem and the CVAE is used to enhance the novelty of the story.

#### [Generating Diverse Story Continuations with Controllable Attributes](https://arxiv.org/abs/1909.13434)
- this paper aims to generate the next sentence given the story context. They find the eixsting works control story generation from a single perspective such as sentiment, length, etc. Therefore, they try to control the attribute of the next sentence including sentiment, length, predicate, semantic frame and cluster. They suggest that their model can effectively control the attribute of the generated sentence.


#### [Fabula Entropy Indexing: Objective Measures of Story Coherence](https://arxiv.org/pdf/2104.07472.pdf)

### Evaluation

#### [Union: An unreferenced metric for evaluating open-ended story generation](https://arxiv.org/abs/2009.07602)
- this paper builds an unreferenced metric for story generation. they find existing evaluation metrics for story generation has a low correlation with human evaluation. Therefore, they proposed an unreferenced metric which is implemented with a bert model finetuned to distinguish human generated story and negative samples. They summarize the errors in stories generated by existing models including repeated plots (repeating similar texts), poor coherence (with unrelated keywords or events but a reasonable main plot), conflicting logic (wrong causal or temporal relationship), and chaotic scenes (difficult to understand or with multiple previous errors). they manually design a set of rules to construct the negative samples by introducing these errors to the human written stories. They uses these data to finetune a bert model to distinguish human written stories and negative samples.

#### [OpenMEVA: A Benchmark for Evaluating Open-ended Story Generation Metrics](https://arxiv.org/abs/2105.08920)
- this paper propose a platform for evaluating the existing evaluation metrics for open-end story generation task. Their platform can be used to analyze the performance of the story generation metrics including (a) the correlation with human judgements and the generalization to different model outputs and datasets, (c) the ability to judge story coherence, and (d) the ro- bustness to perturbations. 

#### [Narrative Incoherence Detection](https://arxiv.org/abs/2012.11157)
- this paper aims to detect the incoherence in generated stories. They mainly focus on two types of incoherence: (1) missiong sentence (2) dicordant sentence. They build a set of baselines to analyze detection ability from the token level and sentence level.  They find token level modeling has better performance on short story and sentence level modeling has a better performance on long story. They also find pretraining and auxiliary sentence prediction objecrive can improvve detection performance.

#### [Plot-guided Adversarial Example Construction for Evaluating Open-domain Story Generation](https://arxiv.org/abs/2104.05801)
- this paper aims to propose an evaluation metric for the open-ended story generation. They find that existing learnable based evaluation metrics have a higher correlation with human evaluation, however, they find that existing learnable metrics are trained with samples created by heuristically manipulating the reference stories. They argure that these heuristically created training samples could be unnatural and oversimplify the characteristics of implausible machine-generated stories. Therefore, they propose to construct the training samples by manipulating the plots of reference stories and generate the training samples with the modified plots. In order to improve the quality, they employ a adversial filtering procedure to get high-quality data.

#### [Predicting generated story quality with quantitative measures](https://www.aaai.org/ocs/index.php/AIIDE/AIIDE18/paper/viewPaper/18106)
- this paper aims to evaluate open-ended story generation. They find existing evaluation metrics are either designed for a specific model or require intensive human source. Therefore, they propose a set of story features which can reflect the quality of the stories, and then they propose a set of methods to evaluate these features.

#### [Generating Narative Text in a Switching Dynamical System](https://arxiv.org/abs/2004.03762)
- this paper 


### Emotion
#### [A Character-based Model for Interactive Storytelling in Games]()
- The paper proposes a character-driven approach to interactive storytelling, where non-player characters (NPCs) are modeled with autonomous behaviors, personalities (e.g., using the Big Five traits), and dynamic goals to influence narrative progression without rigid branching structures . Techniques like hierarchical task decomposition, neural networks for behavior prediction, and nondeterministic planning are used to generate adaptive quests that respond to player actions and traits in real-time . The model emphasizes balancing player agency with narrative coherence by integrating drama management, user modeling, and AI-driven character interactions to create emergent, emotionally engaging stories .

#### []

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


