# Pretrained Word2vec model on web news data .

## Model Details

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

```