## HMM and RNN that Generate Poems
Given the entire corpus of Shakespeare's sonnets, we trained a Hidden Markov Model and Recurrent Neural Network to generate Shakespearen sonnets and other types of poems!
CS155 2024 Winter - By Mia Mutadich, Lana Lubecke, Jena Alsup and Ava Penn.

# Pre-Processing
Sonnets are restricted to having ten syllables per line so we created a hashmap that maps dictionary words to their corresponding number of syllables by parsing syllable_dict.py. In the case of a word having a different number of syllables at the end of a line than in the middle of a line, we used solely latter becasue we figured the word would have a higher frequency of appearing in the middle of a line. We then cleaned the corpus of Shakespeare's sonnets to remove all formatting but maintain the order of the lines of the sonnets. We did the same to the corpus of Spenser's sonnets to get cleaned Spenser's data.
**For HMM**
We tokenized the cleaned Shakespear data into words and verified that our words were valid using the syllable dictionary. We also tokenized the cleand Spenser's data into words, removing any words that were not included in the Shakespear dataset, so that we have more training data that follows the same sonnet pattern. We created a 2D array from the cleaned Shakespear data where each line of a sonnet is an array of the tokens of words that form a line in a sonnet and these arrays are ordered in a way that mirrors the line order of the sonnets.
**For RNN**
We tokenized the cleaned Shakespear data and into characters. 
