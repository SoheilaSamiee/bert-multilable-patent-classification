# bert-multilable-patent-classification
Multilabel classification of patents (based on their highest level IPC classification) using BERT



Requirements
------------

Install requirements text classification with pip:

```
pip install numpy pytorch scipy pandas pytorch_pretrained_bert fastai pandas tqdm apex
```
(You can use anaconda or other tools depending on your Python installation.)

Dataset
-----------
You should download one or a group of patent xml files from https://bulkdata.uspto.gov for this project.
The current version of the code works with "ipg210105.xml", that can be downloaded from:
https://bulkdata.uspto.gov/data/patent/grant/redbook/fulltext/2021/
After downloading, you should unzip it and put in "/data" folder.
(Because of its large size it is not included in this repository.)

Experiments
-----------

Run models:

```
cd codes
python3 patent_classification.py
```

This model is fine tuned and tested on one US patent file (ipg210105.zip), but you can download more datasets from https://bulkdata.uspto.gov/data/patent/grant/redbook/fulltext/2021/. 
In that case, you should first parse the patent:

```
cd codes
python3 parse_patent.py
```
(Jupyter notebook version is also available: data/patent_parsing.ipynb)

and then pre-process and split your dataset:
```
cd codes
python3 patent_classification.py
```
(Jupyter notebook version is also available: codes/data_preproc.ipynb)


Trained Models
-----------

The fine-tuned BERT model for Patent classification can be downloaded from:
```
trained_models/bert/fine_tuned_models
```
