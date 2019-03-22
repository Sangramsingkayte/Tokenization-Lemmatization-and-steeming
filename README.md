# Tokenization-Lemmatization-and-steeming
Natural language processing
The main goal here is , we wanna make the computer understand the language as we do and we wanna make the computer respond as we do.

We can break that into 2 sections

Natural language understanding:
The system should be able to understand the language(parts of speech, context , syntax , semantics, interpretation and etc…)

This can typically be done with the help of machine learning( Although problems are there).

Not much difficult to do and gives good accuracy results.

2. Natural language generation:

The system should be able to respond / generate text (text planning, sentence planning, producing meaningful phrases and etc…)

This can be done with the help of deep learning as deep understanding is required( Although problems are there).

much difficult to do and the results may not be accurate.

so where do we use ML in NLP???
These are the couple of applications where we focus

Text classification and clustering
Information retrieval and extraction
Machine translation(one language to another)
Question and answering system
spelling and grammar checking
Topic modeling and sentiment analysis
Speech recognition
I will try to explain and complete all the topics in next following stories , in this story we learn the basic fundamentals for text/document which is common for many applications.

Note: Assume now that Text , data, document,sentence and paragraph all are same.

What is a text ??
A text is a set words sequentially written.

Each word in the text has a meaning where the text may or may not have a meaning.

in machine leaning we take features right? so here each word is a feature(unique).

Ex :

Text : I love programming → I , love, programming are the features for this input.

How do we derive the features??
First apply Tokenization (a text is divided into token), we can use open source tools like NLTK to get tokens from the text.
