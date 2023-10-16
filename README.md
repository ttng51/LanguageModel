# Semantic Search with Language Model
This repository contains a Python script for concatenating broken sentences in a text and performing text retrieval using embeddings. It also demonstrates the use of the Cohere API for embeddings and reranking.

### Table of Contents
- Prerequisites
- Getting Started
- Usage
- Code Explanation
- License
### Prerequisites
Before using this code, make sure you have the following prerequisites:
- Python 3.x
- Cohere API Key
- Annoy Python library (pip install annoy)
- Pandas Python library (pip install pandas)
- Numpy Python library (pip install numpy)
- Cohere Python library (pip install cohere-api)

### Getting Started
1. Clone this repository to your local machine:
``` git clone https://github.com/ttng51/LanguageModel.git ```
2. Install the required Python libraries listed in the Prerequisites section.
3. Replace the api_key variable with your Cohere API key.
4. Replace the text variable with your desired text for analysis.
5. Run the Python script:

### Usage
#### Sentence Concatenation
The script takes a text containing broken sentences and concatenates them to form complete sentences. It does this by checking if a sentence ends with specific characters (e.g., digits or a dollar sign) and combines it with the following sentence if necessary.

#### Text Retrieval
The script performs text retrieval using the Cohere API for embeddings. It creates an Annoy index based on the embeddings of the sentences and allows you to search for similar sentences to a query.

Run the search(query) function to perform a dense retrieval of similar sentences based on the query.

Run the query and MODEL_NAME variables to perform query and rerank using the Cohere API. This demonstrates how to use Cohere for text reranking.
### Code Explanation
```concatenate_broken_sentences```: A function that concatenates broken sentences in a text.

```co.embed```: Uses the Cohere API to obtain embeddings for the text.

```AnnoyIndex```: Creates an Annoy index for text retrieval based on embeddings.

```search(query)```: Searches for similar sentences to a query using the Annoy index.

```co.rerank```: Reranks the text using the Cohere API.

### License
This project is licensed under the MIT License - see the LICENSE.md file for details.
