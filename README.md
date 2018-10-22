# Text-CNN-Toxic-Comment-Classification
Using text CNN and other methods to classify toxic comments

## Introduction

The dataset for this project came from [Jigsaw Toxic Comment Classification Challenge on Kaggle](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/). I also participated in the challenge and submitted prediction, but the focus was on exploring  _CNN on text_ and comparing it's performance with other methods.

## Challenge
The challenge task was to given a comment predict probabilities for 6 toxic comment classes. The classes where toxic, severe_toxic, obscene, threat, insult, identity_hate. Comment can be classified in more than on those classes, hence the probability for each class is independent (in theory, in practice most comments were also classified toxic if they fall under any other class). The evaluation was the mean of area under [ROC curve](https://en.wikipedia.org/wiki/Receiver_operating_characteristic) for each class.

## Results

Note: Higher is better. The practical range is from 0.5 to 1, with 0.5 being random coin toss and 1 being perfect classification.

|Model|Mean Area Under ROC Curve|
|-----|-------:|
|Bidirectional LSTM|0.9686|
|NB SVM + Bigam Features|0.9762|
|Text CNN with 2 fully connected layers|0.9745|
|**Optimized text CNN**|**0.9771**|
