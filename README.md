# Personalized Movie Recommendation System - PickmyMovie

An end-to-end intelligent recommendation engine built for the AI/ML Hackathon. This system uses a **Hybrid Filtering** approach, combining **Collaborative Filtering (SVD)** with **Deep Learning Content Embeddings (Sentence-Transformers)** to provide high-quality, personalized movie suggestions.

## 🚀 Features
- **Automated Data Pipeline:** Scripts to fetch data from MovieLens and enrich it with TMDB API metadata.
- **Hybrid Recommendation Engine:** Combines user behavior (ratings) with semantic movie analysis (plots/overviews).
- **Explainable AI:** Provides reasoning for each recommendation based on user history.
- **Pre-trained Integration:** Leverages the `all-MiniLM-L6-v2` transformer for state-of-the-art NLP features.

---

## 🛠️ Project Structure
- `phase1_data_collection`: Automates downloading MovieLens and fetching TMDB metadata.
- `phase2_preprocessing`: Cleans data, normalizes ratings, and merges movie titles/descriptions.
- `phase3_model_training`: Trains the SVD model and generates movie embeddings.
- `phase4_inference`: The final pipeline to generate Top 10 recommendations for a specific user.
- `data/`: (Ignored in Git) Stores raw and processed CSVs and model artifacts.

---

## 📦 Installation & Setup

### 1. Clone the repository
```bash
git clone <your-repo-link>
cd <repo-folder-name>bash
git clone <your-repo-link>
cd <repo-folder-name>
```
### 2. Install Dependencies 
```bash
pip install -r requirements.txt
```
### 3. API Configuration

To fetch movie metadata, you need a TMDB API key.

1. Get a key from themoviedb.org.
2. Open `phase1_data_collection` cell and replace `YOUR_TMDB_API_KEY_HERE` with your actual key.

---

## 🏃 How to Run (Reproducibility)
Run the scripts in the following order to build the system from scratch:

### 1. Collect Data

Run the ` phase1_data_collection ` cell for Data retrieval.

### 2. Preprocess & Clean

Run the ` phase2_preprocessing ` cell for converting the raw data into usuable format.

### 3. Train the model

Run the ` phase3_model_training ` cell for Fine tuning the pretrained model.

### 4. Generate the recommendations

Run the ` phase4_inferences ` for generating the recommendations.

---

## 📊 Evaluation & Methodology
Data Engineering: Features are engineered from text overviews using Transformers and normalized ratings to mitigate user bias.

Modeling: We use a weighted Hybrid approach. Content similarity ensures "niche" tastes are met, while SVD captures broader community trends.

Explainability: The system tracks tmdbId to link recommended titles back to the user's highest-rated genres/themes.

---

## 📜 Constraints & Tools
Dataset: MovieLens (Public) + TMDB (API).

Libraries: Pandas, Scikit-Learn, Sentence-Transformers, Requests.

---

Made by Manav with ❤️ 


