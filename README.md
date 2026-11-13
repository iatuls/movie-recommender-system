# 🎬 Movie Recommender System

A content-based movie recommendation web app built with Python and Streamlit. Pick a movie and get 5 similar movies based on its genre, plot overview, director and cast.

## 🌐 Live Demo

[Try the app here](https://movie-recommender-system-atul.streamlit.app/)


## 🔍 How It Works

1. **Data cleaning**: removed duplicates, unused columns and placeholder plot texts from the IMDB movie dataset (1951–2023).
2. **Tag creation**: combined genre, overview, director and cast of each movie into a single `tags` text.
3. **Text processing**: lowercased the text and applied Porter stemming (e.g. *abusing*, *abused*, *abuse* all become *abus*).
4. **Vectorization**: converted tags into vectors using `CountVectorizer` (top 5000 words, English stop words removed).
5. **Similarity**: computed cosine similarity between every pair of movies.
6. **Recommendation**: for the selected movie, the 5 most similar movies are returned.

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- NLTK (stemming)
- Scikit-learn (CountVectorizer, cosine similarity)
- Streamlit (web app)

## 📁 Project Structure

```
├── MRS.ipynb          # Data cleaning, model building and testing
├── app.py             # Streamlit web app
├── movies.pkl         # Processed movie data
├── similarity.pkl     # Precomputed similarity matrix
├── requirements.txt   # Dependencies
└── README.md
```

## 🚀 Run Locally

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# 2. Install dependencies
pip install -r requirements.txt

# 3. Start the app
streamlit run app.py
```

The app opens at `http://localhost:8501`.

## 📸 Usage

1. Select a movie from the dropdown (you can type to search).
2. Click **Recommend**.
3. See 5 similar movies.

## 📊 Dataset

IMDB Movie Dataset (2023–1951) containing movie name, genre, overview, director and cast.

## 🔮 Future Improvements

- Show movie posters using the TMDB API
- Try TF-IDF and give more weight to genre, director and cast
- Add filters by genre and release year

## 👤 Author 


**Your Name**
[GitHub](https://github.com/iatuls) | [LinkedIn](https://linkedin.com/in/atul-singh2)
