# 🎬 Netflix Recommendation Engine

![Python](https://img.shields.io/badge/Python-3.9+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-4C9ABE?style=for-the-badge&logo=python&logoColor=white)

> 🚀 A content recommendation system built on the **Netflix Prize Dataset** using **User-Based Collaborative Filtering** and **Cosine Similarity** — predicting what movies users will love based on their behaviour and ratings.

---

## 📌 Table of Contents

- [📖 Problem Statement](#-problem-statement)
- [🎯 Objectives](#-objectives)
- [📂 Dataset Information](#-dataset-information)
- [🛠️ Tech Stack](#️-tech-stack)
- [📁 Project Structure](#-project-structure)
- [⚙️ Installation & Setup](#️-installation--setup)
- [🚀 How to Run](#-how-to-run)
- [📊 Results & Insights](#-results--insights)
- [🤖 Model Details](#-model-details)
- [📸 Visualizations](#-visualizations)
- [👨‍💻 Author](#-author)

---

## 📖 Problem Statement

Customer behaviour prediction lies at the core of every modern business model. OTT platforms like **Netflix** and **Amazon Prime** analyse user activity patterns to suggest content that better suits individual needs and preferences.

> 💡 **Recommendation Engines** go one step further — they not only provide information but actively suggest strategies to increase user engagement with the platform.

This project builds a **Netflix Movie Recommendation Engine from the ground up**, where every user is recommended a list of movies best suited to their area of interest and ratings history.

---

## 🎯 Objectives

| # | Objective | Status |
|---|-----------|--------|
| 1️⃣ | Find the most **popular and liked genres** among Netflix users | ✅ Done |
| 2️⃣ | Build a model that recommends the **best-suited movie per genre** for each user | ✅ Done |
| 3️⃣ | Identify which genres received the **best and worst ratings** | ✅ Done |

---

## 📂 Dataset Information

**Source:** Netflix Prize Dataset  
**Files Used:**

| File | Description |
|------|-------------|
| `combined_data_1.txt` | Raw ratings data — `MovieID:` headers followed by `CustomerID, Rating, Date` rows |
| `movie_titles.csv` | Movie metadata — `MovieID, Year, Title` |

**Dataset Stats (after loading 600K rows):**

| Metric | Value |
|--------|-------|
| 📝 Total Ratings | 6,00,000 |
| 👤 Unique Customers | 2,29,763 |
| 🎬 Unique Movies | 175 |
| 📅 Date Range | 1999-12-09 → 2005-12-31 |
| ⭐ Average Rating | 3.568 / 5 |

**Columns in merged dataset:**

- 🔑 **MovieID** — Unique movie identifier
- 👤 **CustomerID** — Unique customer identifier
- ⭐ **Rating** — User rating (1–5 stars)
- 📅 **Date** — Date of rating
- 🎬 **Title** — Movie name
- 🎭 **Genre** — Inferred genre from title keywords
- 📆 **Year** — Release year

> ⚠️ **Note:** The Netflix Prize dataset does not include a genre column. Genre is inferred using **keyword-based title classification** across 10 categories.

---

## 🛠️ Tech Stack

| Library | Purpose |
|---------|---------|
| 🐍 `Python 3.9+` | Core programming language |
| 🐼 `Pandas` | Data loading, merging, and manipulation |
| 🔢 `NumPy` | Numerical operations |
| 📊 `Matplotlib` | Static visualizations |
| 🎨 `Seaborn` | Statistical plots (violin, box, heatmap) |
| 🤖 `Scikit-Learn` | Cosine Similarity for collaborative filtering |
| 📓 `Jupyter Notebook` | Interactive development environment |

---

## 📁 Project Structure

```
netflix-recommendation-engine/
│
├── 📓 Netflix_Executed.ipynb        # Fully executed Jupyter Notebook
├── 📄 combined_data_1.txt           # Raw Netflix ratings data
├── 📄 movie_titles.csv              # Movie titles and release years
└── 📖 README.md                     # Project documentation (this file)
```

---

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/MayankJaiswal1/netflix-recommendation-engine.git
cd netflix-recommendation-engine
```

### 2️⃣ Install Required Libraries
```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
```

### 3️⃣ Place Dataset Files
Ensure `combined_data_1.txt` and `movie_titles.csv` are in the **same folder** as the notebook.

---

## 🚀 How to Run

```bash
jupyter notebook Netflix_Executed.ipynb
```

> 💡 The notebook is **pre-executed** — all outputs, charts, and results are already embedded. You can also re-run all cells fresh with your own data.

---

## 📊 Results & Insights

### 🎭 Objective 1 — Most Popular & Liked Genres

**By Popularity (Total Ratings):**

| Rank | Genre | Total Ratings |
|------|-------|--------------|
| 🥇 | Drama | 5,33,355 |
| 🥈 | Horror | 28,210 |
| 🥉 | Romance | 18,901 |
| 4 | Sci-Fi | 7,203 |
| 5 | Comedy | 6,190 |

**By Likability (Average Star Rating):**

| Rank | Genre | Avg Rating |
|------|-------|-----------|
| 🥇 | Sci-Fi | ⭐ 3.880 |
| 🥈 | Action | ⭐ 3.743 |
| 🥉 | Comedy | ⭐ 3.742 |
| 4 | Romance | ⭐ 3.694 |
| 5 | Thriller | ⭐ 3.673 |

> 🏆 **Most Popular:** Drama &nbsp;|&nbsp; ⭐ **Most Liked:** Sci-Fi

---

### 🤖 Objective 2 — Best Movie Recommendations per Genre

| 🎭 Genre | 🎬 Recommended Movie | ⭐ Avg Rating |
|---------|---------------------|-------------|
| Drama | Lord of the Rings: Return of the King (Extended) | 4.552 |
| Fantasy | Elfen Lied | 4.252 |
| Romance | I Love Lucy: Season 2 | 4.090 |
| Thriller | Zatoichi's Conspiracy | 3.989 |
| Sci-Fi | Star Trek: Voyager Season 1 | 3.942 |
| Action | The Battle of Algiers | 3.915 |
| Comedy | Funny Face | 3.742 |
| Horror | The Devil's Brigade | 3.539 |
| Animation | Cartoon Network Halloween | 3.388 |
| Documentary | Full Frame: Documentary Shorts | 3.030 |

---

### 📉 Objective 3 — Best & Worst Rated Genres

| Metric | Genre | Avg Rating |
|--------|-------|-----------|
| 🏆 Best Rated | **Sci-Fi** | ⭐ 3.880 |
| 📉 Worst Rated | **Documentary** | ⭐ 3.028 |
| — | Overall Mean | ⭐ 3.568 |

> 📌 Gap between best and worst: **0.852 stars**

---

## 🤖 Model Details

### Algorithm: User-Based Collaborative Filtering

```
User Ratings Matrix  →  Cosine Similarity  →  Similar Users  →  Top Unseen Movie per Genre
```

**Steps:**
1. 🗃️ Build a **User × Movie rating matrix** (500 most active users)
2. 📐 Compute **Cosine Similarity** between every pair of users
3. 🔍 For a target user, find the **top 20 most similar users**
4. 🎬 From movies they liked (that target hasn't seen), pick the **highest-rated per genre**
5. 🔁 Fallback to **global top** if no similar-user data is available

**Matrix Size:** 500 users × 175 movies  
**Similarity Metric:** Cosine Similarity (sklearn)

---

## 📸 Visualizations

The notebook includes the following charts — all generated from real Netflix data:

| # | Chart | Description |
|---|-------|-------------|
| 📊 | Rating Distribution | Bar + Pie chart of 1–5 star ratings |
| 📊 | Genre Popularity | Horizontal bar — total ratings per genre |
| 📊 | Genre Likability | Horizontal bar — avg rating per genre |
| 🔥 | Similarity Heatmap | Cosine similarity matrix (top 15 users) |
| 🎬 | Recommendations Chart | Best movie per genre for target user |
| 📦 | Box Plot | Rating spread per genre |
| 🎻 | Violin Plot | Rating distribution density per genre |
| 📈 | Trend Line | Quarterly avg rating trend by genre (1999–2005) |

---

## 👨‍💻 Author

**Mayank Jaiswal**  

---

## 📜 License

This project is for educational purposes as part of the **Intellipaat Python Capstone Project**.  
Dataset belongs to **Netflix** (Netflix Prize, 2006).

---

<p align="center">
  Made with ❤️ and 🐍 Python &nbsp;|&nbsp; ⭐ Star this repo if you found it helpful!
</p>
