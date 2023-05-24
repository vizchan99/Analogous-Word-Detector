# Analogous-Word-Detector

This code implements various functions for word embeddings using GloVe vectors. Here's a breakdown of the different components:

The code imports necessary libraries and modules, including numpy and a custom module w2v_utils.

It reads GloVe word vectors from a file (glove.txt) using the read_glove_vecs function from w2v_utils. The loaded word vectors are stored in word_to_vec_map, a dictionary mapping words to their corresponding word vectors.

The code defines a cosine_similarity function, which computes the cosine similarity between two vectors using the dot product and vector norms.

Some example word vectors, such as "father," "mother," "ball," etc., are extracted from word_to_vec_map for demonstration purposes.

The code calculates and prints the cosine similarity between different word vectors, showcasing the similarity relationships between words.

The complete_analogy function performs word analogy completion. Given three words, it finds the fourth word that completes the analogy relationship based on cosine similarity calculations.

Several analogy triads are provided, and the complete_analogy function is applied to each triad. The results are printed to show the completed analogies.

A vector g is constructed by subtracting the "man" vector from the "woman" vector. This vector represents the gender bias direction.

The code calculates and prints the cosine similarity between the constructed vector g and various names and words. This demonstrates how cosine similarity can indicate gender bias or association.

The neutralize function removes the gender bias component from a word vector by projecting it onto the orthogonal space of the bias axis (g). The debiased word vector is returned.

The code applies the neutralize function to the word "receptionist" and calculates and prints the cosine similarity between the original and debiased vectors. The result shows a significant reduction in bias after neutralizing.

The equalize function equalizes the gender bias between word pairs by modifying their word vectors. It calculates the average vector (mu) and the bias component along the bias axis (g). Then, it projects the bias component of each word vector onto the orthogonal space and scales it to maintain the norm. The equalized word vectors are returned.

The code applies the equalize function to the word pair ("man", "woman") and calculates and prints the cosine similarities between the equalized vectors and the gender bias vector (g). This demonstrates how equalization can balance the bias between gendered word pairs.

Overall, this code provides functions to explore and analyze word embeddings, particularly with respect to gender bias. It showcases operations like cosine similarity, analogy completion, neutralization, and equalization to understand and address bias in word embeddings.
