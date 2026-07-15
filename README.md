# Custom Byte-Pair Encoding (BPE) Tokenizer from Scratch using Python

## Overview

This project implements a **Custom Byte-Pair Encoding (BPE) Tokenizer from Scratch** using Python.

Byte-Pair Encoding is a subword tokenization technique used in Natural Language Processing (NLP). It converts words into smaller meaningful subword units by repeatedly merging the most frequent adjacent character pairs.

In this project, the complete BPE algorithm is implemented manually without using any existing NLP tokenizer libraries. The tokenizer learns vocabulary from a given corpus and performs encoding and decoding of text using learned merge rules.

---

# Objective

The main objectives of this project are:

- To understand the internal working of the Byte-Pair Encoding algorithm.
- To implement BPE tokenizer completely from scratch using Python.
- To learn subword vocabulary from a custom text corpus.
- To identify and merge the most frequent symbol pairs.
- To generate a final vocabulary with learned tokens.
- To implement text encoding and decoding functions.
- To convert tokens into unique token IDs.

---

# Technologies Used

- **Programming Language:** Python
- **Libraries Used:**
  - Collections (`defaultdict`)
- **Development Environment:**
  - Jupyter Notebook
  - GitHub

---

# Applications

Byte-Pair Encoding is widely used in various Natural Language Processing applications:

- Machine Translation
- Text Generation
- Sentiment Analysis
- Text Classification
- Search Engines
- Chatbots
- Large Language Models (LLMs)
- Speech and Language Processing Systems

---

# Features

- Implemented BPE algorithm from scratch.
- No pre-trained tokenizer libraries used.
- Character-level tokenization.
- Automatic vocabulary learning.
- Frequent pair identification and merging.
- Stores learned merge rules.
- Generates token IDs.
- Supports encoding of new words.
- Supports decoding back to original text.
- Easy to understand implementation for learning NLP concepts.

---

# Project Structure

```
Custom-BPE-Tokenizer/
│
├── BPE_Tokenizer.ipynb
│
├── README.md
│
└── requirements.txt
```

### File Description

**BPE_Tokenizer.ipynb**
- Contains complete Python implementation of the BPE tokenizer.
- Includes vocabulary creation, merging process, encoding, and decoding.

**README.md**
- Project documentation and explanation.

**requirements.txt**
- Contains required dependencies.

---

# Workflow

```
Input Text Corpus
        |
        ↓
Text Preprocessing
        |
        ↓
Split Words into Characters
        |
        ↓
Add End-of-Word Token (</w>)
        |
        ↓
Create Initial Vocabulary
        |
        ↓
Find Adjacent Symbol Pairs
        |
        ↓
Calculate Pair Frequencies
        |
        ↓
Select Most Frequent Pair
        |
        ↓
Merge Selected Pair
        |
        ↓
Update Vocabulary
        |
        ↓
Repeat Merge Process
        |
        ↓
Store Merge Rules
        |
        ↓
Build Final Vocabulary
        |
        ↓
Encode and Decode Text
```

---

# Algorithm

## Step 1: Select Corpus

A custom text corpus is provided for training the tokenizer.

Example:

```
low
lower
lowest
new
newer
widest
```

---

## Step 2: Preprocessing

The input text is cleaned and converted into lowercase format.

Example:

```
LOW → low
```

---

## Step 3: Character Splitting

Each word is split into individual characters with an end-of-word symbol.

Example:

```
lower

l o w e r </w>
```

---

## Step 4: Pair Frequency Calculation

The algorithm finds all adjacent character pairs and counts their frequency.

Example:

```
l o w </w>

Pairs:

(l,o)
(o,w)
(w,</w>)
```

---

## Step 5: Select Most Frequent Pair

The pair with the highest frequency is selected for merging.

Example:

Before:

```
l o
```

After:

```
lo
```

---

## Step 6: Vocabulary Update

The merged token replaces the original pair in the vocabulary.

The merge process continues until the required number of merges is completed.

---

## Step 7: Encoding

The encoder converts input words into learned subword tokens.

Example:

Input:

```
lower
```

Output:

```
['low','er','</w>']
```

---

## Step 8: Decoding

The decoder reconstructs the original word from generated tokens.

Example:

Input:

```
['low','er','</w>']
```

Output:

```
lower
```

---

# Sample Input Corpus

```
low
lower
lowest
new
newer
widest
```

---

# Result

The implemented BPE tokenizer successfully:

- Learned subword vocabulary from the given corpus.
- Generated merge rules based on pair frequency.
- Created final vocabulary.
- Converted words into subword tokens.
- Generated token IDs.
- Reconstructed original words using decoding.

Example Output:

```
Original Word : lower

Tokens :
['low', 'er', '</w>']

Token IDs :
[5, 3, 0]

Decoded :
lower
```
📸 Output Preview

<img width="638" height="347" alt="image" src="https://github.com/user-attachments/assets/ae0ed154-d6fc-48d0-828b-ee73f43c5c84" />
<img width="277" height="348" alt="image" src="https://github.com/user-attachments/assets/b978036b-48d3-47e4-b573-fa93b874fb48" />


# Conclusion

This project successfully demonstrates the implementation of a **Byte-Pair Encoding tokenizer from scratch using Python**.

The algorithm learns meaningful subword representations by repeatedly merging frequent character pairs. This project helps in understanding the basic mechanism behind modern NLP tokenizers used in transformer-based models and Large Language Models.
