# NLP, MLOps and Telecommunication 

## Purpose
NLP involves extracting information from text in order to leverage it for downstream applications:


I am trying to specialize in Natural Language Processing for the purpose of my job, so here is the repository! 
The core concepts are as follows:

* Tokenization: The process of breaking down a text or sentence into smaller units, called tokens. Tokens can be words, phrases, or even individual characters, depending on the level of granularity required.

* Part-of-Speech (POS) Tagging: Assigning grammatical tags to each word in a sentence, such as noun, verb, adjective, etc. POS tagging helps in understanding the syntactic structure of a sentence.

* Named Entity Recognition (NER): Identifying and classifying named entities in text, such as person names, locations, organizations, dates, etc. NER is used to extract structured information from unstructured text.

* Lemmatization and Stemming: Reducing words to their base or root form. Lemmatization takes into account the morphological analysis of words, whereas stemming uses heuristic rules to truncate words.

* Stop Word Removal: Eliminating commonly used words (such as "a," "the," "is") that do not contribute much to the overall meaning of a sentence. Stop word removal helps reduce noise in NLP tasks like information retrieval and text classification.

* Sentiment Analysis: Determining the sentiment or opinion expressed in a piece of text, whether it is positive, negative, or neutral. Sentiment analysis is useful for tasks like social media monitoring, customer feedback analysis, and brand reputation management.

* Text Classification: Assigning predefined categories or labels to text documents based on their content. This includes tasks like topic classification, spam detection, sentiment analysis, etc. Machine learning algorithms are often used for text classification.

* Word Embeddings: Representing words or phrases as dense vectors in a continuous vector space. Word embeddings capture semantic relationships between words, allowing algorithms to understand word similarities and analogies.

* Language Models: Statistical models that predict the probability of a word or sequence of words given the context. Language models have become increasingly powerful with the development of deep learning techniques and have enabled significant advancements in tasks like machine translation, text generation, and question-answering.

* Machine Translation: The task of automatically translating text from one language to another. Machine translation systems employ various techniques, including statistical methods, rule-based approaches, and neural networks, to achieve accurate translations.



## Word Embeddings
Word embeddings are dense vector representations of words in a continuous vector space. They aim to capture semantic and syntactic relationships between words based on their usage in a given corpus. Each word is represented by a high-dimensional vector, and similar words tend to have vectors that are closer together in the vector space. Word embeddings are typically learned from large text corpora using unsupervised learning techniques like Word2Vec, GloVe, or fastText.

Word embeddings have the advantage of capturing the meaning and context of words, allowing algorithms to understand the semantic relationships between words. They are widely used in various NLP tasks such as word similarity, named entity recognition, sentiment analysis, and machine translation.

Vectorization: Vectorization, on the other hand, is a more general term that refers to the process of converting any kind of data (including text) into numerical vectors that machine learning algorithms can understand. In the context of NLP, vectorization often refers to representing textual data as numerical feature vectors.

There are different techniques for vectorizing text, and word embeddings are one of them. Other vectorization techniques include:

One-Hot Encoding: Each word is represented as a binary vector where only one element is 1 (indicating the presence of that word) and all other elements are 0.

TF-IDF (Term Frequency-Inverse Document Frequency): It represents the importance of a word in a document by considering both the frequency of the word in the document (term frequency) and the rarity of the word in the entire corpus (inverse document frequency).

Bag-of-Words (BoW): It represents a document as a vector of word counts, ignoring the word order but considering the frequency of each word in the document.

N-gram Vectors: It represents contiguous sequences of n words as vectors, capturing the local word order and context.

### unigram, bigram, and N-gram
In natural language processing (NLP), unigram, bigram, and n-gram are terms used to refer to different types of linguistic units or sequences of words.

Unigram:
A unigram refers to a single word occurring in a text or a corpus. It represents the simplest form of analysis, where each word is treated as a separate and independent entity. For example, the sentence "I love cats and dogs" contains the unigrams "I," "love," "cats," "and," and "dogs."

Bigram:
A bigram is a sequence of two consecutive words in a text or a corpus. It involves analyzing the text by considering pairs of adjacent words. For example, in the sentence "I love cats and dogs," the bigrams would be "I love," "love cats," "cats and," and "and dogs."

N-gram:
N-gram is a more general term that refers to a sequence of N consecutive words in a text or a corpus. It can be a unigram, bigram, trigram (three consecutive words), or any higher-order combination of words. For example, in the sentence "I love cats and dogs," the trigrams would be "I love cats," "love cats and," and "cats and dogs." Similarly, a 4-gram would consist of sequences of four consecutive words.

N-grams are often used in NLP for various purposes, such as language modeling, part-of-speech tagging, text classification, and machine translation. They help capture the local context and dependencies between words in a text, which can be useful in understanding and generating natural language.

These vectorization techniques transform textual data into numerical representations that can be used as input for machine learning algorithms. Word embeddings, such as Word2Vec or GloVe, are a more advanced form of vectorization that capture semantic relationships between words in a dense vector space.
Vectorization and cosine similarity are concepts commonly used in natural language processing and information retrieval tasks. Let's explore each one in more detail:

1. Vectorization:
Vectorization refers to the process of representing textual data (such as documents, sentences, or words) as numerical vectors. In natural language processing, this conversion is necessary because most machine learning algorithms and mathematical operations work with numerical data.

There are different methods for vectorizing text, but one common approach is the "bag-of-words" model. In this model, each unique word in a corpus is assigned a dimension in a high-dimensional vector space. The vector representation of a document or sentence is then created by counting the occurrences or frequencies of words in that document. This results in a vector where each dimension represents the presence or absence of a particular word in the document.

Another popular method for vectorization is the "word embeddings" approach, which represents words as dense and continuous vectors in a lower-dimensional space. Word embeddings capture semantic relationships between words, allowing for more nuanced representations compared to simple word frequencies.

Vectorization enables mathematical operations on text data, such as measuring similarity between documents or performing machine learning tasks like clustering or classification.

2. Cosine Similarity:
Cosine similarity is a metric used to measure the similarity between two vectors. It calculates the cosine of the angle between the two vectors, indicating how similar their orientations are in the vector space.

In the context of natural language processing, cosine similarity is often used to determine the similarity between two documents or sentences represented as vectors. To compute the cosine similarity, the vectors are first normalized to unit length. Then, the cosine of the angle between the two vectors is calculated as the dot product of the vectors divided by the product of their magnitudes.

Cosine similarity ranges from -1 to 1, where a value of 1 indicates that the vectors are identical, 0 means they are orthogonal (not similar at all), and -1 signifies that the vectors are diametrically opposed or completely dissimilar.

Cosine similarity is commonly employed in tasks like document retrieval, information retrieval, text clustering, and recommendation systems. It allows for efficient and effective comparison of text data based on their vector representations, providing a measure of similarity that takes into account both the magnitude and direction of the vectors.

