# Technical Notes 


This page gives some additional technical clarifications and links to resources to learn more. We also give some ways to address more advanced questions through the lens of this activity. 

::::::{warning}
The content here is **not** the goal of the activity, but is extra detail that it can be helpful for facilitators to have
::::::::::

The earliest versions of Large Language Models (LLMs) used very simple pattern matching. 

A document is a set of words/terms that express a coherent idea or topic. **Tokenization** is the process of breaking down/splitting these words into units (e.g., words, characters). Once the words are broken down, they can be represented to computers in a digestible way called **embeddings**. When words are embedded, they are represented by a vector of numbers which maintains the semantics of the word. Punctuation marks can also be represented through embeddings and are often counted as separate tokens. 

There are various types of machine learning models which are used for predicting. A language model predicts future words by assigning probabilities of a set of possible _next words_. The model chooses its words from a _corpus_, i.e., a database of language. Naturally, the larger our corpus is, the more likely we are to estimate good probability distributions over each likely word. More concretely:

$\ P(X_{1...n}) = P(X_1)*P(X_2|X_1) * P(X_3|X_{1,2} * ... * P(X_n|X_{1,...,n-1})$, where X represent words.

We tend to use n as our window size for helping us decide on our next best word. This is known as an n-gram model. 

In more recent times, we use more advanced methods than windowing and at much _larger scales_, hence **large language models**. For LLMs we use transformers, which dynamically determine the importance of each token within a fixed context window, limited by the model. 


**References**
**Tokenization**: https://nlp.stanford.edu/IR-book/html/htmledition/tokenization-1.html
