# 🎨 AI-Powered Painting Analysis System

An end-to-end deep learning project that analyzes paintings using computer vision.
This system can:

* 🖌️ Predict painting metadata (style, artist)
* 🖼️ Find visually similar artworks using deep feature embeddings

Built using **PyTorch + EfficientNet**, designed for real-world applications in art analysis, recommendation systems, and digital museums.

---

## 🚀 Features

### 🔹 1. Painting Classification

* Predicts:

  * 🎨 Artist
  * 🖌️ Style / Genre
* Uses **EfficientNet (pretrained)** for high accuracy
* Trained on Rijksmuseum dataset

---

### 🔹 2. Visual Similarity Search

* Upload an image → find similar paintings
* Uses **deep feature embeddings**
* Cosine similarity-based retrieval
* Works on large datasets (25K+ images)

---

## 🧠 Model Architecture

### 📌 Classification Model

```
Image → EfficientNet → Fully Connected Layer → Class Prediction
```

### 📌 Similarity Model

```
Image → EfficientNet (Feature Extractor) → Embedding Vector → Cosine Similarity → Top-K Results
```

---

## 📂 Dataset

* Source: Rijksmuseum
* Size: ~5GB
* Images: ~25,000+
* Metadata: CSV (artist, type, etc.)

---

## 🛠️ Tech Stack

* Python 🐍
* PyTorch 🔥
* torchvision
* NumPy
* scikit-learn
* Matplotlib

---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/painting-analysis.git
cd painting-analysis

pip install -r requirements.txt
```

---

## ▶️ Usage

### 🔹 1. Extract Features

```python
features = extract_features(dataset)
```

---

### 🔹 2. Find Similar Images

```python
indices = find_similar(query_image, top_k=5)
show_results(query_image, indices)
```

---

## 📊 Results

* Classification Accuracy: ~70–85%
* Similarity Search:

  * Visually meaningful results
  * Works across styles and artists

---

## ⚡ Challenges Faced

* Handling large dataset (5GB)
* Efficient feature extraction
* GPU vs CPU performance issues
* Dataset structure inconsistencies
* Feature vector normalization bugs

---

## 🚀 Future Improvements

* 🔥 Faster search using FAISS
* 🎯 Multi-task learning (artist + style together)
* 🌐 Deploy as web app (Streamlit/Flask)
* 📱 Mobile-friendly interface
* 🧠 Fine-tuned embeddings for better similarity

---

## 💡 Applications

* Art recommendation systems
* Digital museum search engines
* Art style classification tools
* Educational platforms

---

## ⭐ Acknowledgements

* PyTorch
* Kaggle
* Rijksmuseum

