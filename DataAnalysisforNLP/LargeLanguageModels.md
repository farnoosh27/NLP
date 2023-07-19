## LLMs
A large language model (LLM) is a computer-based model that uses an artificial neural network with numerous parameters to process language. It is trained on vast amounts of unlabeled text, containing billions or even trillions of tokens, using self-supervised or semi-supervised learning methods. LLMs became prominent in 2018 with the development of transformers, which allowed for faster training compared to previous models like long short-term memory (LSTM). This advancement enabled the use of large language datasets such as the Wikipedia Corpus and Common Crawl, thanks to parallelization techniques. LLMs are versatile models capable of performing well in a wide range of tasks. The effectiveness of language models in various tasks depends more on the size of the training corpus, the number of parameters, and the computational power achieved through parallel computing than on the model's design. Consequently, natural language processing research has shifted away from training specialized supervised models for specific tasks.

## What is LangChain?
LangChain is a framework that simplifies the creation of applications utilizing large language models (LLMs). It acts as an **integration framework** for language models, and its application areas align with those of LLMs, including document analysis and summarization, chatbot development, and code analysis. In essence, LangChain streamlines the process of incorporating language models into diverse applications by offering a structured framework for integration.

You can find out about it at this link: https://python.langchain.com/docs/get_started/introduction
https://www.youtube.com/@DataIndependent
A udemy course on LangChain can be: LangChain- Develop LLM powered applications with LangChain: https://www.udemy.com/course/langchain/

## History
In October 2022, LangChain was introduced as an open source initiative by Harrison Chase during his tenure at the machine learning startup Robust Intelligence. The project gained rapid recognition, attracting contributions from numerous GitHub contributors and generating lively discussions on Twitter. It also fostered an active community on its Discord server, along with the creation of various YouTube tutorials and meetups held in San Francisco and London. In April 2023, LangChain's promising trajectory led to a significant funding achievement. The startup secured over $20 million in funding, valuing the company at a minimum of $200 million. This funding was provided by venture firm Sequoia Capital, following a previous seed investment of $10 million from Benchmark, which was announced just a week earlier.

## Important Elements

Model I/O - Interact with language models

Data linkage - Connect with application-specific data

Sequences - Build a series of function calls

Actors - Allow sequences to select appropriate tools based on high-level instructions

Persistent storage - Retain application state between sequence executions

Event handlers - Record and stream intermediate steps of any sequence


## what is an agent: 
An Agent can be understood as an envelope that encloses a model, functioning to receive user inputs and generate responses. These responses suggest a particular "action" to be executed, along with the relevant "action input" associated with it.

## What is prompt?

Input/Context 
Questions 
Examples
Output Formats

None of these elements have to present. But in order to have a good prompt, at least one instruction and one question should be present. 
* Instruction:
```Translate from English to German: How is the weather?```
* Question:
* ```What is the meaning of life?```
* Example:
  *   Few-shot learning
* Specify the desired format.
* 
  ## Most common use cases:
  - Summarization
  - Classification
  - Translation
  - Text generation/ Completion
  - Question/ Answering
  - Coaching
  - Image Generation
