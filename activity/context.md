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

- how might you train better to make it answer questions?
- k-shot prompting 