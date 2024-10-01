# Retrieval_PostRetrieval_GraphRAG
The retrieval process consists of three steps: 
* pre-retrieval
* retrieval
* post-retrieval

# retrieval process enhanced with re-ranking
Utilizing (large) language models in similarity scoring algorithms like Cross-Encoder and BERTScore to improve retrieval capabilities, particularly as a post-retrieval step in systems like RAG.

![Post Retrieval](Workflow-Reranker_RAG.jpg)



Ranking and Re-ranking:
* Bi-Encode
  * scores sentence pairs by generating embeddings in a vector space
  * a language model independently processes each chunk (sentence)
  * embeddings can be compared using similarity measures
* Cross-Encoder
  * predicts textual similarity by inputting two sentences into a Transformer network, followed by a classifier to determine similarity probability.
  * Cross-Encoders significantly improve re-ranking accuracy by performing attention mechanisms across queries and documents, but are computationally intensive. Therefore, a combination of Bi-Encoder for initial retrieval and Cross-Encoder for re-ranking is effective, balancing speed and accuracy
  * ![Cross-Encoder](cross-encoder.jpg)
* BERTScore 
  * computes similarity scores between reference and candidate sentences using contextual embeddings from a Language Model. It is calculated by summing cosine similarities of token-level embeddings extracted by a pre-trained BERT model, with token importance weighted accordingly
#Experiment
* Language models utilized in extracting embeddings
* The models are DistilBERT from the sentence-transformers library, "msmarco-distilbert-dot-v5," with 66M parameters creating a 768-dimensional vector, and GPT-2 large from the Transformers library with 774M parameters generating a 1280-dimensional vector. DistilBERT handles 512 tokens per sequence, while GPT-2 large can process 1024 tokens
 # Tables
* References 
  *  l 
  *  t
  

