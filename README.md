# Custom Byte-Pair Encoding (BPE) Tokenizer from Scratch

## Project Overview

This project implements a **Custom Byte-Pair Encoding (BPE) Tokenizer from Scratch** using Python.

Byte-Pair Encoding (BPE) is a subword tokenization algorithm widely used in Natural Language Processing (NLP). It learns meaningful subword units by repeatedly merging the most frequent adjacent symbol pairs in a given text corpus.

This implementation does not use any existing tokenizer libraries. The complete BPE algorithm is manually implemented using Python.

---

# Objective

The main objective of this project is to:

- Understand the working process of BPE tokenization.
- Build a tokenizer from scratch using Python.
- Learn subword vocabulary by merging frequent character pairs.
- Implement encoding and decoding functions.
- Generate token IDs from learned vocabulary.

---

# Algorithm Flow


---

# Dataset / Corpus

The input corpus contains simple English words:



Each word is converted into character-level tokens with an end-of-word symbol.

Example:


---

# Technologies Used

- Python
- Collections Library
- Dictionary Data Structures

---

# Implementation Steps

## 1. Corpus Selection

A small text corpus is manually created inside the Python program.

Example:

```python
[
"low",
"lower",
"lowest",
"new",
"newer",
"widest"
]

