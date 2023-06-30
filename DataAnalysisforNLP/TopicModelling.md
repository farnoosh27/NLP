## Why Topic Modelling
Topic modeling is a useful technique in natural language processing and machine learning that allows us to discover hidden themes within a collection of documents. By automatically identifying patterns and relationships in unstructured text data, topic modeling helps us organize documents, improve information retrieval, analyze content, generate summaries, explore data visually, and provide personalized content recommendations. It is valuable in various domains for understanding and extracting insights from large volumes of text data.
## Different Topic Modelling Techniques

Latent Dirichlet Allocation (LDA): LDA is a popular probabilistic model that assumes documents are a mixture of topics, and topics are distributions over words. It is widely used for discovering topics in a text corpus and assigning topic probabilities to each document.

Non-negative Matrix Factorization (NMF): NMF is a matrix factorization technique that decomposes a document-term matrix into topic and weight matrices. It is known for its interpretability and has been widely applied in topic modeling tasks.

Probabilistic Latent Semantic Analysis (pLSA): pLSA is a generative probabilistic model that represents documents as mixtures of topics. It calculates the probability of a word occurring given a particular topic. pLSA can estimate the underlying topic structure for topic modeling.

Word Embedding-based Approaches: Word embedding models like Word2Vec, GloVe, or BERT can be used for topic modeling. These models represent words as dense vectors in a continuous space, capturing semantic relationships. Clustering words based on their vector representations helps identify groups representing different topics.

Topic Coherence Measures: Topic coherence measures are used to evaluate and refine topic modeling results. They assess the semantic coherence of words within each topic, providing a quantitative metric for topic quality. Coherence measures help in determining the optimal number of topics or comparing different topic modeling techniques.

## Top2Vec

Top2Vec is an algorithm used for topic modeling and document clustering. It extends the Word2Vec algorithm to operate at the document level. It discovers topics in a collection of documents by creating document embeddings and applying hierarchical clustering. Each document is then assigned to one or more topics based on its similarity to cluster centroids. Top2Vec focuses on the most representative documents within each topic, allowing for a better understanding of large document collections. It has applications in various areas where extracting underlying themes from documents is important.
