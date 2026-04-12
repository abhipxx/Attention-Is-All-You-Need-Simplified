# **ATTENTION IS  ALL YOU NEED** 

## **Basic Idea**
->Models before used RNN(Recurrent Neural Networks) LSTM(Long Short-Term Memory) for the attention mechanism.
(vanishing gradient problem, tokens are processed one by one, word by word)
->Problems arose when models forgot the initial part of what is being learnt due to their short memory.
->The TRANSFORMER Model that was introduced in the paper is one of the logics used behind 99%  of the models and it introduced the concept of SELF-ATTENTION.(Parallelism)
->SELF ATTENTION mechanism is the process through which attention weights are assigned to understand the relations between tokens.
->While learning through transformers, it ensures that the words similar to each other are mapped in a vector space so they can use the relationships as needed when the model is used.
->It also introduces the concept of MULTIHEAD Attention which basically is running of several SELF-ATTENTION heads parallelly.


## **TRANSFORMERS:**

- They introduce the concept of parallelism which technically increases speed.

- Unlike RNN and LSTM they do not process word by word. They look at a sentence at once.

- So initially each word is provided a fixed value(STATIC EMBEDDING) then the self head mechanism provides it with CONTEXTUAL EMBEDDINGS.

## **INTRODUCTION:**

*SEQUENTIAL DEPENDENCY OF RNNs:*
- RNNs process one word at a time in a specific order. So when they do that essentially the calculation of let's say the 10th word depends on the calculation of the 9th word and so on. This will be a major problem if the sequence is too big and especially in real life we don't necessarily always deal with such short sequences.  {they generate a sequence of hidden states h(t), as a function of the previous hidden state h(t−1) and the input for position t.}

*VANISHING GRADIENT OF RNNs:*
- RNNs essentially forget the initial words by the time they reach the 1000th word, this is the vanishing gradient problem. As the initial value has been multiplied by so many fractions to reach the 1000th value it essentially diminishes which leads to wrong predictions by models. It stops learnign how to process early information.

## **BACKGROUND:**

- So at the time instead of using RNNs or LSTMs people switched to CNNs which is the basis for image processing to use for text as well.
- The other technologies at that time used were
   * Conv2S (Created by meta) -O(n) -Used concept of Sliding Windows.
   * ByteNet (DILATED CONVOLUTIONS)-O(log(n)) -Used pyramid skipping structure

-On the other hand, TRANSFORMERS achieved O(1) time complexity [Path length between any two positions]. But this costed a low resolution due to the weighted average of attention positions. So to overcome this issue of low resolution , multihead attention mechanism which looks over multiple parts in a single sentence like sematic, syntactic, anaphoric meaning as introduced.

## *SELF-ATTENTION(INTRA-ATTENTION):*
Relates different positions of a single sequence in order to represent computation of a sequence.
