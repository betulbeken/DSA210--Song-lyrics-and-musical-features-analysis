# 🎵 Music Features & Lyrics Analysis

**Student:** Betül Eken  
**Course:** DSA210 – Introduction to Data Science  

---

## 🚀 Project Overview

Music is a complex form of expression shaped by both **acoustic properties** and **linguistic content**.  
While platforms like Spotify quantify songs using numerical audio features (e.g., energy, valence, tempo), lyrics reflect emotional and linguistic patterns that are harder to capture.

This project explores **what can and cannot be inferred** from musical and lyrical features by analyzing their relationship with song-level attributes such as **popularity**, **emotional valence**, and **energy**.  
Rather than aiming for high predictive accuracy, the focus is placed on understanding the **limitations and strengths** of surface-level audio and lyrical representations.

The final dataset consists of approximately **1,700 songs**, created by merging two public Spotify-related datasets.

---

## 💡 Motivation

Music recommendation systems often rely heavily on numerical audio features, yet listeners also engage deeply with lyrics.  
This project is motivated by a simple question:

> *To what extent do lyrics and musical features actually explain how songs feel and perform?*

By combining audio features with basic NLP-based lyrical features, this study investigates whether commonly used representations are sufficient to explain complex musical phenomena.

---

## 🎯 Objectives

- Merge and preprocess audio and lyrics datasets  
- Extract basic **lyrical complexity features** using NLP  
- Explore relationships between lyrics, musical features, and emotional attributes  
- Evaluate the predictive power of lyrical and musical features using **statistical analysis and machine learning**  
- Interpret results with a focus on **limitations**, not just performance  

---

## ❓ Research Questions

- Can song **popularity** be predicted using:
  - musical features?
  - lyrical features?
  - a combination of both?
- Are **simpler and more repetitive lyrics** associated with higher popularity?
- Can a song’s **emotional valence (mood)** be predicted from lyrical features?
- Can **song energy level** (high vs. low) be inferred using lyrics alone?

---

## 🗂️ Data Collection & Sources

The analysis uses two public Kaggle datasets:

### 1. Spotify Tracks Dataset  
🔗 https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset  

Includes numerical audio features such as:
`energy`, `valence`, `tempo`, `loudness`, `danceability`

### 2. Audio Features and Lyrics Dataset  
🔗 https://www.kaggle.com/datasets/imuhammad/audio-features-and-lyrics-of-spotify-songs  

Includes:
- full song lyrics  
- track and artist metadata  

After merging and filtering (removing instrumental and very short songs), **1,700+ songs** remain.

---

## 🧠 Tools & Libraries

- **Python**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Scikit-learn**
- **NLTK**

---

## 📊 Key Findings (Summary)

- **Song popularity** cannot be reliably predicted using musical or lyrical features alone  
- **Lyrical simplicity** shows a weak but consistent association with higher popularity  
- **Emotional valence** can be partially predicted from lyrics, but performance remains modest  
- **Song energy** cannot be predicted using lyrics alone, highlighting the dominant role of musical and production features  

Overall, the results suggest that **lyrics convey emotional tone to some extent**, but **popularity and musical intensity are driven by factors beyond surface-level textual features**.

---

## 📁 Repository Structure

- `*.ipynb` – Full analysis notebook  
- `README.md` – Project overview  
- Datasets are accessed via external links (not stored locally)
