---
date created: Wednesday, March 23rd 2022, 11:04:01 am
date modified: Friday, April 8th 2022, 1:48:46 pm
---

# Week 4

## Text Pre-Processing

### Tokenization

- Granularity of a token
    - sentence
    - word
- Token separators

### Case Folding

- convert text to consistent cases
- reduce sparsity

### Stemming

- remove and replace suffices to arrive at root form

### Lemmatization

- transform words to valid roots

### Stop Word Removal

- stop words are function words that structure sentences, they carry low information.

### Text Normalisation

- transform words to standard version

### Noise Removal

- remove unnecessary spaces
- remove punctuation
- unify numbers

## Bag of Words

- simplest vector space representation model for text
- disregard word order or grammatical features
- each document as a vector
    - each dimension is a specific word for corpus
    - the value can be its frequency or occurrence (denoted by 0 and 1)

## TF-IDF

Term Frequency-Inverse Document Frequency

A combination of 2 metrics to weight a term:

- tf (term frequency): how often a given word appears within a document
- idf (inverse document frequency): down-weights words that appear in many documents

Main Idea: reduce the weight of frequent terms and increase the weight of rare and indicative ones

Formula:

- tf: $$tf(t, d) = the\ raw\ count\ of\ the\ word\ in\ the\ document$$
- idf: $$idf(t) = ln(\frac{1 + N}{1 + df_t}) + 1\ or\ ln(\frac{N}{df_t}) + 1$$
  - $N$ is the number of document in the collection
  - $df_t$ is the document frequency, the number of documents containing term $t$
- tf-idf: $$tf\_idf(t, d) = \frac{v_t}{\sqrt{\sum_{t' \in d}v_{t'}^2}}$$, where $$v_t = tf(t, d) \times idf(t)$$

### Part of Speech Tagging

Tag features of text e.g. nouns or noun phrases, adjectives, verbs etc.
