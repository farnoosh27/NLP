## What is regular expressions

In Python, regular expressions are supported through the re module, which provides functions for working with regular expressions. The re module allows you to create regular expressions, search for patterns within strings, and perform various operations on text.

## What to do

* It is important to examine the data first to see if any patterns can be recognized so that parsing operations can be optimized.
* when using re, data in a real-world situation can often contain errant characters, and your program must correctly handle these situations.


## stopwords
In Python, regular expressions don't have a predefined set of stopwords. Stopwords are commonly used words (such as "a," "the," "is," etc.) that are often removed from text data during natural language processing tasks, such as text classification or information retrieval.

To remove stopwords from text using regular expressions in Python, you typically need to define your own list of stopwords and then utilize regular expressions to match and remove those stopwords from your text.

Here's an example of how you can remove stopwords from a text using regular expressions in Python:
```python
import re

def remove_stopwords(text, stopwords):
    pattern = r'\b(?:{})\b'.format('|'.join(stopwords))
    processed_text = re.sub(pattern, '', text, flags=re.IGNORECASE)
    return processed_text

stopwords_list = ['the', 'is', 'and', 'a', 'an']  # Example list of stopwords

text = "This is a sample text, and it contains some common words like the and is."

processed_text = remove_stopwords(text, stopwords_list)

print(processed_text)
```

stopwords_list = ['the', 'is', 'and', 'a', 'an']  # Example list of stopwords

text = "This is a sample text, and it contains some common words like the and is."

processed_text = remove_stopwords(text, stopwords_list)

print(processed_text)


Output:

sql
Copy code
This  sample text,  it contains some common words like  .
In the example above, the remove_stopwords() function takes a text and a list of stopwords as inputs. It constructs a regular expression pattern using the provided stopwords and then uses re.sub() to substitute the stopwords with an empty string. The resulting processed text is returned.

Note that the regular expression pattern \b(?:{})\b is used to match whole words. The flags=re.IGNORECASE argument is passed to re.sub() to perform a case-insensitive replacement.

You can customize the stopwords_list with your desired set of stopwords or even load a predefined set of stopwords from external libraries or resources.
### lemmatizing 
Lemmatizing is a natural language processing technique that aims to reduce words to their base or dictionary form, known as the lemma. The lemma represents the canonical or root form of a word, and lemmatization helps in normalizing words to their standard form.

In contrast to stemming, which simply removes word suffixes to reduce words to a common stem, lemmatization takes into account the part of speech (POS) of the word and applies morphological analysis to produce the correct lemma.

The process of lemmatization involves mapping a word to its lemma using linguistic knowledge and algorithms. This requires access to a dictionary or a lexical resource that provides information about word forms and their corresponding lemmas.

Here's an example to illustrate lemmatization:

Input: "The cats are running and jumping around."

Lemmatized output: "The cat be run and jump around."

In the example above, the word "cats" is lemmatized to "cat" because it represents the singular form. Similarly, "are" is lemmatized to "be" to represent the base form of the verb. The words "running" and "jumping" are lemmatized to "run" and "jump," respectively, to capture their base forms.

Lemmatization is useful for various natural language processing tasks, such as text classification, information retrieval, and sentiment analysis. It helps in reducing word variations and improving the accuracy and efficiency of text analysis by treating different forms of a word as a single entity.

Python provides several libraries and tools that offer lemmatization functionality, including NLTK (Natural Language Toolkit), spaCy, and TextBlob. These libraries often support multiple languages and provide built-in lemmatization algorithms or access to pre-trained models for lemmatization.**




### stemming vs lemmatizing 
Lemmatization:

Lemmatization aims to reduce words to their canonical or dictionary form, known as the lemma.
It takes into account the part of speech (POS) of the word and applies morphological analysis to produce the correct lemma.
Lemmatization typically produces more meaningful and linguistically valid results compared to stemming.
It requires access to a dictionary or a lexical resource that provides information about word forms and their corresponding lemmas.
Lemmatization is slower and computationally more expensive compared to stemming due to the need for POS tagging and dictionary lookups.
Example: Lemmatizing the word "running" to "run" or "better" to "good".
Stemming:

Stemming aims to reduce words to their common base or stem by removing word suffixes.
It applies simple heuristics or rule-based algorithms to remove affixes without considering the word's meaning or part of speech.
Stemming can sometimes result in non-linguistic or invalid word forms.
It doesn't require access to a dictionary or POS tagging, making it faster and computationally less expensive compared to lemmatization.
Example: Stemming the word "running" to "run" or "better" to "bet".


