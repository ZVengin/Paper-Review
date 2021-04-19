# Summary

## Length Control
### [Positional Encoding to Control Output Sequence Length](https://www.aclweb.org/anthology/N19-1401/)
 - what: control the length of generated text
 - motivation: (1) length control is needed in text generation to satisfy space constraint. (2)existing works cannot control text length unseen in training data
 - novelty: instead of specifying each type of length control signal as a specific embedding, they extend the positional embedding of transformer decoder. they modified the position embedding to represent the distance to the last token. In this way, at each step, the model knows when to step.
 - significance: their method has the potential to control arbitray length text
 - Further: sometimes users may not have very clear idea about how many characters to generate, therefore, a coarse control on length, i.e. generating text whose length is with some specified range. 
