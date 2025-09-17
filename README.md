# Music Recommender System

A music recommendation system that suggests similar songs based on lyrics analysis using machine learning techniques.

## Features

- **Song Recommendations**: Select a song from the dropdown and get 5 similar song recommendations.
- **Album Covers**: Displays album cover images fetched from Spotify API.
- **Interactive UI**: Built with Streamlit for a user-friendly web interface.

## Technologies Used

- **Python**: Core programming language
- **Streamlit**: For building the web application
- **Pandas**: Data manipulation and analysis
- **Scikit-learn**: Machine learning algorithms (TF-IDF Vectorizer, Cosine Similarity)
- **NLTK**: Natural language processing for text preprocessing
- **Spotipy**: Spotify API integration for fetching album covers

## Installation

1. Clone the repository:

   ```
   git clone https://github.com/scorpionTaj/Music-Recommender-System.git
   cd Music-Recommender-System
   ```

2. Install the required packages:

   ```
   pip install -r requirements.txt
   ```

3. Download the dataset:

   - Ensure `spotify_millsongdata.csv` is in the project directory.

4. Generate the model files:

   - Run the Jupyter notebook `project.ipynb` to create `df.pkl` and `similarity.pkl`.

5. Set up Spotify API credentials:
   - Obtain your Spotify Client ID and Client Secret from [Spotify Developer Dashboard](https://developer.spotify.com/dashboard).
   - Create a `.env` file in the project root and add your credentials:
     ```
     SPOTIFY_CLIENT_ID=your_client_id_here
     SPOTIFY_CLIENT_SECRET=your_client_secret_here
     ```

## Usage

Run the Streamlit application:

```
streamlit run app.py
```

Open your browser and navigate to the provided URL to start using the recommender system.

## How It Works

1. **Data Preprocessing**: The system processes song lyrics from the Spotify dataset, cleaning and tokenizing the text.
2. **Feature Extraction**: Uses TF-IDF vectorization to convert lyrics into numerical features.
3. **Similarity Calculation**: Computes cosine similarity between songs to find similar tracks.
4. **Recommendations**: For a selected song, returns the top 5 most similar songs.
5. **Visualization**: Fetches and displays album covers using the Spotify API.

## Dataset

The project uses the Spotify Million Song Dataset, which contains song metadata and lyrics.

## Contributing

Feel free to fork the repository and submit pull requests for improvements or bug fixes.

## License

This project is open-source. Please check the license file for more details.
