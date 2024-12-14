# feed_search

## Project Overview
This project involves building a search system .The system retrieves the top 5 most relevant URLs from the Clearfeed knowledge base. The retrieval system is evaluated using an evaluation dataset, and a  generation layer is implemented using Google's Gemini API.

## Project Features

### Retrieval System:

Vectorizes the documents and queries using TF-IDF.  

Computes relevance scores using cosine similarity.  

Outputs the top 5 URLs for a given query.  

### Evaluation:

Measures the system's performance using:  

Mean Reciprocal Rank (MRR): Rewards higher ranks for correct answers.  

Precision: Measures whether the target URL is in the top 5 results.  


### Testing set:

Uses the top 5 retrieved URLs as context for an LLM.  

Generates concise answers to user queries using Google's Gemini API.

## Decision Made for Building the system

### Retrieval Approach:

Used TF-IDF vectorization for its simplicity and efficiency in converting text into feature vectors.  

Chose cosine similarity to compute relevance as it works well with high-dimensional sparse vectors.

### Evaluation Metrics:

MRR: Focuses on ranking quality and a higher score indicates that correct answers are positioned higher.  

Precision: Ensures significant top 5 results, aligning with the system requirements.  

### Answer Generation on Test Set:

Engineered Google's Gemini API to generate answers based on retrieved context.  

Ensures scalable solution for real-world test cases.



