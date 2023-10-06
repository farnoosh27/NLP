## Encoder Layer:

### Self-Attention Focus:
The multi-head self-attention mechanism in the encoder primarily focuses on capturing relationships between words within the **input sequence**. It helps the encoder understand how words in the input are related to each other.
### No Masking:

In the encoder, the **self-attention mechanism is not masked**. Each word in the input sequence can attend to all other words in the sequence, both left and right, without restrictions.
### Position of Interest:

The encoder's role is to create contextual representations of the input sequence. It captures the overall meaning and context of the input data.
## Decoder Layer:

### Self-Attention Focus:

In the decoder layer, the multi-head self-attention mechanism focuses on capturing relationships between words within the **target sequence** being generated. However, it is **masked** to prevent the decoder from "looking ahead" into future words during training. This masking ensures that the decoder generates one word at a time in an autoregressive manner.
### Masked Self-Attention:

The masking in the decoder's self-attention mechanism ensures that each word in the target sequence can only attend to words to its left (previous positions) during training. This autoregressive constraint is crucial for proper word generation.
### Position of Interest:

The decoder's primary role is to generate the target sequence based on the information in the encoder's contextual representations. It ensures that the generated sequence is coherent and contextually relevant.
In summary, while encoder and decoder layers share some architectural components like multi-head self-attention and layer normalization, their roles and behaviors differ significantly. The encoder focuses on understanding the input sequence, whereas the decoder uses the encoder's output to generate a target sequence while adhering to an autoregressive constraint. The masking of self-attention in the decoder is a critical distinction that enables autoregressive generation.


**Masking in Encoder and Decoder Multi-Head Attention**

In the Transformer architecture, masking is applied differently in the multi-head attention mechanisms of the encoder and decoder due to their distinct roles and requirements in sequence-to-sequence tasks.

**Encoder**:

- In the encoder, masking is not typically applied in the self-attention mechanism. The encoder's primary role is to create contextual representations of the input sequence. It's designed to capture relationships between words in a bidirectional manner, allowing each word in the input sequence to attend to both previous and future words.
- For tasks like text classification, where the model needs to understand the entire context of a sentence, bidirectional encoding without masking is beneficial.

**Decoder**:

- In contrast, masking is crucial in the decoder due to its autoregressive nature. The decoder generates the target sequence one token at a time, and each token's prediction depends on previously generated tokens. During training, the model should not have access to future words in the target sequence to maintain the autoregressive constraint.
- To achieve this, the self-attention mechanism in the decoder is masked. Specifically, a triangular mask is applied to the attention scores, setting future positions to very small or negative values. This masking ensures that each token in the decoder can attend only to the left-context (previously generated words) when making predictions.



