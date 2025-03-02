  ![Netflix Logo](https://upload.wikimedia.org/wikipedia/commons/7/75/Netflix_icon.svg)

# 🎬 Netflix Movies & TV Shows Clustering Project 🎭

## 📌 Overview
This project explores the clustering of Netflix shows and movies using **Natural Language Processing (NLP)** and **Machine Learning (ML)** techniques. The dataset, sourced from [Flixable](https://www.flixable.com/), contains details of TV shows and movies available on Netflix as of 2019.

---
## 🚀 Problem Statement
With the rapid expansion of Netflix's content library, categorizing and grouping similar content is crucial. Clustering helps in identifying patterns and structuring the data efficiently. This project aims to:

✅ Perform **Exploratory Data Analysis (EDA)** 📊  
✅ Understand Netflix's **content distribution across different countries** 🌍  
✅ Analyze Netflix’s **shift towards TV shows over time** 📅  
✅ Cluster **similar content using NLP techniques** 🔍  
✅ Build a **Recommender System** 🤖  

---
## 📂 Dataset Description
The dataset consists of **7787 records** with the following attributes:

| Column | Description |
|---|---|
| `title` | Name of the movie or TV show |
| `director` | Director of the movie/show |
| `cast` | List of actors & actresses |
| `country` | Production country |
| `date_added` | When it was added to Netflix |
| `release_year` | Year of release |
| `rating` | Netflix rating |
| `duration` | Length of the movie/show |
| `listed_in` | Genres |
| `description` | Brief summary |

---

![Image](https://github.com/user-attachments/assets/96ef4f6e-24ec-438d-93da-9edfdd165c19)

## 📊 Exploratory Data Analysis (EDA)

### 🔹 Key Findings:
✔ More **movies** than TV shows, but Netflix has focused more on TV shows in recent years.  
✔ Majority of content is rated **TV-MA (Mature Audience)** or **TV-14**.  
✔ Popular genres: **Documentaries, Stand-up Comedy, Drama, International Movies, Comedy**.  
✔ **USA & India** are the top content producers.  
✔ Netflix Originals account for **30%+** of total content.  

![Netflix Data Distribution](https://www.example.com/netflix_data_distribution.png)  

---
## 🛠 Data Preprocessing & Feature Engineering

📌 **Handling Missing Values:**
- Replaced missing values in `director`, `cast`, `country`, and `rating` with **'Unknown'**.
- Dropped `date_added` missing values (~0.09% of total data).

📌 **Feature Engineering:**
- Extracted **year** from `date_added`.
- Converted `duration` to **integer values**.
- Created a **word cloud** for common genres.

---
## 📝 Natural Language Processing (NLP)
To prepare textual data for clustering, we performed:

- **Merging** important text columns (title, director, cast, genres, description).
- **Lowercasing & Removing Punctuation**.
- **Stopword Removal**.
- **Text Normalization (Stemming & Lemmatization)**.
- **TF-IDF Vectorization** (for numerical representation of text).

---
## 🔢 Dimensionality Reduction (PCA)
To handle high-dimensional data after TF-IDF vectorization, we applied **Principal Component Analysis (PCA)**, capturing **95% variance** in **5000 components**.

---
## 🔍 Clustering Techniques
We experimented with different clustering models:

### 🎯 **1. K-Means Clustering**
- Used **Elbow Method** & **Silhouette Score** to find optimal `K`.
- Chose **5 clusters**, achieving **variance of 58,185** and **silhouette score of 0.458**.

### 🎯 **2. Agglomerative Hierarchical Clustering**
- Used **Dendrograms** to select `n_clusters = 11`.
- Achieved a **silhouette score of 0.389**.

📌 **Final Model:** *K-Means performed better, so it was selected.*

---
## 🎯 Recommender System
To enhance the usability of clustering, we built a **content-based recommender system**:
- **Used Cosine Similarity** on TF-IDF matrix.
- **Provided recommendations** for similar shows/movies based on user input.

---
## 📷 Sample Visuals
![Netflix Genre WordCloud](https://www.example.com/netflix_wordcloud.png)
![Elbow Method for KMeans](https://www.example.com/kmeans_elbow.png)
![Dendrogram for Agglomerative Clustering](https://www.example.com/dendrogram.png)

---
## 🏆 Conclusion & Future Scope
✅ Successfully grouped Netflix content into clusters using NLP + ML.  
✅ Identified key **patterns & trends** in Netflix’s content strategy.  
✅ Built an **effective recommendation system** for personalized suggestions.  

🔮 **Future Improvements:**
- Incorporate **IMDB & Rotten Tomatoes ratings** for better clustering.
- Experiment with **DBSCAN** or **Topic Modeling (LDA)**.
- Develop a **web-based app** for interactive recommendations.

---
## 📜 Technologies Used
| Tool | Purpose |
|---|---|
| **Python** | Programming Language |
| **Pandas, NumPy** | Data Wrangling |
| **Matplotlib, Seaborn** | Data Visualization |
| **NLTK, SpaCy** | Natural Language Processing |
| **TF-IDF Vectorization** | Text Processing |
| **PCA** | Dimensionality Reduction |
| **K-Means, Hierarchical Clustering** | Clustering Techniques |
| **Cosine Similarity** | Recommendation System |

---
## 📌 Project Structure
```
📂 Netflix_Movies_and_TV_Shows_Clustering
│── 📁 data                   # Dataset files
│── 📁 images                 # Visuals and plots
│── 📁 notebooks              # Jupyter Notebooks
│── 📄 README.md              # Project Documentation
```

---
## 📬 Contact
🔗 **GitHub:** [Your GitHub Profile](https://github.com/yourusername)  
💼 **LinkedIn:** [Your LinkedIn](https://www.linkedin.com/in/yourname/)  
📧 **Email:** yourname@email.com  

⭐ *If you found this project useful, consider giving it a star! ⭐*
