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
  * x
* References 
  *  l 
  *  t
  

