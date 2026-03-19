# Technical Notes 


This page gives some additional technical clarifications and links to resources to learn more. We also give some ways to address more advanced questions through the lens of this activity. 

::::::{warning}
The content here is **not** the goal of the activity, but is extra detail that it can be helpful for facilitators to have
::::::::::

## Language Models
There are various types of machine learning models which are used for predicting. A language model predicts future words by assigning probabilities of a set of possible _next words_. The model chooses its words from a _corpus_, i.e., a database of language. Naturally, the larger our corpus is, the more likely we are to estimate good probability distributions over each likely word. More concretely:

$\ P(X_{1...n}) = P(X_1)*P(X_2|X_1) * P(X_3|X_{1,2}) * ... * P(X_n|X_{1,...,n-1})$, where X represent words.

We tend to use n as our window size for helping us decide on our next best word. This is known as an n-gram model. In more recent times, we use more advanced methods than windowing and at much _larger scales_, hence LLMs. 

## Tokenization & Embeddings
A document is a set of words/terms that express a coherent idea or topic. **Tokenization** is the process of breaking down/splitting these words into smaller units called {term}`tokens <token>` (e.g., words, subwords, characters). These breaks can occur in a set of various ways, for example, when white space occurs. Once the words are broken down, they can be represented to computers in a digestible way called {term}`embeddings <embedding>`. When words are embedded, they are represented by a vector of numbers which maintains the semantics of the word. These words lay in a high-dimensional space (e.g., $\ R^{50}, R^{1000}$) where vectors (i.e., words) that are similar in meaning are near each other (e.g., _opportunity(v) and chance(w)_ are words that $\lvert \vec{v} - \vec{w} \rvert < \epsilon$, where $\\epsilon$ is small). Punctuation marks can also be represented through embeddings and are often counted as separate tokens. 


## Transformers 
LLMs use {term}`transformers <transformer>`, which dynamically determine the importance of each token within a fixed context window, limited by the model. 

First, a transformer takes in the word embeddings and sends them to the {term}`attention layer`. The attention layer assigns weights to each input {term}`token` {term}`embedding`, reflecting its relevance to the current token of concern, and combines the corresponding value vectors to reveal the importance in context, given the information from the surrounding embeddings and the model's {term}`parameters <parameter>`. Next, the attention-weight adjusted embeddings are passed through a {term}`neural network` (NN). The NN updates the weights on the embeddings and its parameters. This repeats between other attention layers and NNs until we pass through all of the layers in our model. _Backpropagation_ occurs to recalculate the weights given the error. That is, when our model fits a function (e.g., $\ y = mx + b$), the predicted output \hat{y} is tested against the actual outcome y, ($\ L_1 = |\hat{y} - y| < \epsilon$), if the $\ L_1 !< \epsilon$ we pass the loss back through the network to caculate the affect of the loss on each parameter ($\\theta_i$) (i.e., $\ \frac{dL}{d\theta_i}$). By **gradient descent** each parameter ($\\theta_i$) is updated: ($\\theta_i \leftarrow \theta_i - \eta * \frac{dL}{d\theta_i}$) (\eta is our learning rate that helps us decide how large of a step to take into our descent). All of this repeats until our loss no longer _desends_/decreases, we stop early given a number of epochs/runs, or until we reach a _sufficent_ model performance. 

## Output
Once we reach our goal, the last layer (linear layer) produces a 1-D representation of the distributions/probabilities that describe how likely it is that the word represented by each embedding is to be the _next_ word in our sequence. Taking the Softmax ($\ P(word_i) = {e^{x_i}}/ {\sum_j e^{x_j}}$) of these representations (i.e., logits) gives us a distribution over the words that sums to 1. The top word is likely to be chosen. However, depending on the parameter settings, we could choose to sometimes predict/guess the 2nd, 3rd, or other best (top_k). Another hyper-parameter we can adjust is the _temperature_, which would likely affect the top_k words. The temperature when increased gives room for less likely values to have higher logit values. This is sometimes a strategic move that can help with creativity/strictness and accuracy. The word we choose as _next_ is now added to the document and additional words are found if we have not reached the [EOF] (i.e., end of file).


## Resources for more information

**Brief Explanation of LLMs via video**: https://youtu.be/LPZh9BOjkQs?si=xmufmKziYIBCxs7l

**Tokenization**: https://nlp.stanford.edu/IR-book/html/htmledition/tokenization-1.html 

**Overview of Attention**: https://www.ibm.com/think/topics/attention-mechanism 

**Deep Dive into Attention**: https://proceedings.neurips.cc/paper_files/paper/2017/file/3f5ee243547dee91fbd053c1c4a845aa-Paper.pdf

**Longer/Deeper Explanation of Transformers via video**: https://youtu.be/wjZofJX0v4M?si=I7UxWMWOBuqOmNfx
