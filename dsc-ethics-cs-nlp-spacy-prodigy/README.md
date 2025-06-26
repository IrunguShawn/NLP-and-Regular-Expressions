# Case Study: NLP with spaCy and Prodigy

## Introduction
Labeled data for natural language processing models often has ethical implications when humans apply labels to the data. It is important to question the methodology applied to derive the labels when using data for observational studies. When creating your own labels, it is important to have a deep understanding of the field of study in order to apply labels with the most accuracy.

However, as data sets get exponentially larger (especially when it comes to language data) you can use statistical techniques and create a semi-supervised "__human-in-the-loop__" processes to apply your labels. This saves time and resources, allowing researchers that are experts in their subject area to apply labels efficiently, instead of spending countless hours manually applying and reviewing labels.

In this case study, you will learn how spaCy and Prodigy offer researchers and developers the tools to use powerful language models that are customized for their use case and/or create their own custom models from scratch. This can help avoid some of the security issues, reliability issues, and ethical pitfalls of employing third-parties like MTurk for labeling tasks. 

## Learning Objectives
You will be able to...
* Discuss uses for spaCy and Prodigy and how they improve the reliability of language models
* Locate spaCy and Prodigy resources.

## What are spaCy and Prodigy?

### spaCy
spaCy is a free, open-source library for advanced Natural Language Processing (NLP) in Python. Unlike other NLP libraries in Python, spaCy is specifically designed for __production__ (instead of reasearch, like NLTK). It uses Cython to maximize the available computing resources and avoid some of the processing bottlenecks that can occur when working with a lot of text data. 

According the the creators:
> "spaCy is designed specifically for production use and helps you build applications that process and “understand” large volumes of text. It can be used to build information extraction or natural language understanding systems, or to pre-process text for deep learning."

In addition spaCy is very user friendly and follows the basic rules of the Python syntax. You can use regular expressions within spaCy to create powerful patterns and populate custom vocabularies for tasks like POS-tagging, Named Entity Recognition, and more.

spaCy is powered by ongoing research by experts in computational linguistics. The developers at spaCy are apply concepts from cutting edge research, and optimize their application to quickly process large datasets using the library. The project is funded by a proprietary software known as Prodigy, which offers a powerful annotation tool.


### Prodigy
Prodigy is proprietary software (__not__ free or open-source) offered by the creators of spaCy. It is geared towards researchers that want to save time on quantitative coding in order to label large datasets. Prodigy provides a modern annotation tool for creating training and evaluation data for machine learning models with a user friendly interface. This beneficial for human-in-the-loop approach in NLP workflows.

#### What is a Human-in-the-Loop approach?
The human-in-the-loop approach is a semi-supervised technique that uses statistical methods to label a large dataset, based on a small amount of labeled training data. Researchers run the model and analyze the results of the machine generated labels for accuracy. Then, the model adjusted based on their findings. The model is run again with the updated parameters, and the results are audited once again. This process continues until the model has reached a satisfactory level of accuracy. 

#### How does Prodigy makes the Human-in-the-Loop approach more efficient?
Prodigy improves human-in-the-loop workflows for researchers building NLP models with their efficient and user friendly annotation tool. This eliminates some of the common challenges that researches face when building custom NLP pipelines and models, such as:
* fair labor/security concerns from using MTurk or other HITS services
* lack of domain knowledge from annotators
* decision fatigue from human annotators that compromises data integrity.

The reason why Prodigy's annotation tool is so powerful, is that it automatically selects edge cases from the labeled datasets and judiciously presents them to the human annotator. This means that the human annotator only has to label or correct a few edge cases to "retrain" the model. Prodigy is able to do this by using __similarity metrics__ and __blocking techniques__ to assess the similarity between examples. Examples that have the least in common with any of known data are classified as edge cases.

#### Try Prodigy
To see how simple it is to annotate text data for machine learning in Prodigy, [check out the demo on the Prodigy website](https://demo.prodi.gy/?=null&view_id=ner_manual). This page is a working example of how the annotation tool works. One of the coolest things is that developers can customize the appearance of their interface and use Prodigy's many __recipes__ to build customized workflows for novel tasks.


## Summary
Natural language processing is a rapidly advancing field of artificial intelligence that is fueled by increasingly complex language models. There are many use cases where these technologies can be improve our ability to make data-driven decisions in business and government. Poorly labeled data compromises data integrity and can severly undermine our ability to extract value from text. Tools like Prodigy build on the spaCy NLP production framework to provide researchers with intelligent annotation tools that save resources during the labeling process. They also allow us to avoid some common ethical pitfalls associated with using HITS services like MTurk. 
