# Activity 

:::::{tip}
The main content of the page is an outline/ potential script for running the activity. 
The various call outs are facilitator notes. 
::::::

::::::::::::::{exercise}
:label:example

Things that attendees should discuss or think about are shown this way, with solutions separately.  

Based on your available time and size of the group,  you can use these in a few ways:
- let attendees think on their own for a bit, then have them discuss with neighbors, before finally having groups share out
- have them go straight to disucsion in groups; encourage them to meet the people around them, walk around and check for themes or offer hints
- 

::::::{solution} example
:class:dropdown

and the solution is hidden so you can quiz yourself if you like. 
:::::::::::
::::::::::::::::::::::::

## Welcome

- AI is everywhere
- Literacy should be liberatory; learning to consume products is not liberation. 
- The goal of this workshop is to *understand* so that you can critique, that you can decide to trust or not trust appropriately



:::::{important}
Remind attendees of the overall timing you've selected.  See the [relevant tips](#setup:detail:timing) for examples. 
:::::::

## Unplugged, Really

:::::{tip}
Offering this as an invitation helps make it feel less stressful, but feel free to acknowledge the discomfort!
:::::::


This workshop is unplugged. We have no slides. We will explain though demonstration after a *little* bit of setting the stage.  

::::::::::::::{exercise}
:label:nofire

Take a moment and think about the last training event you attended or a day in a recent math, science, computer science or engineering course. Remember how it felt. Now pay attention to your posture and your breath right now. How do you feel?  

::::::{solution} nofire
:class:dropdown

There's a good chance, people will notice that their body got tense, their breath shallow. 

Often, STEM environments tend to a firehose approach to disseminating information. We won't do that here. 

Take a breath. Relax. 
:::::::::::
::::::::::::::::::::::::


This workshop is not designed to give you as much information as possible, instead, it's designed for you to get really comfortable with a few key ideas. To really absorb them. To hold them. For them to stay with you.  To sit with a few ideas long enough that you let them shape your future choices. 

Literacy is liberatory afterall, we want you to feel a bit of liberation. 

So, we invite you to really unplug: 
- silence notifications on any wearables
- take a moment and jot down that thing you're worrying about
- tell the person you're texting you're taking a moment to focus deeply and learn
- put away your devices



## What is a AI? 


Currently the biggest advance in AI is LLMs.  Some are "vision" models or "audio" models, but they all take the same basic idea.


- AI, human like machine decision making,  has been the goal of CS for a long time
- Many strategies exist, most recent success is due to  machine learning, finding patterns in data instead of writing code explicitly
- Current shift is LLMs or more broadly generative models
- LLM = Large Language Models

Let's break down that term. 

### Models

A {term}`model` is a simplification in order to communicate an idea. In ML, our model describes our assumptions about the world that we use to find patterns in the data. 

::::{tip}
It can be good to start off inviting participation by asking attendees to think of models they have seen. Hint about science classes or even hobbies. Depending on the audience this may /may not be generative. Trust your knowledge of the audience. 
::::


Some examples: 
- ex: a volcano demo
- ex: diarama
- ex: globe
- ex: atom model with rings

In computing, our model are always a mathematical model. In ML, typically a statistical model. 

Here w

- familiar mathematical model: line
- 2 params: have meaning

::::{tip}
This is a good place to draw a line and the equation, $y=mx+b$. 

Remind that the parameters move the line. If you have multiple marker colors, you can draw a few lines with different slopes/intercepts
:::::::

### Language

- languages consists of words and grammar
- in Natural Langue Processing we discuss {term}`tokens` (approx words, but sometimes smaller) and documents (units of text to analyze)
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

:::::::::::::::{tab-set}
:::::::::{tab} Informal

Specifically: we assume that the distribution of the next word given the previous words is all we need 
::::{math}
:label: eqgenerativei
P (next| previous)

::::::
::::::::::

:::::::::{tab} Formal
Specifically, to generate word number $j$ given $n$ previous words, called the context length:

::::{math}
:label: eqgenerativef
P (w_j| w_{j-1}, w_{j-2},\ldots, w_{j-n})

::::::
:::::::::::
::::::::::::::::::

::::{tip}
Write this equation too so people can look at it. 
:::::

## A simpler Model

LLMs require a lot of parameters because spoken language is complex. There are a lot of words and meaning can be conveyed over long strings of words.  

So, LLMs use an deep neural network to *implement* that distribution in a computer. 

However, if we use a very simple language, and for now, only the *one* previous word then the equation can be represented by a table. 

Even better, we can do random with physical objects.  

- A coin flip 
- a die roll
- a raffle draw 

So, we will implement this distribution physically. 


## Sampling a Pretrained Model


- tiny language: 4 words
- implement [](#eqgenerativef) with $n=1$ using buckets and ping pong balls
- we have a pretrained model, let's test it so we can really understand that model

::::{tip}
ask the audience for  prompt
::::::


Sampling procedure
1. A {term}`helper` posts a sticky in the color of the prompt on the board
1. The {term}`facilitator` starts in the bin labeled with the prompt and draws a ball
1. A {term}`helper` adds a sticky in the color of the drawn ball
1. The {term}`facilitator` draws from the bin of the last sticky in the document
1. repeat until you draw a white.


::::{tip}
Don't look when drawing.
Do a few documents, depending on the length. 
:::::



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

:::::::{exercise} What does it mean? 
:label: meaning
We have worked with this small language, but what do the documents mean? 


::::{solution} meaning
:class: dropdown
The words have no meaning, we did not assign any. That's how computers work. People give words meanings, the tokens we represent in the computer do not have any meaning to the computer.  

We were able to model and proess this tiny language without assigning meaning, just like the computer does
:::::
:::::::::::