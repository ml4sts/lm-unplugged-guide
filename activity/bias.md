# Model Bias 

<!-- a short description that will help the reader choose this from the main acitivity page -->
This

1. Split the room 
2. Give each group a different [rule](#rules)
3. Train models in [parallel](#parallel)
4. Generate documents and have each group try to guess the other's rule.
5. [Discuss](#discussion:bias) differences in patterns. 


(rules)=
## Rules 

1. Documents must be under X words (X should be 3-5)
1. Documents must be over Y words (if paired with a max, X, Y>=X+2 to make differences visible)
1. Words (colors) cannot repeat back to back. 
1. (untested so far) Tell each group not to use a specific color
1. (untested) Give each group a very limited supply of one color stickies; no sharing across groups 

(parallel)=
## Parallel Training 

1. you can divide the group an train in two stations to save time, then pour to combine. 


(discussion:bias)=
## Discussion Guide
Bias can enter at multiple points in the modeling pipeline, which can negatively affect model outcomes and the decisions made from them.

### Data Level
 During data collection, if the {term}`training data` collected does not _adequately_ reflect the specific population or context in which the model will be used, the resulting training of our models can be skewed. This often appears as overrepresentation of some groups and underrepresentation of others or when data is drawn from a different social or cultural context than the one the model’s predictions are intended to serve. Further, when data is poor, we expect to see similar suboptimal outcomes.
- What are some ways we can ensure our data is good for our context?
- What practices lead to poor data collection?
- How can we better engage communities we would like to help with the design and proper use of LLMs?

### Modeling Assumptions

It is normal to make modeling assumptions; models are simplifications and simplifications require assumptions about what is and is not important. Therefore, assumptions can reflect only the norms and values of majority groups, or they can reflect multiple sets of norms and values. If the assumptions only reflect one group's values, then the choices in model design, data cleaning/filtering, etc will also only reflect that one set of norms and values. 
- How do we ensure assumptions we have fit the context we are predicting for?
- In your life, have you seen examples of societal norms or assumptions that do not align with your own context or experiences?
- Are there particular terms you find important for communicating ideas in your community or field? Why?

### Evaluation & Benchmarking

Metrics we use to test if our outcomes are fair and good for a society may focused on overall accuracy or fluency. This can overlook fairness or representational harms.
- How do you test if something is fair?
- What types of fairness make sense in your context?
- Why is fairness of value in your particular context?
- How can we ensure fairness?
