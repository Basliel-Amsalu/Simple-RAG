# simple RAG
## Description
This is a simple rag project that is implemented from scratch using jupyter notebook. It reads from PDF of any choice and performs the following operations.
1. Extracts text from the PDF
2. Tokenizes the text
3. splits pages into sentences
4. chunks the sentences together
5. Embed the chunks using embedding model (all-mpnet-v2)
6. store the embeddings in a vector database
    - there are two methods used in this step 
        - the first method is to store the embeddings in a file (text_chunks_and_embeddings.csv)
        - the second method is to store the embeddings in a vector database (chromaDB) which contains the step prior to this to as it can do the embedding by it self give it is provided with the chunked sentences.
7. retrieving the relevant chunks
    - the first method is to retrieve the chunks from the file (text_chunks_and_embeddings.csv) by using cosine similarity to perform similarity search
    - the second method is to retrieve the chunks from the vector database (chromaDB) using chromaDBs builtin similaty search by providing the similarity type we want.
8. Prompt engineering
    - the prompt engineering is done by using the retrieved chunks and the original text to generate a prompt that can be used to generate a relevant answer.
9. Answer generation
    - using the model chosen ([https://huggingface.co/google/gemma-2b-it](#gemma-2b-it)) and the prompt that was prepared we generate an answer for the user query


## Table of Contents

- [Installation](#installation)
- [Usage](#usage)

## Installation

To install the project, follow these steps:
1. Clone the repository:
    ```
    git clone https://github.com/Basliel-Amsalu/Simple-RAG.git
    ```
2. Install the requirements:
    ```
    pip install -r requirements.txt
    ```
3. To Run with jupyter notebook:
    ```
    jupyter notebook
    ```
4. To Run with vscode:
    ```
    code.
    ```
## Usage

To use the project, follow these steps:
1. Open the jupyter notebook
2. Run the cells in the notebook
3. Provide the path to the PDF file you want to extract the text from
4. Provide the query you want to ask the model
5. The model will generate an answer based on the query you provided


