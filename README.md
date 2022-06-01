# NLP: Question&Answering in Italian
In this repository I have collected some of the work done on developing a model, based on **Transformers**, for the Q&amp;A task in Italian Language.

## Intro
The successful development of an NLP model depends on the availability of large datasets that you can use to train your model.
For the Q&A task the most famous dataset is the **SQUAD** dataset, in English.

An Italian version of this dataset is available, called **Squad-it**. It has been obtained through semi-automatic translation and is available in the HuggingFace HUB.

In this repository I have collected the code used to develop a Model base on BERT, trained on Italian language, and fine tuned on Squad-it.

## The Q&A task.
In the NLP field several tasks have been defined. The most commonly known is the "Topic" classification task. Sentiment Analysis is a variant of this task.
But there are some more complicated tasks that can be successfully executied today. Question&Answering (Q&A) is one of them.

Within Q&A you have a text document (called the "context") and you waant that your model is able to answer questions based on the context.

One of the way to execute this task is with **"Extractive Question&Answer"**, where you highlight the portion of the context that provides the answer.

## The power of Transfer Learning applied to Q&A.

I have started from a model, available on HF HUb, trained on Italian language.
The model is: dbmdz/bert-base-italian-xxl-cased

Then, the Transformer has been fine-tuned on Italian **SQuAD-it** dataset, again available on HF Hub.

## Metrics.

With 2 epochs these are the result obtained so far:

* EM: 63.57
* F1: 75.16




