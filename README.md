## Description
A small computer vision project in the making. Our goal is to create a simple CNN Keras model to recognize handwritten characters (letters and digits).

## Datasets
[EMNIST](https://arxiv.org/abs/1702.05373) ByMerge and ByClass database /n
[IAM Handwritten Dataset](http://www.fki.inf.unibe.ch/databases/iam-handwriting-database)

## Libraries and framework
* Tensorflow
* OpenCV
* Numpy
* Pandas
* craft-text-detection
* dhsegment

## Progress
We divided our preprocess into several steps of extracting baseline, lines, words, characters:
* For baseline extraction: we employ [dhsegment](https://dhsegment.readthedocs.io/en/latest/start/demo.html) pretrained models.
* To extract lines, we make use of [simple text line extraction](https://github.com/CrazyCrud/simple-text-line-extraction).
* We rely on [CRAFT](https://github.com/clovaai/CRAFT-pytorch) - a PyTorch based model of Clova AI Research to detect words and character text region. 

Each character will be converted to MNIST-like input to be classified.

We developed a CNN model on EMNIST (Extended-MNIST) dataset that returns 91.30% accuracy for EMNIST Bymerge and 88.20% for EMNIST Byclass. However, our current models are not performing well on non-EMNIST testing dataset. We used CRAFT to extract character images from the IAM dataset as a data augmentation method and currently training a new model on the new dataset.

## To-Do
Train a new model on the new dataset. /n
Add RNN for auto correction of words.

## Authors and acknowledgement
* **Minh Quan Huynh**: [hmq1812](https://github.com/hmq1812)
* **Khanh Tran Pham Gia**: [khanhtran2000](https://github.com/khanhtran2000/)
* **Duc Minh Hoang**: [minhduchoang301](https://github.com/minhduchoang301/)