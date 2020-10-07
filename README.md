# Data-Streams-Analyzing-Tool
**Objective:** to approximate the frequency of occurrences of different items in a data stream.

# Datasets
* [words_stream.txt](https://drive.google.com/file/d/1TA01NMOXDoqifBK_X7pnLXtEcO4sYGt4/view?usp=sharing): each line of this file is a number corresponding to the ID of a word in the stream.
* [counts.txt](https://drive.google.com/file/d/17XKrO9Lhtsrgn8L8IRzvqmHt8o5WVVf5/view?usp=sharing): each line is a pair of numbers separated by a tab. The first number is an ID of a word and the second number is its associated exact frequency count in the stream.
* [hash_params.txt](https://drive.google.com/file/d/1BDzy9DSFAOu-Pe7P4BqKXLHjx9yozxdt/view?usp=sharing): each line is a pair of numbers separated by a tab, corresponding to parameters a and for the hash functions

Assume 𝑆 = <𝑎<sub>1</sub>,𝑎<sub>2</sub>,...,𝑎<sub>𝑡</sub>> is a data stream of items from the set {1,2,...,n}. Assume for any 1 ≤ i ≤ n, F[i] is the number of times i has appeared in S. We would like to have good approximations of the values F[i] (1 ≤ i ≤ n) at all times.
A simple way to do this is to just keep the counts for each item 1 ≤ i ≤ n separately. However, this will require O(n) space, and in many applications (e.g., think online advertising and counts of user’s clicks on ads) this can be prohibitively large. We see in this problem that it is possible to approximate these counts using a much smaller amount of space. To do so, we consider the algorithm explained below.
