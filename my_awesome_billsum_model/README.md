---
license: apache-2.0
base_model: t5-small
tags:
- generated_from_trainer
datasets:
- billsum
metrics:
- rouge
model-index:
- name: my_awesome_billsum_model
  results:
  - task:
      name: Sequence-to-sequence Language Modeling
      type: text2text-generation
    dataset:
      name: billsum
      type: billsum
      config: default
      split: ca_test
      args: default
    metrics:
    - name: Rouge1
      type: rouge
      value: 0.1117
---

<!-- This model card has been generated automatically according to the information the Trainer had access to. You
should probably proofread and complete it, then remove this comment. -->

# my_awesome_billsum_model

This model is a fine-tuned version of [t5-small](https://huggingface.co/t5-small) on the billsum dataset.
It achieves the following results on the evaluation set:
- Loss: 2.9403
- Rouge1: 0.1117
- Rouge2: 0.0199
- Rougel: 0.0955
- Rougelsum: 0.0951
- Gen Len: 19.0

## Model description

More information needed

## Intended uses & limitations

More information needed

## Training and evaluation data

More information needed

## Training procedure

### Training hyperparameters

The following hyperparameters were used during training:
- learning_rate: 2e-05
- train_batch_size: 8
- eval_batch_size: 8
- seed: 42
- optimizer: Adam with betas=(0.9,0.999) and epsilon=1e-08
- lr_scheduler_type: linear
- num_epochs: 20

### Training results

| Training Loss | Epoch | Step | Validation Loss | Rouge1 | Rouge2 | Rougel | Rougelsum | Gen Len |
|:-------------:|:-----:|:----:|:---------------:|:------:|:------:|:------:|:---------:|:-------:|
| No log        | 1.0   | 10   | 4.4002          | 0.1333 | 0.0378 | 0.1094 | 0.109     | 19.0    |
| No log        | 2.0   | 20   | 3.8225          | 0.1325 | 0.0351 | 0.1085 | 0.1081    | 19.0    |
| No log        | 3.0   | 30   | 3.5343          | 0.1343 | 0.0361 | 0.1109 | 0.1109    | 19.0    |
| No log        | 4.0   | 40   | 3.3920          | 0.1253 | 0.0307 | 0.1069 | 0.1067    | 19.0    |
| No log        | 5.0   | 50   | 3.2849          | 0.1239 | 0.0275 | 0.1028 | 0.103     | 19.0    |
| No log        | 6.0   | 60   | 3.2041          | 0.1227 | 0.0237 | 0.1015 | 0.1016    | 19.0    |
| No log        | 7.0   | 70   | 3.1439          | 0.1234 | 0.0218 | 0.1022 | 0.1023    | 19.0    |
| No log        | 8.0   | 80   | 3.0979          | 0.1286 | 0.026  | 0.1057 | 0.106     | 19.0    |
| No log        | 9.0   | 90   | 3.0624          | 0.1298 | 0.0289 | 0.1048 | 0.105     | 19.0    |
| No log        | 10.0  | 100  | 3.0351          | 0.1286 | 0.0299 | 0.105  | 0.1053    | 19.0    |
| No log        | 11.0  | 110  | 3.0135          | 0.1292 | 0.0288 | 0.1066 | 0.1068    | 19.0    |
| No log        | 12.0  | 120  | 2.9956          | 0.1148 | 0.0195 | 0.0942 | 0.0938    | 19.0    |
| No log        | 13.0  | 130  | 2.9813          | 0.1167 | 0.0195 | 0.0943 | 0.0939    | 19.0    |
| No log        | 14.0  | 140  | 2.9697          | 0.1129 | 0.0204 | 0.0935 | 0.093     | 19.0    |
| No log        | 15.0  | 150  | 2.9606          | 0.1129 | 0.0204 | 0.0935 | 0.093     | 19.0    |
| No log        | 16.0  | 160  | 2.9534          | 0.1125 | 0.0198 | 0.0934 | 0.0931    | 19.0    |
| No log        | 17.0  | 170  | 2.9478          | 0.1117 | 0.0199 | 0.0955 | 0.0951    | 19.0    |
| No log        | 18.0  | 180  | 2.9436          | 0.1117 | 0.0199 | 0.0955 | 0.0951    | 19.0    |
| No log        | 19.0  | 190  | 2.9411          | 0.1117 | 0.0199 | 0.0955 | 0.0951    | 19.0    |
| No log        | 20.0  | 200  | 2.9403          | 0.1117 | 0.0199 | 0.0955 | 0.0951    | 19.0    |


### Framework versions

- Transformers 4.35.2
- Pytorch 2.2.0.dev20231123
- Datasets 2.15.0
- Tokenizers 0.15.0
