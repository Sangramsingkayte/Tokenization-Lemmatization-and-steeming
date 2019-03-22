# Tokenization-Lemmatization-and-steeming
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
First apply Tokenization (a text is divided into token), we can use open source tools like NLTK to get tokens from the text

from nltk.tokenize import word_tokenize

text = "I love Programming"
word_tokenize(text)

checkout this example

text = "I love programming and programming also loves me"
word_tokenize(text)

so here we have the programming repeated twice as tokens but we only take once so the features for this text are → I , love, programming, and, also, loves, me.

but wait the words love and loves mean same , these are called inflectional forms. we need to remove these

removing these inflectional endings is called lemmatization

from nltk.tokenize import word_tokenize  
text = "I love programming and programming also loves me"
tokens=word_tokenize(text)

from nltk.stem import WordNetLemmatizer
lemmatizer = WordNetLemmatizer()
[lemmatizer.lemmatize(word) for word in tokens]


so now the features for this text are → I , love, programming, and, also,me.

we can even think deep and say the word programming is similar to the word program

there is a concept called Steeming

from nltk.stem import PorterStemmer
from nltk.tokenize import word_tokenize
text = "I love programming and programming also loves me"
tokens=word_tokenize(text)

ps = PorterStemmer()
tokens=[ps.stem(word) for word in tokens]
print(tokens)


so now the features for this text are → I , love, program, and, also,me.

there are couple of words which occur very frequently in every language and don’t have much meaning , these words are called Stop words.

The stop words in English are


