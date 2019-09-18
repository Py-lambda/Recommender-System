# Recommender-System
Content-based recommenders: suggest similar items based on a particular item. The general idea behind this recommender system is that if a person liked a particular item, he or she will also like an item that is similar to it.
More specifically, we will compute pairwise similarity scores for all movies based on their plot descriptions and recommend movies based on that similarity score.
Computing Term Frequency-Inverse Document Frequency (TF-IDF) vectors for each document will give a matrix where each column represents a word in the overview vocabulary (all the words that appear in at least one document) and each column represents a movie, as before.

TF-IDF score = frequency of a word occurring in a document / number of documents in which it occurs

This is done to reduce the importance of words that occur frequently in plot overviews and therefore, their significance in computing the final similarity score.
We will use the cosine similarity to calculate a numeric quantity that denotes the similarity between two movies. We will be using the cosine similarity score since it is independent of magnitude and is relatively easy and fast to calculate (especially when used in conjunction with TF-IDF scores.
Mathematically, it is defined as follows: 

cosine(x,y) = x.y⊺ / ||x||.||y||

Since you have used the TF-IDF vectorizer, calculating the dot product will directly give you the cosine similarity score.
