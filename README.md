# Qestion_QA

Artificial intelligence models for reading documents and answering questions

File: document_qa_demo.ipynb

#### This file is mainly used to learn some functions in pipline, such as calling some pre-trained model, model-to-input transformations, e.g. 'tensors' and 'logits'. They are the main recognition types in Transformers.

```python
raw_inputs = [
    "I enjory my intership time in BOPRC.",
    "I like it so much!",
]
inputs = tokenizer(raw_inputs, padding=True, truncation=True, return_tensors="tf")
print(inputs)
```

Here, any two sentences can be written in raw_inputs, with some forward or reverse expression. After that the inputs returned to me processed by the 'AutoTokenizer' model with distilbert-base-uncased-finetuned-sst-2-english as a checkpoint look like this:

```Python
{'input_ids': <tf.Tensor: shape=(2, 14), dtype=int32, numpy=
    array([[  101,  1045,  4372,  5558,  2854,  2026,  6970,  9650,  2051,
            1999, 29432, 11890,  1012,   102],
        [  101,  1045,  2066,  2009,  2061,  2172,   999,   102,     0,
                0,     0,     0,     0,     0]], dtype=int32)>,
'attention_mask': <tf.Tensor: shape=(2, 14), dtype=int32, numpy=
    array([[1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1],
        [1, 1, 1, 1, 1, 1, 1, 1, 0, 0, 0, 0, 0, 0]], dtype=int32)>}
```
