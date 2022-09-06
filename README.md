# Crypto Named Entity Recognition 
The objective is to perform Named Entity Recognition to recognize terms related to Cryptocurrency from conversational messages of different crypto channels.  
## Dataset

The dataset contains conversational messages scraped from Telegram regarding cryptocurrency. There are two columns, namely:

1. **id:** An arbitrary id column
2. **content:** The content of a crypto channel. Each row corresponds to one message and can contain alphabets, numbers, special symbols and emojis.  

## Folder Description

1. **data:** Contains all the raw unprocessed data
2. **input:** Contains processed data and vocabulary
3. **notebooks:** Contains 2 notebooks for data cleaning and modelling.
4. **output:** Contains the result of passing the input through the model.

## Approach Used

Currently, the approach used is:
1. Create vocabulary using data/term_abb.csv and data/term_def.csv and has been saved as input/crypto_vocabulary.json
2. Read input query
3. Parse input query for NOUNS and PROPER NOUNS
4. Check if the NOUN/PROPER NOUN exists in input/crypto_vocabulary.json and return result
## Future Work
The same approach can be improved upon by creating custom word embeddings to the given corpus of crypto data and then using 
cosine similarity to see how similar two words are. A threshold value can be set and based on that, NER can be performed.
