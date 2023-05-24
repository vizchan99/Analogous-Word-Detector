# Analogous-Word-Detector

This code implements various functions for word embeddings using GloVe vectors. Here's a breakdown of the different components:
To run this code you need to download the GLoVE dataset.

The code imports necessary libraries and modules, including numpy and a custom module w2v_utils.

It reads GloVe word vectors from a file (glove.txt) using the read_glove_vecs function from w2v_utils. The loaded word vectors are stored in word_to_vec_map, a dictionary mapping words to their corresponding word vectors.
Overall, this code provides functions to explore and analyze word embeddings, particularly with respect to gender bias. It showcases operations like cosine similarity, analogy completion, neutralization, and equalization to understand and address bias in word embeddings.
