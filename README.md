# Spell-Checker

Goal : Create a spell checker: correct spelling of a corrupted word

Steps:
1. Train a language model on training data. 
2. Use your model to predict the outputs (correct spelling) for the test data (corrupted words). 
3. Upload your prediction as a file to the in class Kaggle competition for evaluation and ranking (similar to homework 2). 

Sample Model:
We see an observation x (a misspelled word) and our goal is to find the word w which was corrupted to generate the misspelled word, out of all possible words in a vocabulary V. 

Model 1:
Generate all the words from misspelled word x with an edit distance of 0, 1 & 2 including insertions, deletions, and substitutions. Also, use transpositions for generating the words (called as Damerau-Levenshtein edit distance). After generating all the candidate words, select the word w which has the maximum number of occurrences (probability) in your original dataset, as the correct word.
