# movie_recommendation_system

This is a **machine learning project** that builds a content-based movie recommender system. Using cosine similarity, the system suggests movies similar to a user-selected title based on features like genres, cast, and overview. The project is implemented using Python, Streamlit, and TMDB API, showcasing how to develop and interact with a recommendation system.

---

## Features

- **Content-Based Filtering**: Recommends movies similar to a given movie based on content features like genres, cast, and overview.
- **TMDB Integration**: Fetches movie data and posters from The Movie Database (TMDB) API.
- **Interactive UI**: A user-friendly interface built with Streamlit.

---

## How It Works
1. **Data Preparation**: 
   - The system processes the TMDB dataset to combine important features (like genres, cast, and overview) into a single string for each movie.
2. **Similarity Calculation**: 
   - A cosine similarity matrix is generated to measure how closely related movies are based on their combined features.
3. **UI Development**:
   - The user interface (UI) is created in **PyCharm** using **Streamlit**, a Python library for building web apps. 
   - The UI includes:
     - A dropdown menu for selecting a movie.
     - A button to fetch recommendations.
     - A display section showing the recommended movies with their posters.
   - The UI components are coded in `app.py` using Streamlit functions like `st.selectbox` (for dropdown), `st.button` (for user actions), and `st.image` (for displaying posters).
4. **Recommendation**: 
   - When a user selects a movie and clicks the button, the system retrieves the top 5 most similar movies from the similarity matrix.
5. **Poster Retrieval**: 
   - Movie posters for the recommendations are fetched dynamically using the TMDB API.

---

## Usage

1. Run the Streamlit application:

   ```bash
   streamlit run app.py
   ```

2. Select a movie from the dropdown menu.

3. The system will display the top 5 recommended movies along with their posters.

---

## File Structure

- **`app.py`**: Main application file for Streamlit.
- **`movie_list.pkl`**: Preprocessed data file containing the list of movies.
- **`similarity.pkl`**: Precomputed cosine similarity matrix.
- **`requirements.txt`**: Python dependencies for the project.

---

## Technologies Used

- **Python**: Core programming language
- **Streamlit**: Interactive UI framework
- **TMDB API**: For fetching movie posters and metadata
- **Cosine Similarity**: Algorithm for calculating content similarity
- **Machine Learning**: Core methodology for creating recommendations based on content features.

---

## Acknowledgments

- [TMDB API](https://www.themoviedb.org/)
- [Streamlit](https://streamlit.io/)
