#  Glossary 

## Role Glossary
::::::{glossary}

helper
:  people who assist during a {term}`workshop` or {term}`training`, putting up stickies, passing out materials, secondary training during parallel. helpers at a {term}`training` may be new {term}`facilitators <facilitator>` or even {term}`trainees <trainee>`

facilitator
:  person or people (co-facilitators) who are running a {term}`workshop`. should have some more technical depth in understanding AI and its risks and completed this training

participant
:  person who attends the {term}`workshop` to learn what AI is. 

trainee
:  person who attends the {term}`training` to become a {term}`facilitator` in the future

trainer
:  person who runs the {term}`training`; an experienced {term}`facilitator` with deeper background to help prepare people to run the workshop on their own. 

training
:  event to prepare future {term}`facilitators <facilitator>`

workshop
:  the LLM unplugged workshop, with a targt audience of no tech background required

:::::::::::


## Technical Terms

```{glossary}

agent
: an AI that is able to do multiple things (FIXME-anthropic defs)
: <fill in def that is more general>

algorithm
: a set of instructions to complete a task; a recipe

anonymous function
:  a function that's defined on the fly, typically to lighten syntax or return a function within a function. In python, they're defined with the {term}`lambda` keyword.
:  [docs](https://en.wikipedia.org/wiki/Anonymous_function#:~:text=Anonymous%20functions%20are%20often%20arguments,than%20using%20a%20named%20function)

artificial intelligence
: the study of intelligent agents that receive precepts from the environment and take action
: a technology that has input ouptut behavior that appears as an intelligent agent
: a sub field of computer science

artificial neuron
: a type of function that takes a weighted sum of the inputs and passes them to an activation function
: a type of mathematical, or computer, function that approximates some functions of biological neurons

binary
:  a place based number system with base 2

categorical variable
: a variable that can only take one of a fixed discrete number of values, in general unordered

classification
:  a type of machine learning where a {term}`categorical <categorical variable>` {term}`target` variable is predicted from {term}`features <feature>`

class
:  a value of the {term}`target` variable

cluster
:  a group of samples that is similar by some definition

clustering
:  a type of {term}`unsupervised learning` that finds groups or clusters among the samples
compute
:  apply a series of mathematical operations to an input 

deep learning
: a type of machine learning that consists of creating large numbers of hidden layers of {term}`artificial neurons <artificial neuron>`

development
:  a stage in the "life cycle" of code wheere is it not necessarily ready for users, but the developers are actively working on it. 


discriminative model
: a type of statistical model that describes the decision boundary to make a prediction


feature
: in machine learning, one input to the prediction algorithm, typically of many, stored together in a feature vector

generative model
: a type of statistical model that describes the way that the underlying data is distributed with sufficient detail to be able to sample new data that is in the same distribution as the original data; often in 

generative pretrained transformer
: It is a {term}`transformer` model that takes in tokens and can be sampled from to to produce novel token sequences that are similar to its training data
: a specific type of {term}`generative model`

label
: the output value for a particular sample or of a prediction algorithm (ie *true label* or *predicted label*)

lambda
:  the keyword used to define an anonymous function; lambda functions are defined with a compact syntax `<name> = lambda <parameters>: <body>`
: [docs](https://docs.python.org/3.9/reference/expressions.html#lambda)

language
: a vocabulary and a grammar for how to combine the words in order to convey meaning

large language model
: a probability distribution that describes the structure of sequences of tokens and enables next token prediction as well as serves as a mathematical description of tokens using many parameters

learning algorithm
: an algorithm for finding patterns in data 
: a paramter optimization or parameter fitting algorithm

machine learning
: a sub field of AI; emphasizes the use of data to learn relationships, studies the algorithms that find patterns in data

model
: a simplification of some part of the world

model class
: a generic mathematical {term}`model` that can be fit to a specific part of the world by setting {term}`parameter` values

neural network
: a set of {term}`artificial neurons <artificial neuron>` where the outputs of some are the inputs to the others, serving to "connect" them as a set, or network; often described as layers where connections are from one layer to the next. 

neural network architecture
: the general structure of how a neural network is set up, not the specific weights, but the size of the layers, number of layers, types of layers for example 

number
:  a mathematical object used to count, measure and label

number system
:  a cultural artifact that describes the symbols used to represent quantities and how to interpret them as {term}`numbers <number>` 

parameter
:  (general programming) all inputs to a function
:  (in ML) the values that transform a generic function into a specific function

place based
:  a type of {term}`number system` where the position or place of the symbol changes its meaning. So in  1, 10, and 100, the symbol `1` represents different values because of its position.

predictive model
: a mathemtical model, typically implemented in computer code, that predicts a label for an input or an outcome based on past

probability distribution
:  a function that takes an event (or value) as input and returns the likelihood of that even occuring

production
: a state of a system where it is in use by users unaffiliated with the developers and generally unrestricted (except for possibly payment)
: contrast with {term}`research`, {term}`sandbox`, and {term}`development`

programming language
: a human readable {term}`language` that can be processed by computers and translated (either live through an interpreter or in batch through a compiler) to machine instructions that the physical computer can execute

machine representation
: a description of an object that can be stored in a computer


regression
: {term}`supervised learning` that predicts a continuous valued output

research
: a state of a system where is has been built and evaluated, but not deployed to general users, instead is only available to the team that built it and (potentially) other authorized users
: contrast with {term}`production`

retrieval agumented generation
: a  process to produce text that is grounded in content from specific resources in order to improve the factual correctness of the text or augment with specific data that was not available to a base model at the time of traning
: commonly used to "chat with" a document or to prevent false statements 

sandbox
: a state of a system where is is available to test, but is not officially deployed, may have simulated data instead of real data or be isolated from external systems

statistical model
: a type of mathematical model that describes its object of inquiry using probability distributions

supervised learning
: a type of machine learning that requires both features and target variables at time of training
:  machine learning with labeled examples

target
: the variable to be predicted in a machine learning problem setup, the dependent variable
:  the output of a prediction algorithm
:  also called the dependent variable or label

test accuracy
:  percentage of predictions that the model predict correctly, based on held-out (previously unseen) test data

test data
:  data that was not used in training that is instead used to evaluate the perforance of a model 

token 
: the basic units used in computational processing of texts from human spoken (not programming) languages
: a part of a word or a word, approximately like prefix, base, suffix parts, in general 1000 tokens is about 750 words

transformer
: a type of model, specifically, a type of {term}`neural network architecture`


unsupervised learning
: a type of machine learning that does not use target variables at learning (fit) time. 
: machine learning from unlabeled examples
```