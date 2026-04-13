# **MODEL ARCHITECTURE**

- The Transformer model technically consists of an encoder and decoder

- In the paper the N=6 value for stack in an encoder essentially indicates the number of specialized layers they have used for the paper to train the model. 6 here is not a constant and differs based on model requirements and needs but this was used here to show essentially how good the architecture of the model was.

*ENCODER:*

- Each layer has 2 sub layers->Multi Head Attention(Relations between words)  & Feed Forward Network(Understanding of each word).

*DECODER:*

Each layer has 3 sub-layers->Masked Multi Head Attention, Multi Head Attention  & Feed Forward Network.

## **WORKING:**

- The inputs are converted into input embeddings.

- Positional encoding is applied on these input embeddings to make sure that the model is aware about the sequence of the inputs while looking at the input at a glance.

- Multi-Head attention does its work and calculates contextual relationships in the input.

### *RESIDUAL CONNECTIONS / SKIP CONNECTIONS:*
- The output from the Multi-Head Attention layer is added to the input embeddings of the specific sub layer{Output = Layer Norm (x + Sublayer(x))}. This is done to avoid losing the original message while calculating the attention heads also done to avoid the vanishing gradient problem encountered previously in RNNs. The output is further normalized to stop it from becoming too large or too small.

- In the Feed Forward Layer, each of the words are processed and given a meaning or value based on the contextual relationships discovered by the Multi-Head Attention Mechanism. This acts essentially as the brain of the model as it updates the internal meaning of each word.

