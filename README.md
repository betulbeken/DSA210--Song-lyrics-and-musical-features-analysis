# 🎵 Music Features & Lyrics Analysis

I'm **Betül Eken**, a sophomore Computer Science and Engineering student at Sabancı University.  
This is my **term project for DSA210 (Introduction to Data Science)**.

---

## 📘 Table of Contents
1. [Project Overview](#project-overview)  
2. [Motivation](#motivation)  
3. [Objectives](#objectives)  
4. [Research Questions](#research-questions)  
5. [Data Collection & Sources](#data-collection--sources)  
6. [Tools & Libraries](#tools--libraries)  

---

## 🎯 Project Overview
This project explores the relationship between **musical characteristics** (such as energy, loudness, and acousticness) and **lyrics-based properties** (like length, word diversity, and repetition).  
By merging **audio feature data** and **lyrics data**, the goal is to analyze how musical features align with textual patterns.  

The merged dataset contains approximately **1,700 songs**, created by combining two public Kaggle datasets using the song and the artist names as matching keys.

---

## 💡 Motivation
Music is one of the most universal forms of human expression and a beautiful art.  
While platforms like Spotify evaluate songs through numerical attributes (energy, valence, tempo), the lyrics carry emotional and linguistic meaning.  
Through this project, I aim to connect these two perspectives — exploring whether songs that *sound* similar also *read* similarly, even when analyzed through simple statistical and linguistic features.

---

## 🎯 Objectives
- **Merge** and preprocess two different song datasets.  
- **Perform exploratory data analysis (EDA)** to uncover general patterns and correlations.  
- **Analyze** basic textual features of lyrics (e.g., word count, vocabulary diversity, repetition).  
- **Apply** statistical and machine learning techniques (e.g., correlation tests, regression, clustering).  
- **Visualize** results using Python libraries.  
- **Communicate** key findings clearly through graphs and interpretations.

---

## ❓ Research Questions
1. Are there correlations between **lyrics length or complexity** and musical features like energy or valence?  
2. Do songs with higher **danceability or energy** scores have simpler or more repetitive lyrics?  
3. Can basic lyrical characteristics (e.g., word count, vocabulary richness) help **predict audio features** using simple ML models such as Linear Regression or Decision Tree?  
4. How do different **artists or genres** differ when comparing their lyrical and acoustic patterns?

---

## 🗂️ Data Collection & Sources

The analysis uses two public Kaggle datasets:

### **1. Spotify Tracks Dataset**
🔗 [Spotify Tracks Dataset](https://www.kaggle.com/datasets/maharshipandya/-spotify-tracks-dataset?resource=download)  
Includes over 100,000 songs with audio and metadata information:
- `energy`, `loudness`, `acousticness`, `valence`, `tempo`, etc.  
- `artist_name`, `track_name`, `album_name`

### **2. Audio Features and Lyrics Dataset**
🔗 [Audio Features and Lyrics Dataset](https://www.kaggle.com/datasets/imuhammad/audio-features-and-lyrics-of-spotify-songs)  
Contains:
- `track_name`, `artist_name`, `album_name`  
- `lyrics` (full text of each song)  
- some additional audio features

After merging the two datasets on matching fields and getting rid of the same rows, **1,778 common songs** remain and will be used for all analysis steps. If a problem with the datasets emerge, I will find new datasets from Kaggle.

---

## 🧠 Tools & Libraries

- **Python** – main programming language  
- **Pandas**, **NumPy** – data manipulation and preprocessing  
- **Matplotlib**, **Seaborn** – data visualization  
- **Scikit-learn** – applying regression and clustering models  
- **Basic text analysis using Python** – computing word counts, average word length, and frequency statistics

## 📊 Exploratory Data Analysis & Key Findings

In this phase, we merged Spotify Audio Features with lyrics data to analyze the relationship between musicality and textual complexity.

### 1. Feature Engineering
To ensure statistical rigor, we moved beyond simple word counts and implemented **NLP-based feature extraction**:
* **Clean Word Count:** Removed stop-words (e.g., "the", "and") to count only meaningful words.
* **Lexical Diversity (TTR):** Calculated the Type-Token Ratio to measure vocabulary richness.
* **Filtering:** Excluded instrumental tracks (Instrumentalness > 0.5) to prevent skewing the text analysis.

### 2. Hypothesis Testing Results
Since the data followed a Power Law distribution rather than a Normal distribution, we used **Spearman Rank Correlation** and **Mann-Whitney U Tests**.

* **Finding 1: Lyrical Complexity vs. Energy**
    * *Result:* We observed a statistically significant difference (p < 0.05) in lyrical complexity between "High Energy" and "Low Energy" songs.
    * *Insight:* **Low Energy (Sad/Calm)** songs have a **higher median lexical diversity (0.41)** compared to High Energy songs (0.38). This suggests that calmer songs tend to use a richer, more varied vocabulary, while energetic songs rely more on repetition.
    
* **Finding 2: Popularity vs. Lyrics**
    * *Result:* There is a weak negative correlation between **Lexical Diversity** and **Track Popularity**.
    * *Insight:* Mainstream hits tend to feature simpler, more repetitive lyrics, potentially making them "catchier" and easier for global audiences to memorize.

### 3. Visualizations
*Please refer to the `Exploring_Lyrical_and_Musical_Features_of_Songs.ipynb` notebook for full interactive charts including:*
* Correlation Heatmaps (Audio vs. Lyrical Features).
* Scatter plots of Tempo vs. Lexical Diversity.
* Word Clouds of the most frequent meaningful words in the dataset.
