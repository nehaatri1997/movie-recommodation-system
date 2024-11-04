# movie-recommodation-system

This project is a simple movie recommendation system built using TF-IDF and cosine similarity. The code calculates the similarity between movie descriptions to recommend movies that are similar to a given title.

# Requirements
To run this project, you need Python and the following libraries:

pandas
scikit-learn
numpy
scipy

# Data
The code uses a CSV file named movies_metadata.csv containing metadata about movies. The file should include at least the following columns:

title: The title of the movie.
overview: A brief description of the movie plot.
Ensure movies_metadata.csv is in the same directory as the script.

#How It Works
Load the Data: The script loads movies_metadata.csv using pandas and fills any missing values in the overview column with an empty string.

TF-IDF Vectorization: The overview column is transformed into a TF-IDF matrix. TF-IDF (Term Frequency-Inverse Document Frequency) helps quantify the importance of words in each movie description.

Cosine Similarity Calculation: The cosine similarity between each pair of movies is calculated using the TF-IDF matrix. This similarity score indicates how similar two movies are based on their descriptions.

Recommendations: The get_recommendations function finds the most similar movies for a given title by comparing their cosine similarity scores.

# Functions
get_recommendations(title, dot_product=dot_product)
This function returns a list of the top 5 movies similar to the given title.

# Parameters:

title: The title of the movie for which recommendations are needed.
dot_product: (Optional) The precomputed dot product matrix of cosine similarity scores.

# Notes
Ensure the movie titles in the dataset are correctly formatted and do not contain extra spaces or unusual characters.
If a movie title is not found in the dataset, the get_recommendations function will return an error. Make sure the title matches exactly with what's in the dataset.
