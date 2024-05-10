# amharic-news-category-classification
This github repo that contains three notebooks that use the [amharic-news-category-classification](https://huggingface.co/datasets/rasyosef/amharic-news-category-classification) dataset to finetune the following models for a text classification task.

The finetuned model classifies a given Amharic news article into one of the following 6 categories.
- ሀገር አቀፍ ዜና (Local News)
- መዝናኛ (Entertainment)
- ስፖርት (Sports)
- ቢዝነስ (Business)
- ዓለም አቀፍ ዜና (International News)
- ፖለቲካ (Politics)

## Models

* [xlm-roberta-base](https://huggingface.co/FacebookAI/xlm-roberta-base) : a multilingual transformer model with 280M parameters
* [bert-small-amharic](https://huggingface.co/rasyosef/bert-small-amharic) : a new amharic version of the bert-small transformer model with 25.7M parameters, pretrained from scratch using unlabelled amharic text data
* [bert-mini-amharic](https://huggingface.co/rasyosef/bert-mini-amharic) : a new amharic version of the bert-mini transformer model with 9.67M parameters, pretrained from scratch using unlabelled amharic text data

### Fine-tuned Model Performance
Since this is a multi-class classification task, the reported precision, recall, and f1 metrics are macro averages.

|Model|Size (# params)|Accuracy|Precision|Recall|F1|
|-----|----|--------|---------|------|--|
|xlm-roberta-base|279M|0.9|0.88|0.88|0.88|
|bert-small-amharic|25.7M|0.89|0.86|0.87|0.86|
|bert-mini-amharic|9.67M|0.87|0.83|0.83|0.83|