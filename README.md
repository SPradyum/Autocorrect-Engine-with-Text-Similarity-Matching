# Python Autocorrect System Using NLP & Text Similarity

This project implements a simple but effective **autocorrect system** using:
- **Tokenization & vocabulary building**
- **Word frequency probabilities**
- **Jaccard similarity** for string matching
- **Pandas for ranking suggestions**

The script reads a text corpus, builds a vocabulary, computes word frequencies, and suggests the most probable corrections for misspelled words.

---

## 🚀 Features
- Extracts all words from a text file using regex
- Builds a unique vocabulary set
- Calculates word frequency distribution using `Counter`
- Computes probability of each word occurrence
- Uses **TextDistance Jaccard-q2** similarity to measure closeness
- Returns top autocorrect candidates sorted by:
  1. Similarity Score  
  2. Word Probability  

---

## ✅ How It Works

1. Load the text file and convert it to lowercase  
2. Tokenize words using regex  
3. Build the vocabulary  
4. Compute word frequencies and probabilities  
5. For any input word:
   - If it exists in vocabulary → "Your word seems to be correct"
   - If not → compute similarity with all vocabulary words  
   - Sort by similarity & probability  
   - Return top predictions  

---

## 📦 Requirements
Install dependencies:
```bash
  pip install pandas numpy textdistance
```
## Example
```bash
print(my_autocorrect('neverteless'))
```
