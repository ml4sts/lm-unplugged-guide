# Design Notes

Now, we peel back behind the scenes a bit. For you to be ready to run this yourself, knowing *why* will help a lot. 

Key points for attendees:
1. randomness is key
1. artificial neural networks are not like a brain
1. LLM just produce words


Why the activity is formatted the way it is: 
1. Unplugged as resistance
1. No meaning to the words is on purpose; computers do not *understand* the words. 


 Models are simplifications, most people engage with models in grade school science. Language is a set of words and rules to combine them in order to convey meaning from one person to another. We use the simple model of an equation for a line to introduce parameters (2) and then point out that LLMs have hundreds of billions. LLMs are generative models, meaning that they describe a procedure to generate new data that looks like the data used to fit it.  In particular, they use a simple assumption, that the next word is dependent upon the previous words. To model real world spoken languages, we need a lot of parameters because the language is complex, but


We break down each term starting with model, then language and finally explain what large is. We show that the LLMs model language by modeling the distribution of next possible words following previous words\footnote{technically tokens, but words are close enough for anyone not building systems and much easier to relate to; the activity can be adapted to explain tokens for appropriate audiences}. Conditional probability can be hard to relate to, the deep neural network architectures used requires years of mathematical background to deeply understand. Instead, we simplify the language that we model, but use the same idea.  We model a language that has only four words, represented by different colors. In this case, we can represent the distribution of possible next words given a previous word by different proportions of colored ping pong balls in a bucket.  We can represent the whole model with four buckets. We add one extra color (token) that means end of document. With this representation, we can sample documents by drawing colored balls repeatedly until we draw the end of document token. 

We can also train a model by having participants author documents using matching colored sticky notes and building up a model by counting. This is different technically than how a neural network is trained; the representation dictates the related algorithms, but they key ideas are the same. We can then sample from the model trained by the group. THis will have some differences. Next, we engage in a conversation about model biases by splitting the attendees into groups, giving each group a rule,  and having each group author additional documents following the rule. Then we have each group try to guess the other's rule.  Some rules will show up exactly, and others will not.  This facilitates an embodied, technically grounded conversation on biases in models and errors (e.g. those anthropomorphized as ``hallucinations"). 