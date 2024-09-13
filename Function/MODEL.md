

* [build_transformer](#build_transformer)
* [LayerNormalization](#layerNormalization)
* [FeedForwardBlock](#FeedForwardBlock)
* [InputEmbeddings](#InputEmbeddings)
* [PositionalEncoding](#PositionalEncoding)
* [MultiHeadAttentionBlock](#MultiHeadAttentionBlock)
* [ProjectionLayer](#ProjectionLayer)

<!-- , , , , ResidualConnection, , EncoderBlock, Encoder, DecoderBlock, Decoder, , Transformer -->

## build_transformer

- if you are import the model of the Transformer then used to this import 
```
# import the transformer model 
>>> from PSTansformer.model import build_transformer

# how to used this transformer model 
>>> build_transformer(
        vocab_src_len=vocabulary_source_length,   # vocabulary source length of sentence like tokeinzer source length of 
        vocab_tgt_len=vocabulary_target_length,    # same for the target language 
        src_seq_len=config["seq_len"],     # source language  length of you sentence like 350 
        tgt_seq_len=config['seq_len'],     # target language length of you sentence same as source length
        d_model=config['d_model']        # dimension model your language like 512
)
```

## LayerNormalization

```
>>> from PSTransformer.model import LayerNormalization

LayerNormalization(
    features:int,   # 512 features 
    eps:float=10**-5
)
```


## FeedForwardBlock

```

>>> from PSTransformer.model import FeedForwardBlock

FeedForwardBlock(
    d_model:int,       # 512 features 
    d_ff: int,         # 2048 hidden layer 
    dropout: float     # 0.1
)
```


## InputEmbeddings

```
>>> from PSTransformer.model import InputEmbeddings

InputEmbeddings(
    d_model:int,     # dimension model of your data Ex: 512
    vocab_size       # vacabulary size of you data Ex:  1000
)
```


## PositionalEncoding

```
>>> from PSTransformer.model import PositionalEncoding 

PositionalEncoding(
    d_model: int,      # 512
    seq_len: int,      # 2000
    dropout: float     # 0.1
)
```


## MultiHeadAttentionBlock

```
>>> from PSTransformer.model import MultiHeadAttentionBlock

MultiHeadAttentionBlock(
    d_model: int,          # 512
    h: int,                # 8
    dropout: float         # 0.1
)
```




## ProjectionLayer

```
>>> from PSTransformer.model import ProjectionLayer 


ProjectionLayer(
    d_model: int,   
    vocab_size:int

)
```

