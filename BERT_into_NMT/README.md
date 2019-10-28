# Papago: Engineering BERT into NMT

## Machine Translation Challenges

* Context Based Translations

* Model Robustness

* Evaluation is difficult

* No click logs

## Introducing BERT

* Key ingredient of many NLP models/papers

## Combining BERT and NMT

* User bert as the fisrt layers of nmt - encoder
* can easily work for encoder and decoder
* Cans reuse bert /elmo etc
* deep encoders

## BERT Setup

* 6 Layers BERT Encoder  | to be fail with NMT encoder
* Relu and Sinusoidal emdedding    | like original transformer
* MASK=UNK token    | to test robustness
* MLM Task only  | NSP had no impact

## BERT training datasets

IWSLT, WMT14-En-De, Wiki, news

News.FT? News.Emb?

## IWSL
