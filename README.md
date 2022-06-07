# NLP: Question&Answering in Italian
In this repository I have collected some of the work done on developing a model, based on **Transformers**, for the Q&amp;A task in Italian Language.

## Intro.
The successful development of an NLP model depends on the availability of large datasets that you can use to train your model.
For the Q&A task the most famous dataset is the **Stanford Querying and Answering** dataset (SQuAD), in English.

An Italian version of this dataset is available, called **squad_it**. It has been obtained through semi-automatic translation and is available in the HuggingFace HUB.
You can find info on this dataset here: https://huggingface.co/datasets/squad_it

In this repository I have collected the code used to develop a Model, based on BERT, trained on Italian language, and fine tuned on Squad_it.

## The Q&A task.
In the NLP field several tasks have been defined. The most commonly known is the "Topic Classification" task. Sentiment Analysis is a variant of this task.

But there are some more complicated tasks that can be successfully executed today. Question&Answering (Q&A) is one of them.

Within Q&A you have a text document (called the "context") and you want that your model is able to answer to questions based on the context.

One of the way to execute this task is with **"Extractive Question&Answer"**, where you highlight the portion of the context that provides the answer.

## The power of Transfer Learning applied to Q&A.

I have started from a model, available on HF Hub, trained on Italian language.

The model is: **dbmdz/bert-base-italian-xxl-cased**

You can find information regarding the pre-trained model here: https://huggingface.co/dbmdz/bert-base-italian-xxl-cased

Then, the Transformer has been fine-tuned on Italian **SQuAD-it** dataset, again available on HF Hub.

## Metrics.

With 2 epochs these are the results obtained so far:

| Metric | Value |
|--------|-------|
|   EM   | 63.95 |
|   F1.  | 75.27 |

## Training time.

The Italian squad_it dataset is not so big.

Using a **GPU V100** the training for 3 epochs takes around **40 mins**.

## Demo with UI
I have developed a simple demo. The UI is build using the nice library [**Gradio**](https://github.com/gradio-app/gradio)

The NoteBook with the demo is [here](https://github.com/luigisaetta/nlp-qa-italian/blob/main/demo_qa_model.ipynb)

## Wiki.
This repo has a Wiki. I'll update every time I have new details to document.

If you want more info on the details, or want to download the trained model, go to the Wiki.




