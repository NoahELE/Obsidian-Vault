---
date created: Wednesday, March 30th 2022, 12:55:37 pm
date modified: Friday, April 29th 2022, 9:44:25 am
---

# Week 5

## Data Linkage

Combining, grouping and matching electronic records to the same real life entities.

1. Preprocessing
2. Block
3. Score and Match
4. Merge

- Precision: $\#tp / (\#tp + \#fp)$
- Recall: $\#tp / (\#tp + \#fn)$
- Pair Completeness: $\#tp / \#tp + \#fn$
- Reduction Ratio: $1 - (\#fp + \#tp) / (\#fp + \#fn + \#tp + \#tn)$

## Privacy

- Dictionary Attack
- Frequency Attack

Organisation A and B do a data linkage:

- use a trusted third party C
- using one way hashing with a salt
- adding random records

> One way hashing only allows exact match

### Bloom Filter

Data structure: a bit array (an array of binary bits, only 0s and 1s)

A bloom filter with $I$ bits:

- Initialise all bits to 0
- Turn bits using $k$ number of hash functions $H_1, H_2, …, H_k$
- Each hash function maps input to an index in the bit array

#### Compare 2 Strings

- Given 2 strings.
  - Create a string into a set of smaller strings, e.g., bi-grams.
    - 'smith': S1{……}
    - 'smyth': S2{……}
  - Store S1 to a bloom filter B1
  - Store S2 to another bloom filter B2
  - Both B1 and B2 has the same length I and use the same k hash functions
- If 2 strings are similar which means many common bi-grams, B1 and B2 will have many identical bits set to 1.
- Calculate the similarity with Dice Similarity

> Hashing will cause collision and thus the final similarity will be an approximate of the actual similarity.
