# Image Caption Summary

### [Guided Open Vocabulary Image Captioning with Constrained Beam Search](https://www.aclweb.org/anthology/D17-1098.pdf)

- Problems:
  - previous models cannot be applied to out-of-domain cases
- Contribution
  - extend image caption models to out-of-domain cases
  - developed constrained beam search to inject constraints in output sequence

### [Paying More Attention to Saliency: Image Captioning with Saliency and Context Attention](https://arxiv.org/pdf/1706.08474.pdf)

- Problems:
  - when people look at an image, they tend to pay attention to salient regions
- Contribution
  - proved that teaching model to pay attention to salient regions during caption generation will improve caption quality

### [Towards Diverse and Natural Image Descriptions via a Conditional GAN](https://arxiv.org/pdf/1703.06029.pdf)

- Problems:
  - models training with MLE objective tend to generate  repeated and boring captions since it encourage the model to use n-grams appeared in training samples
  - previous works focus on fidelity and ignore other qualities like natural and diversity
  - conventional evaluation metrics tend to favor safe but restrictive way. Under these metrics, sentences that contain matched n-grams would get substantially higher scores than those using variant expressions 
  - on certain metrics, many models has surpass human
- Contributions:
  - extend GAN to caption generation

### [Fast, Diverse and Accurate Image Captioning Guided By Part-of-Speech](https://arxiv.org/pdf/1805.12589.pdf)

- Problems:
  - beam search is computational expensively and is likely to generate generic captions
  - GAN and VAE can generate diverse captions but not accurate, and its latent variables don't have exposed semantics to explicitly show the relationship between latent variables and generated captions
- Contribution:
  - proposed to generate captions based on an image and a sequence of POS

### [DenseCap: Fully Convolutional Localization Networks for Dense Captioning](https://arxiv.org/pdf/1511.07571.pdf)

- Contribution:
  - proposed  dense captioning task which generate a description for each salient region in an image
  - proposed a fully constitutional localization network to identify the salient regions

### [Improved Image Captioning via Policy Gradient optimization of SPIDEr](https://arxiv.org/pdf/1612.00370.pdf)

- Problems:
  - conventional evaluation metrics have low correlation with  human evaluation
  - MLE training objective doesn't correlate with human assessment
- Contributions:
  - applied reinforcement learning to image captions with SPICE as reward function

### [Knowing When to Look: Adaptive Attention via A Visual Sentinel for Image Captioning](https://arxiv.org/pdf/1612.01887.pdf)

- Problems:
  - conventional attention mechanism will pay attention to image at each time step irrespective of the next word.
- Contributions:
  - proposed a adaptive attention model will attend to the image features when necessary

### [Bottom-Up and Top-Down Attention for Image Captioning and Visual Question Answering](https://arxiv.org/pdf/1707.07998.pdf)

- Problems:
  - Conventional attention to each pixel of image irrespective of the content and object in an image
- Contribution:
  - Proposed a top down and bottom up attention mechanism which attend to salient objects and regions in an image

### [Describing like Humans: on Diversity in Image Captioning](https://arxiv.org/pdf/1903.12020.pdf)

- Problem: 
  - existing metrics are incapable of evaluating the semantic diversity of a group captions for the same image.
- Motivation
  - people's demands
  - avoid generating monotonous phrases
  - better fitting in with dataset distribution
- Contribution
  - proposed a diversity evaluation metric, named self-CIDEr, based on CIDEr and LSA  
  - they define diversity from three levels, contents, words and syntactic structures

### [Diverse Beam Search for Improved Description of Complex Scenes](http://web.engr.oregonstate.edu/~leestef/pdfs/diversebeam2018aaai.pdf)

### [Object Counts! Bringing Explicit Detections Back into Image Captioning](https://www.aclweb.org/anthology/N18-1198.pdf)

### [Diverse and accurate image description using a variational auto-encoder with an additive gaussian encoding space. ](https://papers.nips.cc/paper/7158-diverse-and-accurate-image-description-using-a-variational-auto-encoder-with-an-additive-gaussian-encoding-space.pdf)

### [Self-critical Sequence Training for Image Captioning](https://arxiv.org/pdf/1612.00563.pdf)

### [Show and Tell: Lessons learned from the 2015 MSCOCO Image Captioning Challenge](https://arxiv.org/pdf/1609.06647.pdf)
### [Improving Image Captioning by Leveraging Knowledge Graphs](https://arxiv.org/pdf/1901.08942.pdf)

### [Areas of Attention for Image Captioning](https://arxiv.org/pdf/1612.01033.pdf)

### [Aligning where to see and what to tell: image caption withregion-based attention and scene factorization](https://arxiv.org/pdf/1506.06272.pdf)

### [Image Caption with Global-Local Attention](https://www.aaai.org/ocs/index.php/AAAI/AAAI17/paper/download/14880/14291)

### [Show, Control and Tell: A Framework for Generating Controllable and Grounded Captions](https://arxiv.org/pdf/1811.10652.pdf)

### [Natural Language Object Retrieval](https://arxiv.org/pdf/1511.04164.pdf)











