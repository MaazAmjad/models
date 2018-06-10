# Pretrained Word2vec model on web news data .

## Model Description

- Model trained on 50,000 urdu news posts from different categories.
- Model vector size is 300.
- Download link (https://drive.google.com/uc?export=download&id=13KLg3wUTOwWiF_YdAtZFe18j7MQmOWfb)
- Model can be load using python gensim package.

## Code

```python

import gensim, logging
logging.basicConfig(format='%(asctime)s : %(levelname)s : %(message)s', level=logging.INFO)


model = gensim.models.KeyedVectors.load_word2vec_format('urdu_web_news_vector300.bin', binary=True)

print(model.most_similar("پاکستان"))
[('افغانستان', 0.534391462802887)
, ('پاکستانی', 0.527515172958374)
, ('بھارت', 0.5176973342895508)
, ('زمبابوے', 0.5033701062202454) ]

print(model.most_similar(positive=['دہلی', 'پاکستان'], negative=['پنجاب'],topn=5))
[('دلی', 0.47923001646995544)
, ('انڈیا', 0.4310738444328308)
, ('بھارت', 0.4303123652935028)
, ('پاکستانی', 0.42918506264686584)
, ('بیجنگ', 0.42072150111198425)]

```