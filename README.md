# Document Q&A with RAG
Used the Financial Q&A dataset from kaggle, to create a RAG System, answering user queries using the dataset and Gemini

---

### Workflow:
1. Imported the dataset, cleaned it and created a column concatenating the necessary information from other columns titled "train"
2. Created the text-embeddings for the "train" column using the text-embedding-004 model from google. (Only 100 rows were converted due to API restrictions)
3. Created a collection in ChromaDB and stored the embeddings in the collection.
4. Queried the collection and provided the query results to Gemini to produce the well formatted answers to user queries.

<br/>

Also created an alternate version that overcomes the API limit of creating text embeddings, as follows:
1. Created embeddings using Sentence Transformers in Python. (One can also use the default embedding function in chromadb)
2. Saved the embeddings in pickle format for future use. The next steps remained the same as before.

<br/>

While this may be a simple application, I hope to expand upon the same to produce innovative solutions.
Any suggestions regarding improvements, evaluation and other aspects would be highly appreciated!
<br/>

---

### Reference:
* Dataset: https://www.kaggle.com/datasets/yousefsaeedian/financial-q-and-a-10k
* API Key - Google AI Studio
