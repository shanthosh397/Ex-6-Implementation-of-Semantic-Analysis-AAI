

# Experiment-6: Implementation of Semantic Analysis </H1>

### Name: Shanthosh G
### Register Number:2305003008

## Aim: 

To perform Parts of speech identification and Synonym using Natural Language Processing (NLP) techniques.

## Algorithm:

**Step-1:** Import the nltk library.

**Step-2:** Download the 'punkt', 'wordnet', and 'averaged_perceptron_tagger' resources.

**Step-3:** Accept user input for the text.

**Step-4:** Tokenize the input text into words using the word_tokenize function.

**Step-5:** Iterate through each word in the tokenized text.
-	 Perform part-of-speech tagging on the tokenized words using nltk.pos_tag.
-	 Print each word along with its corresponding part-of-speech tag.
-	 For each verb , iterate through its synsets (sets of synonyms) using wordnet.synsets(word).
-	 Extract synonyms and antonyms using lemma.name() and lemma.antonyms()[0].name() respectively.
-  Print the unique sets of synonyms and antonyms.

## Program:

```python
import nltk
#import wordnet
nltk.download( 'punkt' )
nltk.download('wordnet')
from nltk.tokenize import word_tokenize
nltk.download( 'averaged_perceptron_tagger' )
sentence=input ()
# Tokenize the sentence into words
words = word_tokenize(sentence)
# Identify the parts of speech for each word
pos_tags= nltk.pos_tag(words)
from nltk.corpus import wordnet

# Identify synonyms and antonyms for each word
synonyms =[]
antonyms =[]
for word in words:
	for syn in wordnet.synsets(word) :
		for lemma in syn.lemmas():
			synonyms . append (lemma . name( ) )
			if lemma . antonyms():
				antonyms . append ( lemma. antonyms ( ) [0] . name ( ) )
# Print the synonyms and antonyms
print ( "Synonyms : " ,set (synonyms) )
print ( "Antonyms : " ,set(antonyms) )
```
---

## Output:

<img width="835" height="52" alt="image" src="https://github.com/user-attachments/assets/fd0d7125-7407-4dfc-bc06-fda3cdc71ff6" />
<img width="838" height="50" alt="image" src="https://github.com/user-attachments/assets/9e16b62b-d166-41bf-b3a8-0375d33f5f00" />
<img width="835" height="162" alt="image" src="https://github.com/user-attachments/assets/200c4d7c-1226-4c0d-8502-3bd64ecbe34d" />
<img width="845" height="52" alt="image" src="https://github.com/user-attachments/assets/d7caacfa-3f15-4022-9afa-a24b580b3b1e" />


## Result:
Thus ,the program to perform the Parts of Speech identification and Synonymis executed sucessfully.
