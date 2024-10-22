# Sentence Parser

This project is a sentence parsing application using Natural Language Processing (NLP) with the NLTK library. The application reads a sentence, parses it to identify its grammatical structure, and extracts noun phrase chunks.

## Functionality

The main functionality of this script includes:

1. **Reading Input:**
   - The script can read a sentence either from a file (if a filename is specified as a command-line argument) or directly from user input.

2. **Preprocessing:**
   - The `preprocess` function converts the input sentence to lowercase and tokenizes it into words. It removes any word that does not contain at least one alphabetic character.

3. **Parsing:**
   - The script uses a context-free grammar (CFG) defined by `TERMINALS` and `NONTERMINALS` to parse the sentence.
   - The `nltk.ChartParser` is used to generate parse trees for the sentence.

4. **Extracting Noun Phrases:**
   - The `np_chunk` function identifies and returns all noun phrase chunks from the parse trees. A noun phrase chunk is defined as any subtree labeled "NP" that does not contain other noun phrases.

5. **Output:**
   - The script prints the parse tree(s) and the extracted noun phrase chunks.

## Usage

To run the script, use the following command:
python parser.py [filename]


- If `[filename]` is provided, the script will read the sentence from the specified file.
- If no filename is provided, the script will prompt the user to input a sentence.

## Example

Given the sentence "Holmes chuckled and said, 'The little armchair in the corner is red.'", the script will:

- Tokenize and preprocess the sentence.
- Parse the sentence to generate its grammatical structure.
- Extract and print the noun phrase chunks.

## Functions

### `main()`

Orchestrates the reading of input, preprocessing, parsing, and output of noun phrase chunks.

### `preprocess(sentence)`

Converts the input sentence to lowercase, tokenizes it, and removes non-alphabetic words.

### `np_chunk(tree)`

Identifies and returns all noun phrase chunks from the parse tree.

## Dependencies

- Python 3.x
- NLTK

You can install the required packages using pip:
pip install nltk


## License

This project is licensed under the MIT License.
