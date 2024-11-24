## Development of a Named Entity Recognition (NER) Prototype Using a Fine-Tuned BART Model and Gradio Framework

### AIM:
To design and develop a prototype application for Named Entity Recognition (NER) by leveraging a fine-tuned BART model and deploying the application using the Gradio framework for user interaction and evaluation.

### PROBLEM STATEMENT:
The goal is to develop an application that can accurately recognize and categorize named entities such as persons, organizations, locations, dates, etc., from input text. By fine-tuning a pre-trained BART model specifically for NER tasks, the system should be able to understand contextual relationships and identify relevant entities. The Gradio framework will be used to build a user-friendly interface for real-time interaction and evaluation.

### DESIGN STEPS:

#### STEP 1: Data Collection and Preprocessing
Gather a set of research articles or documents relevant to the topic. Preprocess the data by converting the articles into a suitable format (e.g., plain text or structured format). Tokenize the content and remove any irrelevant or noisy information.

#### STEP 2:Index Construction with LlamaIndex
Use LlamaIndex (formerly known as GPT Index) to create an index for the documents.LlamaIndex will help build an optimized index for efficient retrieval, making it easy to query multiple documents at once. Incorporate features like semantic search to improve relevance and accuracy of retrieval.

#### STEP 3: Query Handling and Response Generation
Develop the query interface where users can input questions related to the research articles. Integrate the query interface with the LlamaIndex-powered retrieval system.

#### STEP 4: Evaluation and Testing
Test the system with a range of diverse queries to evaluate its performance in terms of accuracy, relevance, and conciseness of responses. Collect feedback and refine the system based on test results.

### PROGRAM:
```
from llama_index import GPTSimpleVectorIndex, Document

# Step 1: Load and preprocess documents
documents = [
    Document("Research Article 1: Information about topic A..."),
    Document("Research Article 2: Insights into topic B..."),
    Document("Research Article 3: Analysis of topic C...")
]

# Step 2: Construct index using LlamaIndex
index = GPTSimpleVectorIndex(documents)

# Step 3: Query handling and retrieval
def query_system(query):
    response = index.query(query)
    return response

# Example query
user_query = "What is the relationship between topic A and topic B?"
response = query_system(user_query)
print(response)
```

### OUTPUT:
![image](https://github.com/user-attachments/assets/62009057-965d-4b20-95cd-f80a9b3143b6)


### RESULT:
The system successfully retrieves and synthesizes relevant information from multiple documents, providing concise and relevant answers to the user's query. Performance is evaluated based on the accuracy, relevance, and coherence of the responses.
