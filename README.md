# This is Transformer 




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




- if you import the Tensor dataset function, which is convert the tensor data from raw data 
```
# import the Tensor dataset Function
>>> from PSTansformer.dataset import BilingualDataset

# how to used this Tensor dataset which is convert to the Tensor of the row data 
>>> BilingualDataset(
        ds=train_dataset_raw,   # raw dataset like='Ram eats mango'
        tokenizer_src=tokenizer_source,  # source language tokenizer 
        tokenizer_tgt=tokinzer_target,   # target language tokenizer
        src_lang=config['lang_src'],      # source language like engish
        tgt_lang=config['lang_tgt'],     # target language like Hindi
        seq_len=config['seq_len'])      # sequence length like 350
```

- how to used the train model 
```
def get_config():
    return {
        "batch_size": 8,
        "num_epochs": 20,
        "lr": 10**-4,
        "seq_len": 350,
        "d_model": 512,
        "datasource": 'opus_books',
        "lang_src": "en",
        "lang_tgt": "it",
        "model_folder": "weights",
        "model_basename": "tmodel_",
        "preload": "latest",
        "tokenizer_file": "tokenizer_{0}.json",
        "experiment_name": "runs/tmodel"
    }
```

```
    config = get_config()
    train_model(config)
```
