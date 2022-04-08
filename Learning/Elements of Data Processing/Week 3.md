---
date created: Tuesday, March 15th 2022, 7:24:43 am
date modified: Wednesday, April 6th 2022, 3:15:19 pm
---

# Week 3

## Unstructured Data: Text Pre-processing - String Matching and Comparison

Base string transformation:

- insert
- delete
- replace

## Unstructured Data: Text Pre-processing - Edit Distance and Similarity

### Levenshtein Distance

A minimum edit distance algorithm

Normalised Distance = distance / max(string1, string2)

Similarity = 1 - Normalised Distance

## Unstructured Data: Text Pre-processing - N-gram Distance and Similarity Indices

### N-gram Distance

N-gram: a substring of length n.

Bi-gram: substrings of length 2

Tri-gram: substrings of length 3

N-gram Distance between string x and y is : $|G_n(x)| + |G_n(y)| - 2 \times |G_n(x) \cap G_n(y)|$

- less sensitive to relative ordering of the strings (matches can be anywhere)
- more sensitive to long substring matches
- quite useless for very long string or very short alphabets
- potentially useful for (approximate) prefixes or suffixes

### Jaccard Similarity

$S_1, S_2$ stands for 2 strings' n-grams sets.

$$sim_{jac}(S_1, S_2) = \frac{|S_1 \cap S_2|}{|S_1 \cup S_2|}$$

### Sorensen-dice Similarity

$$sim_{dice}(S_1, S_2) = \frac{2 \times |S_1 \cap S_2|}{|S_1| + |S_2|}$$

### Cosine Similarity

Write the n-grams as a vector according to their number as X and Y.

$$cos(X, Y) = \frac{X \cdot Y}{||X|| \times ||Y||}$$

### Jaro-Winkler Similarity

- based on edit distances
- gives more weight to strings with matching prefixes
- useful for matching prefixes
- details not covered
