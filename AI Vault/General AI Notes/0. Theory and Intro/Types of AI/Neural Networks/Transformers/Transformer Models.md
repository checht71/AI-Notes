Transformers are the cutting edge in neural networks as of 2023. Models such as ChatGPT are considered transformer models.

[Great video on how GPT-3 works](https://www.youtube.com/watch?v=MQnJZuBGmSQ)

### Replacement for Recursive
Transformers specialize in processing long sequences as inputs. Previously, recursive models were used to try and process long sequences such as sentences, but the amount of processing time would increase exponentially in relation to the length of the input because the model would recursively call itself for every word or whatever unit the input sequence was split into.

### How Transformers Work
Transformers take the input sequence and split it into elements much like the older recursive models. The input sequence is broken down into a numerical representation which includes data about the element AND the elements next to it. The *transformed* data is passed on to a different neural network to a different section of the network for classification and generation. 

> [!tip] Transformers are *not only* for text generation.
>  Transformers are ***layers*** of a network much like convolutional layers. This allows for classification applications such as Vision Transformers (ViTs). CNNs are Naive Neural Networks with convolutional layers added to them, ViTs are Convolutional Networks with Transformer layers added on top.
>  [More on ViTs here](https://towardsdatascience.com/are-transformers-better-than-cnns-at-image-recognition-ced60ccc7c8)

### Word Embedding
Word Embedding is transforming words into numbers. It is the underpinning of all LLMs. The words are embedded by their spelling as well as their position within a sentence. Words that are commonly used within the same context are more closely clustered within these embeddings.

![[Word Embeddings LLM.png]]
