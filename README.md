# VoiceSearchOpenAI
Voice_Search_OpenAI

Here is the basic concept behind how search happening in background :

 1) We use Langchain API to load all pdfs and make each word as vector.
  ex: if sentences contains these words : ["what", "is", "cover", "period"]
	It uses Vector representation for each character in the sentence or word by using one of the follwing ways :
	ex: BagOfWord, TF-IDF, Word2Vec 

    Vector representation of 'what': [0.03457806 0.01234567 -0.04567890 ...]
    Vector representation of 'is': [-0.02345678 0.04567890 -0.05678901 ...]
    Vector representation of 'cover': [0.05678901 -0.06789012 0.07890123 ...]
    Vector representation of 'period': [-0.06789012 0.07890123 -0.08901234 ...]
	
  2) Cevtor representation has been done for all the word so far present in the docs and indexetion has been done for each words.
  
  4) When user searches any text , voice input converted into text, search text has been converted to vector and it checks the cosine simillarity
     (distance between 2 vectors) in existing indexes and retrurns the results based on that.
     Example to calculate co-sine simillarity : https://www.geeksforgeeks.org/cosine-similarity/ and distance between vectors : https://www.toppr.com/ask/question/find-the-distance-between-the-points-a231-b123-using-vector-method/
  


