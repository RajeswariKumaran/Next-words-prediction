# Next-words-prediction

Identifies the next set of words for a given phrase based on the corpus trained using Keras

Logic used:

a. Tokenize sentences

b. Generate sequences of word tokens, in this case made a sequence of 3 words

c. Make the first two entries as features and last one as label. Make the label as categorical by one hot encoding

d. Create a sequential model with embedding layer, LSTM and dense layer with softmax activation

e. Fit using training features and encoded output label token

f. Predict classification label for each word in the given set of text

g. Find the word corresponding to the predicted label and string it for the length of prediction requested

Eg:

print(generate_seq(model, tokenizer, max_length-1, 'Jack fell down', 10))

Output:

Jack fell down and broke his crown and jill came tumbling after after
