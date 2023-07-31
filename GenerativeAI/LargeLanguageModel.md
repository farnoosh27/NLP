# LLMs

## History 
A brief historical background and development of Large Language Models (LLMs):
This is extracted from Databricks Ebook named as "A Compact Guide to Large Language Models".

1950s–1990s:
Initially, attempts were made to create hard rules for language and follow logical steps to achieve tasks like language translation. However, these strictly defined rules only worked for well-defined tasks that the system had prior knowledge about.

1990s:
Language models evolved into statistical models, and language patterns began to be analyzed. However, large-scale projects were limited due to the lack of computing power.

2000s:
Advancements in machine learning allowed for more complex language models, and the widespread adoption of the internet provided a vast amount of training data.

2012:
Deep learning architectures and larger datasets led to the development of GPT (Generative Pre-trained Transformer).

2018:
Google introduced BERT (Bidirectional Encoder Representations from Transformers), a significant advancement in architecture that paved the way for future large language models.

2020:
OpenAI released GPT-3, the largest model with 175 billion parameters, setting new performance standards for language-related tasks.

2022:
ChatGPT was launched, making GPT-3 and similar models accessible to users through a web interface, leading to increased public awareness of LLMs and generative AI.

2023:
Open-source LLMs like Dolly 2.0, LLaMA, Alpaca, and Vicuna showcased impressive results. Additionally, GPT-4 was released, setting new benchmarks in parameter size and performance.

## How does it work?
Before understanding how LLMs work, we certainly need to get to know some terminology.

* Inputs and Input Embeddings
* Positional Encoding
* Encoder
* Outputs (shifted right)
* Output Embeddings
* Decoder
* Linear Layer and Softmax
## Definition

A large language model (LLM) is a computer-based model that uses an artificial neural network with numerous parameters to process language. It is trained on vast amounts of unlabeled text, containing billions or even trillions of tokens, using self-supervised or semi-supervised learning methods. LLMs became prominent in 2018 with the development of transformers, which allowed for faster training compared to previous models like long short-term memory (LSTM). This advancement enabled the use of large language datasets such as the Wikipedia Corpus and Common Crawl, thanks to parallelization techniques. LLMs are versatile models capable of performing well in a wide range of tasks. The effectiveness of language models in various tasks depends more on the size of the training corpus, the number of parameters, and the computational power achieved through parallel computing than on the model's design. Consequently, natural language processing research has shifted away from training specialized supervised models for specific tasks.

## What is LangChain?

LangChain is a framework that simplifies the creation of applications utilizing large language models (LLMs). It acts as an **integration framework** for language models, and its application areas align with those of LLMs, including document analysis and summarization, chatbot development, and code analysis. In essence, LangChain streamlines the process of incorporating language models into diverse applications by offering a structured framework for integration.

## What is vectorstore?

One of the prevailing methods for storing and searching unstructured data involves embedding it and storing the resultant embedding vectors. During the query process, the unstructured query is also embedded, and the stored embedding vectors that exhibit the highest similarity to the embedded query are retrieved. A vector store manages the storage of embedded data and handles the vector search process on your behalf.





You can find out about it at this link: https://python.langchain.com/docs/get_started/introduction
https://www.youtube.com/@DataIndependent
A udemy course on LangChain can be: LangChain- Develop LLM powered applications with LangChain: https://www.udemy.com/course/langchain/

## History
In October 2022, LangChain was introduced as an open-source initiative by Harrison Chase during his tenure at the machine learning startup Robust Intelligence. The project gained rapid recognition, attracting contributions from numerous GitHub contributors and generating lively discussions on Twitter. It also fostered an active community on its Discord server, along with the creation of various YouTube tutorials and meetups held in San Francisco and London. In April 2023, LangChain's promising trajectory led to a significant funding achievement. The startup secured over $20 million in funding, valuing the company at a minimum of $200 million. This funding was provided by venture firm Sequoia Capital, following a previous seed investment of $10 million from Benchmark, which was announced just a week earlier.

## Important Elements

Model I/O - Interact with language models

Data linkage - Connect with application-specific data

Sequences - Build a series of function calls

Actors - Allow sequences to select appropriate tools based on high-level instructions

Persistent storage - Retain application state between sequence executions

Event handlers - Record and stream intermediate steps of any sequence


## what is an agent: 
An Agent can be understood as an envelope that encloses a model, functioning to receive user inputs and generate responses. These responses suggest a particular "action" to be executed, along with the relevant "action input" associated with it.


