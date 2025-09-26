# 📄 Document Similarity Finder — Run Report

## 📅 Date
2025-09-26

---

## 📂 Dataset
- Filename: `documents.csv`  
- Number of documents: 15  
- Columns:
  - `doc_id` → Unique ID for each document
  - `text` → Raw document content

---

## ⚙️ Environment
- Python version: 3.10 (Colab)  
- Packages:
  - pandas==2.1.x
  - numpy==1.26.x
  - nltk==3.8.x
  - scikit-learn==1.3.x
  - matplotlib==3.7.x
  - seaborn==0.12.x

---

## 🔧 Workflow
1. **Preprocessing**:
   - Lowercased text  
   - Removed punctuation  
   - Removed stopwords  
   - Lemmatization  

2. **TF-IDF Vectorization**:
   - Vectorized all documents into TF-IDF matrix  
   - Shape: `(15, 90)`  

3. **Cosine Similarity**:
   - Computed similarity between all document pairs  
   - Created a similarity matrix (heatmap)

4. **Top 3 Most Similar Pairs**:
   - Ignored self-similarity  

---

## 📊 Results

**Top 3 most similar document pairs:**
| Document Pair | Cosine Similarity |
|---------------|-----------------|
| 3 & 4         | 0.4580          |
| 4 & 3         | 0.4580          |
| 1 & 2         | 0.3612          |

**Similarity Matrix Heatmap:**  
![Similarity Matrix](docs/similarity_heatmap.png)

---

## 🔍 Observations
- Documents 3 & 4: Both discuss birds in the Amazon → high similarity  
- Documents 1 & 2: Both discuss stock market downturn → high similarity  
- Some documents have very low similarity, indicating diverse topics

---

## ⚡ Next Steps / Improvements
- Add **more documents** for richer similarity results  
- Use **cosine similarity threshold** to cluster similar documents  
- Apply **advanced embeddings** (Word2Vec, BERT) for semantic similarity  
- Build a **web interface** to input new documents and find similar ones
