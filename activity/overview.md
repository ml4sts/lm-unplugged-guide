# Activity 

:::::{tip}
The main content of the page is an outline/ potential script for running the activity. 
The various call outs are facilitator notes. 
::::::

::::::::::::::{exercise}
:label:example

questions to discuss are shown this way, with solutions separately

::::::{solution} example
:class:dropdown

and the solution is hidden so you can quiz yourself if you like. 
:::::::::::
::::::::::::::::::::::::

## Welcome

- AI is everywhere
- Literacy should be liberatory; learning to consume prodcuts is not liberation. 
- We want you to understand so that you can critique, trust or not trust appropriately
- LLMs break typical assumptions we have about computers-- even people who know how to code


:::::{important}
Introduce by giving a preview of the timing
:::::::


## What is a model? 

- a simplification
- ex: eqn for a line; 2 params
- all models are wrong but some are useful
- models have to become complex to model complex phenomena
- we can make a simpler language to model 

<!-- eqn for  line figure -->


## LLM

- AI has been the goal of CS for a long time
- Many strategies, most recently machine learning, finding patterns in data instead of writing code explicitly
- Current shift is LLMs or more broadly generative models
- LLM = Large Language Models



### Models

- simplification in order to communicated an idea
- ex: a volcano demo
- ex: diarama
- ex: globe
- ex: atom model with rings
- for computing, always a mathematical model
- in ML, typically a statistical model
- familiar mathematical model: line
- describes assumptions about the world

### Language

- consists of words and grammar
- in NLP we discuss tokens (approx words, but sometimes smaller) and documents (units of text to analyze)
- communicates ideas


### Large

- broadly: "bigger" is more complex
- refers to the number of parameters
- a line has two parameters: slope & intercept
- GPT 3 had 175 Billion parameters

### Putting it together

Over time, ML has done many different models, but the one that happens to have hit is a *generative* language model. 

It starts with a simple assumption:

> We can generate sequences of words by sampling from a distribution of what word comes next given a sequence of past words. 

Specifically, to generate word number $j$ given $n$ previous words, called the context length:

::::{math}
:label: eqgenerative
P (w_j| w_{j-1}, w_{j-2},\ldots, w_{j-n})

::::::::


## Sampling a Pretrained Model


- tiny language: 4 words
- implement [](#eqgenerative) with $n=1$ using buckets and ping pong balls

## Training a Model 

- author your own document using sticky notes. only rule is white = end of document
- Training varies by implementaion of the generator
- for our model: give a document, put a ball in color of word $j$ in the bin labeled with color for word $j-1$ for words $j=2$ to the end of document
- each person comes up to train on thier document


## Discussion

- what observations do you have about the generated documents
- how are they different/similar


## Second Training and Reinforcing Ideas

:::::{note}
Depending on timing, choose one or more variants to reinforce or skip to closing

:::::::::

- [Bias by training under different data](bias.md)
- [Longer Context Windows](context.md)

## Closing 

:::::::{exercise}
:label: meaning
We have worked with this small language, but what do the documents mean? 


::::{solution} meaning
The words have no meaning, we did not assign any. That's how computers work. People give words meanings, the tokens we represent in the computer do not have any meaning to the computer.  

We were able to model and proess this tiny language without assigning meaning, just like the computer does
:::::
:::::::::::