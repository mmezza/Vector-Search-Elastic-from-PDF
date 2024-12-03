# Vector-Search-Elastic-from-PDF
Using the Playground feature in Elasticsearch in order to test semantic search in text content of PDF files indexed. This combines techniques such as embedding generation, RAG, vector search and LLM integration.

# STEP 1 - Importing and deploying the model from Hugging Face
The first step is to choose the model from **huggingface.co**. There's a lot of models you can choose there and for this test, as I'm using documents in portuguese, I choose the **rufimelo/bert-large-portuguese-cased-sts** model.

Use the ELAND nootebook to import the model to Elasticsearch and change the model name in case you choose a different model.
<img width="795" alt="image" src="https://github.com/user-attachments/assets/421183d1-0695-4cc2-a784-73990b1bb5f6">

You may confirm the model is loaded and deployed in the Machine Learning menu Trained Models session
<img width="1705" alt="image" src="https://github.com/user-attachments/assets/40a5720e-069c-42c1-bb79-cf7f3b85e1ed">

# STEP 2 - Getting a PDF file, generating embeddings and loading in Elasticsearch
Choose the model from huggingface you want to use to generate embeddings. 
<img width="810" alt="image" src="https://github.com/user-attachments/assets/c46a4f33-d24a-49b2-872a-d566334243e2">

Connect to the cluster

<img width="806" alt="image" src="https://github.com/user-attachments/assets/eb35aec3-dbc4-4c4e-809a-2cb32603afa1">

Choose and load the PDF file

<img width="648" alt="image" src="https://github.com/user-attachments/assets/5c313326-7bd8-4e42-8963-8d9c5014166d">



# STEP 3 - Querying the documents
This step is optional. You can query the loaded document, however you will be only querying the document, without any integration with LLM, therefore, no RAG. Change the query to the right context.

<img width="519" alt="image" src="https://github.com/user-attachments/assets/1a5d0d14-e023-43b2-9ba3-05bc4d1b520c">

# STEP 4 - Using the Playground for RAG
For my tests I integrated GCP Gemini. You can choose any supported LLM. 

<img width="1701" alt="image" src="https://github.com/user-attachments/assets/09aec983-01e6-45cf-ab80-6d150d6e1a67">


After you integrate the LLM of your choice, choose the index you created in step 2, by clicking in Add Datasource and indicating the field with data. You may try different options in Number of documents sent to LLM

<img width="463" alt="image" src="https://github.com/user-attachments/assets/556a3f5d-bb3f-4b5e-985b-c7c3e4d2e7ca">


Include instructions in order to have better results 

<img width="454" alt="image" src="https://github.com/user-attachments/assets/9a2b510c-59bf-4d31-bb5e-47ddf9c3ece9">

After these configurations, you will be able to ask questions

<img width="963" alt="image" src="https://github.com/user-attachments/assets/1d0fdaa9-652f-484c-a790-48f74e31c3cf">

<img width="840" alt="image" src="https://github.com/user-attachments/assets/d2b5d13e-88d1-4d64-9b16-e281c6b7ed73">
