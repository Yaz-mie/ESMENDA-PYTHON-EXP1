# Python Essentials – Programming Assignment 1

**Author:** ESMENDA, Francine Jasmine Guelle T.  
**Course:** ECE2112 – Advanced Computer Programming and Algorithms

---

## Overview

This repository contains a single Jupyter Notebook that demonstrates core Python ideas using three short problems.  
Concepts covered: **functions**, **string manipulation**, **dictionaries**, and **list unpacking**.

**Notebook:** `ESMENDA_EXP1.ipynb`

---

## Problems & Solutions

### 1) Alphabet Soup (sorting characters)
Sort the letters in a given word and return the alphabetically ordered string.

```python
def alphabet_soup(text):
    return "".join(sorted(text))

#Examples
print(alphabet_soup("hello"))   # 'ehllo'
print(alphabet_soup("hacker"))  # 'acehkr'
```

**Notes**
- `sorted(text)` splits the string into characters and sorts them.
- `"".join(...)` stitches the sorted characters back into a string.
- These print lines are there to test if the function works correctly.

---

### 2) Emotify (word → emoticon)
Replace special words in a sentence with their corresponding emoticons.

```python
def emotify(sentence):
    emoticons = {"smile": ":)", "grin": ":D", "sad": ":(", "mad": ">:("}
    words = sentence.split()
    converted = [emoticons.get(word, word) for word in words]
    return " ".join(result)

#Examples
print(emotify("Make me smile"))  #'Make me :)'
print(emotify("I am mad"))       #'I am >:('
print(emotify("She is grin"))    #'She is :D'
print(emotify("He is sad"))      #'He is :('
```

**Notes**
- Uses a **dictionary** to map keywords → emoticons.
- Keeps all other words unchanged.
- emoticons, dictionary mapping words (smile, grin, etc.) to their symbols.
- sentence.split() separates the sentence into words.
- [emoticons.get(word, word) for word in words] replaces any matching word with its emoticon.
- " ".join(result) puts the words back into a full sentence.
- Print lines are there to show different cases where the dictionary replaces words with emoticons.

---

### 3) List Unpacking (first, middle, last)
Extract the first, all middle elements, and the last element from a list using Python’s unpacking syntax.

```python
numbers = [1, 2, 3, 4, 5, 6]

first, *middle, last = numbers

print("first:", first)     #1
print("middle:", middle)   #[2, 3, 4, 5]
print("last:", last)       #6
```

**Notes**
- `first` receives the first element, `last` the final element.
- `*middle` captures the remaining elements in between as a list.
- The print lines are there to show how unpacking distributes values across variables.

---
### Version History
v1.0 – Initial notebook with Alphabet Soup Problem

v1.1 – Added Emotify Problem function + test cases

v1.2 – Added List Unpacking example and explanations

v1.3 – Improved comments and code formatting for readability

v1.4 – Added detailed README file with problem explanations

---
