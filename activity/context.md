# Context Length 


<!-- a short description that will help the reader choose this from the main acitivity page -->

<!-- outline the steps -->
Overview: 
1. Give a structure that documents should have
2. train  a context length 2 (using `N^2` bins for `N` words) 
3. compute a  context length 1 by summing to marginalize  (can be done later by pouring or if enough bins to copy)
4. Generate samples from length 2, show preserved
5. Generate sampels from length 1, show not there

<!-- subsections to provide details on steps -->

(2gramrules)=
## Rules for Context Two

1. after a double word the next has to be white
2. words have a sequence, but doubles allowed, skips can occur


### Sequence
words can only go in order, unless a double word.
1 skip is okay. 
first can follow last in the sequence, 


Example: 
order: {'purple': 0, 'blue': 1, 'green': 2, 'pink': 3}

-  purple, green, purple is okay
- purple, green, blue is not
- green green pink is okay

doc can end at anytime with a white
<!-- rules that would show up -->

## Discussion Guide
You may imagine having more context (i.e., larger context length) would give better and better outcomes as the length grows. However, this has limits. Think about when someone is telling you a LONG story. You have all of the background, but very limited capacity to recall every detail. While listening to the story, you try distingush what is important, but at times information gets lost. Similar with LLMs, large context windows consume more memory and processing time and eventually become ineffective.
- When you have a lot of information to study/remember, how do you decide what is most important to focus on first?
- How might you train better to make it answer questions?
- What strategies could be used to manage very long contexts effectively and what are the potential downsides of each approach?
-   k-shot prompting
-   summarization
-   cutting out the fluff
